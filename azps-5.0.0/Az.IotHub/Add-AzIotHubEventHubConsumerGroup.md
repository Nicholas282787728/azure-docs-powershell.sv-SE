---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 749bd1329537d165cb7c31850fd15ca23f38db2d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271009"
---
# <span data-ttu-id="5ff16-101">Add-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="5ff16-101">Add-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="5ff16-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5ff16-102">SYNOPSIS</span></span>
<span data-ttu-id="5ff16-103">Skapar en eventhub-konsument grupp.</span><span class="sxs-lookup"><span data-stu-id="5ff16-103">Creates an eventhub consumer group.</span></span>

## <span data-ttu-id="5ff16-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5ff16-104">SYNTAX</span></span>

```
Add-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5ff16-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5ff16-105">DESCRIPTION</span></span>
<span data-ttu-id="5ff16-106">Skapar en konsument grupp i Eventhub som är associerad med angiven IotHub.</span><span class="sxs-lookup"><span data-stu-id="5ff16-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="5ff16-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5ff16-107">EXAMPLES</span></span>

### <span data-ttu-id="5ff16-108">Exempel 1: lägga till en konsument grupp i eventhub-telemetri</span><span class="sxs-lookup"><span data-stu-id="5ff16-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="5ff16-109">Lägger till en ny consumergroup med namnet "myconsumergroup" i eventhub för telemetri-händelser i iothub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="5ff16-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="5ff16-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5ff16-110">PARAMETERS</span></span>

### <span data-ttu-id="5ff16-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ff16-111">-DefaultProfile</span></span>
<span data-ttu-id="5ff16-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="5ff16-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ff16-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="5ff16-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="5ff16-114">Namn på den EventHub-ConsumerGroup som du vill lägga till.</span><span class="sxs-lookup"><span data-stu-id="5ff16-114">Name of the EventHub ConsumerGroup that you want to add.</span></span>

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

### <span data-ttu-id="5ff16-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="5ff16-115">-Name</span></span>
<span data-ttu-id="5ff16-116">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="5ff16-116">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="5ff16-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ff16-117">-ResourceGroupName</span></span>
<span data-ttu-id="5ff16-118">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5ff16-118">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="5ff16-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5ff16-119">-Confirm</span></span>
<span data-ttu-id="5ff16-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5ff16-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ff16-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ff16-121">-WhatIf</span></span>
<span data-ttu-id="5ff16-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5ff16-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ff16-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5ff16-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ff16-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ff16-124">CommonParameters</span></span>
<span data-ttu-id="5ff16-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ff16-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ff16-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ff16-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ff16-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5ff16-127">INPUTS</span></span>

### <span data-ttu-id="5ff16-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5ff16-128">System.String</span></span>

## <span data-ttu-id="5ff16-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5ff16-129">OUTPUTS</span></span>

### <span data-ttu-id="5ff16-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5ff16-130">System.String</span></span>

## <span data-ttu-id="5ff16-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5ff16-131">NOTES</span></span>

## <span data-ttu-id="5ff16-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5ff16-132">RELATED LINKS</span></span>
