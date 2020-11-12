---
title: Använd huvudnamn för tjänsten i Azure med Azure PowerShell
description: Lär dig hur du skapar och använder huvudnamn för tjänsten med Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/23/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 65cf13200c46a955762f4c92b6822033a3723aa8
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/06/2020
ms.locfileid: "93408804"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="12156-103">Skapa tjänstens huvudnamn för Azure med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="12156-103">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="12156-104">Automatiserade verktyg som använder Azure-tjänster bör alltid ha begränsad behörighet.</span><span class="sxs-lookup"><span data-stu-id="12156-104">Automated tools that use Azure services should always have restricted permissions.</span></span> <span data-ttu-id="12156-105">Azure erbjuder tjänstens huvudnamn i stället för att programmen loggar in som användare med fullständig behörighet.</span><span class="sxs-lookup"><span data-stu-id="12156-105">Instead of having applications sign in as a fully privileged user, Azure offers service principals.</span></span>

<span data-ttu-id="12156-106">Ett huvudnamn för tjänsten i Azure är en identitet som skapas för användning med program, värdbaserade tjänster och automatiserade verktyg för att tillgång till Azure-resurser.</span><span class="sxs-lookup"><span data-stu-id="12156-106">An Azure service principal is an identity created for use with applications, hosted services, and automated tools to access Azure resources.</span></span> <span data-ttu-id="12156-107">Åtkomsten begränsas av de roller som tilldelas tjänstens huvudnamn, vilket ger dig kontroll över vilka resurser som kan nås och på vilken nivå.</span><span class="sxs-lookup"><span data-stu-id="12156-107">This access is restricted by the roles assigned to the service principal, giving you control over which resources can be accessed and at which level.</span></span> <span data-ttu-id="12156-108">Av säkerhetsskäl rekommenderar vi att du alltid använder tjänstens huvudnamn med automatiserade verktyg i stället för att tillåta inloggning med en användaridentitet.</span><span class="sxs-lookup"><span data-stu-id="12156-108">For security reasons, it's always recommended to use service principals with automated tools rather than allowing them to log in with a user identity.</span></span>

<span data-ttu-id="12156-109">Den här artikeln visar hur du skapar, hämtar information om och återställer ett tjänsthuvudnamn med Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="12156-109">This article shows you the steps for creating, getting information about, and resetting a service principal with Azure PowerShell.</span></span>

> [!WARNING]
> <span data-ttu-id="12156-110">När du skapar tjänstens huvudnamn med kommandot [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) innehåller utdata autentiseringsuppgifter som du måste skydda.</span><span class="sxs-lookup"><span data-stu-id="12156-110">When you create a service principal using the [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="12156-111">Se till att du inte inkluderar dessa autentiseringsuppgifter i din kod eller kontrollera autentiseringsuppgifterna i källkontrollen.</span><span class="sxs-lookup"><span data-stu-id="12156-111">Be sure that you do not include these credentials in your code or check the credentials into your source control.</span></span> <span data-ttu-id="12156-112">Alternativt bör du överväga att använda [hanterade identiteter](/azure/active-directory/managed-identities-azure-resources/overview) för att undvika att behöva använda autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="12156-112">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="12156-113">Som standard tilldelar [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) [deltagarrollen](/azure/role-based-access-control/built-in-roles#contributor) till tjänstens huvudnamn i prenumerationsomfånget.</span><span class="sxs-lookup"><span data-stu-id="12156-113">By default, [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="12156-114">Om du vill minska risken för att tjänstens huvudnamn komprometteras tilldelar du en mer specifik roll och begränsar omfånget för en resurs eller resursgrupp.</span><span class="sxs-lookup"><span data-stu-id="12156-114">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="12156-115">Mer information finns i [Steg för tillägg av en rolltilldelning](/azure/role-based-access-control/role-assignments-steps).</span><span class="sxs-lookup"><span data-stu-id="12156-115">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <a name="create-a-service-principal"></a><span data-ttu-id="12156-116">Skapa ett huvudnamn för tjänsten</span><span class="sxs-lookup"><span data-stu-id="12156-116">Create a service principal</span></span>

<span data-ttu-id="12156-117">Skapa ett huvudnamn för tjänsten med cmdleten [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal).</span><span class="sxs-lookup"><span data-stu-id="12156-117">Create a service principal with the [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) cmdlet.</span></span> <span data-ttu-id="12156-118">När du skapar ett huvudnamn för tjänsten kan du välja vilken typ av inloggningsinformation som används.</span><span class="sxs-lookup"><span data-stu-id="12156-118">When creating a service principal, you choose the type of sign-in authentication it uses.</span></span>

> [!NOTE]
>
> <span data-ttu-id="12156-119">Om ditt konto inte har behörighet att skapa ett huvudnamn för tjänsten visar `New-AzADServicePrincipal` ett felmeddelande om att du inte har rätt behörigheter för att slutföra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="12156-119">If your account doesn't have permission to create a service principal, `New-AzADServicePrincipal` will return an error message containing "Insufficient privileges to complete the operation."</span></span> <span data-ttu-id="12156-120">Kontakta Azure Active Directory-administratören om du vill skapa ett huvudnamn för tjänsten.</span><span class="sxs-lookup"><span data-stu-id="12156-120">Contact your Azure Active Directory admin to create a service principal.</span></span>

<span data-ttu-id="12156-121">Det finns två typer av autentisering för tjänstens huvudnamn: lösenordsbaserad autentisering och certifikatbaserad autentisering.</span><span class="sxs-lookup"><span data-stu-id="12156-121">There are two types of authentication available for service principals: Password-based authentication, and certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="12156-122">Lösenordsbaserad autentisering</span><span class="sxs-lookup"><span data-stu-id="12156-122">Password-based authentication</span></span>

<span data-ttu-id="12156-123">Om inga andra autentiseringsparametrar finns används lösenordsbaserad autentisering, och ett slumpmässigt lösenord skapas åt dig.</span><span class="sxs-lookup"><span data-stu-id="12156-123">Without any other authentication parameters, password-based authentication is used and a random password created for you.</span></span> <span data-ttu-id="12156-124">Om du vill använda lösenordsbaserad autentisering rekommenderas den här metoden.</span><span class="sxs-lookup"><span data-stu-id="12156-124">If you want password-based authentication, this method is recommended.</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="12156-125">Det returnerade objektet innehåller medlemmen `Secret`, som är en `SecureString` som innehåller det genererade lösenordet.</span><span class="sxs-lookup"><span data-stu-id="12156-125">The returned object contains the `Secret` member, which is a `SecureString` containing the generated password.</span></span> <span data-ttu-id="12156-126">Se till att värdet lagras på en säker plats för autentisering med tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="12156-126">Make sure that you store this value somewhere secure to authenticate with the service principal.</span></span> <span data-ttu-id="12156-127">Värdet visas __inte__ i konsolens utdata.</span><span class="sxs-lookup"><span data-stu-id="12156-127">Its value __won't__ be displayed in the console output.</span></span> <span data-ttu-id="12156-128">Om du tappar bort lösenordet måste du [återställa autentiseringsuppgifterna för tjänstens huvudnamn](#reset-credentials).</span><span class="sxs-lookup"><span data-stu-id="12156-128">If you lose the password, [reset the service principal credentials](#reset-credentials).</span></span>

<span data-ttu-id="12156-129">Med följande kod kan du exportera hemligheten:</span><span class="sxs-lookup"><span data-stu-id="12156-129">The following code will allow you to export the secret:</span></span>

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($sp.Secret)
$UnsecureSecret = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
```

<span data-ttu-id="12156-130">För lösenord som anges av användaren tar argumentet `-PasswordCredential` objekten `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential`.</span><span class="sxs-lookup"><span data-stu-id="12156-130">For user-supplied passwords, the `-PasswordCredential` argument takes `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` objects.</span></span> <span data-ttu-id="12156-131">Objekten måste ha ett giltigt `StartDate` och `EndDate` samt ett `Password` i klartext.</span><span class="sxs-lookup"><span data-stu-id="12156-131">These objects must have a valid `StartDate` and `EndDate`, and take a plaintext `Password`.</span></span> <span data-ttu-id="12156-132">Skapa ett starkt lösenord genom att följa [regler och begränsningar för Azure Active Directory-lösenord](/azure/active-directory/active-directory-passwords-policy).</span><span class="sxs-lookup"><span data-stu-id="12156-132">When creating a password, make sure you follow the [Azure Active Directory password rules and restrictions](/azure/active-directory/active-directory-passwords-policy).</span></span> <span data-ttu-id="12156-133">Använd inte ett svagt lösenord och återanvänd aldrig lösenord.</span><span class="sxs-lookup"><span data-stu-id="12156-133">Don't use a weak password or reuse a password.</span></span>

```azurepowershell-interactive
Import-Module Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

<span data-ttu-id="12156-134">Objektet som returnerades från `New-AzADServicePrincipal` innehåller medlemmarna `Id` och `DisplayName`, som båda kan användas för inloggning med tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="12156-134">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="12156-135">För inloggning med tjänstens huvudnamn krävs det klientorganisations-ID som tjänstens huvudnamn skapades under.</span><span class="sxs-lookup"><span data-stu-id="12156-135">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="12156-136">För att få den klientorganisation som var aktiv när tjänstens huvudnamn skapades kör du följande kommando __omedelbart efter__ att tjänstens huvudnamn har skapats:</span><span class="sxs-lookup"><span data-stu-id="12156-136">To get the active tenant when the service principal was created, run the following command __immediately after__ service principal creation:</span></span>
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

### <a name="certificate-based-authentication"></a><span data-ttu-id="12156-137">Certifikatbaserad autentisering</span><span class="sxs-lookup"><span data-stu-id="12156-137">Certificate-based authentication</span></span>

<span data-ttu-id="12156-138">Tjänstens huvudnamn med certifikatbaserad autentisering skapas med parametern `-CertValue`.</span><span class="sxs-lookup"><span data-stu-id="12156-138">Service principals using certificate-based authentication are created with the `-CertValue` parameter.</span></span> <span data-ttu-id="12156-139">Denna parameter tar en base64-kodad ASCII-sträng för det offentliga certifikatet.</span><span class="sxs-lookup"><span data-stu-id="12156-139">This parameter takes a base64-encoded ASCII string of the public certificate.</span></span> <span data-ttu-id="12156-140">Detta representeras av en PEM-fil eller en textkodad CRT eller CER.</span><span class="sxs-lookup"><span data-stu-id="12156-140">This is represented by a PEM file, or a text-encoded CRT or CER.</span></span> <span data-ttu-id="12156-141">Binär kodning av det offentliga certifikatet stöds inte.</span><span class="sxs-lookup"><span data-stu-id="12156-141">Binary encodings of the public certificate aren't supported.</span></span> <span data-ttu-id="12156-142">I de här anvisningarna förutsätts att du redan har ett tillgängligt certifikat.</span><span class="sxs-lookup"><span data-stu-id="12156-142">These instructions assume that you already have a certificate available.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

<span data-ttu-id="12156-143">Du kan också använda parametern `-KeyCredential`, som tar `PSADKeyCredential`-objekt.</span><span class="sxs-lookup"><span data-stu-id="12156-143">You can also use the `-KeyCredential` parameter, which takes `PSADKeyCredential` objects.</span></span> <span data-ttu-id="12156-144">Objekten måste ha ett giltigt `StartDate` och `EndDate`, och medlemmen `CertValue` måste ha angetts till en base64-kodad ASCII-sträng för det offentliga certifikatet.</span><span class="sxs-lookup"><span data-stu-id="12156-144">These objects must have a valid `StartDate`, `EndDate`, and have the `CertValue` member set to a base64-encoded ASCII string of the public certificate.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

<span data-ttu-id="12156-145">Objektet som returnerades från `New-AzADServicePrincipal` innehåller medlemmarna `Id` och `DisplayName`, som båda kan användas för inloggning med tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="12156-145">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span> <span data-ttu-id="12156-146">Klienter som loggar in med tjänstens huvudnamn måste också ha åtkomst till certifikatets privata nyckel.</span><span class="sxs-lookup"><span data-stu-id="12156-146">Clients which sign in with the service principal also need access to the certificate's private key.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="12156-147">För inloggning med tjänstens huvudnamn krävs det klientorganisations-ID som tjänstens huvudnamn skapades under.</span><span class="sxs-lookup"><span data-stu-id="12156-147">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="12156-148">För att få den klientorganisation som var aktiv när tjänstens huvudnamn skapades kör du följande kommando __omedelbart efter__ att tjänstens huvudnamn har skapats:</span><span class="sxs-lookup"><span data-stu-id="12156-148">To get the active tenant when the service principal was created, run the following command __immediately after__ service principal creation:</span></span>
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

## <a name="get-an-existing-service-principal"></a><span data-ttu-id="12156-149">Hämta ett befintligt tjänsthuvudnamn</span><span class="sxs-lookup"><span data-stu-id="12156-149">Get an existing service principal</span></span>

<span data-ttu-id="12156-150">En lista över tjänsthuvudnamn för den aktiva klientorganisationen kan hämtas med [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal).</span><span class="sxs-lookup"><span data-stu-id="12156-150">A list of service principals for the currently active tenant can be retrieved with [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal).</span></span> <span data-ttu-id="12156-151">Som standard returnerar kommandot __alla__ tjänsthuvudnamn i en klientorganisation, så det kan ta lång tid att returnera resultaten för stora organisationer.</span><span class="sxs-lookup"><span data-stu-id="12156-151">By default this command returns __all__ service principals in a tenant, so for large organizations, it may take a long time to return results.</span></span> <span data-ttu-id="12156-152">Vi rekommenderar att du i stället använder de valfria argumenten för filtrering på serversidan:</span><span class="sxs-lookup"><span data-stu-id="12156-152">Instead, using one of the optional server-side filtering arguments is recommended:</span></span>

* <span data-ttu-id="12156-153">`-DisplayNameBeginsWith` begär tjänsthuvudnamn som har ett _prefix_ som matchar det angivna värdet.</span><span class="sxs-lookup"><span data-stu-id="12156-153">`-DisplayNameBeginsWith` requests service principals that have a _prefix_ that match the provided value.</span></span> <span data-ttu-id="12156-154">Visningsnamnet för ett tjänsthuvudnamn är det värde som anges med `-DisplayName` när det skapas.</span><span class="sxs-lookup"><span data-stu-id="12156-154">The display name of a service principal is the value set with `-DisplayName` during creation.</span></span>
* <span data-ttu-id="12156-155">`-DisplayName` begär en _exakt matchning_ av tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="12156-155">`-DisplayName` requests an _exact match_ of a service principal name.</span></span>

## <a name="manage-service-principal-roles"></a><span data-ttu-id="12156-156">Hantera roller för tjänstens huvudnamn</span><span class="sxs-lookup"><span data-stu-id="12156-156">Manage service principal roles</span></span>

<span data-ttu-id="12156-157">Azure PowerShell har följande cmdletar för hantering av rolltilldelningar:</span><span class="sxs-lookup"><span data-stu-id="12156-157">Azure PowerShell has the following cmdlets to manage role assignments:</span></span>

* [<span data-ttu-id="12156-158">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="12156-158">Get-AzRoleAssignment</span></span>](/powershell/module/az.resources/get-azroleassignment)
* [<span data-ttu-id="12156-159">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="12156-159">New-AzRoleAssignment</span></span>](/powershell/module/az.resources/new-azroleassignment)
* [<span data-ttu-id="12156-160">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="12156-160">Remove-AzRoleAssignment</span></span>](/powershell/module/az.resources/remove-azroleassignment)

<span data-ttu-id="12156-161">Standardrollen för tjänstens huvudnamn är **Deltagare**.</span><span class="sxs-lookup"><span data-stu-id="12156-161">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="12156-162">Den här rollen har fullständig behörighet att läsa och skriva till ett Azure-konto.</span><span class="sxs-lookup"><span data-stu-id="12156-162">This role has full permissions to read and write to an Azure account.</span></span> <span data-ttu-id="12156-163">Rollen **Läsare** är mer begränsad och ger endast läsåtkomst.</span><span class="sxs-lookup"><span data-stu-id="12156-163">The **Reader** role is more restrictive, with read-only access.</span></span>  <span data-ttu-id="12156-164">Mer information om rollbaserad åtkomstkontroll (RBAC) och roller finns i [RBAC: inbyggda roller](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="12156-164">For more information on Role-Based Access Control (RBAC) and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="12156-165">Det här exemplet lägger till rollen **Läsare** och tar bort rollen **Deltagare** :</span><span class="sxs-lookup"><span data-stu-id="12156-165">This example adds the **Reader** role and removes the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Reader"
Remove-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Contributor"
```

> [!IMPORTANT]
> <span data-ttu-id="12156-166">Cmdletar för rolltilldelning tar inte tjänsthuvudnamnsobjektets ID.</span><span class="sxs-lookup"><span data-stu-id="12156-166">Role assignment cmdlets don't take the service principal object ID.</span></span> <span data-ttu-id="12156-167">De tar ID för det associerade programmet, som genereras vid tidpunkten för skapandet.</span><span class="sxs-lookup"><span data-stu-id="12156-167">They take the associated application ID, which is generated at creation time.</span></span> <span data-ttu-id="12156-168">Om du vill hämta program-ID:t för ett tjänsthuvudnamn använder du `Get-AzADServicePrincipal`.</span><span class="sxs-lookup"><span data-stu-id="12156-168">To get the application ID for a service principal, use `Get-AzADServicePrincipal`.</span></span>

> [!NOTE]
> <span data-ttu-id="12156-169">Om ditt konto inte har behörighet att tilldela en roll visas ett felmeddelande om att kontot inte har behörighet att utföra åtgärden "Microsoft.Authorization/roleAssignments/write". Kontakta Azure Active Directory-administratören om du vill hantera roller.</span><span class="sxs-lookup"><span data-stu-id="12156-169">If your account doesn't have permission to assign a role, you see an error message that your account "does not have authorization to perform action 'Microsoft.Authorization/roleAssignments/write'." Contact your Azure Active Directory admin to manage roles.</span></span>

<span data-ttu-id="12156-170">När en roll läggs till begränsas _inte_ tidigare tilldelade behörigheter.</span><span class="sxs-lookup"><span data-stu-id="12156-170">Adding a role _doesn't_ restrict previously assigned permissions.</span></span> <span data-ttu-id="12156-171">När du begränsar behörigheter för tjänstens huvudnamn bör rollen __Deltagare__ tas bort.</span><span class="sxs-lookup"><span data-stu-id="12156-171">When restricting a service principal's permissions, the __Contributor__ role should be removed.</span></span>

<span data-ttu-id="12156-172">Du bekräftar ändringarna genom att ange de roller som är tilldelade:</span><span class="sxs-lookup"><span data-stu-id="12156-172">The changes can be verified by listing the assigned roles:</span></span>

```azurepowershell-interactive
Get-AzRoleAssignment -ServicePrincipalName ServicePrincipalName
```

## <a name="sign-in-using-a-service-principal"></a><span data-ttu-id="12156-173">Logga in med ett tjänsthuvudnamn</span><span class="sxs-lookup"><span data-stu-id="12156-173">Sign in using a service principal</span></span>

<span data-ttu-id="12156-174">Testa det nya tjänsthuvudnamnets autentiseringsuppgifter och behörigheter genom att logga in.</span><span class="sxs-lookup"><span data-stu-id="12156-174">Test the new service principal's credentials and permissions by signing in.</span></span> <span data-ttu-id="12156-175">Om du vill logga in med ett huvudnamn för tjänsten behöver du det `applicationId`-värde som är associerat med det, och den klient som det skapades under.</span><span class="sxs-lookup"><span data-stu-id="12156-175">To sign in with a service principal, you need the `applicationId` value associated with it, and the tenant it was created under.</span></span>

<span data-ttu-id="12156-176">Så här loggar du in med ett huvudnamn för tjänsten med lösenord:</span><span class="sxs-lookup"><span data-stu-id="12156-176">To sign in with a service principal using a password:</span></span>

```azurepowershell-interactive
# Use the application ID as the username, and the secret as password
$credentials = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $credentials -Tenant <tenant ID> 
```

<span data-ttu-id="12156-177">För certifikatbaserad autentisering måste Azure PowerShell kunna hämta information från ett lokalt certifikatarkiv baserat på ett tumavtryck för certifikat.</span><span class="sxs-lookup"><span data-stu-id="12156-177">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -TenantId $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="12156-178">Anvisningar för hur du importerar ett certifikat i ett arkiv för autentiseringsuppgifter som är tillgängliga från PowerShell finns i [Logga in med Azure PowerShell](authenticate-azureps.md#sp-signin)</span><span class="sxs-lookup"><span data-stu-id="12156-178">For instructions on importing a certificate into a credential store accessible by PowerShell, see [Sign in with Azure PowerShell](authenticate-azureps.md#sp-signin)</span></span>

## <a name="reset-credentials"></a><span data-ttu-id="12156-179">Återställ autentiseringsuppgifter</span><span class="sxs-lookup"><span data-stu-id="12156-179">Reset credentials</span></span>

<span data-ttu-id="12156-180">Om du glömmer bort autentiseringsuppgifterna för ett huvudnamn för tjänsten läggar du till en ny autentiseringsuppgift med hjälp av [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential).</span><span class="sxs-lookup"><span data-stu-id="12156-180">If you forget the credentials for a service principal, use [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) to add a new credential.</span></span> <span data-ttu-id="12156-181">Den här cmdleten använder samma argument och datatyper för autentiseringsuppgifter som `New-AzADServicePrincipal`.</span><span class="sxs-lookup"><span data-stu-id="12156-181">This cmdlet takes the same credential arguments and types as `New-AzADServicePrincipal`.</span></span> <span data-ttu-id="12156-182">Utan argument för autentiseringsuppgifter skapas en ny `PasswordCredential` med ett slumpmässigt lösenord.</span><span class="sxs-lookup"><span data-stu-id="12156-182">Without any credential arguments, a new `PasswordCredential` with a random password is created.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="12156-183">Innan du tilldelar några nya autentiseringsuppgifter kan du ta bort befintliga autentiseringsuppgifter för att förhindra att de används för inloggning.</span><span class="sxs-lookup"><span data-stu-id="12156-183">Before assigning any new credentials, you may want to remove existing credentials to prevent sign in with them.</span></span> <span data-ttu-id="12156-184">Det gör du med cmdleten [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential):</span><span class="sxs-lookup"><span data-stu-id="12156-184">To do so, use the [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) cmdlet:</span></span>
>
> ```azurepowershell-interactive
> Remove-AzADSpCredential -DisplayName ServicePrincipalName
> ```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -ServicePrincipalName ServicePrincipalName
```
