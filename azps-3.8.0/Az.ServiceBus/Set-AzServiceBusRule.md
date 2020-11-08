---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
ms.openlocfilehash: b86b9629062515afb1ee70e7c7372cbc7687bfa5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088809"
---
# <span data-ttu-id="728ba-101">Set-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="728ba-101">Set-AzServiceBusRule</span></span>

## <span data-ttu-id="728ba-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="728ba-102">SYNOPSIS</span></span>
<span data-ttu-id="728ba-103">Uppdaterar den angivna regel beskrivningen för det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="728ba-103">Updates the specified rule description for the given subscription.</span></span>

## <span data-ttu-id="728ba-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="728ba-104">SYNTAX</span></span>

```
Set-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-InputObject] <PSRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="728ba-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="728ba-105">DESCRIPTION</span></span>
<span data-ttu-id="728ba-106">Cmdleten **set-AzServiceBusRule** uppdaterar beskrivningen för den angivna regeln för angiven prenumeration.</span><span class="sxs-lookup"><span data-stu-id="728ba-106">The **Set-AzServiceBusRule** cmdlet updates the description for the specified rule of the given subscription.</span></span>

## <span data-ttu-id="728ba-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="728ba-107">EXAMPLES</span></span>

### <span data-ttu-id="728ba-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="728ba-108">Example 1</span></span>
```
PS C:\> $getRule = Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
PS C:\> $getRule.SqlFilter.SqlExpression = "mysqlexpression='condition'"
PS C:\> $setRule = Set-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -InputObject $getRule
```

<span data-ttu-id="728ba-109">Uppdaterar SQL-uttrycket **mysqlexpression = ' villkor '** för regeln `SBRule` för abonnemanget `SBSubscription` i ämnet `SBTopic`</span><span class="sxs-lookup"><span data-stu-id="728ba-109">Updates the sql expression **mysqlexpression='condition'** of the rule `SBRule` of the subscription `SBSubscription` in Topic `SBTopic`</span></span>

## <span data-ttu-id="728ba-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="728ba-110">PARAMETERS</span></span>

### <span data-ttu-id="728ba-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="728ba-111">-DefaultProfile</span></span>
<span data-ttu-id="728ba-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="728ba-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="728ba-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="728ba-113">-InputObject</span></span>
<span data-ttu-id="728ba-114">ServiceBus regel definition.</span><span class="sxs-lookup"><span data-stu-id="728ba-114">ServiceBus Rules definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="728ba-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="728ba-115">-Name</span></span>
<span data-ttu-id="728ba-116">Regel namn.</span><span class="sxs-lookup"><span data-stu-id="728ba-116">Rule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="728ba-117">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="728ba-117">-Namespace</span></span>
<span data-ttu-id="728ba-118">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="728ba-118">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="728ba-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="728ba-119">-ResourceGroupName</span></span>
<span data-ttu-id="728ba-120">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="728ba-120">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="728ba-121">-Abonnemang</span><span class="sxs-lookup"><span data-stu-id="728ba-121">-Subscription</span></span>
<span data-ttu-id="728ba-122">Prenumerationens namn.</span><span class="sxs-lookup"><span data-stu-id="728ba-122">Subscription Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="728ba-123">-Ämne</span><span class="sxs-lookup"><span data-stu-id="728ba-123">-Topic</span></span>
<span data-ttu-id="728ba-124">Avsnitts namn.</span><span class="sxs-lookup"><span data-stu-id="728ba-124">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="728ba-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="728ba-125">-Confirm</span></span>
<span data-ttu-id="728ba-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="728ba-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="728ba-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="728ba-127">-WhatIf</span></span>
<span data-ttu-id="728ba-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="728ba-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="728ba-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="728ba-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="728ba-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="728ba-130">CommonParameters</span></span>
<span data-ttu-id="728ba-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="728ba-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="728ba-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="728ba-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="728ba-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="728ba-133">INPUTS</span></span>

### <span data-ttu-id="728ba-134">System. String</span><span class="sxs-lookup"><span data-stu-id="728ba-134">System.String</span></span>

### <span data-ttu-id="728ba-135">Microsoft. Azure. commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="728ba-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="728ba-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="728ba-136">OUTPUTS</span></span>

### <span data-ttu-id="728ba-137">Microsoft. Azure. commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="728ba-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="728ba-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="728ba-138">NOTES</span></span>

## <span data-ttu-id="728ba-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="728ba-139">RELATED LINKS</span></span>
