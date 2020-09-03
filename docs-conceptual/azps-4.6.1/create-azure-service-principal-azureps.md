---
title: Använd huvudnamn för tjänsten i Azure med Azure PowerShell
description: Lär dig hur du skapar och använder huvudnamn för tjänsten med Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/17/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 3c876454560e4ad421e6d32a8ca8b30a651fd8af
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/01/2020
ms.locfileid: "89239323"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="e3045-103">Skapa tjänstens huvudnamn för Azure med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="e3045-103">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="e3045-104">Automatiserade verktyg som använder Azure-tjänster bör alltid ha begränsad behörighet.</span><span class="sxs-lookup"><span data-stu-id="e3045-104">Automated tools that use Azure services should always have restricted permissions.</span></span> <span data-ttu-id="e3045-105">Azure erbjuder tjänstens huvudnamn i stället för att programmen loggar in som användare med fullständig behörighet.</span><span class="sxs-lookup"><span data-stu-id="e3045-105">Instead of having applications sign in as a fully privileged user, Azure offers service principals.</span></span>

<span data-ttu-id="e3045-106">Ett huvudnamn för tjänsten i Azure är en identitet som skapas för användning med program, värdbaserade tjänster och automatiserade verktyg för att tillgång till Azure-resurser.</span><span class="sxs-lookup"><span data-stu-id="e3045-106">An Azure service principal is an identity created for use with applications, hosted services, and automated tools to access Azure resources.</span></span> <span data-ttu-id="e3045-107">Åtkomsten begränsas av de roller som tilldelas tjänstens huvudnamn, vilket ger dig kontroll över vilka resurser som kan nås och på vilken nivå.</span><span class="sxs-lookup"><span data-stu-id="e3045-107">This access is restricted by the roles assigned to the service principal, giving you control over which resources can be accessed and at which level.</span></span> <span data-ttu-id="e3045-108">Av säkerhetsskäl rekommenderar vi att du alltid använder tjänstens huvudnamn med automatiserade verktyg i stället för att tillåta inloggning med en användaridentitet.</span><span class="sxs-lookup"><span data-stu-id="e3045-108">For security reasons, it's always recommended to use service principals with automated tools rather than allowing them to log in with a user identity.</span></span>

<span data-ttu-id="e3045-109">Den här artikeln visar hur du skapar, hämtar information om och återställer ett tjänsthuvudnamn med Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e3045-109">This article shows you the steps for creating, getting information about, and resetting a service principal with Azure PowerShell.</span></span>

## <a name="create-a-service-principal"></a><span data-ttu-id="e3045-110">Skapa ett huvudnamn för tjänsten</span><span class="sxs-lookup"><span data-stu-id="e3045-110">Create a service principal</span></span>

<span data-ttu-id="e3045-111">Skapa ett huvudnamn för tjänsten med cmdleten [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal).</span><span class="sxs-lookup"><span data-stu-id="e3045-111">Create a service principal with the [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) cmdlet.</span></span> <span data-ttu-id="e3045-112">När du skapar ett huvudnamn för tjänsten kan du välja vilken typ av inloggningsinformation som används.</span><span class="sxs-lookup"><span data-stu-id="e3045-112">When creating a service principal, you choose the type of sign-in authentication it uses.</span></span>

> [!NOTE]
> <span data-ttu-id="e3045-113">Om ditt konto inte har behörighet att skapa ett tjänsthuvudnamn visar `New-AzADServicePrincipal` ett felmeddelande om att du inte har rätt behörigheter för att slutföra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="e3045-113">If your account doesn't have permission to create a service principal, `New-AzADServicePrincipal` will return an error message containing "Insufficient privileges to complete the operation".</span></span>
> <span data-ttu-id="e3045-114">Kontakta Azure Active Directory-administratören om du vill skapa ett huvudnamn för tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e3045-114">Contact your Azure Active Directory admin to create a service principal.</span></span>

<span data-ttu-id="e3045-115">Det finns två typer av autentisering för tjänstens huvudnamn: lösenordsbaserad autentisering och certifikatbaserad autentisering.</span><span class="sxs-lookup"><span data-stu-id="e3045-115">There are two types of authentication available for service principals: Password-based authentication, and certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="e3045-116">Lösenordsbaserad autentisering</span><span class="sxs-lookup"><span data-stu-id="e3045-116">Password-based authentication</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e3045-117">Standardrollen för ett huvudnamn för tjänsten för lösenordsbaserad autentisering är **Deltagare**.</span><span class="sxs-lookup"><span data-stu-id="e3045-117">The default role for a password-based authentication service principal is **Contributor**.</span></span> <span data-ttu-id="e3045-118">Den här rollen har fullständig behörighet att läsa och skriva till ett Azure-konto.</span><span class="sxs-lookup"><span data-stu-id="e3045-118">This role has full permissions to read and write to an Azure account.</span></span> <span data-ttu-id="e3045-119">Information om hur du hanterar rolltilldelningar finns i [Hantera roller för tjänstens huvudnamn](#manage-service-principal-roles).</span><span class="sxs-lookup"><span data-stu-id="e3045-119">For information on managing role assignments, see [Manage service principal roles](#manage-service-principal-roles).</span></span>

<span data-ttu-id="e3045-120">Om inga andra autentiseringsparametrar finns används lösenordsbaserad autentisering, och ett slumpmässigt lösenord skapas åt dig.</span><span class="sxs-lookup"><span data-stu-id="e3045-120">Without any other authentication parameters, password-based authentication is used and a random password created for you.</span></span> <span data-ttu-id="e3045-121">Om du vill använda lösenordsbaserad autentisering rekommenderas den här metoden.</span><span class="sxs-lookup"><span data-stu-id="e3045-121">If you want password-based authentication, this method is recommended.</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="e3045-122">Det returnerade objektet innehåller medlemmen `Secret`, som är en `SecureString` som innehåller det genererade lösenordet.</span><span class="sxs-lookup"><span data-stu-id="e3045-122">The returned object contains the `Secret` member, which is a `SecureString` containing the generated password.</span></span> <span data-ttu-id="e3045-123">Se till att värdet lagras på en säker plats för autentisering med tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="e3045-123">Make sure that you store this value somewhere secure to authenticate with the service principal.</span></span> <span data-ttu-id="e3045-124">Värdet visas _inte_ i konsolens utdata.</span><span class="sxs-lookup"><span data-stu-id="e3045-124">Its value _won't_ be displayed in the console output.</span></span> <span data-ttu-id="e3045-125">Om du tappar bort lösenordet måste du [återställa autentiseringsuppgifterna för tjänstens huvudnamn](#reset-credentials).</span><span class="sxs-lookup"><span data-stu-id="e3045-125">If you lose the password, [reset the service principal credentials](#reset-credentials).</span></span>

<span data-ttu-id="e3045-126">Med följande kod kan du exportera hemligheten:</span><span class="sxs-lookup"><span data-stu-id="e3045-126">The following code will allow you to export the secret:</span></span>

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($sp.Secret)
$UnsecureSecret = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
```

<span data-ttu-id="e3045-127">För lösenord som anges av användaren tar argumentet `-PasswordCredential` objekten `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential`.</span><span class="sxs-lookup"><span data-stu-id="e3045-127">For user-supplied passwords, the `-PasswordCredential` argument takes `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` objects.</span></span> <span data-ttu-id="e3045-128">Objekten måste ha ett giltigt `StartDate` och `EndDate` samt ett `Password` i klartext.</span><span class="sxs-lookup"><span data-stu-id="e3045-128">These objects must have a valid `StartDate` and `EndDate`, and take a plaintext `Password`.</span></span> <span data-ttu-id="e3045-129">Skapa ett starkt lösenord genom att följa [regler och begränsningar för Azure Active Directory-lösenord](/azure/active-directory/active-directory-passwords-policy).</span><span class="sxs-lookup"><span data-stu-id="e3045-129">When creating a password, make sure you follow the [Azure Active Directory password rules and restrictions](/azure/active-directory/active-directory-passwords-policy).</span></span>
<span data-ttu-id="e3045-130">Använd inte ett svagt lösenord och återanvänd aldrig lösenord.</span><span class="sxs-lookup"><span data-stu-id="e3045-130">Don't use a weak password or reuse a password.</span></span>

```azurepowershell-interactive
Import-Module -Name Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

<span data-ttu-id="e3045-131">Objektet som returnerades från `New-AzADServicePrincipal` innehåller medlemmarna `Id` och `DisplayName`, som båda kan användas för inloggning med tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="e3045-131">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e3045-132">För inloggning med tjänstens huvudnamn krävs det klientorganisations-ID som tjänstens huvudnamn skapades under.</span><span class="sxs-lookup"><span data-stu-id="e3045-132">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="e3045-133">För att få den klientorganisation som var aktiv när tjänstens huvudnamn skapades kör du följande kommando _omedelbart efter_ att tjänstens huvudnamn har skapats:</span><span class="sxs-lookup"><span data-stu-id="e3045-133">To get the active tenant when the service principal was created, run the following command _immediately after_ service principal creation:</span></span>

```azurepowershell-interactive
(Get-AzContext).Tenant.Id
```

### <a name="certificate-based-authentication"></a><span data-ttu-id="e3045-134">Certifikatbaserad autentisering</span><span class="sxs-lookup"><span data-stu-id="e3045-134">Certificate-based authentication</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e3045-135">Ingen standardroll tilldelas när du skapar en certifikatbaserad autentisering för tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="e3045-135">There is no default role assigned when creating a certificate-based authentication service principal.</span></span> <span data-ttu-id="e3045-136">Information om hur du hanterar rolltilldelningar finns i [Hantera roller för tjänstens huvudnamn](#manage-service-principal-roles).</span><span class="sxs-lookup"><span data-stu-id="e3045-136">For information on managing role assignments, see [Manage service principal roles](#manage-service-principal-roles).</span></span>

<span data-ttu-id="e3045-137">Tjänstens huvudnamn med certifikatbaserad autentisering skapas med parametern `-CertValue`.</span><span class="sxs-lookup"><span data-stu-id="e3045-137">Service principals using certificate-based authentication are created with the `-CertValue` parameter.</span></span> <span data-ttu-id="e3045-138">Denna parameter tar en base64-kodad ASCII-sträng för det offentliga certifikatet.</span><span class="sxs-lookup"><span data-stu-id="e3045-138">This parameter takes a base64-encoded ASCII string of the public certificate.</span></span> <span data-ttu-id="e3045-139">Detta representeras av en PEM-fil eller en textkodad CRT eller CER.</span><span class="sxs-lookup"><span data-stu-id="e3045-139">This is represented by a PEM file, or a text-encoded CRT or CER.</span></span> <span data-ttu-id="e3045-140">Binär kodning av det offentliga certifikatet stöds inte.</span><span class="sxs-lookup"><span data-stu-id="e3045-140">Binary encodings of the public certificate aren't supported.</span></span> <span data-ttu-id="e3045-141">I de här anvisningarna förutsätts att du redan har ett tillgängligt certifikat.</span><span class="sxs-lookup"><span data-stu-id="e3045-141">These instructions assume that you already have a certificate available.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

<span data-ttu-id="e3045-142">Du kan också använda parametern `-KeyCredential`, som tar `PSADKeyCredential`-objekt.</span><span class="sxs-lookup"><span data-stu-id="e3045-142">You can also use the `-KeyCredential` parameter, which takes `PSADKeyCredential` objects.</span></span> <span data-ttu-id="e3045-143">Objekten måste ha ett giltigt `StartDate` och `EndDate`, och medlemmen `CertValue` måste ha angetts till en base64-kodad ASCII-sträng för det offentliga certifikatet.</span><span class="sxs-lookup"><span data-stu-id="e3045-143">These objects must have a valid `StartDate`, `EndDate`, and have the `CertValue` member set to a base64-encoded ASCII string of the public certificate.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

<span data-ttu-id="e3045-144">Objektet som returnerades från `New-AzADServicePrincipal` innehåller medlemmarna `Id` och `DisplayName`, som båda kan användas för inloggning med tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="e3045-144">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span> <span data-ttu-id="e3045-145">Klienter som loggar in med tjänstens huvudnamn måste också ha åtkomst till certifikatets privata nyckel.</span><span class="sxs-lookup"><span data-stu-id="e3045-145">Clients which sign in with the service principal also need access to the certificate's private key.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e3045-146">För inloggning med tjänstens huvudnamn krävs det klientorganisations-ID som tjänstens huvudnamn skapades under.</span><span class="sxs-lookup"><span data-stu-id="e3045-146">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="e3045-147">För att få den klientorganisation som var aktiv när tjänstens huvudnamn skapades kör du följande kommando _omedelbart efter_ att tjänstens huvudnamn har skapats:</span><span class="sxs-lookup"><span data-stu-id="e3045-147">To get the active tenant when the service principal was created, run the following command _immediately after_ service principal creation:</span></span>

```azurepowershell-interactive
(Get-AzContext).Tenant.Id
```

## <a name="get-an-existing-service-principal"></a><span data-ttu-id="e3045-148">Hämta ett befintligt tjänsthuvudnamn</span><span class="sxs-lookup"><span data-stu-id="e3045-148">Get an existing service principal</span></span>

<span data-ttu-id="e3045-149">En lista över tjänsthuvudnamn för den aktiva klientorganisationen kan hämtas med [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal).</span><span class="sxs-lookup"><span data-stu-id="e3045-149">A list of service principals for the active tenant can be retrieved with [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal).</span></span> <span data-ttu-id="e3045-150">Som standard returnerar detta kommando _alla_ huvudnamn för tjänsten i en klientorganisation.</span><span class="sxs-lookup"><span data-stu-id="e3045-150">By default this command returns _all_ service principals in a tenant.</span></span> <span data-ttu-id="e3045-151">För stora organisationer kan det ta lång tid att returnera resultat.</span><span class="sxs-lookup"><span data-stu-id="e3045-151">For large organizations, it may take a long time to return results.</span></span> <span data-ttu-id="e3045-152">Vi rekommenderar att du i stället använder de valfria argumenten för filtrering på serversidan:</span><span class="sxs-lookup"><span data-stu-id="e3045-152">Instead, using one of the optional server-side filtering arguments is recommended:</span></span>

- <span data-ttu-id="e3045-153">`-DisplayNameBeginsWith` begär tjänsthuvudnamn som har ett _prefix_ som matchar det angivna värdet.</span><span class="sxs-lookup"><span data-stu-id="e3045-153">`-DisplayNameBeginsWith` requests service principals that have a _prefix_ that match the provided value.</span></span> <span data-ttu-id="e3045-154">Visningsnamnet för ett tjänsthuvudnamn är det värde som anges med `-DisplayName` när det skapas.</span><span class="sxs-lookup"><span data-stu-id="e3045-154">The display name of a service principal is the value set with `-DisplayName` during creation.</span></span>
- <span data-ttu-id="e3045-155">`-DisplayName` begär en _exakt matchning_ av tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="e3045-155">`-DisplayName` requests an _exact match_ of a service principal name.</span></span>

## <a name="manage-service-principal-roles"></a><span data-ttu-id="e3045-156">Hantera roller för tjänstens huvudnamn</span><span class="sxs-lookup"><span data-stu-id="e3045-156">Manage service principal roles</span></span>

<span data-ttu-id="e3045-157">Azure PowerShell har följande cmdletar för hantering av rolltilldelningar:</span><span class="sxs-lookup"><span data-stu-id="e3045-157">Azure PowerShell has the following cmdlets to manage role assignments:</span></span>

- [<span data-ttu-id="e3045-158">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e3045-158">Get-AzRoleAssignment</span></span>](/powershell/module/az.resources/get-azroleassignment)
- [<span data-ttu-id="e3045-159">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e3045-159">New-AzRoleAssignment</span></span>](/powershell/module/az.resources/new-azroleassignment)
- [<span data-ttu-id="e3045-160">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e3045-160">Remove-AzRoleAssignment</span></span>](/powershell/module/az.resources/remove-azroleassignment)

<span data-ttu-id="e3045-161">Standardrollen för ett huvudnamn för tjänsten för lösenordsbaserad autentisering är **Deltagare**.</span><span class="sxs-lookup"><span data-stu-id="e3045-161">The default role for a password-based authentication service principal is **Contributor**.</span></span> <span data-ttu-id="e3045-162">Den här rollen har fullständig behörighet att läsa och skriva till ett Azure-konto.</span><span class="sxs-lookup"><span data-stu-id="e3045-162">This role has full permissions to read and write to an Azure account.</span></span> <span data-ttu-id="e3045-163">Rollen **Läsare** är mer begränsad och ger endast läsåtkomst.</span><span class="sxs-lookup"><span data-stu-id="e3045-163">The **Reader** role is more restrictive, with read-only access.</span></span> <span data-ttu-id="e3045-164">Mer information om rollbaserad åtkomstkontroll (RBAC) och roller finns i [RBAC: inbyggda roller](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="e3045-164">For more information on Role-Based Access Control (RBAC) and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="e3045-165">Det här exemplet lägger till rollen **Läsare** och tar bort rollen **Deltagare**:</span><span class="sxs-lookup"><span data-stu-id="e3045-165">This example adds the **Reader** role and removes the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName 'Reader'
Remove-AzRoleAssignment -ObjectId <service principal object ID> -RoleDefinitionName 'Contributor'
```

> [!IMPORTANT]
> <span data-ttu-id="e3045-166">Cmdletar för rolltilldelning tar inte tjänsthuvudnamnsobjektets ID.</span><span class="sxs-lookup"><span data-stu-id="e3045-166">Role assignment cmdlets don't take the service principal object ID.</span></span> <span data-ttu-id="e3045-167">De tar ID för det associerade programmet, som genereras vid tidpunkten för skapandet.</span><span class="sxs-lookup"><span data-stu-id="e3045-167">They take the associated application ID, which is generated at creation time.</span></span> <span data-ttu-id="e3045-168">Om du vill hämta program-ID:t för ett tjänsthuvudnamn använder du `Get-AzADServicePrincipal`.</span><span class="sxs-lookup"><span data-stu-id="e3045-168">To get the application ID for a service principal, use `Get-AzADServicePrincipal`.</span></span>

> [!NOTE]
> <span data-ttu-id="e3045-169">Om ditt konto inte har behörighet att tilldela en roll visas ett felmeddelande om att kontot inte har behörighet att utföra åtgärden "Microsoft.Authorization/roleAssignments/write".</span><span class="sxs-lookup"><span data-stu-id="e3045-169">If your account doesn't have permission to assign a role, you see an error message that your account "does not have authorization to perform action 'Microsoft.Authorization/roleAssignments/write'".</span></span> <span data-ttu-id="e3045-170">Kontakta Azure Active Directory-administratören om du vill hantera roller.</span><span class="sxs-lookup"><span data-stu-id="e3045-170">Contact your Azure Active Directory admin to manage roles.</span></span>

<span data-ttu-id="e3045-171">När en roll läggs till begränsas _inte_ tidigare tilldelade behörigheter.</span><span class="sxs-lookup"><span data-stu-id="e3045-171">Adding a role _doesn't_ restrict previously assigned permissions.</span></span> <span data-ttu-id="e3045-172">När du begränsar behörigheter för tjänstens huvudnamn bör rollen **Deltagare** tas bort.</span><span class="sxs-lookup"><span data-stu-id="e3045-172">When restricting a service principal's permissions, the **Contributor** role should be removed.</span></span>

<span data-ttu-id="e3045-173">Du bekräftar ändringarna genom att ange de roller som är tilldelade:</span><span class="sxs-lookup"><span data-stu-id="e3045-173">The changes can be verified by listing the assigned roles:</span></span>

```azurepowershell-interactive
Get-AzRoleAssignment -ServicePrincipalName ServicePrincipalName
```

## <a name="sign-in-using-a-service-principal"></a><span data-ttu-id="e3045-174">Logga in med ett tjänsthuvudnamn</span><span class="sxs-lookup"><span data-stu-id="e3045-174">Sign in using a service principal</span></span>

<span data-ttu-id="e3045-175">Testa det nya tjänsthuvudnamnets autentiseringsuppgifter och behörigheter genom att logga in.</span><span class="sxs-lookup"><span data-stu-id="e3045-175">Test the new service principal's credentials and permissions by signing in.</span></span> <span data-ttu-id="e3045-176">Om du vill logga in med ett huvudnamn för tjänsten behöver du det `applicationId`-värde som är associerat med det, och den klient som det skapades under.</span><span class="sxs-lookup"><span data-stu-id="e3045-176">To sign in with a service principal, you need the `applicationId` value associated with it, and the tenant it was created under.</span></span>

<span data-ttu-id="e3045-177">Så här loggar du in med ett huvudnamn för tjänsten med lösenord:</span><span class="sxs-lookup"><span data-stu-id="e3045-177">To sign in with a service principal using a password:</span></span>

```azurepowershell-interactive
# Use the application ID as the username, and the secret as password
$credentials = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $credentials -Tenant <tenant ID>
```

<span data-ttu-id="e3045-178">För certifikatbaserad autentisering måste Azure PowerShell kunna hämta information från ett lokalt certifikatarkiv baserat på ett tumavtryck för certifikat.</span><span class="sxs-lookup"><span data-stu-id="e3045-178">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -Tenant <TenantId> -CertificateThumbprint <Thumbprint> -ApplicationId <ApplicationId>
```

<span data-ttu-id="e3045-179">Anvisningar för hur du importerar ett certifikat i ett arkiv för autentiseringsuppgifter som är tillgängliga från PowerShell finns i [Logga in med Azure PowerShell](authenticate-azureps.md#sp-signin)</span><span class="sxs-lookup"><span data-stu-id="e3045-179">For instructions on importing a certificate into a credential store accessible by PowerShell, see [Sign in with Azure PowerShell](authenticate-azureps.md#sp-signin)</span></span>

## <a name="reset-credentials"></a><span data-ttu-id="e3045-180">Återställ autentiseringsuppgifter</span><span class="sxs-lookup"><span data-stu-id="e3045-180">Reset credentials</span></span>

<span data-ttu-id="e3045-181">Om du glömmer bort autentiseringsuppgifterna för ett huvudnamn för tjänsten läggar du till en ny autentiseringsuppgift med ett slumpmässigt lösenord med hjälp av [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential).</span><span class="sxs-lookup"><span data-stu-id="e3045-181">If you forget the credentials for a service principal, use [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) to add a new credential with a random password.</span></span> <span data-ttu-id="e3045-182">Denna cmdlet stöder inte användardefinierade autentiseringsuppgifter när du återställer lösenordet.</span><span class="sxs-lookup"><span data-stu-id="e3045-182">This cmdlet does not support user-defined credentials when resetting the password.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e3045-183">Innan du tilldelar några nya autentiseringsuppgifter kan du ta bort befintliga autentiseringsuppgifter för att förhindra att de används för inloggning.</span><span class="sxs-lookup"><span data-stu-id="e3045-183">Before assigning any new credentials, you may want to remove existing credentials to prevent sign in with them.</span></span> <span data-ttu-id="e3045-184">Det gör du med cmdleten [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential):</span><span class="sxs-lookup"><span data-stu-id="e3045-184">To do so, use the [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) cmdlet:</span></span>

```azurepowershell-interactive
Remove-AzADSpCredential -DisplayName ServicePrincipalName
```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -ServicePrincipalName ServicePrincipalName
```

## <a name="troubleshooting"></a><span data-ttu-id="e3045-185">Felsökning</span><span class="sxs-lookup"><span data-stu-id="e3045-185">Troubleshooting</span></span>

<span data-ttu-id="e3045-186">Om du får följande fel: _"New-AzADServicePrincipal: Ett annat objekt med samma värde för egenskapen identifierUris finns redan."_ så kontrollerar du att det inte redan finns ett tjänsthuvudnamn med samma namn.</span><span class="sxs-lookup"><span data-stu-id="e3045-186">If you receive the error: _"New-AzADServicePrincipal: Another object with the same value for property identifierUris already exists."_, verify that a service principal with the same name doesn't already exist.</span></span>

```azurepowershell-interactive
Get-AzAdServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="e3045-187">Om det befintliga tjänsthuvudnamnet inte längre behövs kan du ta bort det med hjälp av följande exempel.</span><span class="sxs-lookup"><span data-stu-id="e3045-187">If the existing service principal is no longer needed, you can remove it using the following example.</span></span>

```azurepowershell-interactive
Remove-AzAdServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="e3045-188">Det här felet kan också inträffa om du tidigare har skapat ett tjänsthuvudnamn för ett Azure Active Directory-program.</span><span class="sxs-lookup"><span data-stu-id="e3045-188">This error can also occur when you've previously created a service principal for an Azure Active Directory application.</span></span> <span data-ttu-id="e3045-189">Om du tar bort tjänsthuvudnamnet är programmet fortfarande tillgängligt.</span><span class="sxs-lookup"><span data-stu-id="e3045-189">If you remove the service principal, the application is still available.</span></span> <span data-ttu-id="e3045-190">Det här programmet förhindrar att du skapar ett annat tjänsthuvudnamn med samma namn.</span><span class="sxs-lookup"><span data-stu-id="e3045-190">This application prevents you from creating another service principal with the same name.</span></span>

<span data-ttu-id="e3045-191">Du kan använda följande exempel för att kontrollera att det inte finns något Azure Active Directory-program med samma namn:</span><span class="sxs-lookup"><span data-stu-id="e3045-191">You can use the following example to verify that an Azure Active Directory application with the same name doesn't exist:</span></span>

```azurepowershell-interactive
Get-AzADApplication -DisplayName ServicePrincipalName
```

<span data-ttu-id="e3045-192">Om det finns ett program med samma namn som inte längre behövs så kan det tas bort med hjälp av följande exempel.</span><span class="sxs-lookup"><span data-stu-id="e3045-192">If an application with the same name does exist and is no longer needed, it can be removed using the following example.</span></span>

```azurepowershell-interactive
Remove-AzADApplication -DisplayName ServicePrincipalName
```

<span data-ttu-id="e3045-193">Annars väljer du ett alternativt namn för det nya huvudtjänstnamn som du försöker skapa.</span><span class="sxs-lookup"><span data-stu-id="e3045-193">Otherwise, choose an alternate name for the new service principal that you're attempting to create.</span></span>
