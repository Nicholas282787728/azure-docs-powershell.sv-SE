---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/add-azurermiothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 192a20ee3d49bd79dff833a05ffd3ff98bcc30ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584344"
---
# <span data-ttu-id="5b796-101">Add-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="5b796-101">Add-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="5b796-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5b796-102">SYNOPSIS</span></span>
<span data-ttu-id="5b796-103">Skapar en eventhub-konsument grupp.</span><span class="sxs-lookup"><span data-stu-id="5b796-103">Creates an eventhub consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b796-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5b796-104">SYNTAX</span></span>

```
Add-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b796-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5b796-105">DESCRIPTION</span></span>
<span data-ttu-id="5b796-106">Skapar en konsument grupp i Eventhub som är associerad med angiven IotHub.</span><span class="sxs-lookup"><span data-stu-id="5b796-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="5b796-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5b796-107">EXAMPLES</span></span>

### <span data-ttu-id="5b796-108">Exempel 1: lägga till en konsument grupp i eventhub-telemetri</span><span class="sxs-lookup"><span data-stu-id="5b796-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="5b796-109">Lägger till en ny consumergroup med namnet "myconsumergroup" i eventhub för telemetri-händelser i iothub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="5b796-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

### <span data-ttu-id="5b796-110">Exempel 2: lägga till en konsument grupp i eventhub-kontrollen</span><span class="sxs-lookup"><span data-stu-id="5b796-110">Example 2: Add a consumer group to the operations monitoring eventhub</span></span>
```
PS C:\> Add-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "operationsMonitoringEvents" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="5b796-111">Lägger till en ny consumergroup med namnet "myconsumergroup" i eventhub för händelser för åtgärds övervakning i iothub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="5b796-111">Adds a new consumergroup named "myconsumergroup" to the eventhub for operations monitoring events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="5b796-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5b796-112">PARAMETERS</span></span>

### <span data-ttu-id="5b796-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b796-113">-DefaultProfile</span></span>
<span data-ttu-id="5b796-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="5b796-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5b796-115">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="5b796-115">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="5b796-116">Namn på den EventHub-ConsumerGroup som du vill lägga till.</span><span class="sxs-lookup"><span data-stu-id="5b796-116">Name of the EventHub ConsumerGroup that you want to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b796-117">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="5b796-117">-EventHubEndpointName</span></span>
<span data-ttu-id="5b796-118">Namn på EventHub-slutpunkten.</span><span class="sxs-lookup"><span data-stu-id="5b796-118">Name of the EventHub Endpoint.</span></span>
<span data-ttu-id="5b796-119">Möjliga värden, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="5b796-119">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: events, operationsMonitoringEvents

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b796-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="5b796-120">-Name</span></span>
<span data-ttu-id="5b796-121">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="5b796-121">Name of the Iot Hub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b796-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b796-122">-ResourceGroupName</span></span>
<span data-ttu-id="5b796-123">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5b796-123">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="5b796-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5b796-124">-Confirm</span></span>
<span data-ttu-id="5b796-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5b796-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b796-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b796-126">-WhatIf</span></span>
<span data-ttu-id="5b796-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5b796-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b796-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5b796-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b796-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b796-129">CommonParameters</span></span>
<span data-ttu-id="5b796-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b796-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b796-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b796-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b796-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5b796-132">INPUTS</span></span>

### <span data-ttu-id="5b796-133">System. String</span><span class="sxs-lookup"><span data-stu-id="5b796-133">System.String</span></span>

## <span data-ttu-id="5b796-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5b796-134">OUTPUTS</span></span>

### <span data-ttu-id="5b796-135">System. Collections. Generic. IEnumerable ' 1 [[system. String, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="5b796-135">System.Collections.Generic.IEnumerable\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="5b796-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5b796-136">NOTES</span></span>

## <span data-ttu-id="5b796-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5b796-137">RELATED LINKS</span></span>

