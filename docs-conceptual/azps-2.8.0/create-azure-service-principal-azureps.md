---
title: Använd huvudnamn för tjänsten i Azure med Azure PowerShell
description: Lär dig hur du skapar och använder huvudnamn för tjänsten med Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/23/2019
ms.openlocfilehash: 4c47d2bac2c63f13ac0ebbccda3e2eed12cd658f
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/15/2019
ms.locfileid: "72370422"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="5015f-103">Skapa tjänstens huvudnamn för Azure med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="5015f-103">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="5015f-104">Automatiserade verktyg som använder Azure-tjänster bör alltid ha begränsad behörighet.</span><span class="sxs-lookup"><span data-stu-id="5015f-104">Automated tools that use Azure services should always have restricted permissions.</span></span> <span data-ttu-id="5015f-105">Azure erbjuder tjänstens huvudnamn i stället för att programmen loggar in som användare med fullständig behörighet.</span><span class="sxs-lookup"><span data-stu-id="5015f-105">Instead of having applications sign in as a fully privileged user, Azure offers service principals.</span></span>

<span data-ttu-id="5015f-106">Ett huvudnamn för tjänsten i Azure är en identitet som skapas för användning med program, värdbaserade tjänster och automatiserade verktyg för att tillgång till Azure-resurser.</span><span class="sxs-lookup"><span data-stu-id="5015f-106">An Azure service principal is an identity created for use with applications, hosted services, and automated tools to access Azure resources.</span></span> <span data-ttu-id="5015f-107">Åtkomsten begränsas av de roller som tilldelas tjänstens huvudnamn, vilket ger dig kontroll över vilka resurser som kan nås och på vilken nivå.</span><span class="sxs-lookup"><span data-stu-id="5015f-107">This access is restricted by the roles assigned to the service principal, giving you control over which resources can be accessed and at which level.</span></span> <span data-ttu-id="5015f-108">Av säkerhetsskäl rekommenderar vi att du alltid använder tjänstens huvudnamn med automatiserade verktyg i stället för att tillåta inloggning med en användaridentitet.</span><span class="sxs-lookup"><span data-stu-id="5015f-108">For security reasons, it's always recommended to use service principals with automated tools rather than allowing them to log in with a user identity.</span></span>

<span data-ttu-id="5015f-109">Den här artikeln visar hur du skapar, hämtar information om och återställer ett tjänsthuvudnamn med Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5015f-109">This article shows you the steps for creating, getting information about, and resetting a service principal with Azure PowerShell.</span></span>

## <a name="create-a-service-principal"></a><span data-ttu-id="5015f-110">Skapa ett huvudnamn för tjänsten</span><span class="sxs-lookup"><span data-stu-id="5015f-110">Create a service principal</span></span>

<span data-ttu-id="5015f-111">Skapa ett huvudnamn för tjänsten med cmdleten [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal).</span><span class="sxs-lookup"><span data-stu-id="5015f-111">Create a service principal with the [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) cmdlet.</span></span> <span data-ttu-id="5015f-112">När du skapar ett huvudnamn för tjänsten kan du välja vilken typ av inloggningsinformation som används.</span><span class="sxs-lookup"><span data-stu-id="5015f-112">When creating a service principal, you choose the type of sign-in authentication it uses.</span></span>

> [!NOTE]
>
> <span data-ttu-id="5015f-113">Om ditt konto inte har behörighet att skapa ett huvudnamn för tjänsten visar `New-AzADServicePrincipal` ett felmeddelande om att du inte har rätt behörigheter för att slutföra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="5015f-113">If your account doesn't have permission to create a service principal, `New-AzADServicePrincipal` will return an error message containing "Insufficient privileges to complete the operation."</span></span> <span data-ttu-id="5015f-114">Kontakta Azure Active Directory-administratören om du vill skapa ett huvudnamn för tjänsten.</span><span class="sxs-lookup"><span data-stu-id="5015f-114">Contact your Azure Active Directory admin to create a service principal.</span></span>

<span data-ttu-id="5015f-115">Det finns två typer av autentisering för tjänstens huvudnamn: lösenordsbaserad autentisering och certifikatbaserad autentisering.</span><span class="sxs-lookup"><span data-stu-id="5015f-115">There are two types of authentication available for service principals: Password-based authentication, and certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="5015f-116">Lösenordsbaserad autentisering</span><span class="sxs-lookup"><span data-stu-id="5015f-116">Password-based authentication</span></span>

<span data-ttu-id="5015f-117">Om inga andra autentiseringsparametrar finns används lösenordsbaserad autentisering, och ett slumpmässigt lösenord skapas åt dig.</span><span class="sxs-lookup"><span data-stu-id="5015f-117">Without any other authentication parameters, password-based authentication is used and a random password created for you.</span></span> <span data-ttu-id="5015f-118">Om du vill använda lösenordsbaserad autentisering rekommenderas den här metoden.</span><span class="sxs-lookup"><span data-stu-id="5015f-118">If you want password-based authentication, this method is recommended.</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="5015f-119">Det returnerade objektet innehåller medlemmen `Secret`, som är en `SecureString` som innehåller det genererade lösenordet.</span><span class="sxs-lookup"><span data-stu-id="5015f-119">The returned object contains the `Secret` member, which is a `SecureString` containing the generated password.</span></span> <span data-ttu-id="5015f-120">Se till att värdet lagras på en säker plats för autentisering med tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="5015f-120">Make sure that you store this value somewhere secure to authenticate with the service principal.</span></span> <span data-ttu-id="5015f-121">Värdet visas __inte__ i konsolens utdata.</span><span class="sxs-lookup"><span data-stu-id="5015f-121">Its value __won't__ be displayed in the console output.</span></span> <span data-ttu-id="5015f-122">Om du tappar bort lösenordet måste du [återställa autentiseringsuppgifterna för tjänstens huvudnamn](#reset-credentials).</span><span class="sxs-lookup"><span data-stu-id="5015f-122">If you lose the password, [reset the service principal credentials](#reset-credentials).</span></span>

<span data-ttu-id="5015f-123">Med följande kod kan du exportera hemligheten:</span><span class="sxs-lookup"><span data-stu-id="5015f-123">The following code will allow you to export the secret:</span></span>

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($sp.Secret)
$UnsecureSecret = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
```

<span data-ttu-id="5015f-124">För lösenord som anges av användaren tar argumentet `-PasswordCredential` objekten `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential`.</span><span class="sxs-lookup"><span data-stu-id="5015f-124">For user-supplied passwords, the `-PasswordCredential` argument takes `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` objects.</span></span> <span data-ttu-id="5015f-125">Objekten måste ha ett giltigt `StartDate` och `EndDate` samt ett `Password` i klartext.</span><span class="sxs-lookup"><span data-stu-id="5015f-125">These objects must have a valid `StartDate` and `EndDate`, and take a plaintext `Password`.</span></span> <span data-ttu-id="5015f-126">Skapa ett starkt lösenord genom att följa [regler och begränsningar för Azure Active Directory-lösenord](/azure/active-directory/active-directory-passwords-policy).</span><span class="sxs-lookup"><span data-stu-id="5015f-126">When creating a password, make sure you follow the [Azure Active Directory password rules and restrictions](/azure/active-directory/active-directory-passwords-policy).</span></span> <span data-ttu-id="5015f-127">Använd inte ett svagt lösenord och återanvänd aldrig lösenord.</span><span class="sxs-lookup"><span data-stu-id="5015f-127">Don't use a weak password or reuse a password.</span></span>

```azurepowershell-interactive
Import-Module Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

<span data-ttu-id="5015f-128">Objektet som returnerades från `New-AzADServicePrincipal` innehåller medlemmarna `Id` och `DisplayName`, som båda kan användas för inloggning med tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="5015f-128">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="5015f-129">För inloggning med tjänstens huvudnamn krävs det klientorganisations-ID som tjänstens huvudnamn skapades under.</span><span class="sxs-lookup"><span data-stu-id="5015f-129">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="5015f-130">För att få den klientorganisation som var aktiv när tjänstens huvudnamn skapades kör du följande kommando __omedelbart efter__ att tjänstens huvudnamn har skapats:</span><span class="sxs-lookup"><span data-stu-id="5015f-130">To get the active tenant when the service principal was created, run the following command __immediately after__ service principal creation:</span></span>
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

### <a name="certificate-based-authentication"></a><span data-ttu-id="5015f-131">Certifikatbaserad autentisering</span><span class="sxs-lookup"><span data-stu-id="5015f-131">Certificate-based authentication</span></span>

<span data-ttu-id="5015f-132">Tjänstens huvudnamn med certifikatbaserad autentisering skapas med parametern `-CertValue`.</span><span class="sxs-lookup"><span data-stu-id="5015f-132">Service principals using certificate-based authentication are created with the `-CertValue` parameter.</span></span> <span data-ttu-id="5015f-133">Denna parameter tar en base64-kodad ASCII-sträng för det offentliga certifikatet.</span><span class="sxs-lookup"><span data-stu-id="5015f-133">This parameter takes a base64-encoded ASCII string of the public certificate.</span></span> <span data-ttu-id="5015f-134">Detta representeras av en PEM-fil eller en textkodad CRT eller CER.</span><span class="sxs-lookup"><span data-stu-id="5015f-134">This is represented by a PEM file, or a text-encoded CRT or CER.</span></span> <span data-ttu-id="5015f-135">Binär kodning av det offentliga certifikatet stöds inte.</span><span class="sxs-lookup"><span data-stu-id="5015f-135">Binary encodings of the public certificate aren't supported.</span></span> <span data-ttu-id="5015f-136">I de här anvisningarna förutsätts att du redan har ett tillgängligt certifikat.</span><span class="sxs-lookup"><span data-stu-id="5015f-136">These instructions assume that you already have a certificate available.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

<span data-ttu-id="5015f-137">Du kan också använda parametern `-KeyCredential`, som tar `PSADKeyCredential`-objekt.</span><span class="sxs-lookup"><span data-stu-id="5015f-137">You can also use the `-KeyCredential` parameter, which takes `PSADKeyCredential` objects.</span></span> <span data-ttu-id="5015f-138">Objekten måste ha ett giltigt `StartDate` och `EndDate`, och medlemmen `CertValue` måste ha angetts till en base64-kodad ASCII-sträng för det offentliga certifikatet.</span><span class="sxs-lookup"><span data-stu-id="5015f-138">These objects must have a valid `StartDate`, `EndDate`, and have the `CertValue` member set to a base64-encoded ASCII string of the public certificate.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

<span data-ttu-id="5015f-139">Objektet som returnerades från `New-AzADServicePrincipal` innehåller medlemmarna `Id` och `DisplayName`, som båda kan användas för inloggning med tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="5015f-139">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span> <span data-ttu-id="5015f-140">Klienter som loggar in med tjänstens huvudnamn måste också ha åtkomst till certifikatets privata nyckel.</span><span class="sxs-lookup"><span data-stu-id="5015f-140">Clients which sign in with the service principal also need access to the certificate's private key.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="5015f-141">För inloggning med tjänstens huvudnamn krävs det klientorganisations-ID som tjänstens huvudnamn skapades under.</span><span class="sxs-lookup"><span data-stu-id="5015f-141">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="5015f-142">För att få den klientorganisation som var aktiv när tjänstens huvudnamn skapades kör du följande kommando __omedelbart efter__ att tjänstens huvudnamn har skapats:</span><span class="sxs-lookup"><span data-stu-id="5015f-142">To get the active tenant when the service principal was created, run the following command __immediately after__ service principal creation:</span></span>
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

## <a name="get-an-existing-service-principal"></a><span data-ttu-id="5015f-143">Hämta ett befintligt tjänsthuvudnamn</span><span class="sxs-lookup"><span data-stu-id="5015f-143">Get an existing service principal</span></span>

<span data-ttu-id="5015f-144">En lista över tjänsthuvudnamn för den aktiva klientorganisationen kan hämtas med [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal).</span><span class="sxs-lookup"><span data-stu-id="5015f-144">A list of service principals for the currently active tenant can be retrieved with [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal).</span></span> <span data-ttu-id="5015f-145">Som standard returnerar kommandot __alla__ tjänsthuvudnamn i en klientorganisation, så det kan ta lång tid att returnera resultaten för stora organisationer.</span><span class="sxs-lookup"><span data-stu-id="5015f-145">By default this command returns __all__ service principals in a tenant, so for large organizations, it may take a long time to return results.</span></span> <span data-ttu-id="5015f-146">Vi rekommenderar att du i stället använder de valfria argumenten för filtrering på serversidan:</span><span class="sxs-lookup"><span data-stu-id="5015f-146">Instead, using one of the optional server-side filtering arguments is recommended:</span></span>

* <span data-ttu-id="5015f-147">`-DisplayNameBeginsWith` begär tjänsthuvudnamn som har ett _prefix_ som matchar det angivna värdet.</span><span class="sxs-lookup"><span data-stu-id="5015f-147">`-DisplayNameBeginsWith` requests service principals that have a _prefix_ that match the provided value.</span></span> <span data-ttu-id="5015f-148">Visningsnamnet för ett tjänsthuvudnamn är det värde som anges med `-DisplayName` när det skapas.</span><span class="sxs-lookup"><span data-stu-id="5015f-148">The display name of a service principal is the value set with `-DisplayName` during creation.</span></span>
* <span data-ttu-id="5015f-149">`-DisplayName` begär en _exakt matchning_ av tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="5015f-149">`-DisplayName` requests an _exact match_ of a service principal name.</span></span>

## <a name="manage-service-principal-roles"></a><span data-ttu-id="5015f-150">Hantera roller för tjänstens huvudnamn</span><span class="sxs-lookup"><span data-stu-id="5015f-150">Manage service principal roles</span></span>

<span data-ttu-id="5015f-151">Azure PowerShell har följande cmdletar för hantering av rolltilldelningar:</span><span class="sxs-lookup"><span data-stu-id="5015f-151">Azure PowerShell has the following cmdlets to manage role assignments:</span></span>

* [<span data-ttu-id="5015f-152">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="5015f-152">Get-AzRoleAssignment</span></span>](/powershell/module/az.resources/get-azroleassignment)
* [<span data-ttu-id="5015f-153">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="5015f-153">New-AzRoleAssignment</span></span>](/powershell/module/az.resources/new-azroleassignment)
* [<span data-ttu-id="5015f-154">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="5015f-154">Remove-AzRoleAssignment</span></span>](/powershell/module/az.resources/remove-azroleassignment)

<span data-ttu-id="5015f-155">Standardrollen för tjänstens huvudnamn är **Deltagare**.</span><span class="sxs-lookup"><span data-stu-id="5015f-155">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="5015f-156">Den här rollen har fullständig behörighet att läsa och skriva till ett Azure-konto.</span><span class="sxs-lookup"><span data-stu-id="5015f-156">This role has full permissions to read and write to an Azure account.</span></span> <span data-ttu-id="5015f-157">Rollen **Läsare** är mer begränsad och ger endast läsåtkomst.</span><span class="sxs-lookup"><span data-stu-id="5015f-157">The **Reader** role is more restrictive, with read-only access.</span></span>  <span data-ttu-id="5015f-158">Mer information om rollbaserad åtkomstkontroll (RBAC) och roller finns i [RBAC: inbyggda roller](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="5015f-158">For more information on Role-Based Access Control (RBAC) and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="5015f-159">Det här exemplet lägger till rollen **Läsare** och tar bort rollen **Deltagare**:</span><span class="sxs-lookup"><span data-stu-id="5015f-159">This example adds the **Reader** role and removes the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Reader"
Remove-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Contributor"
```

> [!IMPORTANT]
> <span data-ttu-id="5015f-160">Cmdletar för rolltilldelning tar inte tjänsthuvudnamnsobjektets ID.</span><span class="sxs-lookup"><span data-stu-id="5015f-160">Role assignment cmdlets don't take the service principal object ID.</span></span> <span data-ttu-id="5015f-161">De tar ID för det associerade programmet, som genereras vid tidpunkten för skapandet.</span><span class="sxs-lookup"><span data-stu-id="5015f-161">They take the associated application ID, which is generated at creation time.</span></span> <span data-ttu-id="5015f-162">Om du vill hämta program-ID:t för ett tjänsthuvudnamn använder du `Get-AzADServicePrincipal`.</span><span class="sxs-lookup"><span data-stu-id="5015f-162">To get the application ID for a service principal, use `Get-AzADServicePrincipal`.</span></span>

> [!NOTE]
> <span data-ttu-id="5015f-163">Om ditt konto inte har behörighet att tilldela en roll visas ett felmeddelande om att kontot inte har behörighet att utföra åtgärden "Microsoft.Authorization/roleAssignments/write". Kontakta Azure Active Directory-administratören om du vill hantera roller.</span><span class="sxs-lookup"><span data-stu-id="5015f-163">If your account doesn't have permission to assign a role, you see an error message that your account "does not have authorization to perform action 'Microsoft.Authorization/roleAssignments/write'." Contact your Azure Active Directory admin to manage roles.</span></span>

<span data-ttu-id="5015f-164">När en roll läggs till begränsas _inte_ tidigare tilldelade behörigheter.</span><span class="sxs-lookup"><span data-stu-id="5015f-164">Adding a role _doesn't_ restrict previously assigned permissions.</span></span> <span data-ttu-id="5015f-165">När du begränsar behörigheter för tjänstens huvudnamn bör rollen __Deltagare__ tas bort.</span><span class="sxs-lookup"><span data-stu-id="5015f-165">When restricting a service principal's permissions, the __Contributor__ role should be removed.</span></span>

<span data-ttu-id="5015f-166">Du bekräftar ändringarna genom att ange de roller som är tilldelade:</span><span class="sxs-lookup"><span data-stu-id="5015f-166">The changes can be verified by listing the assigned roles:</span></span>

```azurepowershell-interactive
Get-AzRoleAssignment -ServicePrincipalName ServicePrincipalName
```

## <a name="sign-in-using-a-service-principal"></a><span data-ttu-id="5015f-167">Logga in med ett tjänsthuvudnamn</span><span class="sxs-lookup"><span data-stu-id="5015f-167">Sign in using a service principal</span></span>

<span data-ttu-id="5015f-168">Testa det nya tjänsthuvudnamnets autentiseringsuppgifter och behörigheter genom att logga in.</span><span class="sxs-lookup"><span data-stu-id="5015f-168">Test the new service principal's credentials and permissions by signing in.</span></span> <span data-ttu-id="5015f-169">Om du vill logga in med ett huvudnamn för tjänsten behöver du det `applicationId`-värde som är associerat med det, och den klient som det skapades under.</span><span class="sxs-lookup"><span data-stu-id="5015f-169">To sign in with a service principal, you need the `applicationId` value associated with it, and the tenant it was created under.</span></span>

<span data-ttu-id="5015f-170">Så här loggar du in med ett huvudnamn för tjänsten med lösenord:</span><span class="sxs-lookup"><span data-stu-id="5015f-170">To sign in with a service principal using a password:</span></span>

```azurepowershell-interactive
# Use the application ID as the username, and the secret as password
$credentials = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $credentials -Tenant <tenant ID> 
```

<span data-ttu-id="5015f-171">För certifikatbaserad autentisering måste Azure PowerShell kunna hämta information från ett lokalt certifikatarkiv baserat på ett tumavtryck för certifikat.</span><span class="sxs-lookup"><span data-stu-id="5015f-171">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -Tenant <tenant ID> -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="5015f-172">Anvisningar för hur du importerar ett certifikat i ett arkiv för autentiseringsuppgifter som är tillgängliga från PowerShell finns i [Logga in med Azure PowerShell](authenticate-azureps.md#sp-signin)</span><span class="sxs-lookup"><span data-stu-id="5015f-172">For instructions on importing a certificate into a credential store accessible by PowerShell, see [Sign in with Azure PowerShell](authenticate-azureps.md#sp-signin)</span></span>

## <a name="reset-credentials"></a><span data-ttu-id="5015f-173">Återställ autentiseringsuppgifter</span><span class="sxs-lookup"><span data-stu-id="5015f-173">Reset credentials</span></span>

<span data-ttu-id="5015f-174">Om du glömmer bort autentiseringsuppgifterna för ett huvudnamn för tjänsten läggar du till en ny autentiseringsuppgift med hjälp av [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential).</span><span class="sxs-lookup"><span data-stu-id="5015f-174">If you forget the credentials for a service principal, use [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) to add a new credential.</span></span> <span data-ttu-id="5015f-175">Den här cmdleten använder samma argument och datatyper för autentiseringsuppgifter som `New-AzADServicePrincipal`.</span><span class="sxs-lookup"><span data-stu-id="5015f-175">This cmdlet takes the same credential arguments and types as `New-AzADServicePrincipal`.</span></span> <span data-ttu-id="5015f-176">Utan argument för autentiseringsuppgifter skapas en ny `PasswordCredential` med ett slumpmässigt lösenord.</span><span class="sxs-lookup"><span data-stu-id="5015f-176">Without any credential arguments, a new `PasswordCredential` with a random password is created.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5015f-177">Innan du tilldelar några nya autentiseringsuppgifter kan du ta bort befintliga autentiseringsuppgifter för att förhindra att de används för inloggning.</span><span class="sxs-lookup"><span data-stu-id="5015f-177">Before assigning any new credentials, you may want to remove existing credentials to prevent sign in with them.</span></span> <span data-ttu-id="5015f-178">Det gör du med cmdleten [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential):</span><span class="sxs-lookup"><span data-stu-id="5015f-178">To do so, use the [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) cmdlet:</span></span>
>
> ```azurepowershell-interactive
> Remove-AzADSpCredential -DisplayName ServicePrincipalName
> ```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -ServicePrincipalName ServicePrincipalName
```
