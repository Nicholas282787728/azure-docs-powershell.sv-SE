---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: 96ff12056167adaabcb828e2fedfe0c78d59e963
ms.sourcegitcommit: 375232b84336ef5e13052504deaa43f5bd4b7f65
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/05/2020
ms.locfileid: "94326142"
---
# <span data-ttu-id="72f32-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="72f32-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="72f32-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="72f32-102">SYNOPSIS</span></span>
<span data-ttu-id="72f32-103">Skapar ett nytt objekt i Azure Active Directory-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="72f32-103">Creates a new azure active directory service principal.</span></span>

## <span data-ttu-id="72f32-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="72f32-104">SYNTAX</span></span>

### <span data-ttu-id="72f32-105">SimpleParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="72f32-105">SimpleParameterSet (Default)</span></span>
```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-Password <SecureString>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72f32-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="72f32-106">ApplicationWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72f32-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="72f32-107">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72f32-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="72f32-108">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72f32-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="72f32-109">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72f32-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="72f32-110">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72f32-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="72f32-111">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72f32-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="72f32-112">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72f32-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="72f32-113">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72f32-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="72f32-114">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72f32-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="72f32-115">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72f32-116">ApplicationObjectWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="72f32-116">ApplicationObjectWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72f32-117">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="72f32-117">ApplicationObjectWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -Password <SecureString>
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="72f32-118">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="72f32-118">ApplicationObjectWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication>
 -PasswordCredential <PSADPasswordCredential[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="72f32-119">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="72f32-119">ApplicationObjectWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72f32-120">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="72f32-120">ApplicationObjectWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72f32-121">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="72f32-121">DESCRIPTION</span></span>
<span data-ttu-id="72f32-122">Skapar ett nytt objekt i Azure Active Directory-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="72f32-122">Creates a new azure active directory service principal.</span></span> <span data-ttu-id="72f32-123">Standard parameter uppsättningen använder standardvärden för parametrar om användaren inte anger något för dem.</span><span class="sxs-lookup"><span data-stu-id="72f32-123">The default parameter set uses default values for parameters if the user does not provide one for them.</span></span> <span data-ttu-id="72f32-124">Mer information om standardvärden som används finns i beskrivningen av de angivna parametrarna nedan.</span><span class="sxs-lookup"><span data-stu-id="72f32-124">For more information on the default values used, please see the description for the given parameters below.</span></span>
<span data-ttu-id="72f32-125">Denna cmdlet har möjlighet att tilldela tjänstens huvud namn rollen `Role` och `Scope` parametrarna, om ingen av dessa parametrar anges tilldelas tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="72f32-125">This cmdlet has the ability to assign a role to the service principal with the `Role` and `Scope` parameters; if neither of these parameters are provided, no role will be assigned to the service principal.</span></span> <span data-ttu-id="72f32-126">Standardvärdena för `Role` parametrarna och `Scope` är "deltagare" och det aktuella abonnemanget ( _Obs!_ de standardvärden används endast när användaren tillhandahåller ett värde för en av de två parametrarna, men inte på den andra).</span><span class="sxs-lookup"><span data-stu-id="72f32-126">The default values for the `Role` and `Scope` parameters are "Contributor" and the current subscription, respectively ( _note_ : the defaults are only used when the user provides a value for one of the two parameters, but not the other).</span></span>
<span data-ttu-id="72f32-127">Cmdleten skapar också implicit ett program och anger dess egenskaper (om ApplicationId inte finns).</span><span class="sxs-lookup"><span data-stu-id="72f32-127">The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span> <span data-ttu-id="72f32-128">Använd Set-AzADApplication cmdlet för att uppdatera de programspecifika parametrarna.</span><span class="sxs-lookup"><span data-stu-id="72f32-128">In order to update the application specific parameters please use Set-AzADApplication cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="72f32-129">När du skapar ett tjänst huvud med kommandot **New-AzADServicePrincipal** innehåller utdata de autentiseringsuppgifter du måste skydda.</span><span class="sxs-lookup"><span data-stu-id="72f32-129">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="72f32-130">Se till att du inte tar med de här uppgifterna i koden eller kontrol lera uppgifterna i käll kontrollen.</span><span class="sxs-lookup"><span data-stu-id="72f32-130">Be sure that you do not include these credentials in your code or check the credentials into your source control.</span></span> <span data-ttu-id="72f32-131">Som ett alternativ bör du överväga att använda [hanterade identiteter](/azure/active-directory/managed-identities-azure-resources/overview) för att undvika att behöva använda autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="72f32-131">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="72f32-132">Som standard tilldelar **AzADServicePrincipal** rollen [deltagare](/azure/role-based-access-control/built-in-roles#contributor) till tjänstens huvud namn i prenumerations omfattningen.</span><span class="sxs-lookup"><span data-stu-id="72f32-132">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="72f32-133">För att minska risken för en komprometterad tjänstens huvud konto tilldelar du en mer specifik roll och begränsar omfattningen till en resurs eller resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="72f32-133">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="72f32-134">Mer information finns i [steg för att lägga till en roll tilldelning](/azure/role-based-access-control/role-assignments-steps) .</span><span class="sxs-lookup"><span data-stu-id="72f32-134">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="72f32-135">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="72f32-135">EXAMPLES</span></span>

### <span data-ttu-id="72f32-136">Exempel 1 – enkelt att skapa AD-tjänstens huvud objekt</span><span class="sxs-lookup"><span data-stu-id="72f32-136">Example 1 - Simple AD service principal creation</span></span>

```
PS C:\> New-AzADServicePrincipal

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="72f32-137">Med kommandot ovan skapas ett AD-huvudobjekt med standardvärden för parametrar som inte tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="72f32-137">The above command creates an AD service principal using default values for parameters not provided.</span></span> <span data-ttu-id="72f32-138">Eftersom inget program-ID har angetts skapades ett program för tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="72f32-138">Since an application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="72f32-139">Eftersom inga värden angavs för `Role` eller `Scope` så har det skapade tjänstens huvud namn inte någon behörighet.</span><span class="sxs-lookup"><span data-stu-id="72f32-139">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="72f32-140">Exempel 2 – Simple skapa AD-tjänstens huvud objekt med en viss roll och standard omfattning</span><span class="sxs-lookup"><span data-stu-id="72f32-140">Example 2 - Simple AD service principal creation with a specified role and default scope</span></span>

```
PS C:\> New-AzADServicePrincipal -Role Reader

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz' to the new service principal.
```

<span data-ttu-id="72f32-141">Med kommandot ovan skapas ett AD-huvudobjekt med standardvärdena för parametrar som inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="72f32-141">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="72f32-142">Eftersom program-ID inte har angetts skapades ett program för tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="72f32-142">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="72f32-143">Tjänstens huvud namn skapades med "läsare"-behörigheter under den aktuella prenumerationen (sedan inget värde angavs för `Scope` parametern).</span><span class="sxs-lookup"><span data-stu-id="72f32-143">The service principal was created with "Reader" permissions over the current subscription (since no value was provided for the `Scope` parameter).</span></span>

### <span data-ttu-id="72f32-144">Exempel 3 – enkelt att skapa AD-UPN med ett angivet omfång och standard roll</span><span class="sxs-lookup"><span data-stu-id="72f32-144">Example 3 - Simple AD service principal creation with a specified scope and default role</span></span>

```
PS C:\> New-AzADServicePrincipal -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

<span data-ttu-id="72f32-145">Med kommandot ovan skapas ett AD-huvudobjekt med standardvärdena för parametrar som inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="72f32-145">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="72f32-146">Eftersom program-ID inte har angetts skapades ett program för tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="72f32-146">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="72f32-147">Tjänstens huvud namn skapades med behörigheter för "deltagare" (sedan inget värde angavs för `Role` parametern) över den tillhandahållna resurs gruppens omfattning.</span><span class="sxs-lookup"><span data-stu-id="72f32-147">The service principal was created with "Contributor" permissions (since no value was provided for the `Role` parameter) over the provided resource group scope.</span></span>

### <span data-ttu-id="72f32-148">Exempel 4 – Simple skapa AD-tjänstens huvud objekt med ett angivet omfång och en viss roll</span><span class="sxs-lookup"><span data-stu-id="72f32-148">Example 4 - Simple AD service principal creation with a specified scope and role</span></span>

```
PS C:\> New-AzADServicePrincipal -Role Reader -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

<span data-ttu-id="72f32-149">Med kommandot ovan skapas ett AD-huvudobjekt med standardvärdena för parametrar som inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="72f32-149">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="72f32-150">Eftersom program-ID inte har angetts skapades ett program för tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="72f32-150">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="72f32-151">Tjänstens huvud namn skapades med "läsare"-behörigheter via den tillhandahållna resurs gruppens omfattning.</span><span class="sxs-lookup"><span data-stu-id="72f32-151">The service principal was created with "Reader" permissions over the provided resource group scope.</span></span>

### <span data-ttu-id="72f32-152">Exempel 5 – skapa ett nytt AD tjänst-huvudobjekt med program-ID med roll tilldelning</span><span class="sxs-lookup"><span data-stu-id="72f32-152">Example 5 - Create a new AD service principal using application id with role assignment</span></span>

```
PS C:\> New-AzADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e

ServicePrincipalNames : {34a28ad2-dec4-4a41-bc3b-d22ddf90000e, http://my-temp-app}
ApplicationId         : 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
DisplayName           : my-temp-app
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="72f32-153">Skapar en ny AD service-huvudprincip för programmet med program-ID ' 34a28ad2-dec4-4a41-bc3b-d22ddf90000e '.</span><span class="sxs-lookup"><span data-stu-id="72f32-153">Creates a new AD service principal for the application with application id '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'.</span></span> <span data-ttu-id="72f32-154">Eftersom inga värden angavs för `Role` eller `Scope` så har det skapade tjänstens huvud namn inte någon behörighet.</span><span class="sxs-lookup"><span data-stu-id="72f32-154">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="72f32-155">Exempel 6 – skapa ett nytt AD service-huvudobjekt med ledning</span><span class="sxs-lookup"><span data-stu-id="72f32-155">Example 6 - Create a new AD service principal using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

<span data-ttu-id="72f32-156">Hämtar programmet med objekt-ID ' 3ede3c26-B443-4e0b-9efc-b05e68338dc3 ' och pipes till New-AzADServicePrincipal cmdlet för att skapa en ny AD-huvudtjänst för det programmet.</span><span class="sxs-lookup"><span data-stu-id="72f32-156">Gets the application with object id '3ede3c26-b443-4e0b-9efc-b05e68338dc3' and pipes that to the New-AzADServicePrincipal cmdlet to create a new AD service principal for that application.</span></span>

## <span data-ttu-id="72f32-157">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="72f32-157">PARAMETERS</span></span>

### <span data-ttu-id="72f32-158">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="72f32-158">-ApplicationId</span></span>
<span data-ttu-id="72f32-159">Unikt program-ID för tjänstens huvud namn i en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="72f32-159">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="72f32-160">Det går inte att ändra egenskapen när den har skapats.</span><span class="sxs-lookup"><span data-stu-id="72f32-160">Once created this property cannot be changed.</span></span>
<span data-ttu-id="72f32-161">Om inget program-ID anges genereras ett.</span><span class="sxs-lookup"><span data-stu-id="72f32-161">If an application id is not specified, one will be generated.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ApplicationWithoutCredentialParameterSet, ApplicationWithPasswordPlainParameterSet, ApplicationWithPasswordCredentialParameterSet, ApplicationWithKeyPlainParameterSet, ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72f32-162">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="72f32-162">-ApplicationObject</span></span>
<span data-ttu-id="72f32-163">Det objekt som representerar det program som tjänstens huvud namn skapas för.</span><span class="sxs-lookup"><span data-stu-id="72f32-163">The object representing the application for which the service principal is created.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithoutCredentialParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithPasswordCredentialParameterSet, ApplicationObjectWithKeyPlainParameterSet, ApplicationObjectWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72f32-164">-CertValue</span><span class="sxs-lookup"><span data-stu-id="72f32-164">-CertValue</span></span>
<span data-ttu-id="72f32-165">Värdet för autentiseringstypen "asymmetrisk".</span><span class="sxs-lookup"><span data-stu-id="72f32-165">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="72f32-166">Den representerar det grundläggande 64-kodade certifikatet.</span><span class="sxs-lookup"><span data-stu-id="72f32-166">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithKeyPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72f32-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72f32-167">-DefaultProfile</span></span>
<span data-ttu-id="72f32-168">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="72f32-168">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72f32-169">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="72f32-169">-DisplayName</span></span>
<span data-ttu-id="72f32-170">Eget namn på tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="72f32-170">The friendly name of the service principal.</span></span> <span data-ttu-id="72f32-171">Om inget visnings namn anges används det här värdet som standard "Azure-PowerShell-MM-DD-yyyy-HH-SS", där suffixet är det datum då programmet skapades.</span><span class="sxs-lookup"><span data-stu-id="72f32-171">If a display name is not provided, this value will default to 'azure-powershell-MM-dd-yyyy-HH-mm-ss', where the suffix is the time of application creation.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DisplayNameWithoutCredentialParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithPasswordCredentialParameterSet, DisplayNameWithKeyPlainParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72f32-172">-EndDate</span><span class="sxs-lookup"><span data-stu-id="72f32-172">-EndDate</span></span>
<span data-ttu-id="72f32-173">Slutdatum för användning av autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="72f32-173">The effective end date of the credential usage.</span></span>
<span data-ttu-id="72f32-174">Standardvärdet för slutdatumet är ett år från idag.</span><span class="sxs-lookup"><span data-stu-id="72f32-174">The default end date value is one year from today.</span></span> <span data-ttu-id="72f32-175">För en "asymmetrisk" typ autentiseringsuppgift måste detta ställas in på eller före det datum då X509-certifikatet är giltigt.</span><span class="sxs-lookup"><span data-stu-id="72f32-175">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72f32-176">-Inloggnings uppgifter</span><span class="sxs-lookup"><span data-stu-id="72f32-176">-KeyCredential</span></span>
<span data-ttu-id="72f32-177">Insamling av viktiga autentiseringsuppgifter associerade med programmet.</span><span class="sxs-lookup"><span data-stu-id="72f32-177">The collection of key credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationObjectWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72f32-178">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="72f32-178">-Password</span></span>
<span data-ttu-id="72f32-179">Lösen ordet som ska kopplas till tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="72f32-179">The password to be associated with the service principal.</span></span> <span data-ttu-id="72f32-180">Om inget lösen ord anges genereras ett slumpmässigt GUID och används som lösen ord.</span><span class="sxs-lookup"><span data-stu-id="72f32-180">If a password is not provided, a random GUID will be generated and used as the password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationWithPasswordPlainParameterSet, DisplayNameWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationObjectWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72f32-181">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="72f32-181">-PasswordCredential</span></span>
<span data-ttu-id="72f32-182">Den uppsättning autentiseringsuppgifter för lösen ord som är associerad med programmet.</span><span class="sxs-lookup"><span data-stu-id="72f32-182">The collection of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationObjectWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72f32-183">-Roll</span><span class="sxs-lookup"><span data-stu-id="72f32-183">-Role</span></span>
<span data-ttu-id="72f32-184">Rollen som tjänstens huvud namn har.</span><span class="sxs-lookup"><span data-stu-id="72f32-184">The role that the service principal has over the scope.</span></span> <span data-ttu-id="72f32-185">Om ett värde `Scope` är angivet, men inget värde är angivet för `Role` , `Role` används rollen "deltagare" som standard.</span><span class="sxs-lookup"><span data-stu-id="72f32-185">If a value for `Scope` is provided, but no value is provided for `Role`, then `Role` will default to the 'Contributor' role.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72f32-186">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="72f32-186">-Scope</span></span>
<span data-ttu-id="72f32-187">Omfattningen som tjänstens huvud namn har behörighet för.</span><span class="sxs-lookup"><span data-stu-id="72f32-187">The scope that the service principal has permissions on.</span></span> <span data-ttu-id="72f32-188">Om ett värde `Role` är angivet men inget värde är angivet för `Scope` `Scope` det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="72f32-188">If a value for `Role` is provided, but no value is provided for `Scope`, then `Scope` will default to the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72f32-189">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="72f32-189">-SkipAssignment</span></span>
<span data-ttu-id="72f32-190">Om den här inställningen är aktive rad kommer du inte att skapa standard roll tilldelning för tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="72f32-190">If set, will skip creating the default role assignment for the service principal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72f32-191">-StartDate</span><span class="sxs-lookup"><span data-stu-id="72f32-191">-StartDate</span></span>
<span data-ttu-id="72f32-192">Start datum för användning av autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="72f32-192">The effective start date of the credential usage.</span></span>
<span data-ttu-id="72f32-193">Standardvärdet för start datum är idag.</span><span class="sxs-lookup"><span data-stu-id="72f32-193">The default start date value is today.</span></span> <span data-ttu-id="72f32-194">För en "asymmetrisk" typ autentiseringsuppgift måste detta ställas in på eller efter det datum då X509-certifikatet är giltigt från.</span><span class="sxs-lookup"><span data-stu-id="72f32-194">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72f32-195">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="72f32-195">-Confirm</span></span>
<span data-ttu-id="72f32-196">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="72f32-196">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72f32-197">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72f32-197">-WhatIf</span></span>
<span data-ttu-id="72f32-198">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="72f32-198">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72f32-199">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="72f32-199">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72f32-200">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72f32-200">CommonParameters</span></span>
<span data-ttu-id="72f32-201">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72f32-201">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72f32-202">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72f32-202">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72f32-203">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="72f32-203">INPUTS</span></span>

### <span data-ttu-id="72f32-204">System. GUID</span><span class="sxs-lookup"><span data-stu-id="72f32-204">System.Guid</span></span>

### <span data-ttu-id="72f32-205">System. String</span><span class="sxs-lookup"><span data-stu-id="72f32-205">System.String</span></span>

### <span data-ttu-id="72f32-206">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="72f32-206">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="72f32-207">Parametrar: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="72f32-207">Parameters: ApplicationObject (ByValue)</span></span>

### <span data-ttu-id="72f32-208">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="72f32-208">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="72f32-209">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="72f32-209">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="72f32-210">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="72f32-210">System.Security.SecureString</span></span>

### <span data-ttu-id="72f32-211">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="72f32-211">System.DateTime</span></span>

## <span data-ttu-id="72f32-212">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="72f32-212">OUTPUTS</span></span>

### <span data-ttu-id="72f32-213">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="72f32-213">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="72f32-214">Microsoft. Azure. kommandon. sources. Models. Authorization. PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="72f32-214">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="72f32-215">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="72f32-215">NOTES</span></span>
<span data-ttu-id="72f32-216">Nyckelord: Azure, AZ, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="72f32-216">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="72f32-217">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="72f32-217">RELATED LINKS</span></span>

[<span data-ttu-id="72f32-218">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="72f32-218">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="72f32-219">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="72f32-219">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="72f32-220">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="72f32-220">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="72f32-221">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="72f32-221">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="72f32-222">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="72f32-222">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="72f32-223">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="72f32-223">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="72f32-224">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="72f32-224">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

