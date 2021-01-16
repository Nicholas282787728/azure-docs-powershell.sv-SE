---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHub.md
ms.openlocfilehash: a5a1f0bbe0f353014047e795c467a645e244f125
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98390705"
---
# <span data-ttu-id="4ce32-101">Set-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="4ce32-101">Set-AzEventHub</span></span>

## <span data-ttu-id="4ce32-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4ce32-102">SYNOPSIS</span></span>
<span data-ttu-id="4ce32-103">Uppdaterar den angivna händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="4ce32-103">Updates the specified Event Hub.</span></span>

## <span data-ttu-id="4ce32-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4ce32-104">SYNTAX</span></span>

### <span data-ttu-id="4ce32-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4ce32-105">EventhubInputObjectSet</span></span>
```
Set-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ce32-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="4ce32-106">EventhubPropertiesSet</span></span>
```
Set-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-messageRetentionInDays <Int64>] [-partitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ce32-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4ce32-107">DESCRIPTION</span></span>
<span data-ttu-id="4ce32-108">Den Set-AzEventHub cmdleten uppdaterar egenskaperna för den angivna Händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="4ce32-108">The Set-AzEventHub cmdlet updates the properties of the specified Event Hub.</span></span>

## <span data-ttu-id="4ce32-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4ce32-109">EXAMPLES</span></span>

### <span data-ttu-id="4ce32-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4ce32-110">Example 1</span></span>
<span data-ttu-id="4ce32-111">Följ stegen nedan om du vill uppdatera Eventhub med beskrivnings egenskaper för insamling.</span><span class="sxs-lookup"><span data-stu-id="4ce32-111">To update Eventhub with Capture description properties, please follow the below steps.</span></span> 

```
PS C:\> $CreatedEventHub = Get-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
PS C:\> $createdEventHub.CaptureDescription = New-Object -TypeName Microsoft.Azure.Commands.EventHub.Models.PSCaptureDescriptionAttributes
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

<span data-ttu-id="4ce32-112">Uppdaterar den MyEventHubName som \` \` representeras av \` MyCreatedEventHub \` -objektet, ställer in tids perioden för meddelanden till 4 dagar, antalet partitioner till 2 och CaptureDescription egenskaper</span><span class="sxs-lookup"><span data-stu-id="4ce32-112">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, the number of partitions to 2 and CaptureDescription properties</span></span>

### <span data-ttu-id="4ce32-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="4ce32-113">Example 2</span></span>
```
PS C:\> Set-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="4ce32-114">Uppdaterar \` MyEventHubName som \` representeras av \` MyCreatedEventHub \` -objektet, ställer in tids perioden till 4 dagar och antalet partitioner till 2.</span><span class="sxs-lookup"><span data-stu-id="4ce32-114">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, and the number of partitions to 2.</span></span>

## <span data-ttu-id="4ce32-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4ce32-115">PARAMETERS</span></span>

### <span data-ttu-id="4ce32-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ce32-116">-DefaultProfile</span></span>
<span data-ttu-id="4ce32-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4ce32-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ce32-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ce32-118">-InputObject</span></span>
<span data-ttu-id="4ce32-119">EventHub-objekt</span><span class="sxs-lookup"><span data-stu-id="4ce32-119">EventHub object</span></span>

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

### <span data-ttu-id="4ce32-120">-messageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="4ce32-120">-messageRetentionInDays</span></span>
<span data-ttu-id="4ce32-121">Antal dagar för Eventhub-meddelanden</span><span class="sxs-lookup"><span data-stu-id="4ce32-121">Eventhub Message Retention In Days</span></span>

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

### <span data-ttu-id="4ce32-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="4ce32-122">-Name</span></span>
<span data-ttu-id="4ce32-123">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="4ce32-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ce32-124">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="4ce32-124">-Namespace</span></span>
<span data-ttu-id="4ce32-125">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="4ce32-125">Namespace Name</span></span>

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

### <span data-ttu-id="4ce32-126">-partitionCount</span><span class="sxs-lookup"><span data-stu-id="4ce32-126">-partitionCount</span></span>
<span data-ttu-id="4ce32-127">Eventhub-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="4ce32-127">Eventhub PartitionCount</span></span>

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

### <span data-ttu-id="4ce32-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ce32-128">-ResourceGroupName</span></span>
<span data-ttu-id="4ce32-129">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="4ce32-129">Resource Group Name</span></span>

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

### <span data-ttu-id="4ce32-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4ce32-130">-Confirm</span></span>
<span data-ttu-id="4ce32-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4ce32-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ce32-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ce32-132">-WhatIf</span></span>
<span data-ttu-id="4ce32-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4ce32-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ce32-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4ce32-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ce32-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ce32-135">CommonParameters</span></span>
<span data-ttu-id="4ce32-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ce32-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ce32-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ce32-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ce32-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4ce32-138">INPUTS</span></span>

### <span data-ttu-id="4ce32-139">System. String</span><span class="sxs-lookup"><span data-stu-id="4ce32-139">System.String</span></span>

### <span data-ttu-id="4ce32-140">Microsoft. Azure. commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="4ce32-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

### <span data-ttu-id="4ce32-141">System. Nullable ' 1 [[system. Int64, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4ce32-141">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="4ce32-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4ce32-142">OUTPUTS</span></span>

### <span data-ttu-id="4ce32-143">Microsoft. Azure. commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="4ce32-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="4ce32-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4ce32-144">NOTES</span></span>

## <span data-ttu-id="4ce32-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4ce32-145">RELATED LINKS</span></span>
