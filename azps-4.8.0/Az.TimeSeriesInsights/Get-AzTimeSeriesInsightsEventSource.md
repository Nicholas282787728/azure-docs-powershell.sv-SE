---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 5590a89b22c0adc3dfb2df88e6b977dec268a822
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262397"
---
# <span data-ttu-id="e26fe-101">Get-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="e26fe-101">Get-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="e26fe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e26fe-102">SYNOPSIS</span></span>
<span data-ttu-id="e26fe-103">Hämtar händelse källan med det angivna namnet i den angivna miljön.</span><span class="sxs-lookup"><span data-stu-id="e26fe-103">Gets the event source with the specified name in the specified environment.</span></span>

## <span data-ttu-id="e26fe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e26fe-104">SYNTAX</span></span>

### <span data-ttu-id="e26fe-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="e26fe-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e26fe-106">Lära</span><span class="sxs-lookup"><span data-stu-id="e26fe-106">Get</span></span>
```
Get-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e26fe-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e26fe-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e26fe-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e26fe-108">DESCRIPTION</span></span>
<span data-ttu-id="e26fe-109">Hämtar händelse källan med det angivna namnet i den angivna miljön.</span><span class="sxs-lookup"><span data-stu-id="e26fe-109">Gets the event source with the specified name in the specified environment.</span></span>

## <span data-ttu-id="e26fe-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e26fe-110">EXAMPLES</span></span>

### <span data-ttu-id="e26fe-111">Exempel 1: lista alla händelse källor under den angivna miljön</span><span class="sxs-lookup"><span data-stu-id="e26fe-111">Example 1: List all event sources under the specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -EnvironmentName tsitest001

ConsumerGroupName     : testgroup2
EventHubName          : hubname001
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.EventHub/namespaces/spacename001/eventhubs/hu 
                        bname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eve 
                        ntsources/estest001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.EventHub
Location              : eastus
Name                  : estest001
ServiceBusNamespace   : spacename001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eve 
                        ntsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="e26fe-112">Det här kommandot visar alla händelse källor under de angivna miljöerna.</span><span class="sxs-lookup"><span data-stu-id="e26fe-112">This command lists all event sources under the specified environments.</span></span>

### <span data-ttu-id="e26fe-113">Exempel 2: Hämta en angiven händelse källa utifrån namn</span><span class="sxs-lookup"><span data-stu-id="e26fe-113">Example 2: Get a specified event source by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -EnvironmentName tsitest001 -Name iots001

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eve
                        ntsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="e26fe-114">Det här kommandot får en specifik händelse källa.</span><span class="sxs-lookup"><span data-stu-id="e26fe-114">This command gets a specific event source.</span></span>

### <span data-ttu-id="e26fe-115">Exempel 3: Hämta en angiven händelse källa för objekt</span><span class="sxs-lookup"><span data-stu-id="e26fe-115">Example 3: Get a specified event source by object</span></span>
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -ResourceGroupName tsi-test-i01k5l -EnvironmentName tsi-envv8u56x -Name tsi-esrfyi9h
PS C:\> Get-AzTimeSeriesInsightsEventSource -InputObject $es

ConsumerGroupName     : tsi-test-i01k5l
EventHubName          : eventhubname-d2rvmp
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/tsi-test-i01k5l/providers/Microsoft.EventHub/namespaces/eventhubspace-0t3khp/eventhubs/eventhubname-d2rvmp
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/tsi-test-i01k5l/providers/Microsoft.TimeSeriesInsights/environments/tsi-envv8u56x/eventsources/tsi-esrfyi9h
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.EventHub
Location              : eastus2
Name                  : tsi-esrfyi9h
ServiceBusNamespace   : eventhubspace-0t3khp
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="e26fe-116">Det här kommandot får en specifik händelse källa.</span><span class="sxs-lookup"><span data-stu-id="e26fe-116">This command gets a specific event source.</span></span>

## <span data-ttu-id="e26fe-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e26fe-117">PARAMETERS</span></span>

### <span data-ttu-id="e26fe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e26fe-118">-DefaultProfile</span></span>
<span data-ttu-id="e26fe-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e26fe-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e26fe-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="e26fe-120">-EnvironmentName</span></span>
<span data-ttu-id="e26fe-121">Namnet på den miljö för tids serie som är kopplad till den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e26fe-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e26fe-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e26fe-122">-InputObject</span></span>
<span data-ttu-id="e26fe-123">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="e26fe-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e26fe-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="e26fe-124">-Name</span></span>
<span data-ttu-id="e26fe-125">Namnet på den händelse källa för tids serier som är associerad med den angivna miljön.</span><span class="sxs-lookup"><span data-stu-id="e26fe-125">The name of the Time Series Insights event source associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e26fe-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e26fe-126">-ResourceGroupName</span></span>
<span data-ttu-id="e26fe-127">Namn på en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="e26fe-127">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e26fe-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e26fe-128">-SubscriptionId</span></span>
<span data-ttu-id="e26fe-129">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="e26fe-129">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e26fe-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e26fe-130">CommonParameters</span></span>
<span data-ttu-id="e26fe-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e26fe-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e26fe-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e26fe-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e26fe-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e26fe-133">INPUTS</span></span>

### <span data-ttu-id="e26fe-134">Microsoft. Azure. PowerShell. cmdletar. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="e26fe-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="e26fe-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e26fe-135">OUTPUTS</span></span>

### <span data-ttu-id="e26fe-136">Microsoft. Azure. PowerShell. cmdletar. TimeSeriesInsights. Models. Api20200515. IEventSourceResource</span><span class="sxs-lookup"><span data-stu-id="e26fe-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="e26fe-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e26fe-137">NOTES</span></span>

<span data-ttu-id="e26fe-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e26fe-138">ALIASES</span></span>

<span data-ttu-id="e26fe-139">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="e26fe-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e26fe-140">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="e26fe-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e26fe-141">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e26fe-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e26fe-142">INPUTOBJECT <ITimeSeriesInsightsIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="e26fe-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e26fe-143">`[AccessPolicyName <String>]`: Åtkomst Principens namn.</span><span class="sxs-lookup"><span data-stu-id="e26fe-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="e26fe-144">`[EnvironmentName <String>]`: Miljö namnet</span><span class="sxs-lookup"><span data-stu-id="e26fe-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="e26fe-145">`[EventSourceName <String>]`: Namnet på den händelse källa för tids serier som är associerad med den angivna miljön.</span><span class="sxs-lookup"><span data-stu-id="e26fe-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="e26fe-146">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="e26fe-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e26fe-147">`[ReferenceDataSetName <String>]`: Referens data uppsättningens namn.</span><span class="sxs-lookup"><span data-stu-id="e26fe-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="e26fe-148">`[ResourceGroupName <String>]`: Namnet på en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="e26fe-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="e26fe-149">`[SubscriptionId <String>]`: ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="e26fe-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="e26fe-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e26fe-150">RELATED LINKS</span></span>

