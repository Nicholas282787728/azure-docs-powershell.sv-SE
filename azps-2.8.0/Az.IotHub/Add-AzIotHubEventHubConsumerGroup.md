---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 938949ae1eada6d85bb6e01728f5be09655c3e06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744027"
---
# <span data-ttu-id="42dc4-101">Add-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="42dc4-101">Add-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="42dc4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="42dc4-102">SYNOPSIS</span></span>
<span data-ttu-id="42dc4-103">Skapar en eventhub-konsument grupp.</span><span class="sxs-lookup"><span data-stu-id="42dc4-103">Creates an eventhub consumer group.</span></span>

## <span data-ttu-id="42dc4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="42dc4-104">SYNTAX</span></span>

```
Add-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42dc4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="42dc4-105">DESCRIPTION</span></span>
<span data-ttu-id="42dc4-106">Skapar en konsument grupp i Eventhub som är associerad med angiven IotHub.</span><span class="sxs-lookup"><span data-stu-id="42dc4-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="42dc4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="42dc4-107">EXAMPLES</span></span>

### <span data-ttu-id="42dc4-108">Exempel 1: lägga till en konsument grupp i eventhub-telemetri</span><span class="sxs-lookup"><span data-stu-id="42dc4-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="42dc4-109">Lägger till en ny consumergroup med namnet "myconsumergroup" i eventhub för telemetri-händelser i iothub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="42dc4-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="42dc4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="42dc4-110">PARAMETERS</span></span>

### <span data-ttu-id="42dc4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42dc4-111">-DefaultProfile</span></span>
<span data-ttu-id="42dc4-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="42dc4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42dc4-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="42dc4-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="42dc4-114">Namn på den EventHub-ConsumerGroup som du vill lägga till.</span><span class="sxs-lookup"><span data-stu-id="42dc4-114">Name of the EventHub ConsumerGroup that you want to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42dc4-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="42dc4-115">-EventHubEndpointName</span></span>
<span data-ttu-id="42dc4-116">Namn på EventHub-slutpunkten.</span><span class="sxs-lookup"><span data-stu-id="42dc4-116">Name of the EventHub Endpoint.</span></span>
<span data-ttu-id="42dc4-117">Möjliga värden, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="42dc4-117">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: events, operationsMonitoringEvents

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42dc4-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="42dc4-118">-Name</span></span>
<span data-ttu-id="42dc4-119">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="42dc4-119">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42dc4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42dc4-120">-ResourceGroupName</span></span>
<span data-ttu-id="42dc4-121">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="42dc4-121">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="42dc4-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="42dc4-122">-Confirm</span></span>
<span data-ttu-id="42dc4-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="42dc4-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42dc4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42dc4-124">-WhatIf</span></span>
<span data-ttu-id="42dc4-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="42dc4-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42dc4-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="42dc4-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42dc4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42dc4-127">CommonParameters</span></span>
<span data-ttu-id="42dc4-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42dc4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42dc4-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42dc4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42dc4-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="42dc4-130">INPUTS</span></span>

### <span data-ttu-id="42dc4-131">System. String</span><span class="sxs-lookup"><span data-stu-id="42dc4-131">System.String</span></span>

## <span data-ttu-id="42dc4-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="42dc4-132">OUTPUTS</span></span>

### <span data-ttu-id="42dc4-133">System. String</span><span class="sxs-lookup"><span data-stu-id="42dc4-133">System.String</span></span>

## <span data-ttu-id="42dc4-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="42dc4-134">NOTES</span></span>

## <span data-ttu-id="42dc4-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="42dc4-135">RELATED LINKS</span></span>
