---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/remove-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
ms.openlocfilehash: 6668952ba07327482da7ed3c274eb003ac61c73c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523625"
---
# <span data-ttu-id="9da27-101">Remove-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="9da27-101">Remove-AzFunctionAppPlan</span></span>

## <span data-ttu-id="9da27-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9da27-102">SYNOPSIS</span></span>
<span data-ttu-id="9da27-103">Tar bort en program plan för en funktion.</span><span class="sxs-lookup"><span data-stu-id="9da27-103">Deletes a function app plan.</span></span>

## <span data-ttu-id="9da27-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9da27-104">SYNTAX</span></span>

### <span data-ttu-id="9da27-105">ByName (standard)</span><span class="sxs-lookup"><span data-stu-id="9da27-105">ByName (Default)</span></span>
```
Remove-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9da27-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="9da27-106">ByObjectInput</span></span>
```
Remove-AzFunctionAppPlan -InputObject <IAppServicePlan> [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9da27-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9da27-107">DESCRIPTION</span></span>
<span data-ttu-id="9da27-108">Tar bort en program plan för en funktion.</span><span class="sxs-lookup"><span data-stu-id="9da27-108">Deletes a function app plan.</span></span>

## <span data-ttu-id="9da27-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9da27-109">EXAMPLES</span></span>

### <span data-ttu-id="9da27-110">Exempel 1: skaffa en Function app-plan efter namn och ta bort den.</span><span class="sxs-lookup"><span data-stu-id="9da27-110">Example 1: Get a function app plan by name and delete it.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName | Remove-AzFunctionAppPlan -Force
```

<span data-ttu-id="9da27-111">Det här kommandot får en funktions program plan efter namn och tar bort det.</span><span class="sxs-lookup"><span data-stu-id="9da27-111">This command gets a function app plan by name and deletes it.</span></span>

### <span data-ttu-id="9da27-112">Exempel 2: ta bort en funktion program plan efter namn.</span><span class="sxs-lookup"><span data-stu-id="9da27-112">Example 2: Delete a function app plan by name.</span></span>
```powershell
PS C:\> Remove-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

<span data-ttu-id="9da27-113">Detta kommando tar bort en funktion program plan efter namn.</span><span class="sxs-lookup"><span data-stu-id="9da27-113">This command deletes a function app plan by name.</span></span>

## <span data-ttu-id="9da27-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9da27-114">PARAMETERS</span></span>

### <span data-ttu-id="9da27-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9da27-115">-DefaultProfile</span></span>
<span data-ttu-id="9da27-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9da27-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9da27-117">-Force</span><span class="sxs-lookup"><span data-stu-id="9da27-117">-Force</span></span>
<span data-ttu-id="9da27-118">Tvingar cmdleten att ta bort programmet Function utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="9da27-118">Forces the cmdlet to remove the function app plan without prompting for confirmation.</span></span>

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

### <span data-ttu-id="9da27-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9da27-119">-InputObject</span></span>
<span data-ttu-id="9da27-120">För att konstruera kan du läsa avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="9da27-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9da27-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="9da27-121">-Name</span></span>
<span data-ttu-id="9da27-122">Namnet på funktions programmet.</span><span class="sxs-lookup"><span data-stu-id="9da27-122">The name of function app.</span></span>

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

### <span data-ttu-id="9da27-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9da27-123">-PassThru</span></span>
<span data-ttu-id="9da27-124">Returnerar sant när kommandot fungerar.</span><span class="sxs-lookup"><span data-stu-id="9da27-124">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="9da27-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9da27-125">-ResourceGroupName</span></span>


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

### <span data-ttu-id="9da27-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9da27-126">-SubscriptionId</span></span>
<span data-ttu-id="9da27-127">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="9da27-127">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="9da27-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9da27-128">-Confirm</span></span>
<span data-ttu-id="9da27-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9da27-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9da27-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9da27-130">-WhatIf</span></span>
<span data-ttu-id="9da27-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9da27-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9da27-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9da27-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9da27-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9da27-133">CommonParameters</span></span>
<span data-ttu-id="9da27-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9da27-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9da27-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9da27-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9da27-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9da27-136">INPUTS</span></span>

### <span data-ttu-id="9da27-137">Microsoft. Azure. PowerShell. cmdletar. functions. Models. Api20190801. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9da27-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="9da27-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9da27-138">OUTPUTS</span></span>

### <span data-ttu-id="9da27-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9da27-139">System.Boolean</span></span>

## <span data-ttu-id="9da27-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9da27-140">NOTES</span></span>

<span data-ttu-id="9da27-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="9da27-141">ALIASES</span></span>

<span data-ttu-id="9da27-142">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="9da27-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9da27-143">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="9da27-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9da27-144">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9da27-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9da27-145">INPUTOBJECT <IAppServicePlan> :</span><span class="sxs-lookup"><span data-stu-id="9da27-145">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="9da27-146">`Location <String>`: Resurs plats.</span><span class="sxs-lookup"><span data-stu-id="9da27-146">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="9da27-147">`[Kind <String>]`: Typ av resurs.</span><span class="sxs-lookup"><span data-stu-id="9da27-147">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="9da27-148">`[Tag <IResourceTags>]`: Resursfiler.</span><span class="sxs-lookup"><span data-stu-id="9da27-148">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="9da27-149">`[(Any) <String>]`: Detta indikerar att en egenskap kan läggas till i det här objektet.</span><span class="sxs-lookup"><span data-stu-id="9da27-149">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="9da27-150">`[Capacity <Int32?>]`: Aktuellt antal instanser tilldelade till resursen.</span><span class="sxs-lookup"><span data-stu-id="9da27-150">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="9da27-151">`[FreeOfferExpirationTime <DateTime?>]`: Den tid då gratis erbjudandet från Server gruppen upphör.</span><span class="sxs-lookup"><span data-stu-id="9da27-151">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="9da27-152">`[HostingEnvironmentProfileId <String>]`: Resurs-ID för App Service Environment.</span><span class="sxs-lookup"><span data-stu-id="9da27-152">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="9da27-153">`[HyperV <Boolean?>]`: Om programmet för Hyper-V-programtjänsten <code>true</code> , <code>false</code> annars.</span><span class="sxs-lookup"><span data-stu-id="9da27-153">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="9da27-154">`[IsSpot <Boolean?>]`: Om <code>true</code> den här app service-planen äger plats instanser.</span><span class="sxs-lookup"><span data-stu-id="9da27-154">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="9da27-155">`[IsXenon <Boolean?>]`: Överflödig: om programmet för Hyper-V-programtjänsten <code>true</code> , <code>false</code> annars.</span><span class="sxs-lookup"><span data-stu-id="9da27-155">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="9da27-156">`[MaximumElasticWorkerCount <Int32?>]`: Maximalt antal arbetare som är tillåtna för denna ElasticScaleEnabled App Service-plan</span><span class="sxs-lookup"><span data-stu-id="9da27-156">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="9da27-157">`[PerSiteScaling <Boolean?>]`: Om <code>true</code> program som tilldelats den här app service-planen kan skalas oberoende av varandra.</span><span class="sxs-lookup"><span data-stu-id="9da27-157">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="9da27-158">Om <code>false</code> program som tilldelats den här app service-planen anpassas till alla instanser av planen.</span><span class="sxs-lookup"><span data-stu-id="9da27-158">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="9da27-159">`[Reserved <Boolean?>]`: Om programmet Linux app service <code>true</code> är på <code>false</code> annat sätt.</span><span class="sxs-lookup"><span data-stu-id="9da27-159">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="9da27-160">`[SkuCapability <ICapability[]>]`: Med SKU, till exempel, är Traffic Manager aktiverat?</span><span class="sxs-lookup"><span data-stu-id="9da27-160">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="9da27-161">`[Name <String>]`: SKU-funktionens namn.</span><span class="sxs-lookup"><span data-stu-id="9da27-161">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="9da27-162">`[Reason <String>]`: Orsaken till SKU-funktionen.</span><span class="sxs-lookup"><span data-stu-id="9da27-162">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="9da27-163">`[Value <String>]`: Värdet på SKU-funktionen.</span><span class="sxs-lookup"><span data-stu-id="9da27-163">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="9da27-164">`[SkuCapacityDefault <Int32?>]`: Standard antal arbetare för den här app service-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="9da27-164">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="9da27-165">`[SkuCapacityMaximum <Int32?>]`: Det högsta antalet arbetare för den här app service-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="9da27-165">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="9da27-166">`[SkuCapacityMinimum <Int32?>]`: Lägsta antal arbetare för den här app service-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="9da27-166">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="9da27-167">`[SkuCapacityScaleType <String>]`: Tillgängliga skal konfiguration för en app service-plan.</span><span class="sxs-lookup"><span data-stu-id="9da27-167">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="9da27-168">`[SkuFamily <String>]`: Familje kod för resurs-SKU.</span><span class="sxs-lookup"><span data-stu-id="9da27-168">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="9da27-169">`[SkuLocation <String[]>]`: Lager platsens platser.</span><span class="sxs-lookup"><span data-stu-id="9da27-169">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="9da27-170">`[SkuName <String>]`: Resurs-SKU-namnet.</span><span class="sxs-lookup"><span data-stu-id="9da27-170">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="9da27-171">`[SkuSize <String>]`: Ange storlek för resurs-SKU.</span><span class="sxs-lookup"><span data-stu-id="9da27-171">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="9da27-172">`[SkuTier <String>]`: Tjänst nivå för resurs-SKU.</span><span class="sxs-lookup"><span data-stu-id="9da27-172">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="9da27-173">`[SpotExpirationTime <DateTime?>]`: Tiden då Server gruppen upphör att gälla.</span><span class="sxs-lookup"><span data-stu-id="9da27-173">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="9da27-174">Endast giltig om det är en plats Server grupp.</span><span class="sxs-lookup"><span data-stu-id="9da27-174">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="9da27-175">`[TargetWorkerCount <Int32?>]`: Skala antalet arbets tagare.</span><span class="sxs-lookup"><span data-stu-id="9da27-175">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="9da27-176">`[TargetWorkerSizeId <Int32?>]`: Skala arbetarens storleks-ID.</span><span class="sxs-lookup"><span data-stu-id="9da27-176">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="9da27-177">`[WorkerTierName <String>]`: Mål jobb nivå som tilldelats App Service-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="9da27-177">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="9da27-178">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9da27-178">RELATED LINKS</span></span>

