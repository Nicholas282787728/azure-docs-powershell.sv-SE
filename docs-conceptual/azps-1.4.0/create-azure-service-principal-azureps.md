---
title: Använd huvudnamn för tjänsten i Azure med Azure PowerShell
description: Lär dig hur du skapar och använder huvudnamn för tjänsten med Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/20/2019
ms.openlocfilehash: ae8bb8341209fedc3fadf8137f4faaf1ad3fe686
ms.sourcegitcommit: 5630030c5cfa9828c3c024b69de59248263ef17f
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/26/2019
ms.locfileid: "56837460"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="6b5e9-103">Skapa tjänstens huvudnamn för Azure med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="6b5e9-103">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="6b5e9-104">Automatiserade verktyg som använder Azure-tjänster bör alltid ha begränsad behörighet.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-104">Automated tools that use Azure services should always have restricted permissions.</span></span> <span data-ttu-id="6b5e9-105">Azure erbjuder tjänstens huvudnamn i stället för att programmen loggar in som användare med fullständig behörighet.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-105">Instead of having applications sign in as a fully privileged user, Azure offers service principals.</span></span>

<span data-ttu-id="6b5e9-106">Ett huvudnamn för tjänsten i Azure är en identitet som skapas för användning med program, värdbaserade tjänster och automatiserade verktyg för att tillgång till Azure-resurser.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-106">An Azure service principal is an identity created for use with applications, hosted services, and automated tools to access Azure resources.</span></span> <span data-ttu-id="6b5e9-107">Åtkomsten begränsas av de roller som tilldelas tjänstens huvudnamn, vilket ger dig kontroll över vilka resurser som kan nås och på vilken nivå.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-107">This access is restricted by the roles assigned to the service principal, giving you control over which resources can be accessed and at which level.</span></span> <span data-ttu-id="6b5e9-108">Av säkerhetsskäl rekommenderar vi att du alltid använder tjänstens huvudnamn med automatiserade verktyg i stället för att tillåta inloggning med en användaridentitet.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-108">For security reasons, it's always recommended to use service principals with automated tools rather than allowing them to log in with a user identity.</span></span>

<span data-ttu-id="6b5e9-109">Den här artikeln visar hur du skapar, hämtar information om och återställer ett tjänsthuvudnamn med Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-109">This article shows you the steps for creating, getting information about, and resetting a service principal with Azure PowerShell.</span></span>

## <a name="create-a-service-principal"></a><span data-ttu-id="6b5e9-110">Skapa ett huvudnamn för tjänsten</span><span class="sxs-lookup"><span data-stu-id="6b5e9-110">Create a service principal</span></span>

<span data-ttu-id="6b5e9-111">Skapa ett huvudnamn för tjänsten med cmdleten [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal).</span><span class="sxs-lookup"><span data-stu-id="6b5e9-111">Create a service principal with the [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) cmdlet.</span></span> <span data-ttu-id="6b5e9-112">När du skapar ett huvudnamn för tjänsten kan du välja vilken typ av inloggningsinformation som används.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-112">When creating a service principal, you choose the type of sign-in authentication it uses.</span></span>

> [!NOTE]
>
> <span data-ttu-id="6b5e9-113">Om ditt konto inte har behörighet att skapa ett huvudnamn för tjänsten visar `New-AzADServicePrincipal` ett felmeddelande om att du inte har rätt behörigheter för att slutföra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-113">If your account doesn't have permission to create a service principal, `New-AzADServicePrincipal` will return an error message containing "Insufficient privileges to complete the operation."</span></span> <span data-ttu-id="6b5e9-114">Kontakta Azure Active Directory-administratören om du vill skapa ett huvudnamn för tjänsten.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-114">Contact your Azure Active Directory admin to create a service principal.</span></span>

<span data-ttu-id="6b5e9-115">Det finns två typer av autentisering för tjänstens huvudnamn: lösenordsbaserad autentisering och certifikatbaserad autentisering.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-115">There are two types of authentication available for service principals: Password-based authentication, and certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="6b5e9-116">Lösenordsbaserad autentisering</span><span class="sxs-lookup"><span data-stu-id="6b5e9-116">Password-based authentication</span></span>

<span data-ttu-id="6b5e9-117">Om inga andra autentiseringsparametrar finns används lösenordsbaserad autentisering, och ett slumpmässigt lösenord skapas åt dig.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-117">Without any other authentication parameters, password-based authentication is used and a random password created for you.</span></span> <span data-ttu-id="6b5e9-118">Om du vill använda lösenordsbaserad autentisering rekommenderas den här metoden.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-118">If you want password-based authentication, this method is recommended.</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="6b5e9-119">Det returnerade objektet innehåller medlemmen `Secret`, som är en `SecureString` som innehåller det genererade lösenordet.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-119">The returned object contains the `Secret` member, which is a `SecureString` containing the generated password.</span></span> <span data-ttu-id="6b5e9-120">Se till att värdet lagras på en säker plats för autentisering med tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-120">Make sure that you store this value somewhere secure to authenticate with the service principal.</span></span> <span data-ttu-id="6b5e9-121">Värdet visas __inte__ i konsolens utdata.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-121">Its value __won't__ be displayed in the console output.</span></span> <span data-ttu-id="6b5e9-122">Om du tappar bort lösenordet måste du [återställa autentiseringsuppgifterna för tjänstens huvudnamn](#reset-credentials).</span><span class="sxs-lookup"><span data-stu-id="6b5e9-122">If you lose the password, [reset the service principal credentials](#reset-credentials).</span></span> 

<span data-ttu-id="6b5e9-123">För lösenord som anges av användaren tar argumentet `-PasswordCredential` objekten `PSADPasswordCredential`.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-123">For user-supplied passwords, the `-PasswordCredential` argument takes `PSADPasswordCredential` objects.</span></span> <span data-ttu-id="6b5e9-124">Objekten måste ha ett giltigt `StartDate` och `EndDate` samt ett `Password` i klartext.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-124">These objects must have a valid `StartDate` and `EndDate`, and take a plaintext `Password`.</span></span> <span data-ttu-id="6b5e9-125">Skapa ett starkt lösenord genom att följa [regler och begränsningar för Azure Active Directory-lösenord](/azure/active-directory/active-directory-passwords-policy).</span><span class="sxs-lookup"><span data-stu-id="6b5e9-125">When creating a password, make sure you follow the [Azure Active Directory password rules and restrictions](/azure/active-directory/active-directory-passwords-policy).</span></span> <span data-ttu-id="6b5e9-126">Använd inte ett svagt lösenord och återanvänd aldrig lösenord.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-126">Don't use a weak password or reuse a password.</span></span>

```azurepowershell-interactive
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

<span data-ttu-id="6b5e9-127">Objektet som returnerades från `New-AzADServicePrincipal` innehåller medlemmarna `Id` och `DisplayName`, som båda kan användas för inloggning med tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-127">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="6b5e9-128">För inloggning med tjänstens huvudnamn krävs det klientorganisations-ID som tjänstens huvudnamn skapades under.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-128">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="6b5e9-129">För att få den klientorganisation som var aktiv när tjänstens huvudnamn skapades kör du följande kommando __omedelbart efter__ att tjänstens huvudnamn har skapats:</span><span class="sxs-lookup"><span data-stu-id="6b5e9-129">To get the active tenant when the service principal was created, run the following command __immediately after__ service principal creation:</span></span>
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

### <a name="certificate-based-authentication"></a><span data-ttu-id="6b5e9-130">Certifikatbaserad autentisering</span><span class="sxs-lookup"><span data-stu-id="6b5e9-130">Certificate-based authentication</span></span>

<span data-ttu-id="6b5e9-131">Tjänstens huvudnamn med certifikatbaserad autentisering skapas med parametern `-CertValue`.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-131">Service principals using certificate-based authentication are created with the `-CertValue` parameter.</span></span> <span data-ttu-id="6b5e9-132">Denna parameter tar en base64-kodad ASCII-sträng för det offentliga certifikatet.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-132">This parameter takes a base64-encoded ASCII string of the public certificate.</span></span> <span data-ttu-id="6b5e9-133">Detta representeras av en PEM-fil eller en textkodad CRT eller CER.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-133">This is represented by a PEM file, or a text-encoded CRT or CER.</span></span> <span data-ttu-id="6b5e9-134">Binär kodning av det offentliga certifikatet stöds inte.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-134">Binary encodings of the public certificate aren't supported.</span></span> <span data-ttu-id="6b5e9-135">I de här anvisningarna förutsätts att du redan har ett tillgängligt certifikat.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-135">These instructions assume that you already have a certificate available.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

<span data-ttu-id="6b5e9-136">Du kan också använda parametern `-KeyCredential`, som tar `PSADKeyCredential`-objekt.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-136">You can also use the `-KeyCredential` parameter, which takes `PSADKeyCredential` objects.</span></span> <span data-ttu-id="6b5e9-137">Objekten måste ha ett giltigt `StartDate` och `EndDate`, och medlemmen `CertValue` måste ha angetts till en base64-kodad ASCII-sträng för det offentliga certifikatet.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-137">These objects must have a valid `StartDate`, `EndDate`, and have the `CertValue` member set to a base64-encoded ASCII string of the public certificate.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

<span data-ttu-id="6b5e9-138">Objektet som returnerades från `New-AzADServicePrincipal` innehåller medlemmarna `Id` och `DisplayName`, som båda kan användas för inloggning med tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-138">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span> <span data-ttu-id="6b5e9-139">Klienter som loggar in med tjänstens huvudnamn måste också ha åtkomst till certifikatets privata nyckel.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-139">Clients which sign in with the service principal also need access to the certificate's private key.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="6b5e9-140">För inloggning med tjänstens huvudnamn krävs det klientorganisations-ID som tjänstens huvudnamn skapades under.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-140">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="6b5e9-141">För att få den klientorganisation som var aktiv när tjänstens huvudnamn skapades kör du följande kommando __omedelbart efter__ att tjänstens huvudnamn har skapats:</span><span class="sxs-lookup"><span data-stu-id="6b5e9-141">To get the active tenant when the service principal was created, run the following command __immediately after__ service principal creation:</span></span>
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

## <a name="get-an-existing-service-principal"></a><span data-ttu-id="6b5e9-142">Hämta ett befintligt tjänsthuvudnamn</span><span class="sxs-lookup"><span data-stu-id="6b5e9-142">Get an existing service principal</span></span>

<span data-ttu-id="6b5e9-143">En lista över tjänsthuvudnamn för den aktiva klientorganisationen kan hämtas med [Get-AzADServicePrincipal](/module/az.resources/get-azadserviceprincipal).</span><span class="sxs-lookup"><span data-stu-id="6b5e9-143">A list of service principals for the currently active tenant can be retrieved with [Get-AzADServicePrincipal](/module/az.resources/get-azadserviceprincipal).</span></span> <span data-ttu-id="6b5e9-144">Som standard returnerar kommandot __alla__ tjänsthuvudnamn i en klientorganisation, så det kan ta lång tid att returnera resultaten för stora organisationer.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-144">By default this command returns __all__ service principals in a tenant, so for large organizations, it may take a long time to return results.</span></span> <span data-ttu-id="6b5e9-145">Vi rekommenderar att du i stället använder de valfria argumenten för filtrering på serversidan:</span><span class="sxs-lookup"><span data-stu-id="6b5e9-145">Instead, using one of the optional server-side filtering arguments is recommended:</span></span>

* <span data-ttu-id="6b5e9-146">`-DisplayNameBeginsWith` begär tjänsthuvudnamn som har ett _prefix_ som matchar det angivna värdet.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-146">`-DisplayNameBeginsWith` requests service principals that have a _prefix_ that match the provided value.</span></span> <span data-ttu-id="6b5e9-147">Visningsnamnet för ett tjänsthuvudnamn är det värde som anges med `-DisplayName` när det skapas.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-147">The display name of a service principal is the value set with `-DisplayName` during creation.</span></span>
* <span data-ttu-id="6b5e9-148">`-DisplayName` begär en _exakt matchning_ av tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-148">`-DisplayName` requests an _exact match_ of a service principal name.</span></span>

## <a name="manage-service-principal-roles"></a><span data-ttu-id="6b5e9-149">Hantera roller för tjänstens huvudnamn</span><span class="sxs-lookup"><span data-stu-id="6b5e9-149">Manage service principal roles</span></span>

<span data-ttu-id="6b5e9-150">Azure PowerShell har följande cmdletar för hantering av rolltilldelningar:</span><span class="sxs-lookup"><span data-stu-id="6b5e9-150">Azure PowerShell has the following cmdlets to manage role assignments:</span></span>

* [<span data-ttu-id="6b5e9-151">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="6b5e9-151">Get-AzRoleAssignment</span></span>](/powershell/module/az.resources/get-azroleassignment)
* [<span data-ttu-id="6b5e9-152">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="6b5e9-152">New-AzRoleAssignment</span></span>](/powershell/module/az.resources/new-azroleassignment)
* [<span data-ttu-id="6b5e9-153">Delete-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="6b5e9-153">Delete-AzRoleAssignment</span></span>](/powershell/module/az.resources/delete-azroleassignment)

<span data-ttu-id="6b5e9-154">Standardrollen för tjänstens huvudnamn är **Deltagare**.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-154">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="6b5e9-155">Den här rollen har fullständig behörighet att läsa och skriva till ett Azure-konto.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-155">This role has full permissions to read and write to an Azure account.</span></span> <span data-ttu-id="6b5e9-156">Rollen **Läsare** är mer begränsad och ger endast läsåtkomst.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-156">The **Reader** role is more restrictive, with read-only access.</span></span>  <span data-ttu-id="6b5e9-157">Mer information om rollbaserad åtkomstkontroll (RBAC) och roller finns i [RBAC: inbyggda roller](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="6b5e9-157">For more information on Role-Based Access Control (RBAC) and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="6b5e9-158">Det här exemplet lägger till rollen **Läsare** och tar bort rollen **Deltagare**:</span><span class="sxs-lookup"><span data-stu-id="6b5e9-158">This example adds the **Reader** role and removes the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Reader"
Delete-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Contributor"
```

> [!IMPORTANT]
> <span data-ttu-id="6b5e9-159">Cmdletar för rolltilldelning tar inte tjänsthuvudnamnsobjektets ID.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-159">Role assignment cmdlets don't take the service principal object ID.</span></span> <span data-ttu-id="6b5e9-160">De tar ID för det associerade programmet, som genereras vid tidpunkten för skapandet.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-160">They take the associated application ID, which is generated at creation time.</span></span> <span data-ttu-id="6b5e9-161">Hämta program-ID för ett tjänsthuvudnamn med `Get-AzADServicePrincipal`.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-161">To get the application ID for a service prinicpal, use `Get-AzADServicePrincipal`.</span></span>

> [!NOTE]
> <span data-ttu-id="6b5e9-162">Om ditt konto inte har behörighet att tilldela en roll visas ett felmeddelande om att kontot inte har behörighet att utföra åtgärden "Microsoft.Authorization/roleAssignments/write". Kontakta Azure Active Directory-administratören om du vill hantera roller.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-162">If your account doesn't have permission to assign a role, you see an error message that your account "does not have authorization to perform action 'Microsoft.Authorization/roleAssignments/write'." Contact your Azure Active Directory admin to manage roles.</span></span>

<span data-ttu-id="6b5e9-163">När en roll läggs till begränsas _inte_ tidigare tilldelade behörigheter.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-163">Adding a role _doesn't_ restrict previously assigned permissions.</span></span> <span data-ttu-id="6b5e9-164">När du begränsar behörigheter för tjänstens huvudnamn bör rollen __Deltagare__ tas bort.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-164">When restricting a service principal's permissions, the __Contributor__ role should be removed.</span></span>

<span data-ttu-id="6b5e9-165">Du bekräftar ändringarna genom att ange de roller som är tilldelade:</span><span class="sxs-lookup"><span data-stu-id="6b5e9-165">The changes can be verified by listing the assigned roles:</span></span>

```azurepowershell-interactive
Get-AzRoleAssignment -ServicePrinicpalName ServicePrincipalName
```

## <a name="sign-in-using-a-service-principal"></a><span data-ttu-id="6b5e9-166">Logga in med ett tjänsthuvudnamn</span><span class="sxs-lookup"><span data-stu-id="6b5e9-166">Sign in using a service principal</span></span>

<span data-ttu-id="6b5e9-167">Testa det nya tjänsthuvudnamnets autentiseringsuppgifter och behörigheter genom att logga in.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-167">Test the new service principal's credentials and permissions by signing in.</span></span> <span data-ttu-id="6b5e9-168">Om du vill logga in med ett huvudnamn för tjänsten behöver du det `applicationId`-värde som är associerat med det, och den klient som det skapades under.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-168">To sign in with a service principal, you need the `applicationId` value associated with it, and the tenant it was created under.</span></span>

<span data-ttu-id="6b5e9-169">Så här loggar du in med ett huvudnamn för tjänsten med lösenord:</span><span class="sxs-lookup"><span data-stu-id="6b5e9-169">To sign in with a service principal using a password:</span></span>

```azurepowershell-interactive
# Use the application ID as the username, and the secret as password
$credentials = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $credentials -Tenant <tenant ID> 
```

<span data-ttu-id="6b5e9-170">För certifikatbaserad autentisering måste Azure PowerShell kunna hämta information från ett lokalt certifikatarkiv baserat på ett tumavtryck för certifikat.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-170">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -TenantId $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="6b5e9-171">Anvisningar för hur du importerar ett certifikat i ett arkiv för autentiseringsuppgifter som är tillgängliga från PowerShell finns i [Logga in med Azure PowerShell](authenticate-azureps.md#sp-signin)</span><span class="sxs-lookup"><span data-stu-id="6b5e9-171">For instructions on importing a certificate into a credential store accessible by PowerShell, see [Sign in with Azure PowerShell](authenticate-azureps.md#sp-signin)</span></span>

## <a name="reset-credentials"></a><span data-ttu-id="6b5e9-172">Återställ autentiseringsuppgifter</span><span class="sxs-lookup"><span data-stu-id="6b5e9-172">Reset credentials</span></span>

<span data-ttu-id="6b5e9-173">Om du glömmer bort autentiseringsuppgifterna för ett huvudnamn för tjänsten läggar du till en ny autentiseringsuppgift med hjälp av [New-AzADSpCredential](/module/az.resources/new-azadspcredential).</span><span class="sxs-lookup"><span data-stu-id="6b5e9-173">If you forget the credentials for a service principal, use [New-AzADSpCredential](/module/az.resources/new-azadspcredential) to add a new credential.</span></span> <span data-ttu-id="6b5e9-174">Den här cmdleten använder samma argument och datatyper för autentiseringsuppgifter som `New-AzADServicePrincipal`.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-174">This cmdlet takes the same credential arguments and types as `New-AzADServicePrincipal`.</span></span> <span data-ttu-id="6b5e9-175">Utan argument för autentiseringsuppgifter skapas en ny `PasswordCredential` med ett slumpmässigt lösenord.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-175">Without any credential arguments, a new `PasswordCredential` with a random password is created.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6b5e9-176">Innan du tilldelar några nya autentiseringsuppgifter kan du ta bort befintliga autentiseringsuppgifter för att förhindra att de används för inloggning.</span><span class="sxs-lookup"><span data-stu-id="6b5e9-176">Before assigning any new credentials, you may want to remove existing credentials to prevent sign in with them.</span></span> <span data-ttu-id="6b5e9-177">Det gör du med cmdleten [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential):</span><span class="sxs-lookup"><span data-stu-id="6b5e9-177">To do so, use the [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) cmdlet:</span></span>
>
> ```azurepowershell-interactive
> Remove-AzADSpCredential -DisplayName ServicePrincipalName
> ```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -DisplayName ServicePrincipalName
```
