---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHub.md
ms.openlocfilehash: 2c5bf49245da7ecac0f9d4351f5a66a39a663b98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583152"
---
# <span data-ttu-id="a28b2-101">New-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="a28b2-101">New-AzureRmEventHub</span></span>

## <span data-ttu-id="a28b2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a28b2-102">SYNOPSIS</span></span>
<span data-ttu-id="a28b2-103">Skapar en ny händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="a28b2-103">Creates a new Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a28b2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a28b2-104">SYNTAX</span></span>

### <span data-ttu-id="a28b2-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a28b2-105">EventhubInputObjectSet</span></span>
```
New-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a28b2-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="a28b2-106">EventhubPropertiesSet</span></span>
```
New-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-MessageRetentionInDays <Int64>] [-PartitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a28b2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a28b2-107">DESCRIPTION</span></span>
<span data-ttu-id="a28b2-108">New-AzureRmEventHub-cmdleten skapar en ny Azure Event Hub.</span><span class="sxs-lookup"><span data-stu-id="a28b2-108">The New-AzureRmEventHub cmdlet creates a new Azure Event Hub.</span></span>
<span data-ttu-id="a28b2-109">Följ stegen nedan (exempel 2) om du vill skapa Eventhub med beskrivnings egenskaper för insamling.</span><span class="sxs-lookup"><span data-stu-id="a28b2-109">To create Eventhub with Capture description properties, please follow the below steps (Examples 2).</span></span> 

## <span data-ttu-id="a28b2-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a28b2-110">EXAMPLES</span></span>

### <span data-ttu-id="a28b2-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a28b2-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location WestUS -EventHubName MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2
```

<span data-ttu-id="a28b2-112">Skapar en Händelsehubben med namnet \` MyEventHubName \` med en period med 3 dagars meddelande lagring och två partitioner, på \` platsen för västkusten \` , med resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="a28b2-112">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period and two partitions, in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a28b2-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a28b2-113">Example 2</span></span>
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

<span data-ttu-id="a28b2-114">Skapar en Händelsehubben med namnet \` MyEventHubName \` med en period på 3 dagars meddelanden, 2 partitioner och CaptureDescription-egenskaper i \` plats för västkusten \` , med resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="a28b2-114">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period, 2 partitions and CaptureDescription properties in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="a28b2-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a28b2-115">PARAMETERS</span></span>

### <span data-ttu-id="a28b2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a28b2-116">-DefaultProfile</span></span>
<span data-ttu-id="a28b2-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a28b2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a28b2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a28b2-118">-InputObject</span></span>
<span data-ttu-id="a28b2-119">EventHub-Indataområde</span><span class="sxs-lookup"><span data-stu-id="a28b2-119">EventHub Input object</span></span>

```yaml
Type: PSEventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases: EventHubObj

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a28b2-120">-MessageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="a28b2-120">-MessageRetentionInDays</span></span>
<span data-ttu-id="a28b2-121">Antal dagar för Eventhub-meddelanden</span><span class="sxs-lookup"><span data-stu-id="a28b2-121">Eventhub Message Retention In Days</span></span>

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

### <span data-ttu-id="a28b2-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="a28b2-122">-Name</span></span>
<span data-ttu-id="a28b2-123">Namn på Eventhub</span><span class="sxs-lookup"><span data-stu-id="a28b2-123">Eventhub Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a28b2-124">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="a28b2-124">-Namespace</span></span>
<span data-ttu-id="a28b2-125">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="a28b2-125">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a28b2-126">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="a28b2-126">-PartitionCount</span></span>
<span data-ttu-id="a28b2-127">Eventhub-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="a28b2-127">Eventhub PartitionCount</span></span>

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

### <span data-ttu-id="a28b2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a28b2-128">-ResourceGroupName</span></span>
<span data-ttu-id="a28b2-129">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="a28b2-129">Resource Group Name</span></span>

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

### <span data-ttu-id="a28b2-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a28b2-130">-Confirm</span></span>
<span data-ttu-id="a28b2-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a28b2-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a28b2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a28b2-132">-WhatIf</span></span>
<span data-ttu-id="a28b2-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a28b2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a28b2-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a28b2-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a28b2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a28b2-135">CommonParameters</span></span>
<span data-ttu-id="a28b2-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a28b2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a28b2-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a28b2-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a28b2-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a28b2-138">INPUTS</span></span>

### <span data-ttu-id="a28b2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a28b2-139">System.String</span></span>
<span data-ttu-id="a28b2-140">Microsoft. Azure. commands. EventHub. Models. PSEventHubAttributes system. Nullable ' 1 [[system. Int64, mscorlib, version = 4.0.0.0; Culture = neutralt, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a28b2-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes System.Nullable\`1[[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>


## <span data-ttu-id="a28b2-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a28b2-141">OUTPUTS</span></span>

### <span data-ttu-id="a28b2-142">Microsoft. Azure. commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="a28b2-142">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>


## <span data-ttu-id="a28b2-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a28b2-143">NOTES</span></span>

## <span data-ttu-id="a28b2-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a28b2-144">RELATED LINKS</span></span>
