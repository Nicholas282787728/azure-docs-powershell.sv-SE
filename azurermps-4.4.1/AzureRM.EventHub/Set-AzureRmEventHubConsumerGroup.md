---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: c871036c6f3113bd40e17fb5bbc201fa6297573c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582444"
---
# <span data-ttu-id="53214-101">Set-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="53214-101">Set-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="53214-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="53214-102">SYNOPSIS</span></span>
<span data-ttu-id="53214-103">Uppdaterar den angivna konsument gruppen för händelse nav.</span><span class="sxs-lookup"><span data-stu-id="53214-103">Updates the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53214-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="53214-104">SYNTAX</span></span>

```
Set-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 -Name <String> [[-UserMetadata] <String>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="53214-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="53214-105">DESCRIPTION</span></span>
<span data-ttu-id="53214-106">Den Set-AzureRmEventHubConsumerGroup cmdleten uppdaterar den angivna konsument gruppen Event Hubs.</span><span class="sxs-lookup"><span data-stu-id="53214-106">The Set-AzureRmEventHubConsumerGroup cmdlet updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="53214-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="53214-107">EXAMPLES</span></span>

### <span data-ttu-id="53214-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="53214-108">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName -UserMetadata "Testing"
```

<span data-ttu-id="53214-109">Anger användarnas metadata för konsument gruppen \` MyConsumerGroupName \` till "testar".</span><span class="sxs-lookup"><span data-stu-id="53214-109">Sets the user metadata of the consumer group \`MyConsumerGroupName\` to "Testing."</span></span>

## <span data-ttu-id="53214-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="53214-110">PARAMETERS</span></span>

### <span data-ttu-id="53214-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53214-111">-ResourceGroupName</span></span>
<span data-ttu-id="53214-112">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="53214-112">Resource group name.</span></span>

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

### <span data-ttu-id="53214-113">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="53214-113">-UserMetadata</span></span>
<span data-ttu-id="53214-114">Användarens metadata för konsument gruppen (valfritt).</span><span class="sxs-lookup"><span data-stu-id="53214-114">User metadata for the consumer group (optional).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53214-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="53214-115">-Confirm</span></span>
<span data-ttu-id="53214-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="53214-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53214-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53214-117">-WhatIf</span></span>
<span data-ttu-id="53214-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="53214-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53214-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="53214-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53214-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="53214-120">-EventHub</span></span>
<span data-ttu-id="53214-121">Namn på EventHub.</span><span class="sxs-lookup"><span data-stu-id="53214-121">EventHub Name.</span></span>

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

### <span data-ttu-id="53214-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="53214-122">-Name</span></span>
<span data-ttu-id="53214-123">ConsumerGroup namn.</span><span class="sxs-lookup"><span data-stu-id="53214-123">ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="53214-124">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="53214-124">-Namespace</span></span>
<span data-ttu-id="53214-125">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="53214-125">Namespace Name.</span></span>

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

## <span data-ttu-id="53214-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="53214-126">INPUTS</span></span>

### <span data-ttu-id="53214-127">System. String</span><span class="sxs-lookup"><span data-stu-id="53214-127">System.String</span></span>

## <span data-ttu-id="53214-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="53214-128">OUTPUTS</span></span>

### <span data-ttu-id="53214-129">Microsoft. Azure. commands. EventHub. Models. ConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="53214-129">Microsoft.Azure.Commands.EventHub.Models.ConsumerGroupAttributes</span></span>

## <span data-ttu-id="53214-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="53214-130">NOTES</span></span>

## <span data-ttu-id="53214-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="53214-131">RELATED LINKS</span></span>

