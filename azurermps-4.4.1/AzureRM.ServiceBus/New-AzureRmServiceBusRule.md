---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
ms.openlocfilehash: 39cd0759f18c84f78a2e6a75f8e1c9b257fb9da9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758001"
---
# <span data-ttu-id="b93f4-101">New-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="b93f4-101">New-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="b93f4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b93f4-102">SYNOPSIS</span></span>
<span data-ttu-id="b93f4-103">Skapar en ny regel för ett givet abonnemang av ämnet.</span><span class="sxs-lookup"><span data-stu-id="b93f4-103">Creates a new rule for a given Subscription of Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b93f4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b93f4-104">SYNTAX</span></span>

```
New-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="b93f4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b93f4-105">DESCRIPTION</span></span>
<span data-ttu-id="b93f4-106">Cmdleten **New-AzureRmServiceBusRule** skapar en ny regel för angiven prenumeration.</span><span class="sxs-lookup"><span data-stu-id="b93f4-106">The **New-AzureRmServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="b93f4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b93f4-107">EXAMPLES</span></span>

### <span data-ttu-id="b93f4-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b93f4-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="b93f4-109">Cmdleten **New-AzureRmServiceBusRule** skapar en ny regel för det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="b93f4-109">The **New-AzureRmServiceBusRule** cmdlet creates a new rule for the specified Subscription.</span></span>

## <span data-ttu-id="b93f4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b93f4-110">PARAMETERS</span></span>

### <span data-ttu-id="b93f4-111">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b93f4-111">-Confirm</span></span>
<span data-ttu-id="b93f4-112">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b93f4-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b93f4-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="b93f4-113">-Name</span></span>
<span data-ttu-id="b93f4-114">Regel namn</span><span class="sxs-lookup"><span data-stu-id="b93f4-114">Rule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b93f4-115">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="b93f4-115">-Namespace</span></span>
<span data-ttu-id="b93f4-116">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="b93f4-116">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b93f4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b93f4-117">-ResourceGroupName</span></span>
<span data-ttu-id="b93f4-118">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="b93f4-118">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b93f4-119">-SqlExpression</span><span class="sxs-lookup"><span data-stu-id="b93f4-119">-SqlExpression</span></span>
<span data-ttu-id="b93f4-120">SQL filtrera-uttryck</span><span class="sxs-lookup"><span data-stu-id="b93f4-120">Sql Fillter Expression</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b93f4-121">-Abonnemang</span><span class="sxs-lookup"><span data-stu-id="b93f4-121">-Subscription</span></span>
<span data-ttu-id="b93f4-122">Prenumerationens namn</span><span class="sxs-lookup"><span data-stu-id="b93f4-122">Subscription Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b93f4-123">-Ämne</span><span class="sxs-lookup"><span data-stu-id="b93f4-123">-Topic</span></span>
<span data-ttu-id="b93f4-124">Avsnitts namn.</span><span class="sxs-lookup"><span data-stu-id="b93f4-124">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b93f4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b93f4-125">-WhatIf</span></span>
<span data-ttu-id="b93f4-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b93f4-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b93f4-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b93f4-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="b93f4-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b93f4-128">INPUTS</span></span>

### <span data-ttu-id="b93f4-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b93f4-129">System.String</span></span>


## <span data-ttu-id="b93f4-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b93f4-130">OUTPUTS</span></span>

### <span data-ttu-id="b93f4-131">Microsoft. Azure. commands. ServiceBus. Models. RulesAttributes</span><span class="sxs-lookup"><span data-stu-id="b93f4-131">Microsoft.Azure.Commands.ServiceBus.Models.RulesAttributes</span></span>


## <span data-ttu-id="b93f4-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b93f4-132">NOTES</span></span>

## <span data-ttu-id="b93f4-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b93f4-133">RELATED LINKS</span></span>

