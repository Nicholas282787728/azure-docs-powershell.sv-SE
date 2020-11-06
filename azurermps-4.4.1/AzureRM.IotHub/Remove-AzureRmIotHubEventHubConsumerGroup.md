---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: b326f7228a60f7549fc6dcd227b9bad947f22add
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584711"
---
# <span data-ttu-id="057d8-101">Remove-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="057d8-101">Remove-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="057d8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="057d8-102">SYNOPSIS</span></span>
<span data-ttu-id="057d8-103">Tar bort en eventhub-consumergroup.</span><span class="sxs-lookup"><span data-stu-id="057d8-103">Deletes an eventhub consumergroup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="057d8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="057d8-104">SYNTAX</span></span>

```
Remove-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="057d8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="057d8-105">DESCRIPTION</span></span>
<span data-ttu-id="057d8-106">Tar bort en eventhub-consumergroup.</span><span class="sxs-lookup"><span data-stu-id="057d8-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="057d8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="057d8-107">EXAMPLES</span></span>

### <span data-ttu-id="057d8-108">Exempel 1 ta bort eventhub-consumergroup från eventhub-telemetri</span><span class="sxs-lookup"><span data-stu-id="057d8-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName events -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="057d8-109">Tar bort consumergroup med namnet myconsumergroup från IotHub som heter "myiothub"</span><span class="sxs-lookup"><span data-stu-id="057d8-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="057d8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="057d8-110">PARAMETERS</span></span>

### <span data-ttu-id="057d8-111">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="057d8-111">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="057d8-112">EventHub-ConsumerGroup namn.</span><span class="sxs-lookup"><span data-stu-id="057d8-112">EventHub ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="057d8-113">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="057d8-113">-EventHubEndpointName</span></span>
<span data-ttu-id="057d8-114">Namn på EventHub-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="057d8-114">EventHub Endpoint Name.</span></span>
<span data-ttu-id="057d8-115">Möjliga värden, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="057d8-115">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="057d8-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="057d8-116">-Name</span></span>
<span data-ttu-id="057d8-117">Namn på IotHub</span><span class="sxs-lookup"><span data-stu-id="057d8-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="057d8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="057d8-118">-ResourceGroupName</span></span>
<span data-ttu-id="057d8-119">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="057d8-119">Resource Group Name</span></span>

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

### <span data-ttu-id="057d8-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="057d8-120">-Confirm</span></span>
<span data-ttu-id="057d8-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="057d8-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="057d8-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="057d8-122">-WhatIf</span></span>
<span data-ttu-id="057d8-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="057d8-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="057d8-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="057d8-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="057d8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="057d8-125">-DefaultProfile</span></span>
<span data-ttu-id="057d8-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="057d8-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="057d8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="057d8-127">CommonParameters</span></span>
<span data-ttu-id="057d8-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="057d8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="057d8-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="057d8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="057d8-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="057d8-130">INPUTS</span></span>

### <span data-ttu-id="057d8-131">System. String</span><span class="sxs-lookup"><span data-stu-id="057d8-131">System.String</span></span>

## <span data-ttu-id="057d8-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="057d8-132">OUTPUTS</span></span>

### <span data-ttu-id="057d8-133">System. Collections. Generic. IEnumerable ' 1 [[system. String, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="057d8-133">System.Collections.Generic.IEnumerable\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="057d8-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="057d8-134">NOTES</span></span>

## <span data-ttu-id="057d8-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="057d8-135">RELATED LINKS</span></span>

