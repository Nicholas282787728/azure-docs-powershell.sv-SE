---
title: Skapa tjänstens huvudnamn för Azure med Azure PowerShell
description: Lär dig hur du skapar ett huvudnamn för tjänsten för din app eller tjänst med Azure PowerShell.
keywords: Azure PowerShell, Azure Active Directory, Azure Active directory, AD, RBAC
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 3e1c5ad280bdb29ce479dd0a478d0ed58237f969
ms.sourcegitcommit: 797c18f93aaa495ef005993b2e202d7378588dfa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/19/2018
ms.locfileid: "53595164"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="5a8a7-104">Skapa tjänstens huvudnamn för Azure med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="5a8a7-104">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="5a8a7-105">Om du planerar att hantera appen eller tjänsten med Azure PowerShell bör du köra denna under tjänstens huvudnamn för Azure Active Directory (AAD), i stället för dina autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="5a8a7-105">If you plan to manage your app or service with Azure PowerShell, you should run it under an Azure Active Directory (AAD) service principal, rather than your own credentials.</span></span> <span data-ttu-id="5a8a7-106">Den här artikeln vägleder dig genom att skapa ett säkerhetsobjekt med Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5a8a7-106">This article steps you through creating a security principal with Azure PowerShell.</span></span>

## <a name="what-is-a-service-principal"></a><span data-ttu-id="5a8a7-107">Vad är ett huvudnamn för tjänsten?</span><span class="sxs-lookup"><span data-stu-id="5a8a7-107">What is a service principal?</span></span>

<span data-ttu-id="5a8a7-108">Ett huvudnamn för Azure-tjänsten är en säkerhetsidentitet som används av appar som skapats av användare, tjänster och automatiseringsverktyg för att få åtkomst till specifika Azure-resurser.</span><span class="sxs-lookup"><span data-stu-id="5a8a7-108">An Azure service principal is a security identity used by user-created apps, services, and automation tools to access specific Azure resources.</span></span> <span data-ttu-id="5a8a7-109">Huvudnamn för tjänster tilldelas specifika behörigheter som är relaterade till tjänstens uppgifter, vilket ger dig bättre säkerhetskontroll.</span><span class="sxs-lookup"><span data-stu-id="5a8a7-109">Service principals are assigned specific permissions related to their tasks, giving you better security control.</span></span> <span data-ttu-id="5a8a7-110">Detta skiljer sig från en allmän användaridentitet, som vanligtvis har behörighet att göra ändringar.</span><span class="sxs-lookup"><span data-stu-id="5a8a7-110">This is unlike a general user identity, which is usually authorized to make any changes.</span></span>

## <a name="verify-your-own-permission-level"></a><span data-ttu-id="5a8a7-111">Kontrollera din egen behörighetsnivå</span><span class="sxs-lookup"><span data-stu-id="5a8a7-111">Verify your own permission level</span></span>

<span data-ttu-id="5a8a7-112">Först måste du ha tillräcklig behörighet i Azure Active Directory och Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="5a8a7-112">First, you must have sufficient permissions in both your Azure Active Directory and your Azure subscription.</span></span> <span data-ttu-id="5a8a7-113">Du måste kunna skapa en app i Active Directory och tilldela en roll till tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="5a8a7-113">You must be able to create an app in the Active Directory and assign a role to the service principal.</span></span>

<span data-ttu-id="5a8a7-114">Det enklaste sättet att kontrollera om kontot har rätt behörighet är via portalen.</span><span class="sxs-lookup"><span data-stu-id="5a8a7-114">The easiest way to check whether your account has the right permissions is through the portal.</span></span> <span data-ttu-id="5a8a7-115">Se [Kontrollera behörighet som krävs i portalen](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span><span class="sxs-lookup"><span data-stu-id="5a8a7-115">See [Check required permission in portal](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span></span>

## <a name="create-a-service-principal-for-your-app"></a><span data-ttu-id="5a8a7-116">Skapa ett huvudnamn för tjänsten för appen</span><span class="sxs-lookup"><span data-stu-id="5a8a7-116">Create a service principal for your app</span></span>

<span data-ttu-id="5a8a7-117">När du är inloggad på ditt Azure-konto kan du skapa tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="5a8a7-117">Once signed in to your Azure account, you can create the service principal.</span></span> <span data-ttu-id="5a8a7-118">Du måste ha någon av följande metoder för att identifiera den distribuerade appen:</span><span class="sxs-lookup"><span data-stu-id="5a8a7-118">You must have one of the following ways to identify your deployed app:</span></span>

* <span data-ttu-id="5a8a7-119">Den distribuerade appens unika namn, till exempel "MyDemoWebApp", i följande exempel</span><span class="sxs-lookup"><span data-stu-id="5a8a7-119">The unique name of your deployed app, such as "MyDemoWebApp" in the following examples</span></span>
* <span data-ttu-id="5a8a7-120">Program-ID, unikt GUID som är kopplat till den distribuerade appen, tjänsten eller objektet</span><span class="sxs-lookup"><span data-stu-id="5a8a7-120">The Application ID, the unique GUID associated with your deployed app, service, or object</span></span>

### <a name="get-information-about-your-application"></a><span data-ttu-id="5a8a7-121">Hämta information om programmet</span><span class="sxs-lookup"><span data-stu-id="5a8a7-121">Get information about your application</span></span>

<span data-ttu-id="5a8a7-122">Cmdleten `Get-AzADApplication` kan användas för att hämta information om programmet.</span><span class="sxs-lookup"><span data-stu-id="5a8a7-122">The `Get-AzADApplication` cmdlet can be used to get information about your application.</span></span>

```azurepowershell-interactive
$app = Get-AzADApplication -DisplayNameStartWith MyDemoWebApp
$app
```

```output
DisplayName             : MyDemoWebApp
ObjectId                : 775f64cd-0ec8-4b9b-b69a-8b8946022d9f
IdentifierUris          : {http://MyDemoWebApp}
HomePage                : http://www.contoso.com
Type                    : Application
ApplicationId           : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
AvailableToOtherTenants : False
AppPermissions          :
ReplyUrls               : {}
```

### <a name="create-a-service-principal-for-your-application"></a><span data-ttu-id="5a8a7-123">Skapa ett huvudnamn för tjänsten för programmet</span><span class="sxs-lookup"><span data-stu-id="5a8a7-123">Create a service principal for your application</span></span>

<span data-ttu-id="5a8a7-124">Cmdleten `New-AzADServicePrincipal` används för att skapa tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="5a8a7-124">The `New-AzADServicePrincipal` cmdlet is used to create the service principal.</span></span>

```azurepowershell-interactive
$servicePrincipal = New-AzADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4
```

```output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00c01aaa-1603-49fc-b6df-b78c4e5138b4, http://MyDemoWebApp}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
AdfsId                :
Type                  : ServicePrincipal
```

<span data-ttu-id="5a8a7-125">Härifrån kan du antingen direkt använda egenskapen `$servicePrincipal.Secret` som ett argument till `Connect-AzAccount` (se ”Logga in med tjänstens huvudnamn”) eller konvertera denna `SecureString` till en oformaterad textsträng:</span><span class="sxs-lookup"><span data-stu-id="5a8a7-125">From here, you can either directly use the `$servicePrincipal.Secret` property as an argument to `Connect-AzAccount` (see "Sign in using the service principal"), or you can convert this `SecureString` to a plain text string:</span></span>

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($servicePrincipal.Secret)
$password = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
[Runtime.InteropServices.Marshal]::ZeroFreeBSTR($BSTR)
```

### <a name="sign-in-using-the-service-principal"></a><span data-ttu-id="5a8a7-126">Logga in med tjänstens huvudnamn</span><span class="sxs-lookup"><span data-stu-id="5a8a7-126">Sign in using the service principal</span></span>

<span data-ttu-id="5a8a7-127">Nu kan du logga in som det nya huvudnamnet för tjänsten för appen med hjälp av det `appId` du angav och det `password` som</span><span class="sxs-lookup"><span data-stu-id="5a8a7-127">You can now sign in as the new service principal for your app using the `appId` you provided and `password` that was</span></span>  
<span data-ttu-id="5a8a7-128">genererades.</span><span class="sxs-lookup"><span data-stu-id="5a8a7-128">generated.</span></span> <span data-ttu-id="5a8a7-129">Du behöver också klient-ID:t för tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="5a8a7-129">You also need the Tenant ID for the service principal.</span></span> <span data-ttu-id="5a8a7-130">Ditt klient-ID visas när du loggar in på Azure med dina personliga autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="5a8a7-130">Your Tenant ID is displayed when you sign into Azure with your personal credentials.</span></span> <span data-ttu-id="5a8a7-131">Använd de här kommandona för att logga in med ett huvudnamn för tjänsten:</span><span class="sxs-lookup"><span data-stu-id="5a8a7-131">To sign in with a service principal, use the commands:</span></span>

```azurepowershell-interactive
$cred = New-Object System.Management.Automation.PSCredential ("00c01aaa-1603-49fc-b6df-b78c4e5138b4", $servicePrincipal.Secret)
Connect-AzAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="5a8a7-132">Efter en lyckad inloggning visas utdata som liknar följande:</span><span class="sxs-lookup"><span data-stu-id="5a8a7-132">After a successful sign-in you see output like:</span></span>

```output
Environment           : AzureCloud
Account               : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
SubscriptionId        :
SubscriptionName      :
CurrentStorageAccount :
```

<span data-ttu-id="5a8a7-133">Grattis!</span><span class="sxs-lookup"><span data-stu-id="5a8a7-133">Congratulations!</span></span> <span data-ttu-id="5a8a7-134">Du kan använda dessa autentiseringsuppgifter för att köra appen.</span><span class="sxs-lookup"><span data-stu-id="5a8a7-134">You can use these credentials to run your app.</span></span> <span data-ttu-id="5a8a7-135">Därefter måste du justera behörigheterna för tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="5a8a7-135">Next, you need to adjust the permissions of the service principal.</span></span>

## <a name="managing-roles"></a><span data-ttu-id="5a8a7-136">Hantera roller</span><span class="sxs-lookup"><span data-stu-id="5a8a7-136">Managing roles</span></span>

> [!NOTE]
> <span data-ttu-id="5a8a7-137">Rollbaserad åtkomst i Azure (RBAC) är en modell för att definiera och hantera roller för användar- och säkerhetsobjekt.</span><span class="sxs-lookup"><span data-stu-id="5a8a7-137">Azure Role-Based Access Control (RBAC) is a model for defining and managing roles for user and service principals.</span></span> <span data-ttu-id="5a8a7-138">Rollerna är kopplade till en uppsättning med behörigheter, som avgör vilka resurser en princip kan läsa, få åtkomst till, skriva till eller hantera.</span><span class="sxs-lookup"><span data-stu-id="5a8a7-138">Roles have sets of permissions associated with them, which determine the resources a principal can read, access, write, or manage.</span></span> <span data-ttu-id="5a8a7-139">Mer information om RBAC och roller finns i [RBAC: inbyggda roller](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="5a8a7-139">For more information on RBAC and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="5a8a7-140">Azure PowerShell tillhandahåller följande cmdletar för att hantera rolltilldelningar:</span><span class="sxs-lookup"><span data-stu-id="5a8a7-140">Azure PowerShell provides the following cmdlets to manage role assignments:</span></span>

* [<span data-ttu-id="5a8a7-141">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="5a8a7-141">Get-AzRoleAssignment</span></span>](/powershell/module/az.resources/get-azroleassignment)
* [<span data-ttu-id="5a8a7-142">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="5a8a7-142">New-AzRoleAssignment</span></span>](/powershell/module/az.resources/new-azroleassignment)
* [<span data-ttu-id="5a8a7-143">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="5a8a7-143">Remove-AzRoleAssignment</span></span>](/powershell/module/az.resources/remove-azroleassignment)

<span data-ttu-id="5a8a7-144">Standardrollen för tjänstens huvudnamn är **Deltagare**.</span><span class="sxs-lookup"><span data-stu-id="5a8a7-144">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="5a8a7-145">Det kanske inte är det bästa valet beroende på omfattningen av appens interaktioner med Azure-tjänster, med tanke på dess breda behörighet.</span><span class="sxs-lookup"><span data-stu-id="5a8a7-145">It may not be the best choice depending on the scope of your app's interactions with Azure services, given its broad permissions.</span></span>
<span data-ttu-id="5a8a7-146">Rollen **Läsare** är mer begränsad och kan vara ett bra val för skrivskyddade appar.</span><span class="sxs-lookup"><span data-stu-id="5a8a7-146">The **Reader** role is more restrictive and can be a good choice for read-only apps.</span></span> <span data-ttu-id="5a8a7-147">Du kan visa information om rollspecifik behörighet eller skapa anpassad behörighet via Azure Portal.</span><span class="sxs-lookup"><span data-stu-id="5a8a7-147">You can view details on role-specific permissions or create custom ones through the Azure portal.</span></span>

<span data-ttu-id="5a8a7-148">I det här exemplet lägger vi till rollen **Läsare** i vårt tidigare exempel och tar bort rollen **Deltagare**:</span><span class="sxs-lookup"><span data-stu-id="5a8a7-148">In this example, we add the **Reader** role to our prior example, and delete the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/818892f2-d075-46a1-a3a2-3a4e1a12fcd5
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : b24988ac-6180-42a0-ab88-20f7382dd24c
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

```azurepowershell-interactive
Remove-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

<span data-ttu-id="5a8a7-149">Visa de tilldelade rollerna:</span><span class="sxs-lookup"><span data-stu-id="5a8a7-149">To view the current roles assigned:</span></span>

```azurepowershell-interactive
Get-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/0906bbd8-9982-4c03-8dae-aeaae8b13f9e
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : acdd72a7-3385-48ef-bd42-f606fba81ae7
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

<span data-ttu-id="5a8a7-150">Andra Azure PowerShell-cmdletar för rollhantering:</span><span class="sxs-lookup"><span data-stu-id="5a8a7-150">Other Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="5a8a7-151">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="5a8a7-151">Get-AzRoleDefinition</span></span>](/powershell/module/az.resources/Get-azRoleDefinition)
* [<span data-ttu-id="5a8a7-152">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="5a8a7-152">New-AzRoleDefinition</span></span>](/powershell/module/az.resources/New-azRoleDefinition)
* [<span data-ttu-id="5a8a7-153">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="5a8a7-153">Remove-AzRoleDefinition</span></span>](/powershell/module/az.resources/Remove-azRoleDefinition)
* [<span data-ttu-id="5a8a7-154">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="5a8a7-154">Set-AzRoleDefinition</span></span>](/powershell/module/az.resources/Set-azRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a><span data-ttu-id="5a8a7-155">Ändra autentiseringsuppgifter för säkerhetsobjektet</span><span class="sxs-lookup"><span data-stu-id="5a8a7-155">Change the credentials of the security principal</span></span>

<span data-ttu-id="5a8a7-156">Det är en bra säkerhetsrutin att granska behörigheter och uppdatera lösenordet regelbundet.</span><span class="sxs-lookup"><span data-stu-id="5a8a7-156">It's a good security practice to review the permissions and update the password regularly.</span></span> <span data-ttu-id="5a8a7-157">Du kanske också vill hantera och ändra säkerhetsreferenser när appen förändras.</span><span class="sxs-lookup"><span data-stu-id="5a8a7-157">You may also want to manage and modify the security credentials as your app changes.</span></span> <span data-ttu-id="5a8a7-158">Det går till exempel att ändra lösenordet för tjänstens huvudnamn genom att skapa ett nytt lösenord och ta bort det gamla.</span><span class="sxs-lookup"><span data-stu-id="5a8a7-158">For example, we can change the password of the service principal by creating a new password and removing the old one.</span></span>

### <a name="add-a-new-password-for-the-service-principal"></a><span data-ttu-id="5a8a7-159">Lägga till ett nytt lösenord för tjänstens huvudnamn</span><span class="sxs-lookup"><span data-stu-id="5a8a7-159">Add a new password for the service principal</span></span>

```azurepowershell-interactive
New-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
Secret    : System.Security.SecureString
StartDate : 11/16/2018 12:38:23 AM
EndDate   : 11/16/2019 12:38:23 AM
KeyId     : 6f801c3e-6fcd-42b9-be8e-320b17ba1d36
Type      : Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="5a8a7-160">Hämta en lista över autentiseringsuppgifter för tjänstens huvudnamn</span><span class="sxs-lookup"><span data-stu-id="5a8a7-160">Get a list of credentials for the service principal</span></span>

```azurepowershell-interactive
Get-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a><span data-ttu-id="5a8a7-161">Ta bort det gamla lösenordet för tjänstens huvudnamn</span><span class="sxs-lookup"><span data-stu-id="5a8a7-161">Remove the old password from the service principal</span></span>

```azurepowershell-interactive
Remove-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```output
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="5a8a7-162">Bekräfta listan över autentiseringsuppgifter för tjänstens huvudnamn</span><span class="sxs-lookup"><span data-stu-id="5a8a7-162">Verify the list of credentials for the service principal</span></span>

```azurepowershell-interactive
Get-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-information-about-the-service-principal"></a><span data-ttu-id="5a8a7-163">Hämta information om tjänstens huvudnamn</span><span class="sxs-lookup"><span data-stu-id="5a8a7-163">Get information about the service principal</span></span>

```azurepowershell-interactive
$svcprincipal = Get-AzADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```output
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```
