---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 7f647da2543a4675dad53f88e2494aa7f6c39419
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521895"
---
# <span data-ttu-id="5e393-101">Remove-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="5e393-101">Remove-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="5e393-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5e393-102">SYNOPSIS</span></span>
<span data-ttu-id="5e393-103">Tar bort händelse källan med det angivna namnet i angiven prenumeration, resurs grupp och miljö</span><span class="sxs-lookup"><span data-stu-id="5e393-103">Deletes the event source with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="5e393-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5e393-104">SYNTAX</span></span>

### <span data-ttu-id="5e393-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="5e393-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5e393-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5e393-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5e393-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5e393-107">DESCRIPTION</span></span>
<span data-ttu-id="5e393-108">Tar bort händelse källan med det angivna namnet i angiven prenumeration, resurs grupp och miljö</span><span class="sxs-lookup"><span data-stu-id="5e393-108">Deletes the event source with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="5e393-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5e393-109">EXAMPLES</span></span>

### <span data-ttu-id="5e393-110">Exempel 1: ta bort en viss händelse källa utifrån namn</span><span class="sxs-lookup"><span data-stu-id="5e393-110">Example 1: Remove a specified event source by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -Name iots001 -ResourceGroupName testgroup

```

<span data-ttu-id="5e393-111">Detta tar bort en specifik händelse källa.</span><span class="sxs-lookup"><span data-stu-id="5e393-111">This removes a specific event source.</span></span>

### <span data-ttu-id="5e393-112">Exempel 2: ta bort en angiven händelse källa för objekt</span><span class="sxs-lookup"><span data-stu-id="5e393-112">Example 2: Remove a specified event source by object</span></span>
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name iots001
PS C:\> Remove-AzTimeSeriesInsightsEventSource -InputObject $es

```

<span data-ttu-id="5e393-113">Detta tar bort en specifik händelse källa.</span><span class="sxs-lookup"><span data-stu-id="5e393-113">This removes a specific event source.</span></span>

## <span data-ttu-id="5e393-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5e393-114">PARAMETERS</span></span>

### <span data-ttu-id="5e393-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e393-115">-DefaultProfile</span></span>
<span data-ttu-id="5e393-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5e393-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e393-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="5e393-117">-EnvironmentName</span></span>
<span data-ttu-id="5e393-118">Namnet på den miljö för tids serie som är kopplad till den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5e393-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e393-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e393-119">-InputObject</span></span>
<span data-ttu-id="5e393-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="5e393-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e393-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="5e393-121">-Name</span></span>
<span data-ttu-id="5e393-122">Namnet på den händelse källa för tids serier som är associerad med den angivna miljön.</span><span class="sxs-lookup"><span data-stu-id="5e393-122">The name of the Time Series Insights event source associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e393-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e393-123">-PassThru</span></span>
<span data-ttu-id="5e393-124">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="5e393-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5e393-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e393-125">-ResourceGroupName</span></span>
<span data-ttu-id="5e393-126">Namn på en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="5e393-126">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e393-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5e393-127">-SubscriptionId</span></span>
<span data-ttu-id="5e393-128">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="5e393-128">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e393-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5e393-129">-Confirm</span></span>
<span data-ttu-id="5e393-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5e393-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e393-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e393-131">-WhatIf</span></span>
<span data-ttu-id="5e393-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5e393-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e393-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5e393-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e393-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e393-134">CommonParameters</span></span>
<span data-ttu-id="5e393-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e393-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e393-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e393-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e393-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5e393-137">INPUTS</span></span>

### <span data-ttu-id="5e393-138">Microsoft. Azure. PowerShell. cmdletar. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="5e393-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="5e393-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5e393-139">OUTPUTS</span></span>

### <span data-ttu-id="5e393-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5e393-140">System.Boolean</span></span>

## <span data-ttu-id="5e393-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5e393-141">NOTES</span></span>

<span data-ttu-id="5e393-142">ALIAS</span><span class="sxs-lookup"><span data-stu-id="5e393-142">ALIASES</span></span>

<span data-ttu-id="5e393-143">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="5e393-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5e393-144">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="5e393-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5e393-145">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5e393-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5e393-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="5e393-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5e393-147">`[AccessPolicyName <String>]`: Åtkomst Principens namn.</span><span class="sxs-lookup"><span data-stu-id="5e393-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="5e393-148">`[EnvironmentName <String>]`: Miljö namnet</span><span class="sxs-lookup"><span data-stu-id="5e393-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="5e393-149">`[EventSourceName <String>]`: Namnet på den händelse källa för tids serier som är associerad med den angivna miljön.</span><span class="sxs-lookup"><span data-stu-id="5e393-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="5e393-150">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="5e393-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5e393-151">`[ReferenceDataSetName <String>]`: Referens data uppsättningens namn.</span><span class="sxs-lookup"><span data-stu-id="5e393-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="5e393-152">`[ResourceGroupName <String>]`: Namnet på en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="5e393-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="5e393-153">`[SubscriptionId <String>]`: ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="5e393-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="5e393-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5e393-154">RELATED LINKS</span></span>

