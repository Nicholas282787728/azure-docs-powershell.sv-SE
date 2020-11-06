---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 2ff36708ba9b8303c8b8763146c81ee4e4d8b209
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580623"
---
# <span data-ttu-id="ae962-101">Set-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="ae962-101">Set-AzureRmEventHub</span></span>

## <span data-ttu-id="ae962-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ae962-102">SYNOPSIS</span></span>
<span data-ttu-id="ae962-103">Uppdaterar den angivna händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="ae962-103">Updates the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae962-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ae962-104">SYNTAX</span></span>

### <span data-ttu-id="ae962-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ae962-105">EventhubInputObjectSet</span></span>
```
Set-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-InputObject <EventHubAttributes>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="ae962-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="ae962-106">EventhubPropertiesSet</span></span>
```
Set-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-messageRetentionInDays <Int64>] [-partitionCount <Int64>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="ae962-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ae962-107">DESCRIPTION</span></span>
<span data-ttu-id="ae962-108">Den Set-AzureRmEventHub cmdleten uppdaterar egenskaperna för den angivna Händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="ae962-108">The Set-AzureRmEventHub cmdlet updates the properties of the specified Event Hub.</span></span>

## <span data-ttu-id="ae962-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ae962-109">EXAMPLES</span></span>

### <span data-ttu-id="ae962-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ae962-110">Example 1</span></span>
<span data-ttu-id="ae962-111">Följ stegen nedan om du vill uppdatera Eventhub med beskrivnings egenskaper för insamling.</span><span class="sxs-lookup"><span data-stu-id="ae962-111">To update Eventhub with Capture description properties, please follow the below steps.</span></span> 

```
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

<span data-ttu-id="ae962-112">Uppdaterar den MyEventHubName som \` \` representeras av \` MyCreatedEventHub \` -objektet, ställer in tids perioden för meddelanden till 4 dagar, antalet partitioner till 2 och CaptureDescription egenskaper</span><span class="sxs-lookup"><span data-stu-id="ae962-112">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, the number of partitions to 2 and CaptureDescription properties</span></span>

### <span data-ttu-id="ae962-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ae962-113">Example 2</span></span>

```
PS C:\> Set-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="ae962-114">Uppdaterar \` MyEventHubName som \` representeras av \` MyCreatedEventHub \` -objektet, ställer in tids perioden till 4 dagar och antalet partitioner till 2.</span><span class="sxs-lookup"><span data-stu-id="ae962-114">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, and the number of partitions to 2.</span></span>

## <span data-ttu-id="ae962-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ae962-115">PARAMETERS</span></span>

### <span data-ttu-id="ae962-116">-messageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="ae962-116">-messageRetentionInDays</span></span>
<span data-ttu-id="ae962-117">Logg period för meddelanden om händelsehubben under dagar.</span><span class="sxs-lookup"><span data-stu-id="ae962-117">Event Hub message retention period, in days.</span></span>

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

### <span data-ttu-id="ae962-118">-partitionCount</span><span class="sxs-lookup"><span data-stu-id="ae962-118">-partitionCount</span></span>
<span data-ttu-id="ae962-119">Antal partitioner i den här händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="ae962-119">Number of partitions on this Event Hub.</span></span>

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

### <span data-ttu-id="ae962-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae962-120">-ResourceGroupName</span></span>
<span data-ttu-id="ae962-121">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="ae962-121">Resource group name.</span></span>

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

### <span data-ttu-id="ae962-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ae962-122">-Confirm</span></span>
<span data-ttu-id="ae962-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ae962-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae962-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae962-124">-WhatIf</span></span>
<span data-ttu-id="ae962-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ae962-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae962-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ae962-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae962-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae962-127">-InputObject</span></span>
<span data-ttu-id="ae962-128">EventHub-objekt.</span><span class="sxs-lookup"><span data-stu-id="ae962-128">EventHub object.</span></span>

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

### <span data-ttu-id="ae962-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="ae962-129">-Name</span></span>
<span data-ttu-id="ae962-130">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="ae962-130">Namespace Name.</span></span>

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

### <span data-ttu-id="ae962-131">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="ae962-131">-Namespace</span></span>
<span data-ttu-id="ae962-132">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="ae962-132">Namespace Name.</span></span>

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

## <span data-ttu-id="ae962-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ae962-133">INPUTS</span></span>

### <span data-ttu-id="ae962-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ae962-134">System.String</span></span>

## <span data-ttu-id="ae962-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ae962-135">OUTPUTS</span></span>

### <span data-ttu-id="ae962-136">Microsoft. Azure. commands. EventHub. Models. EventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="ae962-136">Microsoft.Azure.Commands.EventHub.Models.EventHubAttributes</span></span>

## <span data-ttu-id="ae962-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ae962-137">NOTES</span></span>

## <span data-ttu-id="ae962-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ae962-138">RELATED LINKS</span></span>

