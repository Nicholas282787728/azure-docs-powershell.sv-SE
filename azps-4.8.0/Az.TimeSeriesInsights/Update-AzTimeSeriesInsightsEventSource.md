---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: e87487e55ce285aa5c430dabaa274ee70c34ba00
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258443"
---
# <span data-ttu-id="bdf0d-101">Update-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="bdf0d-101">Update-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="bdf0d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bdf0d-102">SYNOPSIS</span></span>
<span data-ttu-id="bdf0d-103">Uppdaterar händelse källan med angivet namn i angiven prenumeration, resurs grupp och miljö.</span><span class="sxs-lookup"><span data-stu-id="bdf0d-103">Updates the event source with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="bdf0d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bdf0d-104">SYNTAX</span></span>

### <span data-ttu-id="bdf0d-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="bdf0d-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="bdf0d-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="bdf0d-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bdf0d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bdf0d-107">DESCRIPTION</span></span>
<span data-ttu-id="bdf0d-108">Uppdaterar händelse källan med angivet namn i angiven prenumeration, resurs grupp och miljö.</span><span class="sxs-lookup"><span data-stu-id="bdf0d-108">Updates the event source with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="bdf0d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bdf0d-109">EXAMPLES</span></span>

### <span data-ttu-id="bdf0d-110">Exempel 1: uppdatera en angiven händelse källa utifrån namn</span><span class="sxs-lookup"><span data-stu-id="bdf0d-110">Example 1: Update a specified event source by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -Name iots001 -ResourceGroupName testgroup -Tag @{"tgk"="001"}

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eventsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="bdf0d-111">Det här kommandot uppdaterar en specifik händelse källa.</span><span class="sxs-lookup"><span data-stu-id="bdf0d-111">This command updates a specific event source.</span></span>

### <span data-ttu-id="bdf0d-112">Exempel 3: uppdatera en angiven händelse källa efter objekt</span><span class="sxs-lookup"><span data-stu-id="bdf0d-112">Example 3: Update a specified event source by object</span></span>
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name iots001
PS C:\> Update-AzTimeSeriesInsightsEventSource -InputObject $es -Tag @{"tgb"="002"}

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eventsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="bdf0d-113">Det här kommandot uppdaterar en specifik händelse källa.</span><span class="sxs-lookup"><span data-stu-id="bdf0d-113">This command updates a specific event source.</span></span>

## <span data-ttu-id="bdf0d-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bdf0d-114">PARAMETERS</span></span>

### <span data-ttu-id="bdf0d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdf0d-115">-DefaultProfile</span></span>
<span data-ttu-id="bdf0d-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bdf0d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdf0d-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="bdf0d-117">-EnvironmentName</span></span>
<span data-ttu-id="bdf0d-118">Namnet på den miljö för tids serie som är kopplad till den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="bdf0d-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdf0d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bdf0d-119">-InputObject</span></span>
<span data-ttu-id="bdf0d-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="bdf0d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdf0d-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="bdf0d-121">-Name</span></span>
<span data-ttu-id="bdf0d-122">Namnet på den händelse källa för tids serier som är associerad med den angivna miljön.</span><span class="sxs-lookup"><span data-stu-id="bdf0d-122">The name of the Time Series Insights event source associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdf0d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdf0d-123">-ResourceGroupName</span></span>
<span data-ttu-id="bdf0d-124">Namn på en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="bdf0d-124">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdf0d-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bdf0d-125">-SubscriptionId</span></span>
<span data-ttu-id="bdf0d-126">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="bdf0d-126">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdf0d-127">-Tagg</span><span class="sxs-lookup"><span data-stu-id="bdf0d-127">-Tag</span></span>
<span data-ttu-id="bdf0d-128">Nyckeltal för ytterligare egenskaper för händelse källan.</span><span class="sxs-lookup"><span data-stu-id="bdf0d-128">Key-value pairs of additional properties for the event source.</span></span>

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

### <span data-ttu-id="bdf0d-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bdf0d-129">-Confirm</span></span>
<span data-ttu-id="bdf0d-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bdf0d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdf0d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdf0d-131">-WhatIf</span></span>
<span data-ttu-id="bdf0d-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bdf0d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdf0d-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bdf0d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdf0d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdf0d-134">CommonParameters</span></span>
<span data-ttu-id="bdf0d-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdf0d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdf0d-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bdf0d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdf0d-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bdf0d-137">INPUTS</span></span>

### <span data-ttu-id="bdf0d-138">Microsoft. Azure. PowerShell. cmdletar. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="bdf0d-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="bdf0d-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bdf0d-139">OUTPUTS</span></span>

### <span data-ttu-id="bdf0d-140">Microsoft. Azure. PowerShell. cmdletar. TimeSeriesInsights. Models. Api20200515. IEventSourceResource</span><span class="sxs-lookup"><span data-stu-id="bdf0d-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="bdf0d-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bdf0d-141">NOTES</span></span>

<span data-ttu-id="bdf0d-142">ALIAS</span><span class="sxs-lookup"><span data-stu-id="bdf0d-142">ALIASES</span></span>

<span data-ttu-id="bdf0d-143">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="bdf0d-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bdf0d-144">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="bdf0d-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bdf0d-145">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bdf0d-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bdf0d-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="bdf0d-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bdf0d-147">`[AccessPolicyName <String>]`: Åtkomst Principens namn.</span><span class="sxs-lookup"><span data-stu-id="bdf0d-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="bdf0d-148">`[EnvironmentName <String>]`: Miljö namnet</span><span class="sxs-lookup"><span data-stu-id="bdf0d-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="bdf0d-149">`[EventSourceName <String>]`: Namnet på den händelse källa för tids serier som är associerad med den angivna miljön.</span><span class="sxs-lookup"><span data-stu-id="bdf0d-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="bdf0d-150">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="bdf0d-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bdf0d-151">`[ReferenceDataSetName <String>]`: Referens data uppsättningens namn.</span><span class="sxs-lookup"><span data-stu-id="bdf0d-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="bdf0d-152">`[ResourceGroupName <String>]`: Namnet på en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="bdf0d-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="bdf0d-153">`[SubscriptionId <String>]`: ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="bdf0d-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="bdf0d-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bdf0d-154">RELATED LINKS</span></span>

