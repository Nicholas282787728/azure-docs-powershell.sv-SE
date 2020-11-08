---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 9fa0a9d85dc9c7b1a6cc56c3c329b1810cceaa18
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091523"
---
# <span data-ttu-id="29bc7-101">Remove-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="29bc7-101">Remove-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="29bc7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="29bc7-102">SYNOPSIS</span></span>
<span data-ttu-id="29bc7-103">Tar bort en eventhub-consumergroup.</span><span class="sxs-lookup"><span data-stu-id="29bc7-103">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="29bc7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="29bc7-104">SYNTAX</span></span>

```
Remove-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="29bc7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="29bc7-105">DESCRIPTION</span></span>
<span data-ttu-id="29bc7-106">Tar bort en eventhub-consumergroup.</span><span class="sxs-lookup"><span data-stu-id="29bc7-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="29bc7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="29bc7-107">EXAMPLES</span></span>

### <span data-ttu-id="29bc7-108">Exempel 1 ta bort eventhub-consumergroup från eventhub-telemetri</span><span class="sxs-lookup"><span data-stu-id="29bc7-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="29bc7-109">Tar bort consumergroup med namnet myconsumergroup från IotHub som heter "myiothub"</span><span class="sxs-lookup"><span data-stu-id="29bc7-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="29bc7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="29bc7-110">PARAMETERS</span></span>

### <span data-ttu-id="29bc7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29bc7-111">-DefaultProfile</span></span>
<span data-ttu-id="29bc7-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="29bc7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29bc7-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="29bc7-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="29bc7-114">EventHub-ConsumerGroup namn.</span><span class="sxs-lookup"><span data-stu-id="29bc7-114">EventHub ConsumerGroup Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29bc7-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="29bc7-115">-Name</span></span>
<span data-ttu-id="29bc7-116">Namn på IotHub</span><span class="sxs-lookup"><span data-stu-id="29bc7-116">Name of the IotHub</span></span>

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

### <span data-ttu-id="29bc7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29bc7-117">-ResourceGroupName</span></span>
<span data-ttu-id="29bc7-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="29bc7-118">Resource Group Name</span></span>

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

### <span data-ttu-id="29bc7-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="29bc7-119">-Confirm</span></span>
<span data-ttu-id="29bc7-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="29bc7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29bc7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29bc7-121">-WhatIf</span></span>
<span data-ttu-id="29bc7-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="29bc7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29bc7-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="29bc7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29bc7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29bc7-124">CommonParameters</span></span>
<span data-ttu-id="29bc7-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29bc7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29bc7-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29bc7-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29bc7-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="29bc7-127">INPUTS</span></span>

### <span data-ttu-id="29bc7-128">System. String</span><span class="sxs-lookup"><span data-stu-id="29bc7-128">System.String</span></span>

## <span data-ttu-id="29bc7-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="29bc7-129">OUTPUTS</span></span>

### <span data-ttu-id="29bc7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="29bc7-130">System.String</span></span>

## <span data-ttu-id="29bc7-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="29bc7-131">NOTES</span></span>

## <span data-ttu-id="29bc7-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="29bc7-132">RELATED LINKS</span></span>