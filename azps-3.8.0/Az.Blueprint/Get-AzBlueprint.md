---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
ms.openlocfilehash: 512efeff7d89c8c9a95a3db8bbfe755564f8dadc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090102"
---
# <span data-ttu-id="26e43-101">Get-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="26e43-101">Get-AzBlueprint</span></span>

## <span data-ttu-id="26e43-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="26e43-102">SYNOPSIS</span></span>
<span data-ttu-id="26e43-103">Få en eller flera utkast.</span><span class="sxs-lookup"><span data-stu-id="26e43-103">Get one or more blueprint definitions.</span></span>

## <span data-ttu-id="26e43-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="26e43-104">SYNTAX</span></span>

### <span data-ttu-id="26e43-105">SubscriptionScope (standard)</span><span class="sxs-lookup"><span data-stu-id="26e43-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprint [[-SubscriptionId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26e43-106">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="26e43-106">BySubscriptionAndName</span></span>
```
Get-AzBlueprint [[-SubscriptionId] <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="26e43-107">BySubscriptionNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="26e43-107">BySubscriptionNameAndVersion</span></span>
```
Get-AzBlueprint [[-SubscriptionId] <String>] [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26e43-108">BySubscriptionNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="26e43-108">BySubscriptionNameAndLatestPublished</span></span>
```
Get-AzBlueprint [[-SubscriptionId] <String>] [-Name] <String> [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26e43-109">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="26e43-109">ManagementGroupScope</span></span>
```
Get-AzBlueprint [-ManagementGroupId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26e43-110">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="26e43-110">ByManagementGroupAndName</span></span>
```
Get-AzBlueprint [-ManagementGroupId] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="26e43-111">ByManagementGroupNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="26e43-111">ByManagementGroupNameAndVersion</span></span>
```
Get-AzBlueprint [-ManagementGroupId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26e43-112">ByManagementGroupNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="26e43-112">ByManagementGroupNameAndLatestPublished</span></span>
```
Get-AzBlueprint [-ManagementGroupId] <String> [-Name] <String> [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26e43-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="26e43-113">DESCRIPTION</span></span>
<span data-ttu-id="26e43-114">Få en eller flera utkast.</span><span class="sxs-lookup"><span data-stu-id="26e43-114">Get one or more blueprint definitions.</span></span> <span data-ttu-id="26e43-115">Skissa definitioner finns i hanterings gruppen eller prenumerations omfattningen.</span><span class="sxs-lookup"><span data-stu-id="26e43-115">Blueprint definitions exist at the management group or subscription scope.</span></span>

## <span data-ttu-id="26e43-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="26e43-116">EXAMPLES</span></span>

### <span data-ttu-id="26e43-117">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="26e43-117">Example 1</span></span>
```powershell
PS> Get-AzBlueprint

Name                 : PS-BlueprintDefinition
Id                   : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprints/PS-BlueprintDefinition
SubscriptionId       : 00000000-1111-0000-1111-000000000000
Versions             : {1.0}
Description          : Powershell test blueprint
TimeCreated          : 2019-02-01
TargetScope          : Subscription
Parameters           : {storageData_storageAccountType, storageData_location, allowedlocations_listOfAllowedLocations}
ResourceGroups       : ResourceGroup
```

<span data-ttu-id="26e43-118">Få skiss-definitionerna i det aktuella abonnemanget och hierarkin för hanterings grupp för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="26e43-118">Get the blueprint definitions within the current subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="26e43-119">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="26e43-119">Example 2</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId"

Name                 : PS-MG-BlueprintDefinition
Id                   : /providers/Microsoft.Management/managementGroups/myManagementGroupId/providers/Microsoft.Blueprint/blueprints/PS-MG-BlueprintDefinition
ManagementGroupId    : myManagementGroupId
Versions             : {1.0, 2.0, 3.0, 4.0}
TimeCreated          : 2019-03-04
TargetScope          : Subscription
Parameters           : {enforcetaganditsvalue_tagName, enforcetaganditsvalue_tagValue, [Usergrouporapplicationname]:Contributor_RoleAssignmentName,
                       [Usergrouporapplicationname]:Owner_RoleAssignmentName}
ResourceGroups       : {ResourceGroup, ResourceGroup2}
```

<span data-ttu-id="26e43-120">Få skiss-definitionerna i den angivna hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="26e43-120">Get the blueprint definitions within the specified management group.</span></span>

### <span data-ttu-id="26e43-121">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="26e43-121">Example 3</span></span>
```powershell
PS> Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000"

Name                 : PS-BlueprintDefinition
Id                   : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprints/PS-BlueprintDefinition
SubscriptionId       : 00000000-1111-0000-1111-000000000000
Versions             : {1.0}
Description          : Powershell test blueprint
TimeCreated          : 2019-02-01
TargetScope          : Subscription
Parameters           : {storageData_storageAccountType, storageData_location, allowedlocations_listOfAllowedLocations}
ResourceGroups       : ResourceGroup
```

<span data-ttu-id="26e43-122">Få skiss-definitionerna i det angivna abonnemanget och grupphierarkin i hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="26e43-122">Get the blueprint definitions within the specified subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="26e43-123">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="26e43-123">Example 4</span></span>
```powershell
PS> Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
```

<span data-ttu-id="26e43-124">Få skiss-definitionen med det angivna namnet inom det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="26e43-124">Get the blueprint definition with the given name within the specified subscription.</span></span>

### <span data-ttu-id="26e43-125">Exempel 5</span><span class="sxs-lookup"><span data-stu-id="26e43-125">Example 5</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -Version "myBlueprintVersion"
```

<span data-ttu-id="26e43-126">Få ritnings definitionen med angivet namn och version i den angivna hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="26e43-126">Get the blueprint definition with the given name and version within the specified management group.</span></span>

### <span data-ttu-id="26e43-127">Exempel 6</span><span class="sxs-lookup"><span data-stu-id="26e43-127">Example 6</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -LatestPublished
```

<span data-ttu-id="26e43-128">Hämta den senaste publicerade utkasts definitionen med det angivna namnet i den angivna hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="26e43-128">Get the latest published blueprint definition with the given name within the specified management group.</span></span>

## <span data-ttu-id="26e43-129">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="26e43-129">PARAMETERS</span></span>

### <span data-ttu-id="26e43-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26e43-130">-DefaultProfile</span></span>
<span data-ttu-id="26e43-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="26e43-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26e43-132">-LatestPublished</span><span class="sxs-lookup"><span data-stu-id="26e43-132">-LatestPublished</span></span>
<span data-ttu-id="26e43-133">Den senaste publicerade utkasts flaggan.</span><span class="sxs-lookup"><span data-stu-id="26e43-133">The latest published blueprint definition flag.</span></span>
<span data-ttu-id="26e43-134">När funktionen är aktive rad returnerar exekvering den senaste publicerade versionen av ritnings definitionen.</span><span class="sxs-lookup"><span data-stu-id="26e43-134">When set, execution returns the latest published version of the blueprint definition.</span></span>
<span data-ttu-id="26e43-135">Standardvärdet är falskt.</span><span class="sxs-lookup"><span data-stu-id="26e43-135">Defaults to false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BySubscriptionNameAndLatestPublished, ByManagementGroupNameAndLatestPublished
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26e43-136">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="26e43-136">-ManagementGroupId</span></span>
<span data-ttu-id="26e43-137">Hanterings grupp-ID där utkastet sparas.</span><span class="sxs-lookup"><span data-stu-id="26e43-137">Management Group Id where the blueprint definition is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupScope, ByManagementGroupAndName, ByManagementGroupNameAndVersion, ByManagementGroupNameAndLatestPublished
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26e43-138">-Namn</span><span class="sxs-lookup"><span data-stu-id="26e43-138">-Name</span></span>
<span data-ttu-id="26e43-139">Utkastets namn.</span><span class="sxs-lookup"><span data-stu-id="26e43-139">Blueprint definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName, BySubscriptionNameAndVersion, BySubscriptionNameAndLatestPublished, ByManagementGroupAndName, ByManagementGroupNameAndVersion, ByManagementGroupNameAndLatestPublished
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26e43-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="26e43-140">-SubscriptionId</span></span>
<span data-ttu-id="26e43-141">Abonnemangs-ID där ritnings definitionen sparas.</span><span class="sxs-lookup"><span data-stu-id="26e43-141">Subscription Id where the blueprint definition is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, BySubscriptionAndName, BySubscriptionNameAndVersion, BySubscriptionNameAndLatestPublished
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26e43-142">-Version</span><span class="sxs-lookup"><span data-stu-id="26e43-142">-Version</span></span>
<span data-ttu-id="26e43-143">Publicerad version för ritnings definition.</span><span class="sxs-lookup"><span data-stu-id="26e43-143">Published blueprint definition version.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionNameAndVersion, ByManagementGroupNameAndVersion
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26e43-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26e43-144">CommonParameters</span></span>
<span data-ttu-id="26e43-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26e43-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26e43-146">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26e43-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26e43-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="26e43-147">INPUTS</span></span>

### <span data-ttu-id="26e43-148">System. String</span><span class="sxs-lookup"><span data-stu-id="26e43-148">System.String</span></span>

## <span data-ttu-id="26e43-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="26e43-149">OUTPUTS</span></span>

### <span data-ttu-id="26e43-150">System. Object</span><span class="sxs-lookup"><span data-stu-id="26e43-150">System.Object</span></span>
## <span data-ttu-id="26e43-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="26e43-151">NOTES</span></span>

## <span data-ttu-id="26e43-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="26e43-152">RELATED LINKS</span></span>