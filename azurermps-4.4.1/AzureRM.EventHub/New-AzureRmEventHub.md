---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 656e010a05ce1272355f689be8513ecadd330e7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585599"
---
# <span data-ttu-id="fa9f4-101">New-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="fa9f4-101">New-AzureRmEventHub</span></span>

## <span data-ttu-id="fa9f4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fa9f4-102">SYNOPSIS</span></span>
<span data-ttu-id="fa9f4-103">Skapar en ny händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="fa9f4-103">Creates a new Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa9f4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fa9f4-104">SYNTAX</span></span>

### <span data-ttu-id="fa9f4-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fa9f4-105">EventhubInputObjectSet</span></span>
```
New-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> [[-Location] <String>] -Name <String>
 [-InputObject <EventHubAttributes>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="fa9f4-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="fa9f4-106">EventhubPropertiesSet</span></span>
```
New-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> [[-Location] <String>] -Name <String>
 [-MessageRetentionInDays <Int64>] [-PartitionCount <Int64>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="fa9f4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fa9f4-107">DESCRIPTION</span></span>
<span data-ttu-id="fa9f4-108">New-AzureRmEventHub-cmdleten skapar en ny Azure Event Hub.</span><span class="sxs-lookup"><span data-stu-id="fa9f4-108">The New-AzureRmEventHub cmdlet creates a new Azure Event Hub.</span></span>
<span data-ttu-id="fa9f4-109">Följ stegen nedan (exempel 2) om du vill skapa Eventhub med beskrivnings egenskaper för insamling.</span><span class="sxs-lookup"><span data-stu-id="fa9f4-109">To create Eventhub with Capture description properties, please follow the below steps (Examples 2).</span></span> 


## <span data-ttu-id="fa9f4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fa9f4-110">EXAMPLES</span></span>

### <span data-ttu-id="fa9f4-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fa9f4-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location WestUS -EventHubName MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2
```

<span data-ttu-id="fa9f4-112">Skapar en Händelsehubben med namnet \` MyEventHubName \` med en period med 3 dagars meddelande lagring och två partitioner, på \` platsen för västkusten \` , med resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="fa9f4-112">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period and two partitions, in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="fa9f4-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="fa9f4-113">Example 2</span></span>
```
PS C:\> New-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location WestUS -EventHubName MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2

PS C:\> $CreatedEventHub = Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName

PS C:\> $createdEventHub.CaptureDescription = New-Object -TypeName Microsoft.Azure.Commands.EventHub.Models.CaptureDescriptionAttributes

PS C:\> $createdEventHub.CaptureDescription.Enabled = $true
PS C:\> $createdEventHub.CaptureDescription.IntervalInSeconds  = 120
PS C:\> $createdEventHub.CaptureDescription.Encoding  = "Avro"
PS C:\> $createdEventHub.CaptureDescription.SizeLimitInBytes = 10485763
PS C:\> $createdEventHub.CaptureDescription.Destination.Name = "EventHubArchive.AzureBlockBlob"
PS C:\> $createdEventHub.CaptureDescription.Destination.BlobContainer = "container"
PS C:\> $createdEventHub.CaptureDescription.Destination.ArchiveNameFormat = "{Namespace}/{EventHub}/{PartitionId}/{Year}/{Month}/{Day}/{Hour}/{Minute}/{Second}"
PS C:\> $createdEventHub.CaptureDescription.Destination.StorageAccountResourceId = "/subscriptions/{SubscriptionId}/resourceGroups/MyResourceGroupName/providers/Microsoft.ClassicStorage/storageAccounts/arjunteststorage"
PS C:\> Set-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="fa9f4-114">Skapar en Händelsehubben med namnet \` MyEventHubName \` med en period på 3 dagars meddelanden, 2 partitioner och CaptureDescription-egenskaper i \` plats för västkusten \` , med resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="fa9f4-114">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period, 2 partitions and CaptureDescription properties in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="fa9f4-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fa9f4-115">PARAMETERS</span></span>

### <span data-ttu-id="fa9f4-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="fa9f4-116">-Location</span></span>
<span data-ttu-id="fa9f4-117">Geografisk plats i namn området.</span><span class="sxs-lookup"><span data-stu-id="fa9f4-117">Namespace geographic location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa9f4-118">-MessageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="fa9f4-118">-MessageRetentionInDays</span></span>
<span data-ttu-id="fa9f4-119">Meddelande lagrings tid för händelse nav i dagar.</span><span class="sxs-lookup"><span data-stu-id="fa9f4-119">Event Hubs message retention time in days.</span></span>

```yaml
Type: Int64
Parameter Sets: EventhubPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa9f4-120">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="fa9f4-120">-PartitionCount</span></span>
<span data-ttu-id="fa9f4-121">Antalet partitioner i händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="fa9f4-121">Number of partitions in the Event Hub.</span></span>

```yaml
Type: Int64
Parameter Sets: EventhubPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa9f4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa9f4-122">-ResourceGroupName</span></span>
<span data-ttu-id="fa9f4-123">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="fa9f4-123">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa9f4-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fa9f4-124">-Confirm</span></span>
<span data-ttu-id="fa9f4-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fa9f4-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa9f4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa9f4-126">-WhatIf</span></span>
<span data-ttu-id="fa9f4-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fa9f4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa9f4-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fa9f4-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa9f4-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa9f4-129">-InputObject</span></span>
<span data-ttu-id="fa9f4-130">EventHub-Indataområde.</span><span class="sxs-lookup"><span data-stu-id="fa9f4-130">EventHub Input object.</span></span>

```yaml
Type: EventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases: EventHubObj

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa9f4-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="fa9f4-131">-Name</span></span>
<span data-ttu-id="fa9f4-132">Namn på Eventhub.</span><span class="sxs-lookup"><span data-stu-id="fa9f4-132">Eventhub Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa9f4-133">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="fa9f4-133">-Namespace</span></span>
<span data-ttu-id="fa9f4-134">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="fa9f4-134">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="fa9f4-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fa9f4-135">INPUTS</span></span>

### <span data-ttu-id="fa9f4-136">System. String</span><span class="sxs-lookup"><span data-stu-id="fa9f4-136">System.String</span></span>

## <span data-ttu-id="fa9f4-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fa9f4-137">OUTPUTS</span></span>

### <span data-ttu-id="fa9f4-138">Microsoft. Azure. commands. EventHub. Models. EventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="fa9f4-138">Microsoft.Azure.Commands.EventHub.Models.EventHubAttributes</span></span>

## <span data-ttu-id="fa9f4-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fa9f4-139">NOTES</span></span>

## <span data-ttu-id="fa9f4-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fa9f4-140">RELATED LINKS</span></span>

