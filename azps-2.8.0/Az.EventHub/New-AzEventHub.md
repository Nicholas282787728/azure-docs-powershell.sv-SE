---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHub.md
ms.openlocfilehash: ac61b1f0bec6ea6b76fcc2b0ea4cf1438359197b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744211"
---
# <span data-ttu-id="5cb09-101">New-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="5cb09-101">New-AzEventHub</span></span>

## <span data-ttu-id="5cb09-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5cb09-102">SYNOPSIS</span></span>
<span data-ttu-id="5cb09-103">Skapar en ny händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="5cb09-103">Creates a new Event Hub.</span></span>

## <span data-ttu-id="5cb09-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5cb09-104">SYNTAX</span></span>

### <span data-ttu-id="5cb09-105">EventhubPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5cb09-105">EventhubPropertiesSet (Default)</span></span>
```
New-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-MessageRetentionInDays <Int64>] [-PartitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cb09-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5cb09-106">EventhubInputObjectSet</span></span>
```
New-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5cb09-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5cb09-107">DESCRIPTION</span></span>
<span data-ttu-id="5cb09-108">New-AzEventHub-cmdleten skapar en ny Azure Event Hub.</span><span class="sxs-lookup"><span data-stu-id="5cb09-108">The New-AzEventHub cmdlet creates a new Azure Event Hub.</span></span>
<span data-ttu-id="5cb09-109">Följ stegen nedan (exempel 2) om du vill skapa Eventhub med beskrivnings egenskaper för insamling.</span><span class="sxs-lookup"><span data-stu-id="5cb09-109">To create Eventhub with Capture description properties, please follow the below steps (Examples 2).</span></span> 

## <span data-ttu-id="5cb09-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5cb09-110">EXAMPLES</span></span>

### <span data-ttu-id="5cb09-111">Exempel 1 – Skapa ny EventHub</span><span class="sxs-lookup"><span data-stu-id="5cb09-111">Example 1  - Create new EventHub</span></span>
```
PS C:\> New-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="5cb09-112">Skapar en Händelsehubben med namnet \` MyEventHubName \` med en period med 3 dagars meddelande lagring och två partitioner, på \` platsen för västkusten \` , med resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="5cb09-112">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period and two partitions, in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="5cb09-113">Exempel 2 uppdatera Eventhub med ' CaptureDescription '</span><span class="sxs-lookup"><span data-stu-id="5cb09-113">Example 2 Update Eventhub with 'CaptureDescription'</span></span>
```
PS C:\> New-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2

PS C:\> $CreatedEventHub = Get-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName

PS C:\> $createdEventHub.CaptureDescription = New-Object -TypeName Microsoft.Azure.Commands.EventHub.Models.CaptureDescriptionAttributes

PS C:\> $createdEventHub.CaptureDescription.Enabled = $true
PS C:\> $createdEventHub.CaptureDescription.IntervalInSeconds  = 120
PS C:\> $createdEventHub.CaptureDescription.Encoding  = "Avro"
PS C:\> $createdEventHub.CaptureDescription.SizeLimitInBytes = 10485763
PS C:\> $createdEventHub.CaptureDescription.Destination.Name = "EventHubArchive.AzureBlockBlob"
PS C:\> $createdEventHub.CaptureDescription.Destination.BlobContainer = "container"
PS C:\> $createdEventHub.CaptureDescription.Destination.ArchiveNameFormat = "{Namespace}/{EventHub}/{PartitionId}/{Year}/{Month}/{Day}/{Hour}/{Minute}/{Second}"
PS C:\> $createdEventHub.CaptureDescription.Destination.StorageAccountResourceId = "/subscriptions/{SubscriptionId}/resourceGroups/MyResourceGroupName/providers/Microsoft.ClassicStorage/storageAccounts/arjunteststorage"
PS C:\> Set-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="5cb09-114">Skapar en Händelsehubben med namnet \` MyEventHubName \` med en period på 3 dagars meddelanden, 2 partitioner och CaptureDescription-egenskaper i \` plats för västkusten \` , med resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="5cb09-114">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period, 2 partitions and CaptureDescription properties in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="5cb09-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5cb09-115">PARAMETERS</span></span>

### <span data-ttu-id="5cb09-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cb09-116">-DefaultProfile</span></span>
<span data-ttu-id="5cb09-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5cb09-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cb09-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5cb09-118">-InputObject</span></span>
<span data-ttu-id="5cb09-119">EventHub-Indataområde</span><span class="sxs-lookup"><span data-stu-id="5cb09-119">EventHub Input object</span></span>

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

### <span data-ttu-id="5cb09-120">-MessageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="5cb09-120">-MessageRetentionInDays</span></span>
<span data-ttu-id="5cb09-121">Antal dagar för Eventhub-meddelanden</span><span class="sxs-lookup"><span data-stu-id="5cb09-121">Eventhub Message Retention In Days</span></span>

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

### <span data-ttu-id="5cb09-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="5cb09-122">-Name</span></span>
<span data-ttu-id="5cb09-123">Namn på Eventhub</span><span class="sxs-lookup"><span data-stu-id="5cb09-123">Eventhub Name</span></span>

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

### <span data-ttu-id="5cb09-124">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="5cb09-124">-Namespace</span></span>
<span data-ttu-id="5cb09-125">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="5cb09-125">Namespace Name</span></span>

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

### <span data-ttu-id="5cb09-126">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="5cb09-126">-PartitionCount</span></span>
<span data-ttu-id="5cb09-127">Eventhub-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="5cb09-127">Eventhub PartitionCount</span></span>

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

### <span data-ttu-id="5cb09-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cb09-128">-ResourceGroupName</span></span>
<span data-ttu-id="5cb09-129">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="5cb09-129">Resource Group Name</span></span>

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

### <span data-ttu-id="5cb09-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5cb09-130">-Confirm</span></span>
<span data-ttu-id="5cb09-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5cb09-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cb09-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cb09-132">-WhatIf</span></span>
<span data-ttu-id="5cb09-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5cb09-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cb09-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5cb09-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cb09-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cb09-135">CommonParameters</span></span>
<span data-ttu-id="5cb09-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cb09-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cb09-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cb09-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cb09-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5cb09-138">INPUTS</span></span>

### <span data-ttu-id="5cb09-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5cb09-139">System.String</span></span>

### <span data-ttu-id="5cb09-140">Microsoft. Azure. commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="5cb09-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

### <span data-ttu-id="5cb09-141">System. Nullable ' 1 [[system. Int64, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5cb09-141">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="5cb09-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5cb09-142">OUTPUTS</span></span>

### <span data-ttu-id="5cb09-143">Microsoft. Azure. commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="5cb09-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="5cb09-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5cb09-144">NOTES</span></span>

## <span data-ttu-id="5cb09-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5cb09-145">RELATED LINKS</span></span>
