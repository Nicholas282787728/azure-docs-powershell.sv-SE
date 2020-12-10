---
title: Använd huvudnamn för tjänsten i Azure med Azure PowerShell
description: Lär dig hur du skapar och använder huvudnamn för tjänsten med Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.service: azure-powershell
ms.date: 06/17/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: a5640ded6fc8c6478084374f7808450f6a99d6e5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "96856836"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="6618f-103">Skapa tjänstens huvudnamn för Azure med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="6618f-103">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="6618f-104">Automatiserade verktyg som använder Azure-tjänster bör alltid ha begränsad behörighet.</span><span class="sxs-lookup"><span data-stu-id="6618f-104">Automated tools that use Azure services should always have restricted permissions.</span></span> <span data-ttu-id="6618f-105">Azure erbjuder tjänstens huvudnamn i stället för att programmen loggar in som användare med fullständig behörighet.</span><span class="sxs-lookup"><span data-stu-id="6618f-105">Instead of having applications sign in as a fully privileged user, Azure offers service principals.</span></span>

<span data-ttu-id="6618f-106">Ett huvudnamn för tjänsten i Azure är en identitet som skapas för användning med program, värdbaserade tjänster och automatiserade verktyg för att tillgång till Azure-resurser.</span><span class="sxs-lookup"><span data-stu-id="6618f-106">An Azure service principal is an identity created for use with applications, hosted services, and automated tools to access Azure resources.</span></span> <span data-ttu-id="6618f-107">Åtkomsten begränsas av de roller som tilldelas tjänstens huvudnamn, vilket ger dig kontroll över vilka resurser som kan nås och på vilken nivå.</span><span class="sxs-lookup"><span data-stu-id="6618f-107">This access is restricted by the roles assigned to the service principal, giving you control over which resources can be accessed and at which level.</span></span> <span data-ttu-id="6618f-108">Av säkerhetsskäl rekommenderar vi att du alltid använder tjänstens huvudnamn med automatiserade verktyg i stället för att tillåta inloggning med en användaridentitet.</span><span class="sxs-lookup"><span data-stu-id="6618f-108">For security reasons, it's always recommended to use service principals with automated tools rather than allowing them to log in with a user identity.</span></span>

<span data-ttu-id="6618f-109">Den här artikeln visar hur du skapar, hämtar information om och återställer ett tjänsthuvudnamn med Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6618f-109">This article shows you the steps for creating, getting information about, and resetting a service principal with Azure PowerShell.</span></span>

> [!WARNING]
> <span data-ttu-id="6618f-110">När du skapar tjänstens huvudnamn med kommandot [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) innehåller utdata autentiseringsuppgifter som du måste skydda.</span><span class="sxs-lookup"><span data-stu-id="6618f-110">When you create a service principal using the [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="6618f-111">Se till att du inte inkluderar dessa autentiseringsuppgifter i din kod eller kontrollera autentiseringsuppgifterna i källkontrollen.</span><span class="sxs-lookup"><span data-stu-id="6618f-111">Be sure that you do not include these credentials in your code or check the credentials into your source control.</span></span> <span data-ttu-id="6618f-112">Alternativt bör du överväga att använda [hanterade identiteter](/azure/active-directory/managed-identities-azure-resources/overview) för att undvika att behöva använda autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="6618f-112">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="6618f-113">Som standard tilldelar [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) [deltagarrollen](/azure/role-based-access-control/built-in-roles#contributor) till tjänstens huvudnamn i prenumerationsomfånget.</span><span class="sxs-lookup"><span data-stu-id="6618f-113">By default, [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="6618f-114">Om du vill minska risken för att tjänstens huvudnamn komprometteras tilldelar du en mer specifik roll och begränsar omfånget för en resurs eller resursgrupp.</span><span class="sxs-lookup"><span data-stu-id="6618f-114">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="6618f-115">Mer information finns i [Steg för tillägg av en rolltilldelning](/azure/role-based-access-control/role-assignments-steps).</span><span class="sxs-lookup"><span data-stu-id="6618f-115">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <a name="create-a-service-principal"></a><span data-ttu-id="6618f-116">Skapa ett huvudnamn för tjänsten</span><span class="sxs-lookup"><span data-stu-id="6618f-116">Create a service principal</span></span>

<span data-ttu-id="6618f-117">Skapa ett huvudnamn för tjänsten med cmdleten [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal).</span><span class="sxs-lookup"><span data-stu-id="6618f-117">Create a service principal with the [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) cmdlet.</span></span> <span data-ttu-id="6618f-118">När du skapar ett huvudnamn för tjänsten kan du välja vilken typ av inloggningsinformation som används.</span><span class="sxs-lookup"><span data-stu-id="6618f-118">When creating a service principal, you choose the type of sign-in authentication it uses.</span></span>

> [!NOTE]
> <span data-ttu-id="6618f-119">Om ditt konto inte har behörighet att skapa ett tjänsthuvudnamn visar `New-AzADServicePrincipal` ett felmeddelande om att du inte har rätt behörigheter för att slutföra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="6618f-119">If your account doesn't have permission to create a service principal, `New-AzADServicePrincipal` will return an error message containing "Insufficient privileges to complete the operation".</span></span>
> <span data-ttu-id="6618f-120">Kontakta Azure Active Directory-administratören om du vill skapa ett huvudnamn för tjänsten.</span><span class="sxs-lookup"><span data-stu-id="6618f-120">Contact your Azure Active Directory admin to create a service principal.</span></span>

<span data-ttu-id="6618f-121">Det finns två typer av autentisering för tjänstens huvudnamn: lösenordsbaserad autentisering och certifikatbaserad autentisering.</span><span class="sxs-lookup"><span data-stu-id="6618f-121">There are two types of authentication available for service principals: Password-based authentication, and certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="6618f-122">Lösenordsbaserad autentisering</span><span class="sxs-lookup"><span data-stu-id="6618f-122">Password-based authentication</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6618f-123">Standardrollen för ett huvudnamn för tjänsten för lösenordsbaserad autentisering är **Deltagare**.</span><span class="sxs-lookup"><span data-stu-id="6618f-123">The default role for a password-based authentication service principal is **Contributor**.</span></span> <span data-ttu-id="6618f-124">Den här rollen har fullständig behörighet att läsa och skriva till ett Azure-konto.</span><span class="sxs-lookup"><span data-stu-id="6618f-124">This role has full permissions to read and write to an Azure account.</span></span> <span data-ttu-id="6618f-125">Information om hur du hanterar rolltilldelningar finns i [Hantera roller för tjänstens huvudnamn](#manage-service-principal-roles).</span><span class="sxs-lookup"><span data-stu-id="6618f-125">For information on managing role assignments, see [Manage service principal roles](#manage-service-principal-roles).</span></span>

<span data-ttu-id="6618f-126">Om inga andra autentiseringsparametrar finns används lösenordsbaserad autentisering, och ett slumpmässigt lösenord skapas åt dig.</span><span class="sxs-lookup"><span data-stu-id="6618f-126">Without any other authentication parameters, password-based authentication is used and a random password created for you.</span></span> <span data-ttu-id="6618f-127">Om du vill använda lösenordsbaserad autentisering rekommenderas den här metoden.</span><span class="sxs-lookup"><span data-stu-id="6618f-127">If you want password-based authentication, this method is recommended.</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="6618f-128">Det returnerade objektet innehåller medlemmen `Secret`, som är en `SecureString` som innehåller det genererade lösenordet.</span><span class="sxs-lookup"><span data-stu-id="6618f-128">The returned object contains the `Secret` member, which is a `SecureString` containing the generated password.</span></span> <span data-ttu-id="6618f-129">Se till att värdet lagras på en säker plats för autentisering med tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="6618f-129">Make sure that you store this value somewhere secure to authenticate with the service principal.</span></span> <span data-ttu-id="6618f-130">Värdet visas _inte_ i konsolens utdata.</span><span class="sxs-lookup"><span data-stu-id="6618f-130">Its value _won't_ be displayed in the console output.</span></span> <span data-ttu-id="6618f-131">Om du tappar bort lösenordet måste du [återställa autentiseringsuppgifterna för tjänstens huvudnamn](#reset-credentials).</span><span class="sxs-lookup"><span data-stu-id="6618f-131">If you lose the password, [reset the service principal credentials](#reset-credentials).</span></span>

<span data-ttu-id="6618f-132">Med följande kod kan du exportera hemligheten:</span><span class="sxs-lookup"><span data-stu-id="6618f-132">The following code will allow you to export the secret:</span></span>

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($sp.Secret)
$UnsecureSecret = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
```

<span data-ttu-id="6618f-133">För lösenord som anges av användaren tar argumentet `-PasswordCredential` objekten `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential`.</span><span class="sxs-lookup"><span data-stu-id="6618f-133">For user-supplied passwords, the `-PasswordCredential` argument takes `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` objects.</span></span> <span data-ttu-id="6618f-134">Objekten måste ha ett giltigt `StartDate` och `EndDate` samt ett `Password` i klartext.</span><span class="sxs-lookup"><span data-stu-id="6618f-134">These objects must have a valid `StartDate` and `EndDate`, and take a plaintext `Password`.</span></span> <span data-ttu-id="6618f-135">Skapa ett starkt lösenord genom att följa [regler och begränsningar för Azure Active Directory-lösenord](/azure/active-directory/active-directory-passwords-policy).</span><span class="sxs-lookup"><span data-stu-id="6618f-135">When creating a password, make sure you follow the [Azure Active Directory password rules and restrictions](/azure/active-directory/active-directory-passwords-policy).</span></span>
<span data-ttu-id="6618f-136">Använd inte ett svagt lösenord och återanvänd aldrig lösenord.</span><span class="sxs-lookup"><span data-stu-id="6618f-136">Don't use a weak password or reuse a password.</span></span>

```azurepowershell-interactive
Import-Module -Name Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

<span data-ttu-id="6618f-137">Objektet som returnerades från `New-AzADServicePrincipal` innehåller medlemmarna `Id` och `DisplayName`, som båda kan användas för inloggning med tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="6618f-137">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6618f-138">För inloggning med tjänstens huvudnamn krävs det klientorganisations-ID som tjänstens huvudnamn skapades under.</span><span class="sxs-lookup"><span data-stu-id="6618f-138">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="6618f-139">För att få den klientorganisation som var aktiv när tjänstens huvudnamn skapades kör du följande kommando _omedelbart efter_ att tjänstens huvudnamn har skapats:</span><span class="sxs-lookup"><span data-stu-id="6618f-139">To get the active tenant when the service principal was created, run the following command _immediately after_ service principal creation:</span></span>

```azurepowershell-interactive
(Get-AzContext).Tenant.Id
```

### <a name="certificate-based-authentication"></a><span data-ttu-id="6618f-140">Certifikatbaserad autentisering</span><span class="sxs-lookup"><span data-stu-id="6618f-140">Certificate-based authentication</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6618f-141">Ingen standardroll tilldelas när du skapar en certifikatbaserad autentisering för tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="6618f-141">There is no default role assigned when creating a certificate-based authentication service principal.</span></span> <span data-ttu-id="6618f-142">Information om hur du hanterar rolltilldelningar finns i [Hantera roller för tjänstens huvudnamn](#manage-service-principal-roles).</span><span class="sxs-lookup"><span data-stu-id="6618f-142">For information on managing role assignments, see [Manage service principal roles](#manage-service-principal-roles).</span></span>

<span data-ttu-id="6618f-143">Tjänstens huvudnamn med certifikatbaserad autentisering skapas med parametern `-CertValue`.</span><span class="sxs-lookup"><span data-stu-id="6618f-143">Service principals using certificate-based authentication are created with the `-CertValue` parameter.</span></span> <span data-ttu-id="6618f-144">Denna parameter tar en base64-kodad ASCII-sträng för det offentliga certifikatet.</span><span class="sxs-lookup"><span data-stu-id="6618f-144">This parameter takes a base64-encoded ASCII string of the public certificate.</span></span> <span data-ttu-id="6618f-145">Detta representeras av en PEM-fil eller en textkodad CRT eller CER.</span><span class="sxs-lookup"><span data-stu-id="6618f-145">This is represented by a PEM file, or a text-encoded CRT or CER.</span></span> <span data-ttu-id="6618f-146">Binär kodning av det offentliga certifikatet stöds inte.</span><span class="sxs-lookup"><span data-stu-id="6618f-146">Binary encodings of the public certificate aren't supported.</span></span> <span data-ttu-id="6618f-147">I de här anvisningarna förutsätts att du redan har ett tillgängligt certifikat.</span><span class="sxs-lookup"><span data-stu-id="6618f-147">These instructions assume that you already have a certificate available.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

<span data-ttu-id="6618f-148">Du kan också använda parametern `-KeyCredential`, som tar `PSADKeyCredential`-objekt.</span><span class="sxs-lookup"><span data-stu-id="6618f-148">You can also use the `-KeyCredential` parameter, which takes `PSADKeyCredential` objects.</span></span> <span data-ttu-id="6618f-149">Objekten måste ha ett giltigt `StartDate` och `EndDate`, och medlemmen `CertValue` måste ha angetts till en base64-kodad ASCII-sträng för det offentliga certifikatet.</span><span class="sxs-lookup"><span data-stu-id="6618f-149">These objects must have a valid `StartDate`, `EndDate`, and have the `CertValue` member set to a base64-encoded ASCII string of the public certificate.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

<span data-ttu-id="6618f-150">Objektet som returnerades från `New-AzADServicePrincipal` innehåller medlemmarna `Id` och `DisplayName`, som båda kan användas för inloggning med tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="6618f-150">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span> <span data-ttu-id="6618f-151">Klienter som loggar in med tjänstens huvudnamn måste också ha åtkomst till certifikatets privata nyckel.</span><span class="sxs-lookup"><span data-stu-id="6618f-151">Clients which sign in with the service principal also need access to the certificate's private key.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6618f-152">För inloggning med tjänstens huvudnamn krävs det klientorganisations-ID som tjänstens huvudnamn skapades under.</span><span class="sxs-lookup"><span data-stu-id="6618f-152">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="6618f-153">För att få den klientorganisation som var aktiv när tjänstens huvudnamn skapades kör du följande kommando _omedelbart efter_ att tjänstens huvudnamn har skapats:</span><span class="sxs-lookup"><span data-stu-id="6618f-153">To get the active tenant when the service principal was created, run the following command _immediately after_ service principal creation:</span></span>

```azurepowershell-interactive
(Get-AzContext).Tenant.Id
```

## <a name="get-an-existing-service-principal"></a><span data-ttu-id="6618f-154">Hämta ett befintligt tjänsthuvudnamn</span><span class="sxs-lookup"><span data-stu-id="6618f-154">Get an existing service principal</span></span>

<span data-ttu-id="6618f-155">En lista över tjänsthuvudnamn för den aktiva klientorganisationen kan hämtas med [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal).</span><span class="sxs-lookup"><span data-stu-id="6618f-155">A list of service principals for the active tenant can be retrieved with [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal).</span></span> <span data-ttu-id="6618f-156">Som standard returnerar detta kommando _alla_ huvudnamn för tjänsten i en klientorganisation.</span><span class="sxs-lookup"><span data-stu-id="6618f-156">By default this command returns _all_ service principals in a tenant.</span></span> <span data-ttu-id="6618f-157">För stora organisationer kan det ta lång tid att returnera resultat.</span><span class="sxs-lookup"><span data-stu-id="6618f-157">For large organizations, it may take a long time to return results.</span></span> <span data-ttu-id="6618f-158">Vi rekommenderar att du i stället använder de valfria argumenten för filtrering på serversidan:</span><span class="sxs-lookup"><span data-stu-id="6618f-158">Instead, using one of the optional server-side filtering arguments is recommended:</span></span>

- <span data-ttu-id="6618f-159">`-DisplayNameBeginsWith` begär tjänsthuvudnamn som har ett _prefix_ som matchar det angivna värdet.</span><span class="sxs-lookup"><span data-stu-id="6618f-159">`-DisplayNameBeginsWith` requests service principals that have a _prefix_ that match the provided value.</span></span> <span data-ttu-id="6618f-160">Visningsnamnet för ett tjänsthuvudnamn är det värde som anges med `-DisplayName` när det skapas.</span><span class="sxs-lookup"><span data-stu-id="6618f-160">The display name of a service principal is the value set with `-DisplayName` during creation.</span></span>
- <span data-ttu-id="6618f-161">`-DisplayName` begär en _exakt matchning_ av tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="6618f-161">`-DisplayName` requests an _exact match_ of a service principal name.</span></span>

## <a name="manage-service-principal-roles"></a><span data-ttu-id="6618f-162">Hantera roller för tjänstens huvudnamn</span><span class="sxs-lookup"><span data-stu-id="6618f-162">Manage service principal roles</span></span>

<span data-ttu-id="6618f-163">Azure PowerShell har följande cmdletar för hantering av rolltilldelningar:</span><span class="sxs-lookup"><span data-stu-id="6618f-163">Azure PowerShell has the following cmdlets to manage role assignments:</span></span>

- [<span data-ttu-id="6618f-164">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="6618f-164">Get-AzRoleAssignment</span></span>](/powershell/module/az.resources/get-azroleassignment)
- [<span data-ttu-id="6618f-165">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="6618f-165">New-AzRoleAssignment</span></span>](/powershell/module/az.resources/new-azroleassignment)
- [<span data-ttu-id="6618f-166">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="6618f-166">Remove-AzRoleAssignment</span></span>](/powershell/module/az.resources/remove-azroleassignment)

<span data-ttu-id="6618f-167">Standardrollen för ett huvudnamn för tjänsten för lösenordsbaserad autentisering är **Deltagare**.</span><span class="sxs-lookup"><span data-stu-id="6618f-167">The default role for a password-based authentication service principal is **Contributor**.</span></span> <span data-ttu-id="6618f-168">Den här rollen har fullständig behörighet att läsa och skriva till ett Azure-konto.</span><span class="sxs-lookup"><span data-stu-id="6618f-168">This role has full permissions to read and write to an Azure account.</span></span> <span data-ttu-id="6618f-169">Rollen **Läsare** är mer begränsad och ger endast läsåtkomst.</span><span class="sxs-lookup"><span data-stu-id="6618f-169">The **Reader** role is more restrictive, with read-only access.</span></span> <span data-ttu-id="6618f-170">Mer information om rollbaserad åtkomstkontroll (RBAC) och roller finns i [RBAC: inbyggda roller](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="6618f-170">For more information on Role-Based Access Control (RBAC) and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="6618f-171">Det här exemplet lägger till rollen **Läsare** och tar bort rollen **Deltagare**:</span><span class="sxs-lookup"><span data-stu-id="6618f-171">This example adds the **Reader** role and removes the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName 'Reader'
Remove-AzRoleAssignment -ObjectId <service principal object ID> -RoleDefinitionName 'Contributor'
```

> [!IMPORTANT]
> <span data-ttu-id="6618f-172">Cmdletar för rolltilldelning tar inte tjänsthuvudnamnsobjektets ID.</span><span class="sxs-lookup"><span data-stu-id="6618f-172">Role assignment cmdlets don't take the service principal object ID.</span></span> <span data-ttu-id="6618f-173">De tar ID för det associerade programmet, som genereras vid tidpunkten för skapandet.</span><span class="sxs-lookup"><span data-stu-id="6618f-173">They take the associated application ID, which is generated at creation time.</span></span> <span data-ttu-id="6618f-174">Om du vill hämta program-ID:t för ett tjänsthuvudnamn använder du `Get-AzADServicePrincipal`.</span><span class="sxs-lookup"><span data-stu-id="6618f-174">To get the application ID for a service principal, use `Get-AzADServicePrincipal`.</span></span>

> [!NOTE]
> <span data-ttu-id="6618f-175">Om ditt konto inte har behörighet att tilldela en roll visas ett felmeddelande om att kontot inte har behörighet att utföra åtgärden "Microsoft.Authorization/roleAssignments/write".</span><span class="sxs-lookup"><span data-stu-id="6618f-175">If your account doesn't have permission to assign a role, you see an error message that your account "does not have authorization to perform action 'Microsoft.Authorization/roleAssignments/write'".</span></span> <span data-ttu-id="6618f-176">Kontakta Azure Active Directory-administratören om du vill hantera roller.</span><span class="sxs-lookup"><span data-stu-id="6618f-176">Contact your Azure Active Directory admin to manage roles.</span></span>

<span data-ttu-id="6618f-177">När en roll läggs till begränsas _inte_ tidigare tilldelade behörigheter.</span><span class="sxs-lookup"><span data-stu-id="6618f-177">Adding a role _doesn't_ restrict previously assigned permissions.</span></span> <span data-ttu-id="6618f-178">När du begränsar behörigheter för tjänstens huvudnamn bör rollen **Deltagare** tas bort.</span><span class="sxs-lookup"><span data-stu-id="6618f-178">When restricting a service principal's permissions, the **Contributor** role should be removed.</span></span>

<span data-ttu-id="6618f-179">Du bekräftar ändringarna genom att ange de roller som är tilldelade:</span><span class="sxs-lookup"><span data-stu-id="6618f-179">The changes can be verified by listing the assigned roles:</span></span>

```azurepowershell-interactive
Get-AzRoleAssignment -ServicePrincipalName ServicePrincipalName
```

## <a name="sign-in-using-a-service-principal"></a><span data-ttu-id="6618f-180">Logga in med ett tjänsthuvudnamn</span><span class="sxs-lookup"><span data-stu-id="6618f-180">Sign in using a service principal</span></span>

<span data-ttu-id="6618f-181">Testa det nya tjänsthuvudnamnets autentiseringsuppgifter och behörigheter genom att logga in.</span><span class="sxs-lookup"><span data-stu-id="6618f-181">Test the new service principal's credentials and permissions by signing in.</span></span> <span data-ttu-id="6618f-182">Om du vill logga in med ett huvudnamn för tjänsten behöver du det `applicationId`-värde som är associerat med det, och den klient som det skapades under.</span><span class="sxs-lookup"><span data-stu-id="6618f-182">To sign in with a service principal, you need the `applicationId` value associated with it, and the tenant it was created under.</span></span>

<span data-ttu-id="6618f-183">Så här loggar du in med ett huvudnamn för tjänsten med lösenord:</span><span class="sxs-lookup"><span data-stu-id="6618f-183">To sign in with a service principal using a password:</span></span>

```azurepowershell-interactive
# Use the application ID as the username, and the secret as password
$credentials = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $credentials -Tenant <tenant ID>
```

<span data-ttu-id="6618f-184">För certifikatbaserad autentisering måste Azure PowerShell kunna hämta information från ett lokalt certifikatarkiv baserat på ett tumavtryck för certifikat.</span><span class="sxs-lookup"><span data-stu-id="6618f-184">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -Tenant <TenantId> -CertificateThumbprint <Thumbprint> -ApplicationId <ApplicationId>
```

<span data-ttu-id="6618f-185">Anvisningar för hur du importerar ett certifikat i ett arkiv för autentiseringsuppgifter som är tillgängliga från PowerShell finns i [Logga in med Azure PowerShell](authenticate-azureps.md#sp-signin)</span><span class="sxs-lookup"><span data-stu-id="6618f-185">For instructions on importing a certificate into a credential store accessible by PowerShell, see [Sign in with Azure PowerShell](authenticate-azureps.md#sp-signin)</span></span>

## <a name="reset-credentials"></a><span data-ttu-id="6618f-186">Återställ autentiseringsuppgifter</span><span class="sxs-lookup"><span data-stu-id="6618f-186">Reset credentials</span></span>

<span data-ttu-id="6618f-187">Om du glömmer bort autentiseringsuppgifterna för ett huvudnamn för tjänsten läggar du till en ny autentiseringsuppgift med ett slumpmässigt lösenord med hjälp av [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential).</span><span class="sxs-lookup"><span data-stu-id="6618f-187">If you forget the credentials for a service principal, use [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) to add a new credential with a random password.</span></span> <span data-ttu-id="6618f-188">Denna cmdlet stöder inte användardefinierade autentiseringsuppgifter när du återställer lösenordet.</span><span class="sxs-lookup"><span data-stu-id="6618f-188">This cmdlet does not support user-defined credentials when resetting the password.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6618f-189">Innan du tilldelar några nya autentiseringsuppgifter kan du ta bort befintliga autentiseringsuppgifter för att förhindra att de används för inloggning.</span><span class="sxs-lookup"><span data-stu-id="6618f-189">Before assigning any new credentials, you may want to remove existing credentials to prevent sign in with them.</span></span> <span data-ttu-id="6618f-190">Det gör du med cmdleten [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential):</span><span class="sxs-lookup"><span data-stu-id="6618f-190">To do so, use the [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) cmdlet:</span></span>

```azurepowershell-interactive
Remove-AzADSpCredential -DisplayName ServicePrincipalName
```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -ServicePrincipalName ServicePrincipalName
```

## <a name="troubleshooting"></a><span data-ttu-id="6618f-191">Felsökning</span><span class="sxs-lookup"><span data-stu-id="6618f-191">Troubleshooting</span></span>

<span data-ttu-id="6618f-192">Om du får följande fel: _"New-AzADServicePrincipal: Ett annat objekt med samma värde för egenskapen identifierUris finns redan."_ så kontrollerar du att det inte redan finns ett tjänsthuvudnamn med samma namn.</span><span class="sxs-lookup"><span data-stu-id="6618f-192">If you receive the error: _"New-AzADServicePrincipal: Another object with the same value for property identifierUris already exists."_, verify that a service principal with the same name doesn't already exist.</span></span>

```azurepowershell-interactive
Get-AzAdServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="6618f-193">Om det befintliga tjänsthuvudnamnet inte längre behövs kan du ta bort det med hjälp av följande exempel.</span><span class="sxs-lookup"><span data-stu-id="6618f-193">If the existing service principal is no longer needed, you can remove it using the following example.</span></span>

```azurepowershell-interactive
Remove-AzAdServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="6618f-194">Det här felet kan också inträffa om du tidigare har skapat ett tjänsthuvudnamn för ett Azure Active Directory-program.</span><span class="sxs-lookup"><span data-stu-id="6618f-194">This error can also occur when you've previously created a service principal for an Azure Active Directory application.</span></span> <span data-ttu-id="6618f-195">Om du tar bort tjänsthuvudnamnet är programmet fortfarande tillgängligt.</span><span class="sxs-lookup"><span data-stu-id="6618f-195">If you remove the service principal, the application is still available.</span></span> <span data-ttu-id="6618f-196">Det här programmet förhindrar att du skapar ett annat tjänsthuvudnamn med samma namn.</span><span class="sxs-lookup"><span data-stu-id="6618f-196">This application prevents you from creating another service principal with the same name.</span></span>

<span data-ttu-id="6618f-197">Du kan använda följande exempel för att kontrollera att det inte finns något Azure Active Directory-program med samma namn:</span><span class="sxs-lookup"><span data-stu-id="6618f-197">You can use the following example to verify that an Azure Active Directory application with the same name doesn't exist:</span></span>

```azurepowershell-interactive
Get-AzADApplication -DisplayName ServicePrincipalName
```

<span data-ttu-id="6618f-198">Om det finns ett program med samma namn som inte längre behövs så kan det tas bort med hjälp av följande exempel.</span><span class="sxs-lookup"><span data-stu-id="6618f-198">If an application with the same name does exist and is no longer needed, it can be removed using the following example.</span></span>

```azurepowershell-interactive
Remove-AzADApplication -DisplayName ServicePrincipalName
```

<span data-ttu-id="6618f-199">Annars väljer du ett alternativt namn för det nya huvudtjänstnamn som du försöker skapa.</span><span class="sxs-lookup"><span data-stu-id="6618f-199">Otherwise, choose an alternate name for the new service principal that you're attempting to create.</span></span>
