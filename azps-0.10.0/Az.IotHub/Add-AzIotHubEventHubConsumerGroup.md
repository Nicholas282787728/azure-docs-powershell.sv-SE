---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 2592284be483793ea246d30e95a4c9065fdd6e3c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924573"
---
# <span data-ttu-id="ec60f-101">Add-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="ec60f-101">Add-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="ec60f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ec60f-102">SYNOPSIS</span></span>
<span data-ttu-id="ec60f-103">Skapar en eventhub-konsument grupp.</span><span class="sxs-lookup"><span data-stu-id="ec60f-103">Creates an eventhub consumer group.</span></span>

## <span data-ttu-id="ec60f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ec60f-104">SYNTAX</span></span>

```
Add-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ec60f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ec60f-105">DESCRIPTION</span></span>
<span data-ttu-id="ec60f-106">Skapar en konsument grupp i Eventhub som är associerad med angiven IotHub.</span><span class="sxs-lookup"><span data-stu-id="ec60f-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="ec60f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ec60f-107">EXAMPLES</span></span>

### <span data-ttu-id="ec60f-108">Exempel 1: lägga till en konsument grupp i eventhub-telemetri</span><span class="sxs-lookup"><span data-stu-id="ec60f-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="ec60f-109">Lägger till en ny consumergroup med namnet "myconsumergroup" i eventhub för telemetri-händelser i iothub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="ec60f-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="ec60f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ec60f-110">PARAMETERS</span></span>

### <span data-ttu-id="ec60f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec60f-111">-DefaultProfile</span></span>
<span data-ttu-id="ec60f-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ec60f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ec60f-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="ec60f-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="ec60f-114">Namn på den EventHub-ConsumerGroup som du vill lägga till.</span><span class="sxs-lookup"><span data-stu-id="ec60f-114">Name of the EventHub ConsumerGroup that you want to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec60f-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="ec60f-115">-Name</span></span>
<span data-ttu-id="ec60f-116">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="ec60f-116">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="ec60f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec60f-117">-ResourceGroupName</span></span>
<span data-ttu-id="ec60f-118">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ec60f-118">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="ec60f-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ec60f-119">-Confirm</span></span>
<span data-ttu-id="ec60f-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ec60f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec60f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec60f-121">-WhatIf</span></span>
<span data-ttu-id="ec60f-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ec60f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec60f-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ec60f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec60f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec60f-124">CommonParameters</span></span>
<span data-ttu-id="ec60f-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec60f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec60f-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec60f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec60f-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ec60f-127">INPUTS</span></span>

### <span data-ttu-id="ec60f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ec60f-128">System.String</span></span>

## <span data-ttu-id="ec60f-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ec60f-129">OUTPUTS</span></span>

### <span data-ttu-id="ec60f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ec60f-130">System.String</span></span>

## <span data-ttu-id="ec60f-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ec60f-131">NOTES</span></span>

## <span data-ttu-id="ec60f-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ec60f-132">RELATED LINKS</span></span>