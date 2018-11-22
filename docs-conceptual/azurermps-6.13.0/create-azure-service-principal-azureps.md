---
title: Skapa tjänstens huvudnamn för Azure med Azure PowerShell
description: Lär dig hur du skapar ett huvudnamn för tjänsten för din app eller tjänst med Azure PowerShell.
keywords: Azure PowerShell, Azure Active Directory, Azure Active directory, AD, RBAC
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 433a638187f024883c177457e420a759968fed9a
ms.sourcegitcommit: 80a3da199954d0ab78765715fb49793e89a30f12
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/22/2018
ms.locfileid: "52259933"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="e88c1-104">Skapa tjänstens huvudnamn för Azure med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="e88c1-104">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="e88c1-105">Om du planerar att hantera appen eller tjänsten med Azure PowerShell bör du köra denna under tjänstens huvudnamn för Azure Active Directory (AAD), i stället för dina autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="e88c1-105">If you plan to manage your app or service with Azure PowerShell, you should run it under an Azure Active Directory (AAD) service principal, rather than your own credentials.</span></span> <span data-ttu-id="e88c1-106">Den här artikeln vägleder dig genom att skapa ett säkerhetsobjekt med Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e88c1-106">This article steps you through creating a security principal with Azure PowerShell.</span></span>

> [!NOTE]
> <span data-ttu-id="e88c1-107">Du kan också skapa ett huvudnamn för tjänsten via Azure Portal.</span><span class="sxs-lookup"><span data-stu-id="e88c1-107">You can also create a service principal through the Azure portal.</span></span> <span data-ttu-id="e88c1-108">Läs [Använd portalen för att skapa Active Directory-program och ett huvudnamn för tjänsten som får åtkomst till resurser](/azure/azure-resource-manager/resource-group-create-service-principal-portal) för mer information.</span><span class="sxs-lookup"><span data-stu-id="e88c1-108">Read [Use portal to create Active Directory application and service principal that can access resources](/azure/azure-resource-manager/resource-group-create-service-principal-portal) for more details.</span></span>

## <a name="what-is-a-service-principal"></a><span data-ttu-id="e88c1-109">Vad är ett huvudnamn för tjänsten?</span><span class="sxs-lookup"><span data-stu-id="e88c1-109">What is a 'service principal'?</span></span>

<span data-ttu-id="e88c1-110">Ett huvudnamn för Azure-tjänsten är en säkerhetsidentitet som används av appar som skapats av användare, tjänster och automatiseringsverktyg för att få åtkomst till specifika Azure-resurser.</span><span class="sxs-lookup"><span data-stu-id="e88c1-110">An Azure service principal is a security identity used by user-created apps, services, and automation tools to access specific Azure resources.</span></span> <span data-ttu-id="e88c1-111">Se det som en användaridentitet (användarnamn och lösenord eller certifikat) med en specifik roll och väl kontrollerade behörigheter.</span><span class="sxs-lookup"><span data-stu-id="e88c1-111">Think of it as a 'user identity' (username and password or certificate) with a specific role, and tightly controlled permissions.</span></span> <span data-ttu-id="e88c1-112">Ett huvudnamn för tjänsten bör bara behöva utföra vissa åtgärder, till skillnad från en allmän användaridentitet.</span><span class="sxs-lookup"><span data-stu-id="e88c1-112">A service principal should only need to do specific things, unlike a general user identity.</span></span> <span data-ttu-id="e88c1-113">Det ger bättre säkerhet om du bara ger den lägsta behörighetsnivån som krävs för att den ska kunna utföra sina administrativa uppgifter.</span><span class="sxs-lookup"><span data-stu-id="e88c1-113">It improves security if you only grant it the minimum permissions level needed to perform its management tasks.</span></span>

## <a name="verify-your-own-permission-level"></a><span data-ttu-id="e88c1-114">Kontrollera din egen behörighetsnivå</span><span class="sxs-lookup"><span data-stu-id="e88c1-114">Verify your own permission level</span></span>

<span data-ttu-id="e88c1-115">Först måste du ha tillräcklig behörighet i Azure Active Directory och Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="e88c1-115">First, you must have sufficient permissions in both your Azure Active Directory and your Azure subscription.</span></span> <span data-ttu-id="e88c1-116">Du måste kunna skapa en app i Active Directory och tilldela en roll till tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="e88c1-116">You must be able to create an app in the Active Directory and assign a role to the service principal.</span></span>

<span data-ttu-id="e88c1-117">Det enklaste sättet att kontrollera om kontot har rätt behörighet är via portalen.</span><span class="sxs-lookup"><span data-stu-id="e88c1-117">The easiest way to check whether your account has the right permissions is through the portal.</span></span> <span data-ttu-id="e88c1-118">Se [Kontrollera behörighet som krävs i portalen](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span><span class="sxs-lookup"><span data-stu-id="e88c1-118">See [Check required permission in portal](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span></span>

## <a name="create-a-service-principal-for-your-app"></a><span data-ttu-id="e88c1-119">Skapa ett huvudnamn för tjänsten för appen</span><span class="sxs-lookup"><span data-stu-id="e88c1-119">Create a service principal for your app</span></span>

<span data-ttu-id="e88c1-120">När du är inloggad på ditt Azure-konto kan du skapa tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="e88c1-120">Once signed in to your Azure account, you can create the service principal.</span></span> <span data-ttu-id="e88c1-121">Du måste ha någon av följande metoder för att identifiera den distribuerade appen:</span><span class="sxs-lookup"><span data-stu-id="e88c1-121">You must have one of the following ways to identify your deployed app:</span></span>

* <span data-ttu-id="e88c1-122">Det unika namnet för den distribuerade appen, t.ex. "MyDemoWebApp" i följande exempel, eller</span><span class="sxs-lookup"><span data-stu-id="e88c1-122">The unique name of your deployed app, such as "MyDemoWebApp" in the following examples, or</span></span>
* <span data-ttu-id="e88c1-123">program-ID, unikt GUID som är kopplat till den distribuerade appen, tjänsten eller objektet</span><span class="sxs-lookup"><span data-stu-id="e88c1-123">the Application ID, the unique GUID associated with your deployed app, service, or object</span></span>

### <a name="get-information-about-your-application"></a><span data-ttu-id="e88c1-124">Hämta information om programmet</span><span class="sxs-lookup"><span data-stu-id="e88c1-124">Get information about your application</span></span>

<span data-ttu-id="e88c1-125">Cmdleten `Get-AzureRmADApplication` kan användas för att hämta information om programmet.</span><span class="sxs-lookup"><span data-stu-id="e88c1-125">The `Get-AzureRmADApplication` cmdlet can be used to get information about your application.</span></span>

```azurepowershell-interactive
Get-AzureRmADApplication -DisplayNameStartWith MyDemoWebApp
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

### <a name="create-a-service-principal-for-your-application"></a><span data-ttu-id="e88c1-126">Skapa ett huvudnamn för tjänsten för programmet</span><span class="sxs-lookup"><span data-stu-id="e88c1-126">Create a service principal for your application</span></span>

<span data-ttu-id="e88c1-127">Cmdleten `New-AzureRmADServicePrincipal` används för att skapa tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="e88c1-127">The `New-AzureRmADServicePrincipal` cmdlet is used to create the service principal.</span></span>

```azurepowershell-interactive
Add-Type -Assembly System.Web
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
$securePassword = ConvertTo-SecureString -Force -AsPlainText -String $password
New-AzureRmADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4 -Password $securePassword
```

```output
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
MyDemoWebApp                   ServicePrincipal               698138e7-d7b6-4738-a866-b4e3081a69e4
```

### <a name="get-information-about-the-service-principal"></a><span data-ttu-id="e88c1-128">Hämta information om tjänstens huvudnamn</span><span class="sxs-lookup"><span data-stu-id="e88c1-128">Get information about the service principal</span></span>

```azurepowershell-interactive
$svcprincipal = Get-AzureRmADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```output
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```

### <a name="sign-in-using-the-service-principal"></a><span data-ttu-id="e88c1-129">Logga in med tjänstens huvudnamn</span><span class="sxs-lookup"><span data-stu-id="e88c1-129">Sign in using the service principal</span></span>

<span data-ttu-id="e88c1-130">Du kan nu logga in som det nya huvudnamnet för tjänsten för appen med hjälp av det *appId* och *lösenord* du angav.</span><span class="sxs-lookup"><span data-stu-id="e88c1-130">You can now sign in as the new service principal for your app using the *appId* and *password* you provided.</span></span> <span data-ttu-id="e88c1-131">Du behöver också klient-ID:t för tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="e88c1-131">You also need the Tenant ID for the service principal.</span></span> <span data-ttu-id="e88c1-132">Ditt klient-ID visas när du loggar in på Azure med dina personliga autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="e88c1-132">Your Tenant ID is displayed when you sign into Azure with your personal credentials.</span></span> <span data-ttu-id="e88c1-133">Använd följande kommandon för att logga in med ett huvudnamn för tjänsten:</span><span class="sxs-lookup"><span data-stu-id="e88c1-133">To sign in with a service principal, use the following commands:</span></span>

```azurepowershell-interactive
$cred = Get-Credential -UserName $svcprincipal.ApplicationId -Message "Enter Password"
Connect-AzureRmAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="e88c1-134">Efter en lyckad inloggning visas utdata som liknar följande:</span><span class="sxs-lookup"><span data-stu-id="e88c1-134">After a successful sign-in you see output like:</span></span>

```output
Environment           : AzureCloud
Account               : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
SubscriptionId        :
SubscriptionName      :
CurrentStorageAccount :
```

<span data-ttu-id="e88c1-135">Grattis!</span><span class="sxs-lookup"><span data-stu-id="e88c1-135">Congratulations!</span></span> <span data-ttu-id="e88c1-136">Du kan använda dessa autentiseringsuppgifter för att köra appen.</span><span class="sxs-lookup"><span data-stu-id="e88c1-136">You can use these credentials to run your app.</span></span> <span data-ttu-id="e88c1-137">Därefter måste du justera behörigheterna för tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="e88c1-137">Next, you need to adjust the permissions of the service principal.</span></span>

## <a name="managing-roles"></a><span data-ttu-id="e88c1-138">Hantera roller</span><span class="sxs-lookup"><span data-stu-id="e88c1-138">Managing roles</span></span>

> [!NOTE]
> <span data-ttu-id="e88c1-139">Rollbaserad åtkomst i Azure (RBAC) är en modell för att definiera och hantera roller för användar- och säkerhetsobjekt.</span><span class="sxs-lookup"><span data-stu-id="e88c1-139">Azure Role-Based Access Control (RBAC) is a model for defining and managing roles for user and service principals.</span></span> <span data-ttu-id="e88c1-140">Rollerna är kopplade till en uppsättning med behörigheter, som avgör vilka resurser en princip kan läsa, få åtkomst till, skriva till eller hantera.</span><span class="sxs-lookup"><span data-stu-id="e88c1-140">Roles have sets of permissions associated with them, which determine the resources a principal can read, access, write, or manage.</span></span> <span data-ttu-id="e88c1-141">Mer information om RBAC och roller finns i [RBAC: inbyggda roller](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="e88c1-141">For more information on RBAC and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="e88c1-142">Azure PowerShell tillhandahåller följande cmdletar för att hantera rolltilldelningar:</span><span class="sxs-lookup"><span data-stu-id="e88c1-142">Azure PowerShell provides the following cmdlets to manage role assignments:</span></span>

* [<span data-ttu-id="e88c1-143">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e88c1-143">Get-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/get-azurermroleassignment)
* [<span data-ttu-id="e88c1-144">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e88c1-144">New-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/new-azurermroleassignment)
* [<span data-ttu-id="e88c1-145">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e88c1-145">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/remove-azurermroleassignment)

<span data-ttu-id="e88c1-146">Standardrollen för tjänstens huvudnamn är **Deltagare**.</span><span class="sxs-lookup"><span data-stu-id="e88c1-146">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="e88c1-147">Det kanske inte är det bästa valet beroende på omfattningen av appens interaktioner med Azure-tjänster, med tanke på dess breda behörighet.</span><span class="sxs-lookup"><span data-stu-id="e88c1-147">It may not be the best choice depending on the scope of your app's interactions with Azure services, given its broad permissions.</span></span>
<span data-ttu-id="e88c1-148">Rollen **Läsare** är mer begränsad och kan vara ett bra val för skrivskyddade appar.</span><span class="sxs-lookup"><span data-stu-id="e88c1-148">The **Reader** role is more restrictive and can be a good choice for read-only apps.</span></span> <span data-ttu-id="e88c1-149">Du kan visa information om rollspecifik behörighet eller skapa anpassad behörighet via Azure Portal.</span><span class="sxs-lookup"><span data-stu-id="e88c1-149">You can view details on role-specific permissions or create custom ones through the Azure portal.</span></span>

<span data-ttu-id="e88c1-150">I det här exemplet lägger vi till rollen **Läsare** i vårt tidigare exempel och tar bort rollen **Deltagare**:</span><span class="sxs-lookup"><span data-stu-id="e88c1-150">In this example, we add the **Reader** role to our prior example, and delete the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
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
Remove-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

<span data-ttu-id="e88c1-151">Visa de tilldelade rollerna:</span><span class="sxs-lookup"><span data-stu-id="e88c1-151">To view the current roles assigned:</span></span>

```azurepowershell-interactive
Get-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
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

<span data-ttu-id="e88c1-152">Andra Azure PowerShell-cmdletar för rollhantering:</span><span class="sxs-lookup"><span data-stu-id="e88c1-152">Other Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="e88c1-153">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e88c1-153">Get-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="e88c1-154">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e88c1-154">New-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="e88c1-155">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e88c1-155">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="e88c1-156">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e88c1-156">Set-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Set-AzureRmRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a><span data-ttu-id="e88c1-157">Ändra autentiseringsuppgifter för säkerhetsobjektet</span><span class="sxs-lookup"><span data-stu-id="e88c1-157">Change the credentials of the security principal</span></span>

<span data-ttu-id="e88c1-158">Det är en bra säkerhetsrutin att granska behörigheter och uppdatera lösenordet regelbundet.</span><span class="sxs-lookup"><span data-stu-id="e88c1-158">It's a good security practice to review the permissions and update the password regularly.</span></span> <span data-ttu-id="e88c1-159">Du kanske också vill hantera och ändra säkerhetsreferenser när appen förändras.</span><span class="sxs-lookup"><span data-stu-id="e88c1-159">You may also want to manage and modify the security credentials as your app changes.</span></span> <span data-ttu-id="e88c1-160">Det går till exempel att ändra lösenordet för tjänstens huvudnamn genom att skapa ett nytt lösenord och ta bort det gamla.</span><span class="sxs-lookup"><span data-stu-id="e88c1-160">For example, we can change the password of the service principal by creating a new password and removing the old one.</span></span>

### <a name="add-a-new-password-for-the-service-principal"></a><span data-ttu-id="e88c1-161">Lägga till ett nytt lösenord för tjänstens huvudnamn</span><span class="sxs-lookup"><span data-stu-id="e88c1-161">Add a new password for the service principal</span></span>

```azurepowershell-interactive
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
New-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -Password $password
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="e88c1-162">Hämta en lista över autentiseringsuppgifter för tjänstens huvudnamn</span><span class="sxs-lookup"><span data-stu-id="e88c1-162">Get a list of credentials for the service principal</span></span>

```azurepowershell-interactive
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a><span data-ttu-id="e88c1-163">Ta bort det gamla lösenordet för tjänstens huvudnamn</span><span class="sxs-lookup"><span data-stu-id="e88c1-163">Remove the old password from the service principal</span></span>

```azurepowershell-interactive
Remove-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```output
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="e88c1-164">Bekräfta listan över autentiseringsuppgifter för tjänstens huvudnamn</span><span class="sxs-lookup"><span data-stu-id="e88c1-164">Verify the list of credentials for the service principal</span></span>

```azurepowershell-interactive
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```
