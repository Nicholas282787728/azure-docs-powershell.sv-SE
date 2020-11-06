---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHub.md
ms.openlocfilehash: 74921cb6ccfc77e2c45d734316cb2a67817c7ede
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573970"
---
# <span data-ttu-id="095c0-101">New-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="095c0-101">New-AzureRmEventHub</span></span>

## <span data-ttu-id="095c0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="095c0-102">SYNOPSIS</span></span>
<span data-ttu-id="095c0-103">Skapar en ny händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="095c0-103">Creates a new Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="095c0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="095c0-104">SYNTAX</span></span>

### <span data-ttu-id="095c0-105">EventhubPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="095c0-105">EventhubPropertiesSet (Default)</span></span>
```
New-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-MessageRetentionInDays <Int64>] [-PartitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="095c0-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="095c0-106">EventhubInputObjectSet</span></span>
```
New-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="095c0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="095c0-107">DESCRIPTION</span></span>
<span data-ttu-id="095c0-108">New-AzureRmEventHub-cmdleten skapar en ny Azure Event Hub.</span><span class="sxs-lookup"><span data-stu-id="095c0-108">The New-AzureRmEventHub cmdlet creates a new Azure Event Hub.</span></span>
<span data-ttu-id="095c0-109">Följ stegen nedan (exempel 2) om du vill skapa Eventhub med beskrivnings egenskaper för insamling.</span><span class="sxs-lookup"><span data-stu-id="095c0-109">To create Eventhub with Capture description properties, please follow the below steps (Examples 2).</span></span> 

## <span data-ttu-id="095c0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="095c0-110">EXAMPLES</span></span>

### <span data-ttu-id="095c0-111">Exempel 1 – Skapa ny EventHub</span><span class="sxs-lookup"><span data-stu-id="095c0-111">Example 1  - Create new EventHub</span></span>
```
PS C:\> New-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="095c0-112">Skapar en Händelsehubben med namnet \` MyEventHubName \` med en period med 3 dagars meddelande lagring och två partitioner, på \` platsen för västkusten \` , med resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="095c0-112">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period and two partitions, in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="095c0-113">Exempel 2 uppdatera Eventhub med ' CaptureDescription '</span><span class="sxs-lookup"><span data-stu-id="095c0-113">Example 2 Update Eventhub with 'CaptureDescription'</span></span>
```
PS C:\> New-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2

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

<span data-ttu-id="095c0-114">Skapar en Händelsehubben med namnet \` MyEventHubName \` med en period på 3 dagars meddelanden, 2 partitioner och CaptureDescription-egenskaper i \` plats för västkusten \` , med resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="095c0-114">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period, 2 partitions and CaptureDescription properties in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="095c0-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="095c0-115">PARAMETERS</span></span>

### <span data-ttu-id="095c0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="095c0-116">-DefaultProfile</span></span>
<span data-ttu-id="095c0-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="095c0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="095c0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="095c0-118">-InputObject</span></span>
<span data-ttu-id="095c0-119">EventHub-Indataområde</span><span class="sxs-lookup"><span data-stu-id="095c0-119">EventHub Input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases: EventHubObj

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="095c0-120">-MessageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="095c0-120">-MessageRetentionInDays</span></span>
<span data-ttu-id="095c0-121">Antal dagar för Eventhub-meddelanden</span><span class="sxs-lookup"><span data-stu-id="095c0-121">Eventhub Message Retention In Days</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: EventhubPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="095c0-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="095c0-122">-Name</span></span>
<span data-ttu-id="095c0-123">Namn på Eventhub</span><span class="sxs-lookup"><span data-stu-id="095c0-123">Eventhub Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="095c0-124">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="095c0-124">-Namespace</span></span>
<span data-ttu-id="095c0-125">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="095c0-125">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="095c0-126">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="095c0-126">-PartitionCount</span></span>
<span data-ttu-id="095c0-127">Eventhub-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="095c0-127">Eventhub PartitionCount</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: EventhubPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="095c0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="095c0-128">-ResourceGroupName</span></span>
<span data-ttu-id="095c0-129">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="095c0-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="095c0-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="095c0-130">-Confirm</span></span>
<span data-ttu-id="095c0-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="095c0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="095c0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="095c0-132">-WhatIf</span></span>
<span data-ttu-id="095c0-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="095c0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="095c0-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="095c0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="095c0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="095c0-135">CommonParameters</span></span>
<span data-ttu-id="095c0-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="095c0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="095c0-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="095c0-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="095c0-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="095c0-138">INPUTS</span></span>

### <span data-ttu-id="095c0-139">System. String</span><span class="sxs-lookup"><span data-stu-id="095c0-139">System.String</span></span>

### <span data-ttu-id="095c0-140">Microsoft. Azure. commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="095c0-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

### <span data-ttu-id="095c0-141">System. Nullable ' 1 [[system. Int64, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="095c0-141">System.Nullable\`1[[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="095c0-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="095c0-142">OUTPUTS</span></span>

### <span data-ttu-id="095c0-143">Microsoft. Azure. commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="095c0-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="095c0-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="095c0-144">NOTES</span></span>

## <span data-ttu-id="095c0-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="095c0-145">RELATED LINKS</span></span>
