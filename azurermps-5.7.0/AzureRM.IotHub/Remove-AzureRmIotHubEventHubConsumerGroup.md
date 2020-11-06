---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 5f4324ab7a27b711d33042eede5c3b88d38c4511
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575651"
---
# <span data-ttu-id="7768a-101">Remove-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="7768a-101">Remove-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="7768a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7768a-102">SYNOPSIS</span></span>
<span data-ttu-id="7768a-103">Tar bort en eventhub-consumergroup.</span><span class="sxs-lookup"><span data-stu-id="7768a-103">Deletes an eventhub consumergroup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7768a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7768a-104">SYNTAX</span></span>

```
Remove-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7768a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7768a-105">DESCRIPTION</span></span>
<span data-ttu-id="7768a-106">Tar bort en eventhub-consumergroup.</span><span class="sxs-lookup"><span data-stu-id="7768a-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="7768a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7768a-107">EXAMPLES</span></span>

### <span data-ttu-id="7768a-108">Exempel 1 ta bort eventhub-consumergroup från eventhub-telemetri</span><span class="sxs-lookup"><span data-stu-id="7768a-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName events -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="7768a-109">Tar bort consumergroup med namnet myconsumergroup från IotHub som heter "myiothub"</span><span class="sxs-lookup"><span data-stu-id="7768a-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="7768a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7768a-110">PARAMETERS</span></span>

### <span data-ttu-id="7768a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7768a-111">-DefaultProfile</span></span>
<span data-ttu-id="7768a-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7768a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7768a-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="7768a-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="7768a-114">EventHub-ConsumerGroup namn.</span><span class="sxs-lookup"><span data-stu-id="7768a-114">EventHub ConsumerGroup Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7768a-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="7768a-115">-EventHubEndpointName</span></span>
<span data-ttu-id="7768a-116">Namn på EventHub-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="7768a-116">EventHub Endpoint Name.</span></span>
<span data-ttu-id="7768a-117">Möjliga värden, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="7768a-117">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="7768a-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="7768a-118">-Name</span></span>
<span data-ttu-id="7768a-119">Namn på IotHub</span><span class="sxs-lookup"><span data-stu-id="7768a-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="7768a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7768a-120">-ResourceGroupName</span></span>
<span data-ttu-id="7768a-121">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="7768a-121">Resource Group Name</span></span>

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

### <span data-ttu-id="7768a-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7768a-122">-Confirm</span></span>
<span data-ttu-id="7768a-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7768a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7768a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7768a-124">-WhatIf</span></span>
<span data-ttu-id="7768a-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7768a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7768a-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7768a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7768a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7768a-127">CommonParameters</span></span>
<span data-ttu-id="7768a-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7768a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7768a-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7768a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7768a-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7768a-130">INPUTS</span></span>

### <span data-ttu-id="7768a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="7768a-131">System.String</span></span>

## <span data-ttu-id="7768a-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7768a-132">OUTPUTS</span></span>

### <span data-ttu-id="7768a-133">System. Collections. Generic. IEnumerable ' 1 [[system. String, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7768a-133">System.Collections.Generic.IEnumerable\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="7768a-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7768a-134">NOTES</span></span>

## <span data-ttu-id="7768a-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7768a-135">RELATED LINKS</span></span>

