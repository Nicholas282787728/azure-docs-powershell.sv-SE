---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 59a180d422a27ca9d2c3e1e4932d843ba7c70093
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916421"
---
# <span data-ttu-id="b3359-101">Remove-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="b3359-101">Remove-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="b3359-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b3359-102">SYNOPSIS</span></span>
<span data-ttu-id="b3359-103">Tar bort en eventhub-consumergroup.</span><span class="sxs-lookup"><span data-stu-id="b3359-103">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="b3359-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b3359-104">SYNTAX</span></span>

```
Remove-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3359-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b3359-105">DESCRIPTION</span></span>
<span data-ttu-id="b3359-106">Tar bort en eventhub-consumergroup.</span><span class="sxs-lookup"><span data-stu-id="b3359-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="b3359-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b3359-107">EXAMPLES</span></span>

### <span data-ttu-id="b3359-108">Exempel 1 ta bort eventhub-consumergroup från eventhub-telemetri</span><span class="sxs-lookup"><span data-stu-id="b3359-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName events -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="b3359-109">Tar bort consumergroup med namnet myconsumergroup från IotHub som heter "myiothub"</span><span class="sxs-lookup"><span data-stu-id="b3359-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="b3359-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b3359-110">PARAMETERS</span></span>

### <span data-ttu-id="b3359-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3359-111">-DefaultProfile</span></span>
<span data-ttu-id="b3359-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b3359-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3359-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="b3359-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="b3359-114">EventHub-ConsumerGroup namn.</span><span class="sxs-lookup"><span data-stu-id="b3359-114">EventHub ConsumerGroup Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3359-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="b3359-115">-EventHubEndpointName</span></span>
<span data-ttu-id="b3359-116">Namn på EventHub-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="b3359-116">EventHub Endpoint Name.</span></span>
<span data-ttu-id="b3359-117">Möjliga värden, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="b3359-117">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="b3359-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="b3359-118">-Name</span></span>
<span data-ttu-id="b3359-119">Namn på IotHub</span><span class="sxs-lookup"><span data-stu-id="b3359-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="b3359-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3359-120">-ResourceGroupName</span></span>
<span data-ttu-id="b3359-121">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="b3359-121">Resource Group Name</span></span>

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

### <span data-ttu-id="b3359-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b3359-122">-Confirm</span></span>
<span data-ttu-id="b3359-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b3359-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3359-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3359-124">-WhatIf</span></span>
<span data-ttu-id="b3359-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b3359-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3359-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b3359-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3359-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3359-127">CommonParameters</span></span>
<span data-ttu-id="b3359-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3359-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3359-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3359-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3359-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b3359-130">INPUTS</span></span>

### <span data-ttu-id="b3359-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b3359-131">System.String</span></span>

## <span data-ttu-id="b3359-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b3359-132">OUTPUTS</span></span>

### <span data-ttu-id="b3359-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b3359-133">System.String</span></span>

## <span data-ttu-id="b3359-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b3359-134">NOTES</span></span>

## <span data-ttu-id="b3359-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b3359-135">RELATED LINKS</span></span>
