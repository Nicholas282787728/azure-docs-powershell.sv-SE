---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: f921cceb3692032f61f99db825efeea074773faa
ms.sourcegitcommit: 375232b84336ef5e13052504deaa43f5bd4b7f65
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/05/2020
ms.locfileid: "94326136"
---
# <span data-ttu-id="9cab9-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="9cab9-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="9cab9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9cab9-102">SYNOPSIS</span></span>
<span data-ttu-id="9cab9-103">Skapar ett nytt objekt i Azure Active Directory-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="9cab9-103">Creates a new azure active directory service principal.</span></span>

## <span data-ttu-id="9cab9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9cab9-104">SYNTAX</span></span>

### <span data-ttu-id="9cab9-105">SimpleParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9cab9-105">SimpleParameterSet (Default)</span></span>
```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cab9-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cab9-106">ApplicationWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9cab9-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cab9-107">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cab9-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cab9-108">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cab9-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cab9-109">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cab9-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cab9-110">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cab9-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cab9-111">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9cab9-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cab9-112">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cab9-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cab9-113">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cab9-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cab9-114">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cab9-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cab9-115">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cab9-116">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cab9-116">ApplicationObjectWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cab9-117">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cab9-117">ApplicationObjectWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cab9-118">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cab9-118">ApplicationObjectWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cab9-119">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cab9-119">ApplicationObjectWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cab9-120">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9cab9-120">DESCRIPTION</span></span>
<span data-ttu-id="9cab9-121">Skapar ett nytt objekt i Azure Active Directory-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="9cab9-121">Creates a new azure active directory service principal.</span></span> <span data-ttu-id="9cab9-122">Standard parameter uppsättningen använder standardvärden för parametrar om användaren inte anger något för dem.</span><span class="sxs-lookup"><span data-stu-id="9cab9-122">The default parameter set uses default values for parameters if the user does not provide one for them.</span></span> <span data-ttu-id="9cab9-123">Mer information om standardvärden som används finns i beskrivningen av de angivna parametrarna nedan.</span><span class="sxs-lookup"><span data-stu-id="9cab9-123">For more information on the default values used, please see the description for the given parameters below.</span></span>
<span data-ttu-id="9cab9-124">Denna cmdlet har möjlighet att tilldela tjänstens huvud namn rollen `Role` och `Scope` parametrarna, om ingen av dessa parametrar anges tilldelas tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="9cab9-124">This cmdlet has the ability to assign a role to the service principal with the `Role` and `Scope` parameters; if neither of these parameters are provided, no role will be assigned to the service principal.</span></span> <span data-ttu-id="9cab9-125">Standardvärdena för `Role` parametrarna och `Scope` är "deltagare" och det aktuella abonnemanget ( _Obs!_ de standardvärden används endast när användaren tillhandahåller ett värde för en av de två parametrarna, men inte på den andra).</span><span class="sxs-lookup"><span data-stu-id="9cab9-125">The default values for the `Role` and `Scope` parameters are "Contributor" and the current subscription, respectively ( _note_ : the defaults are only used when the user provides a value for one of the two parameters, but not the other).</span></span>
<span data-ttu-id="9cab9-126">Cmdleten skapar också implicit ett program och anger dess egenskaper (om ApplicationId inte finns).</span><span class="sxs-lookup"><span data-stu-id="9cab9-126">The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span> <span data-ttu-id="9cab9-127">Använd Set-AzADApplication cmdlet för att uppdatera de programspecifika parametrarna.</span><span class="sxs-lookup"><span data-stu-id="9cab9-127">In order to update the application specific parameters please use Set-AzADApplication cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="9cab9-128">När du skapar ett tjänst huvud med kommandot **New-AzADServicePrincipal** innehåller utdata de autentiseringsuppgifter du måste skydda.</span><span class="sxs-lookup"><span data-stu-id="9cab9-128">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="9cab9-129">Se till att du inte tar med de här uppgifterna i koden eller kontrol lera uppgifterna i käll kontrollen.</span><span class="sxs-lookup"><span data-stu-id="9cab9-129">Be sure that you do not include these credentials in your code or check the credentials into your source control.</span></span> <span data-ttu-id="9cab9-130">Som ett alternativ bör du överväga att använda [hanterade identiteter](/azure/active-directory/managed-identities-azure-resources/overview) för att undvika att behöva använda autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="9cab9-130">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="9cab9-131">Som standard tilldelar **AzADServicePrincipal** rollen [deltagare](/azure/role-based-access-control/built-in-roles#contributor) till tjänstens huvud namn i prenumerations omfattningen.</span><span class="sxs-lookup"><span data-stu-id="9cab9-131">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="9cab9-132">För att minska risken för en komprometterad tjänstens huvud konto tilldelar du en mer specifik roll och begränsar omfattningen till en resurs eller resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="9cab9-132">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="9cab9-133">Mer information finns i [steg för att lägga till en roll tilldelning](/azure/role-based-access-control/role-assignments-steps) .</span><span class="sxs-lookup"><span data-stu-id="9cab9-133">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="9cab9-134">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9cab9-134">EXAMPLES</span></span>

### <span data-ttu-id="9cab9-135">Exempel 1 – enkelt att skapa AD-tjänstens huvud objekt</span><span class="sxs-lookup"><span data-stu-id="9cab9-135">Example 1 - Simple AD service principal creation</span></span>

```
PS C:\> New-AzADServicePrincipal

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="9cab9-136">Med kommandot ovan skapas ett AD-huvudobjekt med standardvärden för parametrar som inte tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="9cab9-136">The above command creates an AD service principal using default values for parameters not provided.</span></span> <span data-ttu-id="9cab9-137">Eftersom inget program-ID har angetts skapades ett program för tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="9cab9-137">Since an application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="9cab9-138">Eftersom inga värden angavs för `Role` eller `Scope` så har det skapade tjänstens huvud namn inte någon behörighet.</span><span class="sxs-lookup"><span data-stu-id="9cab9-138">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="9cab9-139">Exempel 2 – Simple skapa AD-tjänstens huvud objekt med en viss roll och standard omfattning</span><span class="sxs-lookup"><span data-stu-id="9cab9-139">Example 2 - Simple AD service principal creation with a specified role and default scope</span></span>

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

<span data-ttu-id="9cab9-140">Med kommandot ovan skapas ett AD-huvudobjekt med standardvärdena för parametrar som inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="9cab9-140">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="9cab9-141">Eftersom program-ID inte har angetts skapades ett program för tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="9cab9-141">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="9cab9-142">Tjänstens huvud namn skapades med "läsare"-behörigheter under den aktuella prenumerationen (sedan inget värde angavs för `Scope` parametern).</span><span class="sxs-lookup"><span data-stu-id="9cab9-142">The service principal was created with "Reader" permissions over the current subscription (since no value was provided for the `Scope` parameter).</span></span>

### <span data-ttu-id="9cab9-143">Exempel 3 – enkelt att skapa AD-UPN med ett angivet omfång och standard roll</span><span class="sxs-lookup"><span data-stu-id="9cab9-143">Example 3 - Simple AD service principal creation with a specified scope and default role</span></span>

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

<span data-ttu-id="9cab9-144">Med kommandot ovan skapas ett AD-huvudobjekt med standardvärdena för parametrar som inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="9cab9-144">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="9cab9-145">Eftersom program-ID inte har angetts skapades ett program för tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="9cab9-145">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="9cab9-146">Tjänstens huvud namn skapades med behörigheter för "deltagare" (sedan inget värde angavs för `Role` parametern) över den tillhandahållna resurs gruppens omfattning.</span><span class="sxs-lookup"><span data-stu-id="9cab9-146">The service principal was created with "Contributor" permissions (since no value was provided for the `Role` parameter) over the provided resource group scope.</span></span>

### <span data-ttu-id="9cab9-147">Exempel 4 – Simple skapa AD-tjänstens huvud objekt med ett angivet omfång och en viss roll</span><span class="sxs-lookup"><span data-stu-id="9cab9-147">Example 4 - Simple AD service principal creation with a specified scope and role</span></span>

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

<span data-ttu-id="9cab9-148">Med kommandot ovan skapas ett AD-huvudobjekt med standardvärdena för parametrar som inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="9cab9-148">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="9cab9-149">Eftersom program-ID inte har angetts skapades ett program för tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="9cab9-149">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="9cab9-150">Tjänstens huvud namn skapades med "läsare"-behörigheter via den tillhandahållna resurs gruppens omfattning.</span><span class="sxs-lookup"><span data-stu-id="9cab9-150">The service principal was created with "Reader" permissions over the provided resource group scope.</span></span>

### <span data-ttu-id="9cab9-151">Exempel 5 – skapa ett nytt AD tjänst-huvudobjekt med program-ID med roll tilldelning</span><span class="sxs-lookup"><span data-stu-id="9cab9-151">Example 5 - Create a new AD service principal using application id with role assignment</span></span>

```
PS C:\> New-AzADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e

ServicePrincipalNames : {34a28ad2-dec4-4a41-bc3b-d22ddf90000e, http://my-temp-app}
ApplicationId         : 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
DisplayName           : my-temp-app
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="9cab9-152">Skapar en ny AD service-huvudprincip för programmet med program-ID ' 34a28ad2-dec4-4a41-bc3b-d22ddf90000e '.</span><span class="sxs-lookup"><span data-stu-id="9cab9-152">Creates a new AD service principal for the application with application id '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'.</span></span> <span data-ttu-id="9cab9-153">Eftersom inga värden angavs för `Role` eller `Scope` så har det skapade tjänstens huvud namn inte någon behörighet.</span><span class="sxs-lookup"><span data-stu-id="9cab9-153">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="9cab9-154">Exempel 6 – skapa ett nytt AD service-huvudobjekt med ledning</span><span class="sxs-lookup"><span data-stu-id="9cab9-154">Example 6 - Create a new AD service principal using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

<span data-ttu-id="9cab9-155">Hämtar programmet med objekt-ID ' 3ede3c26-B443-4e0b-9efc-b05e68338dc3 ' och pipes till New-AzADServicePrincipal cmdlet för att skapa en ny AD-huvudtjänst för det programmet.</span><span class="sxs-lookup"><span data-stu-id="9cab9-155">Gets the application with object id '3ede3c26-b443-4e0b-9efc-b05e68338dc3' and pipes that to the New-AzADServicePrincipal cmdlet to create a new AD service principal for that application.</span></span>

### <span data-ttu-id="9cab9-156">Exempel 7 – skapa ett nytt AD service-huvudobjekt med DisplayName och lösen ords identifiering</span><span class="sxs-lookup"><span data-stu-id="9cab9-156">Example 7 - Create a new AD service principal using DisplayName and password credential</span></span>

```
PS C:\> $credentials = New-Object -TypeName Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password="StrongPassworld!23"}
PS C:\> $sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials

ServicePrincipalNames : {exxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxc, http://ServicePrincipalName}
ApplicationId         : exxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxcc
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 6xxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxb
Type                  :
```

<span data-ttu-id="9cab9-157">Skapar ett nytt program med namnet "ServicePrincipalName" och lösen ord "StrongPassworld! 23" och skapar tjänstens huvud konto baserat på det program du just skapade.</span><span class="sxs-lookup"><span data-stu-id="9cab9-157">Creates a new application with name "ServicePrincipalName" and password "StrongPassworld!23" and creates the service principal based on the application just created.</span></span> <span data-ttu-id="9cab9-158">Start datum och slutdatum läggs till i lösen ords informationen.</span><span class="sxs-lookup"><span data-stu-id="9cab9-158">The start date and end date are added to password credential.</span></span>

### <span data-ttu-id="9cab9-159">Exempel 8 – skapa ett nytt AD service-huvudobjekt med hjälp av DisplayName och vanliga autentiseringsuppgifter</span><span class="sxs-lookup"><span data-stu-id="9cab9-159">Example 8 - Create a new AD service principal using DisplayName and plain key credential</span></span>

```
PS C:\> $cert = <public certificate as base64-encoded string>
PS C:\> $sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert  -EndDate "2021-01-01"

ServicePrincipalNames : {cxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxx6, http://ServicePrincipalName}
ApplicationId         : cxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxx6
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : cxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxc
Type                  :
```

<span data-ttu-id="9cab9-160">Skapar ett nytt program med namnet "ServicePrincipalName" och certifcate "$cert" och skapar tjänstens huvud konto baserat på det program du just skapade.</span><span class="sxs-lookup"><span data-stu-id="9cab9-160">Creates a new application with name "ServicePrincipalName" and certifcate "$cert" and creates the service principal based on the application just created.</span></span> <span data-ttu-id="9cab9-161">Slutdatumet läggs till för viktiga autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="9cab9-161">The end date is added to key credential.</span></span>

## <span data-ttu-id="9cab9-162">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9cab9-162">PARAMETERS</span></span>

### <span data-ttu-id="9cab9-163">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="9cab9-163">-ApplicationId</span></span>
<span data-ttu-id="9cab9-164">Unikt program-ID för tjänstens huvud namn i en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="9cab9-164">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="9cab9-165">Det går inte att ändra egenskapen när den har skapats.</span><span class="sxs-lookup"><span data-stu-id="9cab9-165">Once created this property cannot be changed.</span></span>
<span data-ttu-id="9cab9-166">Om inget program-ID anges genereras ett.</span><span class="sxs-lookup"><span data-stu-id="9cab9-166">If an application id is not specified, one will be generated.</span></span>

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

### <span data-ttu-id="9cab9-167">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="9cab9-167">-ApplicationObject</span></span>
<span data-ttu-id="9cab9-168">Det objekt som representerar det program som tjänstens huvud namn skapas för.</span><span class="sxs-lookup"><span data-stu-id="9cab9-168">The object representing the application for which the service principal is created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithPasswordCredentialParameterSet, ApplicationObjectWithKeyPlainParameterSet, ApplicationObjectWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9cab9-169">-CertValue</span><span class="sxs-lookup"><span data-stu-id="9cab9-169">-CertValue</span></span>
<span data-ttu-id="9cab9-170">Värdet för autentiseringstypen "asymmetrisk".</span><span class="sxs-lookup"><span data-stu-id="9cab9-170">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="9cab9-171">Den representerar det grundläggande 64-kodade certifikatet.</span><span class="sxs-lookup"><span data-stu-id="9cab9-171">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="9cab9-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cab9-172">-DefaultProfile</span></span>
<span data-ttu-id="9cab9-173">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9cab9-173">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cab9-174">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9cab9-174">-DisplayName</span></span>
<span data-ttu-id="9cab9-175">Eget namn på tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="9cab9-175">The friendly name of the service principal.</span></span> <span data-ttu-id="9cab9-176">Om inget visnings namn anges används det här värdet som standard "Azure-PowerShell-MM-DD-yyyy-HH-SS", där suffixet är det datum då programmet skapades.</span><span class="sxs-lookup"><span data-stu-id="9cab9-176">If a display name is not provided, this value will default to 'azure-powershell-MM-dd-yyyy-HH-mm-ss', where the suffix is the time of application creation.</span></span>

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

### <span data-ttu-id="9cab9-177">-EndDate</span><span class="sxs-lookup"><span data-stu-id="9cab9-177">-EndDate</span></span>
<span data-ttu-id="9cab9-178">Slutdatum för användning av autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="9cab9-178">The effective end date of the credential usage.</span></span>
<span data-ttu-id="9cab9-179">Standardvärdet för slutdatumet är ett år från idag.</span><span class="sxs-lookup"><span data-stu-id="9cab9-179">The default end date value is one year from today.</span></span> <span data-ttu-id="9cab9-180">För en "asymmetrisk" typ autentiseringsuppgift måste detta ställas in på eller före det datum då X509-certifikatet är giltigt.</span><span class="sxs-lookup"><span data-stu-id="9cab9-180">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="9cab9-181">-Inloggnings uppgifter</span><span class="sxs-lookup"><span data-stu-id="9cab9-181">-KeyCredential</span></span>
<span data-ttu-id="9cab9-182">Insamling av viktiga autentiseringsuppgifter associerade med programmet.</span><span class="sxs-lookup"><span data-stu-id="9cab9-182">The collection of key credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationObjectWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cab9-183">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="9cab9-183">-PasswordCredential</span></span>
<span data-ttu-id="9cab9-184">Den uppsättning autentiseringsuppgifter för lösen ord som är associerad med programmet.</span><span class="sxs-lookup"><span data-stu-id="9cab9-184">The collection of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationObjectWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cab9-185">-Roll</span><span class="sxs-lookup"><span data-stu-id="9cab9-185">-Role</span></span>
<span data-ttu-id="9cab9-186">Rollen som tjänstens huvud namn har.</span><span class="sxs-lookup"><span data-stu-id="9cab9-186">The role that the service principal has over the scope.</span></span> <span data-ttu-id="9cab9-187">Om ett värde `Scope` är angivet, men inget värde är angivet för `Role` , `Role` används rollen "deltagare" som standard.</span><span class="sxs-lookup"><span data-stu-id="9cab9-187">If a value for `Scope` is provided, but no value is provided for `Role`, then `Role` will default to the 'Contributor' role.</span></span>

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

### <span data-ttu-id="9cab9-188">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="9cab9-188">-Scope</span></span>
<span data-ttu-id="9cab9-189">Omfattningen som tjänstens huvud namn har behörighet för.</span><span class="sxs-lookup"><span data-stu-id="9cab9-189">The scope that the service principal has permissions on.</span></span> <span data-ttu-id="9cab9-190">Om ett värde `Role` är angivet men inget värde är angivet för `Scope` `Scope` det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="9cab9-190">If a value for `Role` is provided, but no value is provided for `Scope`, then `Scope` will default to the current subscription.</span></span>

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

### <span data-ttu-id="9cab9-191">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="9cab9-191">-SkipAssignment</span></span>
<span data-ttu-id="9cab9-192">Om den här inställningen är aktive rad kommer du inte att skapa standard roll tilldelning för tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="9cab9-192">If set, will skip creating the default role assignment for the service principal.</span></span>

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

### <span data-ttu-id="9cab9-193">-StartDate</span><span class="sxs-lookup"><span data-stu-id="9cab9-193">-StartDate</span></span>
<span data-ttu-id="9cab9-194">Start datum för användning av autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="9cab9-194">The effective start date of the credential usage.</span></span>
<span data-ttu-id="9cab9-195">Standardvärdet för start datum är idag.</span><span class="sxs-lookup"><span data-stu-id="9cab9-195">The default start date value is today.</span></span> <span data-ttu-id="9cab9-196">För en "asymmetrisk" typ autentiseringsuppgift måste detta ställas in på eller efter det datum då X509-certifikatet är giltigt från.</span><span class="sxs-lookup"><span data-stu-id="9cab9-196">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="9cab9-197">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9cab9-197">-Confirm</span></span>
<span data-ttu-id="9cab9-198">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9cab9-198">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cab9-199">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cab9-199">-WhatIf</span></span>
<span data-ttu-id="9cab9-200">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9cab9-200">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cab9-201">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9cab9-201">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cab9-202">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cab9-202">CommonParameters</span></span>
<span data-ttu-id="9cab9-203">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cab9-203">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cab9-204">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9cab9-204">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cab9-205">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9cab9-205">INPUTS</span></span>

### <span data-ttu-id="9cab9-206">System. GUID</span><span class="sxs-lookup"><span data-stu-id="9cab9-206">System.Guid</span></span>

### <span data-ttu-id="9cab9-207">System. String</span><span class="sxs-lookup"><span data-stu-id="9cab9-207">System.String</span></span>

### <span data-ttu-id="9cab9-208">Microsoft. Azure. commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="9cab9-208">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="9cab9-209">Microsoft. Azure. commands. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="9cab9-209">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="9cab9-210">Microsoft. Azure. commands. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="9cab9-210">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="9cab9-211">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="9cab9-211">System.DateTime</span></span>

## <span data-ttu-id="9cab9-212">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9cab9-212">OUTPUTS</span></span>

### <span data-ttu-id="9cab9-213">Microsoft. Azure. commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="9cab9-213">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="9cab9-214">Microsoft. Azure. kommandon. sources. Models. Authorization. PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="9cab9-214">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="9cab9-215">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9cab9-215">NOTES</span></span>
<span data-ttu-id="9cab9-216">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="9cab9-216">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="9cab9-217">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9cab9-217">RELATED LINKS</span></span>

[<span data-ttu-id="9cab9-218">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="9cab9-218">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="9cab9-219">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="9cab9-219">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="9cab9-220">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="9cab9-220">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="9cab9-221">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="9cab9-221">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="9cab9-222">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="9cab9-222">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="9cab9-223">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="9cab9-223">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="9cab9-224">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="9cab9-224">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

