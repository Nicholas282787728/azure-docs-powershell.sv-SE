---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusRule.md
ms.openlocfilehash: 8a8c60f486980fef6005cb4f4070af31689fae92
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575498"
---
# <span data-ttu-id="89e16-101">Set-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="89e16-101">Set-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="89e16-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="89e16-102">SYNOPSIS</span></span>
<span data-ttu-id="89e16-103">Uppdaterar den angivna regel beskrivningen för det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="89e16-103">Updates the specified rule description for the given subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89e16-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="89e16-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-InputObject] <RulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89e16-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="89e16-105">DESCRIPTION</span></span>
<span data-ttu-id="89e16-106">Cmdleten **set-AzureRmServiceBusRule** uppdaterar beskrivningen för den angivna regeln för angiven prenumeration.</span><span class="sxs-lookup"><span data-stu-id="89e16-106">The **Set-AzureRmServiceBusRule** cmdlet updates the description for the specified rule of the given subscription.</span></span>

## <span data-ttu-id="89e16-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="89e16-107">EXAMPLES</span></span>

### <span data-ttu-id="89e16-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="89e16-108">Example 1</span></span>
```
PS C:\> $getRule = Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
PS C:\> $getRule.SqlFilter.SqlExpression = "mysqlexpression='condition'"
PS C:\> $setRule = Set-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -InputObject $getRule
```

<span data-ttu-id="89e16-109">uppdaterar sqlexpression **mysqlexpression = ' villkor** för regeln `SBEule` för abonnemanget `SBSubscription` i ämnet `SBTopic`</span><span class="sxs-lookup"><span data-stu-id="89e16-109">updates the sqlexpression **mysqlexpression='condition'** of the rule `SBEule` of the subscription `SBSubscription` in Topic `SBTopic`</span></span>

## <span data-ttu-id="89e16-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="89e16-110">PARAMETERS</span></span>

### <span data-ttu-id="89e16-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89e16-111">-DefaultProfile</span></span>
<span data-ttu-id="89e16-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="89e16-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89e16-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89e16-113">-InputObject</span></span>
<span data-ttu-id="89e16-114">ServiceBus regel definition.</span><span class="sxs-lookup"><span data-stu-id="89e16-114">ServiceBus Rules definition.</span></span>

```yaml
Type: PSRulesAttributes
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89e16-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="89e16-115">-Name</span></span>
<span data-ttu-id="89e16-116">Regel namn.</span><span class="sxs-lookup"><span data-stu-id="89e16-116">Rule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89e16-117">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="89e16-117">-Namespace</span></span>
<span data-ttu-id="89e16-118">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="89e16-118">Namespace Name.</span></span>

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

### <span data-ttu-id="89e16-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89e16-119">-ResourceGroupName</span></span>
<span data-ttu-id="89e16-120">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="89e16-120">The name of the resource group</span></span>

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

### <span data-ttu-id="89e16-121">-Abonnemang</span><span class="sxs-lookup"><span data-stu-id="89e16-121">-Subscription</span></span>
<span data-ttu-id="89e16-122">Prenumerationens namn.</span><span class="sxs-lookup"><span data-stu-id="89e16-122">Subscription Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89e16-123">-Ämne</span><span class="sxs-lookup"><span data-stu-id="89e16-123">-Topic</span></span>
<span data-ttu-id="89e16-124">Avsnitts namn.</span><span class="sxs-lookup"><span data-stu-id="89e16-124">Topic Name.</span></span>

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

### <span data-ttu-id="89e16-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="89e16-125">-Confirm</span></span>
<span data-ttu-id="89e16-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="89e16-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89e16-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89e16-127">-WhatIf</span></span>
<span data-ttu-id="89e16-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="89e16-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89e16-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="89e16-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89e16-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89e16-130">CommonParameters</span></span>
<span data-ttu-id="89e16-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89e16-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89e16-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89e16-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89e16-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="89e16-133">INPUTS</span></span>

### <span data-ttu-id="89e16-134">System. String</span><span class="sxs-lookup"><span data-stu-id="89e16-134">System.String</span></span>
<span data-ttu-id="89e16-135">Microsoft. Azure. commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="89e16-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="89e16-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="89e16-136">OUTPUTS</span></span>

### <span data-ttu-id="89e16-137">Microsoft. Azure. commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="89e16-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="89e16-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="89e16-138">NOTES</span></span>

## <span data-ttu-id="89e16-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="89e16-139">RELATED LINKS</span></span>
