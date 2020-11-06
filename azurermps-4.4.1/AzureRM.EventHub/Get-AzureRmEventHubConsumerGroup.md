---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 4a2608ee3d3f874183a35fe6b81f7cd169123416
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585608"
---
# <span data-ttu-id="958ae-101">Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="958ae-101">Get-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="958ae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="958ae-102">SYNOPSIS</span></span>
<span data-ttu-id="958ae-103">Hämtar information om en viss konsument grupp för händelse nav eller hämtar en lista över konsument grupper i en Händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="958ae-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="958ae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="958ae-104">SYNTAX</span></span>

```
Get-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 [-Name <String>]
```

## <span data-ttu-id="958ae-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="958ae-105">DESCRIPTION</span></span>
<span data-ttu-id="958ae-106">Get-AzureRmEventHubConsumerGroup-cmdleten får antingen information om en viss konsument grupp för händelse nav eller en lista över konsument grupper i en viss händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="958ae-106">The Get-AzureRmEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="958ae-107">Om namnet på en konsument grupp är angivet returneras informationen om en enskild konsument grupp information.</span><span class="sxs-lookup"><span data-stu-id="958ae-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="958ae-108">Om namnet på en konsument grupp inte har angetts returneras en lista över konsument grupper i den angivna Händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="958ae-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="958ae-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="958ae-109">EXAMPLES</span></span>

### <span data-ttu-id="958ae-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="958ae-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="958ae-111">Hämtar gruppen konsument \` MyConsumerGroupName \` i \` MyEventHubName \` som finns i namn området \` MyNamespaceName \` med resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="958ae-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="958ae-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="958ae-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="958ae-113">Hämtar en lista över konsument grupper i Händelsehubben \` MyEventHubName \` , som finns i namn området \` MyNamespaceName \` med resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="958ae-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="958ae-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="958ae-114">PARAMETERS</span></span>

### <span data-ttu-id="958ae-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="958ae-115">-ResourceGroupName</span></span>
<span data-ttu-id="958ae-116">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="958ae-116">Resource group name.</span></span>

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

### <span data-ttu-id="958ae-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="958ae-117">-EventHub</span></span>
<span data-ttu-id="958ae-118">Namn på EventHub.</span><span class="sxs-lookup"><span data-stu-id="958ae-118">EventHub Name.</span></span>

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

### <span data-ttu-id="958ae-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="958ae-119">-Name</span></span>
<span data-ttu-id="958ae-120">ConsumerGroup namn.</span><span class="sxs-lookup"><span data-stu-id="958ae-120">ConsumerGroup Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="958ae-121">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="958ae-121">-Namespace</span></span>
<span data-ttu-id="958ae-122">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="958ae-122">Namespace Name.</span></span>

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

## <span data-ttu-id="958ae-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="958ae-123">INPUTS</span></span>

### <span data-ttu-id="958ae-124">System. String</span><span class="sxs-lookup"><span data-stu-id="958ae-124">System.String</span></span>

## <span data-ttu-id="958ae-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="958ae-125">OUTPUTS</span></span>

### <span data-ttu-id="958ae-126">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. EventHub. Models. ConsumerGroupAttributes, Microsoft. Azure. commands. EventHub, version = 0.0.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="958ae-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.ConsumerGroupAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="958ae-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="958ae-127">NOTES</span></span>

## <span data-ttu-id="958ae-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="958ae-128">RELATED LINKS</span></span>

