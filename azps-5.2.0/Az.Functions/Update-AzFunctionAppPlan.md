---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
ms.openlocfilehash: e0831e95a5601d3558af7089825684cc48e7838c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401288"
---
# <span data-ttu-id="a6128-101">Update-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="a6128-101">Update-AzFunctionAppPlan</span></span>

## <span data-ttu-id="a6128-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a6128-102">SYNOPSIS</span></span>
<span data-ttu-id="a6128-103">Uppdaterar en tjänste plan för en funktion.</span><span class="sxs-lookup"><span data-stu-id="a6128-103">Updates a function app service plan.</span></span>

## <span data-ttu-id="a6128-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a6128-104">SYNTAX</span></span>

### <span data-ttu-id="a6128-105">ByName (standard)</span><span class="sxs-lookup"><span data-stu-id="a6128-105">ByName (Default)</span></span>
```
Update-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a6128-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="a6128-106">ByObjectInput</span></span>
```
Update-AzFunctionAppPlan -InputObject <IAppServicePlan> [-MaximumWorkerCount <Int32>]
 [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a6128-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a6128-107">DESCRIPTION</span></span>
<span data-ttu-id="a6128-108">Uppdaterar en tjänste plan för en funktion.</span><span class="sxs-lookup"><span data-stu-id="a6128-108">Updates a function app service plan.</span></span>

## <span data-ttu-id="a6128-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a6128-109">EXAMPLES</span></span>

### <span data-ttu-id="a6128-110">Exempel 1: uppdatera en app service-plan till EP2 SKU med 20 högsta arbets kraft.</span><span class="sxs-lookup"><span data-stu-id="a6128-110">Example 1: Update an app service plan to EP2 sku with twenty maximum workers.</span></span>
```powershell
PS C:\> Update-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                                 -Name MyPremiumPlan `
                                 -MaximumWorkerCount 20 `
                                 -Sku EP2

```

<span data-ttu-id="a6128-111">Det här kommandot uppdaterar en app service-plan till EP2 SKU med högst tjugo anställda.</span><span class="sxs-lookup"><span data-stu-id="a6128-111">This command updates an app service plan to EP2 sku with twenty maximum workers.</span></span>

## <span data-ttu-id="a6128-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a6128-112">PARAMETERS</span></span>

### <span data-ttu-id="a6128-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6128-113">-AsJob</span></span>
<span data-ttu-id="a6128-114">Kör kommandot som ett jobb.</span><span class="sxs-lookup"><span data-stu-id="a6128-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="a6128-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6128-115">-DefaultProfile</span></span>


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

### <span data-ttu-id="a6128-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6128-116">-InputObject</span></span>
<span data-ttu-id="a6128-117">För att konstruera kan du läsa avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="a6128-117">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6128-118">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="a6128-118">-MaximumWorkerCount</span></span>
<span data-ttu-id="a6128-119">Maximalt antal arbetare för App Service-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="a6128-119">The maximum number of workers for the app service plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MaxBurst

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6128-120">-MinimumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="a6128-120">-MinimumWorkerCount</span></span>
<span data-ttu-id="a6128-121">Det minsta antalet arbetare för App Service-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="a6128-121">The minimum number of workers for the app service plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MinInstances

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6128-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="a6128-122">-Name</span></span>
<span data-ttu-id="a6128-123">Namn på App Service-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="a6128-123">Name of the App Service plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6128-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="a6128-124">-NoWait</span></span>
<span data-ttu-id="a6128-125">Kör kommandot asynkront.</span><span class="sxs-lookup"><span data-stu-id="a6128-125">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="a6128-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6128-126">-ResourceGroupName</span></span>
<span data-ttu-id="a6128-127">Namnet på den resurs grupp som resursen tillhör.</span><span class="sxs-lookup"><span data-stu-id="a6128-127">Name of the resource group to which the resource belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6128-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="a6128-128">-Sku</span></span>
<span data-ttu-id="a6128-129">Abonnemangs-SKU.</span><span class="sxs-lookup"><span data-stu-id="a6128-129">The plan sku.</span></span>
<span data-ttu-id="a6128-130">Giltiga indata är: EP1, EP2, EP3</span><span class="sxs-lookup"><span data-stu-id="a6128-130">Valid inputs are: EP1, EP2, EP3</span></span>

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

### <span data-ttu-id="a6128-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a6128-131">-SubscriptionId</span></span>
<span data-ttu-id="a6128-132">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="a6128-132">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6128-133">-Tagg</span><span class="sxs-lookup"><span data-stu-id="a6128-133">-Tag</span></span>
<span data-ttu-id="a6128-134">Resource-taggar.</span><span class="sxs-lookup"><span data-stu-id="a6128-134">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6128-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a6128-135">-Confirm</span></span>
<span data-ttu-id="a6128-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a6128-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6128-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6128-137">-WhatIf</span></span>
<span data-ttu-id="a6128-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a6128-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6128-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a6128-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6128-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6128-140">CommonParameters</span></span>
<span data-ttu-id="a6128-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6128-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6128-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6128-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6128-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a6128-143">INPUTS</span></span>

### <span data-ttu-id="a6128-144">Microsoft. Azure. PowerShell. cmdletar. functions. Models. Api20190801. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a6128-144">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="a6128-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a6128-145">OUTPUTS</span></span>

### <span data-ttu-id="a6128-146">Microsoft. Azure. PowerShell. cmdletar. functions. Models. Api20190801. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a6128-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="a6128-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a6128-147">NOTES</span></span>

<span data-ttu-id="a6128-148">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a6128-148">ALIASES</span></span>

<span data-ttu-id="a6128-149">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="a6128-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a6128-150">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="a6128-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a6128-151">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a6128-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a6128-152">INPUTOBJECT <IAppServicePlan> :</span><span class="sxs-lookup"><span data-stu-id="a6128-152">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="a6128-153">`Location <String>`: Resurs plats.</span><span class="sxs-lookup"><span data-stu-id="a6128-153">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="a6128-154">`[Kind <String>]`: Typ av resurs.</span><span class="sxs-lookup"><span data-stu-id="a6128-154">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="a6128-155">`[Tag <IResourceTags>]`: Resursfiler.</span><span class="sxs-lookup"><span data-stu-id="a6128-155">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="a6128-156">`[(Any) <String>]`: Detta indikerar att en egenskap kan läggas till i det här objektet.</span><span class="sxs-lookup"><span data-stu-id="a6128-156">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="a6128-157">`[Capacity <Int32?>]`: Aktuellt antal instanser tilldelade till resursen.</span><span class="sxs-lookup"><span data-stu-id="a6128-157">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="a6128-158">`[FreeOfferExpirationTime <DateTime?>]`: Den tid då gratis erbjudandet från Server gruppen upphör.</span><span class="sxs-lookup"><span data-stu-id="a6128-158">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="a6128-159">`[HostingEnvironmentProfileId <String>]`: Resurs-ID för App Service Environment.</span><span class="sxs-lookup"><span data-stu-id="a6128-159">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="a6128-160">`[HyperV <Boolean?>]`: Om programmet för Hyper-V-programtjänsten <code>true</code> , <code>false</code> annars.</span><span class="sxs-lookup"><span data-stu-id="a6128-160">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="a6128-161">`[IsSpot <Boolean?>]`: Om <code>true</code> den här app service-planen äger plats instanser.</span><span class="sxs-lookup"><span data-stu-id="a6128-161">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="a6128-162">`[IsXenon <Boolean?>]`: Överflödig: om programmet för Hyper-V-programtjänsten <code>true</code> , <code>false</code> annars.</span><span class="sxs-lookup"><span data-stu-id="a6128-162">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="a6128-163">`[MaximumElasticWorkerCount <Int32?>]`: Maximalt antal arbetare som är tillåtna för denna ElasticScaleEnabled App Service-plan</span><span class="sxs-lookup"><span data-stu-id="a6128-163">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="a6128-164">`[PerSiteScaling <Boolean?>]`: Om <code>true</code> program som tilldelats den här app service-planen kan skalas oberoende av varandra.</span><span class="sxs-lookup"><span data-stu-id="a6128-164">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="a6128-165">Om <code>false</code> program som tilldelats den här app service-planen anpassas till alla instanser av planen.</span><span class="sxs-lookup"><span data-stu-id="a6128-165">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="a6128-166">`[Reserved <Boolean?>]`: Om programmet Linux app service <code>true</code> är på <code>false</code> annat sätt.</span><span class="sxs-lookup"><span data-stu-id="a6128-166">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="a6128-167">`[SkuCapability <ICapability[]>]`: Med SKU, till exempel, är Traffic Manager aktiverat?</span><span class="sxs-lookup"><span data-stu-id="a6128-167">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="a6128-168">`[Name <String>]`: SKU-funktionens namn.</span><span class="sxs-lookup"><span data-stu-id="a6128-168">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="a6128-169">`[Reason <String>]`: Orsaken till SKU-funktionen.</span><span class="sxs-lookup"><span data-stu-id="a6128-169">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="a6128-170">`[Value <String>]`: Värdet på SKU-funktionen.</span><span class="sxs-lookup"><span data-stu-id="a6128-170">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="a6128-171">`[SkuCapacityDefault <Int32?>]`: Standard antal arbetare för den här app service-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="a6128-171">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="a6128-172">`[SkuCapacityMaximum <Int32?>]`: Det högsta antalet arbetare för den här app service-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="a6128-172">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="a6128-173">`[SkuCapacityMinimum <Int32?>]`: Lägsta antal arbetare för den här app service-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="a6128-173">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="a6128-174">`[SkuCapacityScaleType <String>]`: Tillgängliga skal konfiguration för en app service-plan.</span><span class="sxs-lookup"><span data-stu-id="a6128-174">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="a6128-175">`[SkuFamily <String>]`: Familje kod för resurs-SKU.</span><span class="sxs-lookup"><span data-stu-id="a6128-175">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="a6128-176">`[SkuLocation <String[]>]`: Lager platsens platser.</span><span class="sxs-lookup"><span data-stu-id="a6128-176">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="a6128-177">`[SkuName <String>]`: Resurs-SKU-namnet.</span><span class="sxs-lookup"><span data-stu-id="a6128-177">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="a6128-178">`[SkuSize <String>]`: Ange storlek för resurs-SKU.</span><span class="sxs-lookup"><span data-stu-id="a6128-178">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="a6128-179">`[SkuTier <String>]`: Tjänst nivå för resurs-SKU.</span><span class="sxs-lookup"><span data-stu-id="a6128-179">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="a6128-180">`[SpotExpirationTime <DateTime?>]`: Tiden då Server gruppen upphör att gälla.</span><span class="sxs-lookup"><span data-stu-id="a6128-180">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="a6128-181">Endast giltig om det är en plats Server grupp.</span><span class="sxs-lookup"><span data-stu-id="a6128-181">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="a6128-182">`[TargetWorkerCount <Int32?>]`: Skala antalet arbets tagare.</span><span class="sxs-lookup"><span data-stu-id="a6128-182">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="a6128-183">`[TargetWorkerSizeId <Int32?>]`: Skala arbetarens storleks-ID.</span><span class="sxs-lookup"><span data-stu-id="a6128-183">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="a6128-184">`[WorkerTierName <String>]`: Mål jobb nivå som tilldelats App Service-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="a6128-184">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="a6128-185">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a6128-185">RELATED LINKS</span></span>

