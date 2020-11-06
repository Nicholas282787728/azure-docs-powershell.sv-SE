---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: c8684e9af0bca55dca52f336a458f4c428ca67a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580628"
---
# <span data-ttu-id="228e9-101">Remove-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="228e9-101">Remove-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="228e9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="228e9-102">SYNOPSIS</span></span>
<span data-ttu-id="228e9-103">Tar bort den angivna konsument gruppen Event Hubs.</span><span class="sxs-lookup"><span data-stu-id="228e9-103">Deletes the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="228e9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="228e9-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 -Name <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="228e9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="228e9-105">DESCRIPTION</span></span>
<span data-ttu-id="228e9-106">Remove-AzureRmEventHubConsumerGroup-cmdleten tar bort och tar bort den angivna konsument gruppen från den angivna händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="228e9-106">The Remove-AzureRmEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="228e9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="228e9-107">EXAMPLES</span></span>

### <span data-ttu-id="228e9-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="228e9-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="228e9-109">Tar bort gruppen konsument \` MyConsumerGroupName \` från \` MyEventHubName med \` \` MyNamespaceName- \` namnområdet.</span><span class="sxs-lookup"><span data-stu-id="228e9-109">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

## <span data-ttu-id="228e9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="228e9-110">PARAMETERS</span></span>

### <span data-ttu-id="228e9-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="228e9-111">-ResourceGroupName</span></span>
<span data-ttu-id="228e9-112">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="228e9-112">Resource group name.</span></span>

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

### <span data-ttu-id="228e9-113">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="228e9-113">-Confirm</span></span>
<span data-ttu-id="228e9-114">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="228e9-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="228e9-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="228e9-115">-WhatIf</span></span>
<span data-ttu-id="228e9-116">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="228e9-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="228e9-117">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="228e9-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="228e9-118">-EventHub</span><span class="sxs-lookup"><span data-stu-id="228e9-118">-EventHub</span></span>
<span data-ttu-id="228e9-119">Namn på EventHub.</span><span class="sxs-lookup"><span data-stu-id="228e9-119">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="228e9-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="228e9-120">-Name</span></span>
<span data-ttu-id="228e9-121">ConsumerGroup namn.</span><span class="sxs-lookup"><span data-stu-id="228e9-121">ConsumerGroup Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="228e9-122">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="228e9-122">-Namespace</span></span>
<span data-ttu-id="228e9-123">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="228e9-123">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="228e9-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="228e9-124">INPUTS</span></span>

### <span data-ttu-id="228e9-125">System. String</span><span class="sxs-lookup"><span data-stu-id="228e9-125">System.String</span></span>

## <span data-ttu-id="228e9-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="228e9-126">OUTPUTS</span></span>

### <span data-ttu-id="228e9-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="228e9-127">System.Object</span></span>

## <span data-ttu-id="228e9-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="228e9-128">NOTES</span></span>

## <span data-ttu-id="228e9-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="228e9-129">RELATED LINKS</span></span>

