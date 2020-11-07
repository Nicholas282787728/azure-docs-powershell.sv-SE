---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadserviceprincipal
schema: 2.0.0
ms.openlocfilehash: 9d0fb4f188b3753e22258a27cf8632d85fe866dc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930869"
---
# <span data-ttu-id="50eb9-101">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="50eb9-101">New-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="50eb9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="50eb9-102">SYNOPSIS</span></span>
<span data-ttu-id="50eb9-103">Skapar ett nytt objekt i Azure Active Directory-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="50eb9-103">Creates a new azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50eb9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="50eb9-104">SYNTAX</span></span>

### <span data-ttu-id="50eb9-105">SimpleParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="50eb9-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-Password <SecureString>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50eb9-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="50eb9-106">ApplicationWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50eb9-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="50eb9-107">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50eb9-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="50eb9-108">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50eb9-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="50eb9-109">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50eb9-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="50eb9-110">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50eb9-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="50eb9-111">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50eb9-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="50eb9-112">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50eb9-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="50eb9-113">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50eb9-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="50eb9-114">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50eb9-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="50eb9-115">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50eb9-116">ApplicationObjectWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="50eb9-116">ApplicationObjectWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50eb9-117">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="50eb9-117">ApplicationObjectWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> -Password <SecureString>
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="50eb9-118">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="50eb9-118">ApplicationObjectWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication>
 -PasswordCredential <PSADPasswordCredential[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="50eb9-119">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="50eb9-119">ApplicationObjectWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50eb9-120">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="50eb9-120">ApplicationObjectWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50eb9-121">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="50eb9-121">DESCRIPTION</span></span>
<span data-ttu-id="50eb9-122">Skapar ett nytt objekt i Azure Active Directory-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="50eb9-122">Creates a new azure active directory service principal.</span></span> <span data-ttu-id="50eb9-123">Standard parameter uppsättningen använder standardvärden för parametrar om användaren inte anger något för dem.</span><span class="sxs-lookup"><span data-stu-id="50eb9-123">The default parameter set uses default values for parameters if the user does not provide one for them.</span></span> <span data-ttu-id="50eb9-124">Mer information om standardvärden som används finns i beskrivningen av de angivna parametrarna nedan.</span><span class="sxs-lookup"><span data-stu-id="50eb9-124">For more information on the default values used, please see the description for the given parameters below.</span></span>
<span data-ttu-id="50eb9-125">Denna cmdlet har möjlighet att tilldela tjänstens huvud namn rollen `Role` och `Scope` parametrarna, om ingen av dessa parametrar anges tilldelas tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="50eb9-125">This cmdlet has the ability to assign a role to the service principal with the `Role` and `Scope` parameters; if neither of these parameters are provided, no role will be assigned to the service principal.</span></span> <span data-ttu-id="50eb9-126">Standardvärdena för `Role` parametrarna och `Scope` är "deltagare" och det aktuella abonnemanget ( _Obs!_ de standardvärden används endast när användaren tillhandahåller ett värde för en av de två parametrarna, men inte på den andra).</span><span class="sxs-lookup"><span data-stu-id="50eb9-126">The default values for the `Role` and `Scope` parameters are "Contributor" and the current subscription, respectively ( _note_ : the defaults are only used when the user provides a value for one of the two parameters, but not the other).</span></span>
<span data-ttu-id="50eb9-127">Cmdleten skapar också implicit ett program och anger dess egenskaper (om ApplicationId inte finns).</span><span class="sxs-lookup"><span data-stu-id="50eb9-127">The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span> <span data-ttu-id="50eb9-128">Använd Set-AzureRmADApplication cmdlet för att uppdatera de programspecifika parametrarna.</span><span class="sxs-lookup"><span data-stu-id="50eb9-128">In order to update the application specific parameters please use Set-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="50eb9-129">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="50eb9-129">EXAMPLES</span></span>

### <span data-ttu-id="50eb9-130">Exempel 1 – enkelt att skapa AD-tjänstens huvud objekt</span><span class="sxs-lookup"><span data-stu-id="50eb9-130">Example 1 - Simple AD service principal creation</span></span>

```
PS C:\> New-AzureRmADServicePrincipal

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="50eb9-131">Med kommandot ovan skapas ett AD-huvudobjekt med standardvärden för parametrar som inte tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="50eb9-131">The above command creates an AD service principal using default values for parameters not provided.</span></span> <span data-ttu-id="50eb9-132">Eftersom inget program-ID har angetts skapades ett program för tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="50eb9-132">Since an application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="50eb9-133">Eftersom inga värden angavs för `Role` eller `Scope` så har det skapade tjänstens huvud namn inte någon behörighet.</span><span class="sxs-lookup"><span data-stu-id="50eb9-133">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="50eb9-134">Exempel 2 – Simple skapa AD-tjänstens huvud objekt med en viss roll och standard omfattning</span><span class="sxs-lookup"><span data-stu-id="50eb9-134">Example 2 - Simple AD service principal creation with a specified role and default scope</span></span>

```
PS C:\> New-AzureRmADServicePrincipal -Role Reader

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz' to the new service principal.
```

<span data-ttu-id="50eb9-135">Med kommandot ovan skapas ett AD-huvudobjekt med standardvärdena för parametrar som inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="50eb9-135">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="50eb9-136">Eftersom program-ID inte har angetts skapades ett program för tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="50eb9-136">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="50eb9-137">Tjänstens huvud namn skapades med "läsare"-behörigheter under den aktuella prenumerationen (sedan inget värde angavs för `Scope` parametern).</span><span class="sxs-lookup"><span data-stu-id="50eb9-137">The service principal was created with "Reader" permissions over the current subscription (since no value was provided for the `Scope` parameter).</span></span>

### <span data-ttu-id="50eb9-138">Exempel 3 – enkelt att skapa AD-UPN med ett angivet omfång och standard roll</span><span class="sxs-lookup"><span data-stu-id="50eb9-138">Example 3 - Simple AD service principal creation with a specified scope and default role</span></span>

```
PS C:\> New-AzureRmADServicePrincipal -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

<span data-ttu-id="50eb9-139">Med kommandot ovan skapas ett AD-huvudobjekt med standardvärdena för parametrar som inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="50eb9-139">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="50eb9-140">Eftersom program-ID inte har angetts skapades ett program för tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="50eb9-140">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="50eb9-141">Tjänstens huvud namn skapades med behörigheter för "deltagare" (sedan inget värde angavs för `Role` parametern) över den tillhandahållna resurs gruppens omfattning.</span><span class="sxs-lookup"><span data-stu-id="50eb9-141">The service principal was created with "Contributor" permissions (since no value was provided for the `Role` parameter) over the provided resource group scope.</span></span>

### <span data-ttu-id="50eb9-142">Exempel 4 – Simple skapa AD-tjänstens huvud objekt med ett angivet omfång och en viss roll</span><span class="sxs-lookup"><span data-stu-id="50eb9-142">Example 4 - Simple AD service principal creation with a specified scope and role</span></span>

```
PS C:\> New-AzureRmADServicePrincipal -Role Reader -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

<span data-ttu-id="50eb9-143">Med kommandot ovan skapas ett AD-huvudobjekt med standardvärdena för parametrar som inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="50eb9-143">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="50eb9-144">Eftersom program-ID inte har angetts skapades ett program för tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="50eb9-144">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="50eb9-145">Tjänstens huvud namn skapades med "läsare"-behörigheter via den tillhandahållna resurs gruppens omfattning.</span><span class="sxs-lookup"><span data-stu-id="50eb9-145">The service principal was created with "Reader" permissions over the provided resource group scope.</span></span>

### <span data-ttu-id="50eb9-146">Exempel 5 – skapa ett nytt AD tjänst-huvudobjekt med program-ID med roll tilldelning</span><span class="sxs-lookup"><span data-stu-id="50eb9-146">Example 5 - Create a new AD service principal using application id with role assignment</span></span>

```
PS C:\> New-AzureRmADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e

ServicePrincipalNames : {34a28ad2-dec4-4a41-bc3b-d22ddf90000e, http://my-temp-app}
ApplicationId         : 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
DisplayName           : my-temp-app
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="50eb9-147">Skapar en ny AD service-huvudprincip för programmet med program-ID ' 34a28ad2-dec4-4a41-bc3b-d22ddf90000e '.</span><span class="sxs-lookup"><span data-stu-id="50eb9-147">Creates a new AD service principal for the application with application id '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'.</span></span> <span data-ttu-id="50eb9-148">Eftersom inga värden angavs för `Role` eller `Scope` så har det skapade tjänstens huvud namn inte någon behörighet.</span><span class="sxs-lookup"><span data-stu-id="50eb9-148">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="50eb9-149">Exempel 6 – skapa ett nytt AD service-huvudobjekt med ledning</span><span class="sxs-lookup"><span data-stu-id="50eb9-149">Example 6 - Create a new AD service principal using piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzureRmADServicePrincipal
```

<span data-ttu-id="50eb9-150">Hämtar programmet med objekt-ID ' 3ede3c26-B443-4e0b-9efc-b05e68338dc3 ' och pipes till New-AzureRmADServicePrincipal cmdlet för att skapa en ny AD-huvudtjänst för det programmet.</span><span class="sxs-lookup"><span data-stu-id="50eb9-150">Gets the application with object id '3ede3c26-b443-4e0b-9efc-b05e68338dc3' and pipes that to the New-AzureRmADServicePrincipal cmdlet to create a new AD service principal for that application.</span></span>

## <span data-ttu-id="50eb9-151">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="50eb9-151">PARAMETERS</span></span>

### <span data-ttu-id="50eb9-152">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="50eb9-152">-ApplicationId</span></span>
<span data-ttu-id="50eb9-153">Unikt program-ID för tjänstens huvud namn i en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="50eb9-153">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="50eb9-154">Det går inte att ändra egenskapen när den har skapats.</span><span class="sxs-lookup"><span data-stu-id="50eb9-154">Once created this property cannot be changed.</span></span>
<span data-ttu-id="50eb9-155">Om inget program-ID anges genereras ett.</span><span class="sxs-lookup"><span data-stu-id="50eb9-155">If an application id is not specified, one will be generated.</span></span>

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

### <span data-ttu-id="50eb9-156">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="50eb9-156">-ApplicationObject</span></span>
<span data-ttu-id="50eb9-157">Det objekt som representerar det program som tjänstens huvud namn skapas för.</span><span class="sxs-lookup"><span data-stu-id="50eb9-157">The object representing the application for which the service principal is created.</span></span>

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

### <span data-ttu-id="50eb9-158">-CertValue</span><span class="sxs-lookup"><span data-stu-id="50eb9-158">-CertValue</span></span>
<span data-ttu-id="50eb9-159">Värdet för autentiseringstypen "asymmetrisk".</span><span class="sxs-lookup"><span data-stu-id="50eb9-159">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="50eb9-160">Den representerar det grundläggande 64-kodade certifikatet.</span><span class="sxs-lookup"><span data-stu-id="50eb9-160">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="50eb9-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50eb9-161">-DefaultProfile</span></span>
<span data-ttu-id="50eb9-162">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="50eb9-162">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50eb9-163">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="50eb9-163">-DisplayName</span></span>
<span data-ttu-id="50eb9-164">Eget namn på tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="50eb9-164">The friendly name of the service principal.</span></span> <span data-ttu-id="50eb9-165">Om inget visnings namn anges används det här värdet som standard "Azure-PowerShell-MM-DD-yyyy-HH-SS", där suffixet är det datum då programmet skapades.</span><span class="sxs-lookup"><span data-stu-id="50eb9-165">If a display name is not provided, this value will default to 'azure-powershell-MM-dd-yyyy-HH-mm-ss', where the suffix is the time of application creation.</span></span>

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

### <span data-ttu-id="50eb9-166">-EndDate</span><span class="sxs-lookup"><span data-stu-id="50eb9-166">-EndDate</span></span>
<span data-ttu-id="50eb9-167">Slutdatum för användning av autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="50eb9-167">The effective end date of the credential usage.</span></span>
<span data-ttu-id="50eb9-168">Standardvärdet för slutdatumet är ett år från idag.</span><span class="sxs-lookup"><span data-stu-id="50eb9-168">The default end date value is one year from today.</span></span> <span data-ttu-id="50eb9-169">För en "asymmetrisk" typ autentiseringsuppgift måste detta ställas in på eller före det datum då X509-certifikatet är giltigt.</span><span class="sxs-lookup"><span data-stu-id="50eb9-169">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="50eb9-170">-Inloggnings uppgifter</span><span class="sxs-lookup"><span data-stu-id="50eb9-170">-KeyCredential</span></span>
<span data-ttu-id="50eb9-171">Insamling av viktiga autentiseringsuppgifter associerade med programmet.</span><span class="sxs-lookup"><span data-stu-id="50eb9-171">The collection of key credentials associated with the application.</span></span>

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

### <span data-ttu-id="50eb9-172">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="50eb9-172">-Password</span></span>
<span data-ttu-id="50eb9-173">Lösen ordet som ska kopplas till tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="50eb9-173">The password to be associated with the service principal.</span></span> <span data-ttu-id="50eb9-174">Om inget lösen ord anges genereras ett slumpmässigt GUID och används som lösen ord.</span><span class="sxs-lookup"><span data-stu-id="50eb9-174">If a password is not provided, a random GUID will be generated and used as the password.</span></span>

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

### <span data-ttu-id="50eb9-175">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="50eb9-175">-PasswordCredential</span></span>
<span data-ttu-id="50eb9-176">Den uppsättning autentiseringsuppgifter för lösen ord som är associerad med programmet.</span><span class="sxs-lookup"><span data-stu-id="50eb9-176">The collection of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="50eb9-177">-Roll</span><span class="sxs-lookup"><span data-stu-id="50eb9-177">-Role</span></span>
<span data-ttu-id="50eb9-178">Rollen som tjänstens huvud namn har.</span><span class="sxs-lookup"><span data-stu-id="50eb9-178">The role that the service principal has over the scope.</span></span> <span data-ttu-id="50eb9-179">Om ett värde `Scope` är angivet, men inget värde är angivet för `Role` , `Role` används rollen "deltagare" som standard.</span><span class="sxs-lookup"><span data-stu-id="50eb9-179">If a value for `Scope` is provided, but no value is provided for `Role`, then `Role` will default to the 'Contributor' role.</span></span>

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

### <span data-ttu-id="50eb9-180">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="50eb9-180">-Scope</span></span>
<span data-ttu-id="50eb9-181">Omfattningen som tjänstens huvud namn har behörighet för.</span><span class="sxs-lookup"><span data-stu-id="50eb9-181">The scope that the service principal has permissions on.</span></span> <span data-ttu-id="50eb9-182">Om ett värde `Role` är angivet men inget värde är angivet för `Scope` `Scope` det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="50eb9-182">If a value for `Role` is provided, but no value is provided for `Scope`, then `Scope` will default to the current subscription.</span></span>

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

### <span data-ttu-id="50eb9-183">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="50eb9-183">-SkipAssignment</span></span>
<span data-ttu-id="50eb9-184">Om den här inställningen är aktive rad kommer du inte att skapa standard roll tilldelning för tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="50eb9-184">If set, will skip creating the default role assignment for the service principal.</span></span>

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

### <span data-ttu-id="50eb9-185">-StartDate</span><span class="sxs-lookup"><span data-stu-id="50eb9-185">-StartDate</span></span>
<span data-ttu-id="50eb9-186">Start datum för användning av autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="50eb9-186">The effective start date of the credential usage.</span></span>
<span data-ttu-id="50eb9-187">Standardvärdet för start datum är idag.</span><span class="sxs-lookup"><span data-stu-id="50eb9-187">The default start date value is today.</span></span> <span data-ttu-id="50eb9-188">För en "asymmetrisk" typ autentiseringsuppgift måste detta ställas in på eller efter det datum då X509-certifikatet är giltigt från.</span><span class="sxs-lookup"><span data-stu-id="50eb9-188">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="50eb9-189">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="50eb9-189">-Confirm</span></span>
<span data-ttu-id="50eb9-190">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="50eb9-190">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50eb9-191">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50eb9-191">-WhatIf</span></span>
<span data-ttu-id="50eb9-192">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="50eb9-192">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50eb9-193">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="50eb9-193">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50eb9-194">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50eb9-194">CommonParameters</span></span>
<span data-ttu-id="50eb9-195">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50eb9-195">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50eb9-196">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50eb9-196">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50eb9-197">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="50eb9-197">INPUTS</span></span>

### <span data-ttu-id="50eb9-198">System. GUID</span><span class="sxs-lookup"><span data-stu-id="50eb9-198">System.Guid</span></span>

### <span data-ttu-id="50eb9-199">System. String</span><span class="sxs-lookup"><span data-stu-id="50eb9-199">System.String</span></span>

### <span data-ttu-id="50eb9-200">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="50eb9-200">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="50eb9-201">Parametrar: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="50eb9-201">Parameters: ApplicationObject (ByValue)</span></span>

### <span data-ttu-id="50eb9-202">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="50eb9-202">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="50eb9-203">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="50eb9-203">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="50eb9-204">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="50eb9-204">System.Security.SecureString</span></span>

### <span data-ttu-id="50eb9-205">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="50eb9-205">System.DateTime</span></span>

## <span data-ttu-id="50eb9-206">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="50eb9-206">OUTPUTS</span></span>

### <span data-ttu-id="50eb9-207">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="50eb9-207">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="50eb9-208">Microsoft. Azure. kommandon. sources. Models. Authorization. PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="50eb9-208">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="50eb9-209">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="50eb9-209">NOTES</span></span>
<span data-ttu-id="50eb9-210">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="50eb9-210">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="50eb9-211">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="50eb9-211">RELATED LINKS</span></span>

[<span data-ttu-id="50eb9-212">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="50eb9-212">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="50eb9-213">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="50eb9-213">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="50eb9-214">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="50eb9-214">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="50eb9-215">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="50eb9-215">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="50eb9-216">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="50eb9-216">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="50eb9-217">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="50eb9-217">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="50eb9-218">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="50eb9-218">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

