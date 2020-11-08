---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/add-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Add-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Add-AzResourceMoverMoveResource.md
ms.openlocfilehash: bafba030de13cdee2c4b7026f498c07cf4231fdd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259675"
---
# <span data-ttu-id="e6761-101">Add-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="e6761-101">Add-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="e6761-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e6761-102">SYNOPSIS</span></span>
<span data-ttu-id="e6761-103">Skapar eller uppdaterar en flytt resurs i flytt mängden.</span><span class="sxs-lookup"><span data-stu-id="e6761-103">Creates or updates a Move Resource in the move collection.</span></span>

## <span data-ttu-id="e6761-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e6761-104">SYNTAX</span></span>

```
Add-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DependsOnOverride <IMoveResourceDependencyOverride[]>]
 [-ExistingTargetId <String>] [-ResourceSettingResourceType <String>]
 [-ResourceSettingTargetResourceName <String>] [-SourceId <String>]
 [-SourceResourceSettingResourceType <String>] [-SourceResourceSettingTargetResourceName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e6761-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e6761-105">DESCRIPTION</span></span>
<span data-ttu-id="e6761-106">Skapar eller uppdaterar en flytt resurs i flytt mängden.</span><span class="sxs-lookup"><span data-stu-id="e6761-106">Creates or updates a Move Resource in the move collection.</span></span>

## <span data-ttu-id="e6761-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e6761-107">EXAMPLES</span></span>

### <span data-ttu-id="e6761-108">Exempel 1: lägga till en resurs i flytt mängden.</span><span class="sxs-lookup"><span data-stu-id="e6761-108">Example 1: Adding a resource to the move collection.</span></span>
```powershell
PS C:\> Add-AzResourceMoverMoveResource -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName "PS-centralus-westcentralus-demoRM" -SourceId "/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachines/PSDemoVM" -Name PSDemoVM -ResourceSettingResourceType "Microsoft.Compute/virtualMachines" -ResourceSettingTargetResourceName PSDemoVM

Output:

Code                                    :
DependsOn                               : {}
DependsOnOverride                       : {}
Detail                                  :
ExistingTargetId                        :
Id                                      : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migr
                                          ate/MoveCollections/PS-centralus-westcentralus-demoRM/MoveResources/PSDemoVM
Message                                 :
MoveStatusCode                          : DependencyComputationPending
MoveStatusDetail                        : {}
MoveStatusJobName                       :
MoveStatusJobProgress                   :
MoveStatusMessage                       : The dependency computation is not completed for resource - /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resou
                                          rceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachines/PSDemoVM.
                                              Possible Causes: Dependency computation is pending for resource.
                                              Recommended Action: Validate dependencies to compute the dependencies.

MoveStatusMoveState                     : PreparePending
MoveStatusTarget                        :
MoveStatusTargetId                      :
Name                                    : PSDemoVM
ProvisioningState                       : Succeeded
ResourceSettingResourceType             : Microsoft.Compute/virtualMachines
ResourceSettingTargetResourceName       : PSDemoVM
SourceId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachi
                                          nes/PSDemoVM
SourceResourceSettingResourceType       : Microsoft.Compute/virtualMachines
SourceResourceSettingTargetResourceName : PSDemoVM
Target                                  :
TargetId                                :
Type          

```

<span data-ttu-id="e6761-109">Lägga till en resurs i flytt samlingen inom det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="e6761-109">Adding a resource to the move collection within the specified subscription.</span></span>

## <span data-ttu-id="e6761-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e6761-110">PARAMETERS</span></span>

### <span data-ttu-id="e6761-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6761-111">-AsJob</span></span>
<span data-ttu-id="e6761-112">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="e6761-112">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6761-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6761-113">-DefaultProfile</span></span>
<span data-ttu-id="e6761-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e6761-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6761-115">-DependsOnOverride</span><span class="sxs-lookup"><span data-stu-id="e6761-115">-DependsOnOverride</span></span>
<span data-ttu-id="e6761-116">Hämtar eller anger åsidosättningar för flytt av resurs beroenden.</span><span class="sxs-lookup"><span data-stu-id="e6761-116">Gets or sets the move resource dependencies overrides.</span></span>
<span data-ttu-id="e6761-117">För att konstruera kan du läsa avsnittet anteckningar för DEPENDSONOVERRIDE-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="e6761-117">To construct, see NOTES section for DEPENDSONOVERRIDE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveResourceDependencyOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6761-118">-ExistingTargetId</span><span class="sxs-lookup"><span data-stu-id="e6761-118">-ExistingTargetId</span></span>
<span data-ttu-id="e6761-119">Hämtar eller anger resursens befintliga Målprogram-ID.</span><span class="sxs-lookup"><span data-stu-id="e6761-119">Gets or sets the existing target ARM Id of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6761-120">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="e6761-120">-MoveCollectionName</span></span>
<span data-ttu-id="e6761-121">Namn på flytta-samlingen.</span><span class="sxs-lookup"><span data-stu-id="e6761-121">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6761-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="e6761-122">-Name</span></span>
<span data-ttu-id="e6761-123">Namnet på den flyttade resursen.</span><span class="sxs-lookup"><span data-stu-id="e6761-123">The Move Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6761-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="e6761-124">-NoWait</span></span>
<span data-ttu-id="e6761-125">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="e6761-125">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6761-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6761-126">-ResourceGroupName</span></span>
<span data-ttu-id="e6761-127">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="e6761-127">The Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6761-128">-ResourceSettingResourceType</span><span class="sxs-lookup"><span data-stu-id="e6761-128">-ResourceSettingResourceType</span></span>
<span data-ttu-id="e6761-129">Resurs typen.</span><span class="sxs-lookup"><span data-stu-id="e6761-129">The resource type.</span></span>
<span data-ttu-id="e6761-130">Värdet kan till exempel vara Microsoft. Compute/virtualMachines.</span><span class="sxs-lookup"><span data-stu-id="e6761-130">For example, the value can be Microsoft.Compute/virtualMachines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6761-131">-ResourceSettingTargetResourceName</span><span class="sxs-lookup"><span data-stu-id="e6761-131">-ResourceSettingTargetResourceName</span></span>
<span data-ttu-id="e6761-132">Hämtar eller anger mål resursens namn.</span><span class="sxs-lookup"><span data-stu-id="e6761-132">Gets or sets the target Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6761-133">-SourceId</span><span class="sxs-lookup"><span data-stu-id="e6761-133">-SourceId</span></span>
<span data-ttu-id="e6761-134">Hämtar eller anger resursens käll ARM-ID.</span><span class="sxs-lookup"><span data-stu-id="e6761-134">Gets or sets the Source ARM Id of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6761-135">-SourceResourceSettingResourceType</span><span class="sxs-lookup"><span data-stu-id="e6761-135">-SourceResourceSettingResourceType</span></span>
<span data-ttu-id="e6761-136">Resurs typen.</span><span class="sxs-lookup"><span data-stu-id="e6761-136">The resource type.</span></span>
<span data-ttu-id="e6761-137">Värdet kan till exempel vara Microsoft. Compute/virtualMachines.</span><span class="sxs-lookup"><span data-stu-id="e6761-137">For example, the value can be Microsoft.Compute/virtualMachines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6761-138">-SourceResourceSettingTargetResourceName</span><span class="sxs-lookup"><span data-stu-id="e6761-138">-SourceResourceSettingTargetResourceName</span></span>
<span data-ttu-id="e6761-139">Hämtar eller anger mål resursens namn.</span><span class="sxs-lookup"><span data-stu-id="e6761-139">Gets or sets the target Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6761-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e6761-140">-SubscriptionId</span></span>
<span data-ttu-id="e6761-141">Abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="e6761-141">The Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6761-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e6761-142">-Confirm</span></span>
<span data-ttu-id="e6761-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e6761-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6761-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6761-144">-WhatIf</span></span>
<span data-ttu-id="e6761-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e6761-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6761-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e6761-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6761-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6761-147">CommonParameters</span></span>
<span data-ttu-id="e6761-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6761-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6761-149">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6761-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6761-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e6761-150">INPUTS</span></span>

## <span data-ttu-id="e6761-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e6761-151">OUTPUTS</span></span>

### <span data-ttu-id="e6761-152">Microsoft. Azure. PowerShell. cmdletar. ResourceMover. Models. Api20191001Preview. IMoveResource</span><span class="sxs-lookup"><span data-stu-id="e6761-152">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveResource</span></span>

## <span data-ttu-id="e6761-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e6761-153">NOTES</span></span>

<span data-ttu-id="e6761-154">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e6761-154">ALIASES</span></span>

<span data-ttu-id="e6761-155">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="e6761-155">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e6761-156">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="e6761-156">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e6761-157">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e6761-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e6761-158">DEPENDSONOVERRIDE <IMoveResourceDependencyOverride [] >: hämtar eller anger åsidosättningarna för att flytta resurs beroenden.</span><span class="sxs-lookup"><span data-stu-id="e6761-158">DEPENDSONOVERRIDE <IMoveResourceDependencyOverride[]>: Gets or sets the move resource dependencies overrides.</span></span>
  - <span data-ttu-id="e6761-159">`[Id <String>]`: Hämtar eller anger ID för den beroende resursen.</span><span class="sxs-lookup"><span data-stu-id="e6761-159">`[Id <String>]`: Gets or sets the ARM ID of the dependent resource.</span></span>
  - <span data-ttu-id="e6761-160">`[TargetId <String>]`: Hämtar eller anger Resource ARM-ID för antingen MoveResource eller Resource ARM-ID för den beroende resursen.</span><span class="sxs-lookup"><span data-stu-id="e6761-160">`[TargetId <String>]`: Gets or sets the resource ARM id of either the MoveResource or the resource ARM ID of         the dependent resource.</span></span>

## <span data-ttu-id="e6761-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e6761-161">RELATED LINKS</span></span>

