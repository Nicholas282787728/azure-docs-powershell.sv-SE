---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 1c5e14fa71ded51d91792f462d01cb463ff36c61
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413627"
---
# <span data-ttu-id="07ed6-101">New-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="07ed6-101">New-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="07ed6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="07ed6-102">SYNOPSIS</span></span>
<span data-ttu-id="07ed6-103">Skapa en händelse källa under den angivna miljön.</span><span class="sxs-lookup"><span data-stu-id="07ed6-103">Create an event source under the specified environment.</span></span>

## <span data-ttu-id="07ed6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="07ed6-104">SYNTAX</span></span>

### <span data-ttu-id="07ed6-105">eventhub (standard)</span><span class="sxs-lookup"><span data-stu-id="07ed6-105">eventhub (Default)</span></span>
```
New-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -ConsumerGroupName <String> -EventHubName <String> -EventSourceResourceId <String> -KeyName <String>
 -Kind <Kind> -Location <String> -ServiceBusNameSpace <String> -SharedAccessKey <SecureString>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-TimeStampPropertyName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="07ed6-106">iothub</span><span class="sxs-lookup"><span data-stu-id="07ed6-106">iothub</span></span>
```
New-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -ConsumerGroupName <String> -EventSourceResourceId <String> -IoTHubName <String> -KeyName <String>
 -Kind <Kind> -Location <String> -SharedAccessKey <SecureString> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-TimeStampPropertyName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="07ed6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="07ed6-107">DESCRIPTION</span></span>
<span data-ttu-id="07ed6-108">Skapa en händelse källa under den angivna miljön.</span><span class="sxs-lookup"><span data-stu-id="07ed6-108">Create an event source under the specified environment.</span></span>

## <span data-ttu-id="07ed6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="07ed6-109">EXAMPLES</span></span>

### <span data-ttu-id="07ed6-110">Exempel 1: skapa en händelse källa för eventhub under den angivna miljön</span><span class="sxs-lookup"><span data-stu-id="07ed6-110">Example 1: Create an eventhub event source under the specified environment</span></span>
```powershell
PS C:\> New-AzEventHubNamespace -Name spacename002 -ResourceGroupName testgroup -Location eastus
PS C:\> $ev = New-AzEventHub -ResourceGroupName testgroup -NamespaceName spacename002 -Name hubname001 -MessageRetentionInDays 3 -PartitionCount 2
PS C:\> $ks = Get-AzEventHubKey -ResourceGroupName testgroup -NamespaceName spacename002 -AuthorizationRuleName RootManageSharedAccessKey
PS C:\> $k  = $ks.PrimaryKey | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -Name estest001 -EnvironmentName tsitest001 -Kind Microsoft.EventHub -ConsumerGroupName testgroup -Location eastus -KeyName RootManageSharedAccessKey -ServiceBusNameSpace spacename002 -EventHubName hubname001 -EventSourceResourceId $ev.id -SharedAccessKey $k

Kind               Location Name      Type
----               -------- ----      ----
Microsoft.EventHub eastus   estest001 Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="07ed6-111">Det här kommandot skapar en händelse källa för eventhub under den angivna miljön.</span><span class="sxs-lookup"><span data-stu-id="07ed6-111">This command creates an eventhub event source under the specified environment.</span></span>

### <span data-ttu-id="07ed6-112">Exempel 2: skapa en iothub-händelse källa under den angivna miljön</span><span class="sxs-lookup"><span data-stu-id="07ed6-112">Example 2: Create an iothub event source under the specified environment</span></span>
```powershell
PS C:\> $ev = New-AzIotHub -ResourceGroupName testgroup -Location eastus -Name iotname001 -SkuName S1 -Units 100
PS C:\> $ks = Get-AzIotHubKey -ResourceGroupName testgroup -Name iotname001
PS C:\> $k  = $ks[0].PrimaryKey | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -Name iots001 -EnvironmentName tsitest001 -Kind Microsoft.IoTHub -ConsumerGroupName testgroup -Location eastus -KeyName RootManageSharedAccessKey -IoTHubName iotname001 -EventSourceResourceId $ev.id -SharedAccessKey $k

Location Name    Type                                                   Kind
-------- ----    ----                                                   ----
eastus   iots001 Microsoft.TimeSeriesInsights/Environments/EventSources Microsoft.IoTHub
```

<span data-ttu-id="07ed6-113">Det här kommandot skapar en iothub-händelse under den angivna miljön.</span><span class="sxs-lookup"><span data-stu-id="07ed6-113">This command creates an iothub event source under the specified environment.</span></span>

## <span data-ttu-id="07ed6-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="07ed6-114">PARAMETERS</span></span>

### <span data-ttu-id="07ed6-115">-ConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="07ed6-115">-ConsumerGroupName</span></span>
<span data-ttu-id="07ed6-116">Namnet på den konsument grupp för evenemanget/IoT Hub som innehåller de partitioner som händelser kommer att läsas ifrån.</span><span class="sxs-lookup"><span data-stu-id="07ed6-116">The name of the event/iot hub's consumer group that holds the partitions from which events will be read.</span></span>

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

### <span data-ttu-id="07ed6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07ed6-117">-DefaultProfile</span></span>
<span data-ttu-id="07ed6-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="07ed6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07ed6-119">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="07ed6-119">-EnvironmentName</span></span>
<span data-ttu-id="07ed6-120">Namnet på den miljö för tids serie som är kopplad till den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="07ed6-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="07ed6-121">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="07ed6-121">-EventHubName</span></span>
<span data-ttu-id="07ed6-122">Namnet på händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="07ed6-122">The name of the event hub.</span></span>

```yaml
Type: System.String
Parameter Sets: eventhub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07ed6-123">-EventSourceResourceId</span><span class="sxs-lookup"><span data-stu-id="07ed6-123">-EventSourceResourceId</span></span>
<span data-ttu-id="07ed6-124">Resurs-ID för händelse källan i Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="07ed6-124">The resource id of the event source in Azure Resource Manager.</span></span>

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

### <span data-ttu-id="07ed6-125">-IoTHubName</span><span class="sxs-lookup"><span data-stu-id="07ed6-125">-IoTHubName</span></span>
<span data-ttu-id="07ed6-126">Namnet på IoT-navet.</span><span class="sxs-lookup"><span data-stu-id="07ed6-126">The name of the iot hub.</span></span>

```yaml
Type: System.String
Parameter Sets: iothub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07ed6-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="07ed6-127">-KeyName</span></span>
<span data-ttu-id="07ed6-128">Namnet på den SAS-nycklar som beviljar åtkomst till Event/IoT-navet för tids serie.</span><span class="sxs-lookup"><span data-stu-id="07ed6-128">The name of the SAS key that grants the Time Series Insights service access to the event/iot hub.</span></span>

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

### <span data-ttu-id="07ed6-129">-Sort</span><span class="sxs-lookup"><span data-stu-id="07ed6-129">-Kind</span></span>
<span data-ttu-id="07ed6-130">Typen av händelse källa.</span><span class="sxs-lookup"><span data-stu-id="07ed6-130">The kind of the event source.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07ed6-131">-Plats</span><span class="sxs-lookup"><span data-stu-id="07ed6-131">-Location</span></span>
<span data-ttu-id="07ed6-132">Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="07ed6-132">The location of the resource.</span></span>

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

### <span data-ttu-id="07ed6-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="07ed6-133">-Name</span></span>
<span data-ttu-id="07ed6-134">Namn på händelse källan.</span><span class="sxs-lookup"><span data-stu-id="07ed6-134">Name of the event source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07ed6-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07ed6-135">-ResourceGroupName</span></span>
<span data-ttu-id="07ed6-136">Namn på en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="07ed6-136">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="07ed6-137">-ServiceBusNameSpace</span><span class="sxs-lookup"><span data-stu-id="07ed6-137">-ServiceBusNameSpace</span></span>
<span data-ttu-id="07ed6-138">Namnet på den tjänst buss som innehåller händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="07ed6-138">The name of the service bus that contains the event hub.</span></span>

```yaml
Type: System.String
Parameter Sets: eventhub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07ed6-139">-SharedAccessKey</span><span class="sxs-lookup"><span data-stu-id="07ed6-139">-SharedAccessKey</span></span>
<span data-ttu-id="07ed6-140">Värdet på den delade åtkomst-tangenten som beviljar tjänsten Time Series Insights Läs åtkomst till evenemanget/IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="07ed6-140">The value of the shared access key that grants the Time Series Insights service read access to the event/iot hub.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07ed6-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="07ed6-141">-SubscriptionId</span></span>
<span data-ttu-id="07ed6-142">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="07ed6-142">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="07ed6-143">-Tagg</span><span class="sxs-lookup"><span data-stu-id="07ed6-143">-Tag</span></span>
<span data-ttu-id="07ed6-144">Nyckeltal för fler egenskaper för resursen.</span><span class="sxs-lookup"><span data-stu-id="07ed6-144">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="07ed6-145">-TimeStampPropertyName</span><span class="sxs-lookup"><span data-stu-id="07ed6-145">-TimeStampPropertyName</span></span>
<span data-ttu-id="07ed6-146">Händelse egenskapen som kommer att användas som händelse källans tidsstämpel.</span><span class="sxs-lookup"><span data-stu-id="07ed6-146">The event property that will be used as the event source's timestamp.</span></span>

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

### <span data-ttu-id="07ed6-147">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="07ed6-147">-Confirm</span></span>
<span data-ttu-id="07ed6-148">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="07ed6-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07ed6-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07ed6-149">-WhatIf</span></span>
<span data-ttu-id="07ed6-150">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="07ed6-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07ed6-151">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="07ed6-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07ed6-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07ed6-152">CommonParameters</span></span>
<span data-ttu-id="07ed6-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07ed6-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07ed6-154">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07ed6-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07ed6-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="07ed6-155">INPUTS</span></span>

## <span data-ttu-id="07ed6-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="07ed6-156">OUTPUTS</span></span>

### <span data-ttu-id="07ed6-157">Microsoft. Azure. PowerShell. cmdletar. TimeSeriesInsights. Models. Api20200515. IEventSourceResource</span><span class="sxs-lookup"><span data-stu-id="07ed6-157">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="07ed6-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="07ed6-158">NOTES</span></span>

<span data-ttu-id="07ed6-159">ALIAS</span><span class="sxs-lookup"><span data-stu-id="07ed6-159">ALIASES</span></span>

## <span data-ttu-id="07ed6-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="07ed6-160">RELATED LINKS</span></span>

