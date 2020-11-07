---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bcd20fc9c6f0c08af2ae735558a6fccc6c9814d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758085"
---
# <span data-ttu-id="ab403-101">New-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="ab403-101">New-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="ab403-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ab403-102">SYNOPSIS</span></span>
<span data-ttu-id="ab403-103">Skapar en ny konsument grupp för den angivna Händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="ab403-103">Creates a new consumer group for the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab403-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ab403-104">SYNTAX</span></span>

```
New-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 -Name <String> [[-UserMetadata] <String>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="ab403-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ab403-105">DESCRIPTION</span></span>
<span data-ttu-id="ab403-106">New-AzureRmEventHubConsumerGroup-cmdleten skapar en ny konsument grupp för den angivna Händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="ab403-106">The New-AzureRmEventHubConsumerGroup cmdlet creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="ab403-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ab403-107">EXAMPLES</span></span>

### <span data-ttu-id="ab403-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ab403-108">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="ab403-109">Skapar gruppen konsument MyConsumerGroupName i MyEventHubName som bevaras \` \` \` \` till namn området \` MyNamespaceName \` , med resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="ab403-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="ab403-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ab403-110">PARAMETERS</span></span>

### <span data-ttu-id="ab403-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab403-111">-ResourceGroupName</span></span>
<span data-ttu-id="ab403-112">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="ab403-112">Resource group name.</span></span>

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

### <span data-ttu-id="ab403-113">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="ab403-113">-UserMetadata</span></span>
<span data-ttu-id="ab403-114">Användarens metadata för konsument gruppen.</span><span class="sxs-lookup"><span data-stu-id="ab403-114">User metadata for the consumer group.</span></span>

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

### <span data-ttu-id="ab403-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ab403-115">-Confirm</span></span>
<span data-ttu-id="ab403-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ab403-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab403-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab403-117">-WhatIf</span></span>
<span data-ttu-id="ab403-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ab403-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab403-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ab403-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab403-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="ab403-120">-EventHub</span></span>
<span data-ttu-id="ab403-121">Namn på EventHub.</span><span class="sxs-lookup"><span data-stu-id="ab403-121">EventHub Name.</span></span>

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

### <span data-ttu-id="ab403-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="ab403-122">-Name</span></span>
<span data-ttu-id="ab403-123">ConsumerGroup namn.</span><span class="sxs-lookup"><span data-stu-id="ab403-123">ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="ab403-124">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="ab403-124">-Namespace</span></span>
<span data-ttu-id="ab403-125">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="ab403-125">Namespace Name.</span></span>

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

## <span data-ttu-id="ab403-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ab403-126">INPUTS</span></span>

### <span data-ttu-id="ab403-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ab403-127">System.String</span></span>

## <span data-ttu-id="ab403-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ab403-128">OUTPUTS</span></span>

### <span data-ttu-id="ab403-129">Microsoft. Azure. commands. EventHub. Models. ConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="ab403-129">Microsoft.Azure.Commands.EventHub.Models.ConsumerGroupAttributes</span></span>

## <span data-ttu-id="ab403-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ab403-130">NOTES</span></span>

## <span data-ttu-id="ab403-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ab403-131">RELATED LINKS</span></span>

