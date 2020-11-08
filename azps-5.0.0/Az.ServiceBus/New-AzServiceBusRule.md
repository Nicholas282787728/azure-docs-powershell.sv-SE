---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
ms.openlocfilehash: d667049fb512545aebfd9681b3ad3d9f44651951
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270060"
---
# <span data-ttu-id="c0601-101">New-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="c0601-101">New-AzServiceBusRule</span></span>

## <span data-ttu-id="c0601-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c0601-102">SYNOPSIS</span></span>
<span data-ttu-id="c0601-103">Skapar en ny regel för ett givet abonnemang av ämnet.</span><span class="sxs-lookup"><span data-stu-id="c0601-103">Creates a new rule for a given Subscription of Topic.</span></span> 

## <span data-ttu-id="c0601-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c0601-104">SYNTAX</span></span>

### <span data-ttu-id="c0601-105">RulePropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c0601-105">RulePropertiesSet (Default)</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0601-106">RuleActionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="c0601-106">RuleActionPropertiesSet</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> -ActionSqlExpression <String>
 [-RequiresPreprocessing] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0601-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c0601-107">DESCRIPTION</span></span>
<span data-ttu-id="c0601-108">Cmdleten **New-AzServiceBusRule** skapar en ny regel för angiven prenumeration.</span><span class="sxs-lookup"><span data-stu-id="c0601-108">The **New-AzServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="c0601-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c0601-109">EXAMPLES</span></span>

### <span data-ttu-id="c0601-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c0601-110">Example 1</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="c0601-111">New-AzServiceBusRule cmdlet skapar en ny regel för det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="c0601-111">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription.</span></span>

### <span data-ttu-id="c0601-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="c0601-112">Example 2</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'" -ActionSqlExpression "SET myAction='test'" -RequiresPreprocessing
```

<span data-ttu-id="c0601-113">New-AzServiceBusRule cmdlet skapar en ny regel för den angivna prenumerationen med ActionFilter.</span><span class="sxs-lookup"><span data-stu-id="c0601-113">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription with ActionFilter.</span></span>

## <span data-ttu-id="c0601-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c0601-114">PARAMETERS</span></span>

### <span data-ttu-id="c0601-115">-ActionSqlExpression</span><span class="sxs-lookup"><span data-stu-id="c0601-115">-ActionSqlExpression</span></span>
<span data-ttu-id="c0601-116">Instruktionen SqlFilter</span><span class="sxs-lookup"><span data-stu-id="c0601-116">Action SqlFilter Expression</span></span>

```yaml
Type: System.String
Parameter Sets: RuleActionPropertiesSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0601-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0601-117">-DefaultProfile</span></span>
<span data-ttu-id="c0601-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c0601-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0601-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="c0601-119">-Name</span></span>
<span data-ttu-id="c0601-120">Regel namn</span><span class="sxs-lookup"><span data-stu-id="c0601-120">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0601-121">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="c0601-121">-Namespace</span></span>
<span data-ttu-id="c0601-122">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="c0601-122">Namespace Name</span></span>

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

### <span data-ttu-id="c0601-123">-RequiresPreprocessing</span><span class="sxs-lookup"><span data-stu-id="c0601-123">-RequiresPreprocessing</span></span>
<span data-ttu-id="c0601-124">Åtgärden kräver förbehandling</span><span class="sxs-lookup"><span data-stu-id="c0601-124">Action Requires Preprocessing</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RuleActionPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0601-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0601-125">-ResourceGroupName</span></span>
<span data-ttu-id="c0601-126">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="c0601-126">The name of the resource group</span></span>

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

### <span data-ttu-id="c0601-127">-SqlExpression</span><span class="sxs-lookup"><span data-stu-id="c0601-127">-SqlExpression</span></span>
<span data-ttu-id="c0601-128">SQL filter-uttryck</span><span class="sxs-lookup"><span data-stu-id="c0601-128">Sql Filter Expression</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0601-129">-Abonnemang</span><span class="sxs-lookup"><span data-stu-id="c0601-129">-Subscription</span></span>
<span data-ttu-id="c0601-130">Prenumerationens namn</span><span class="sxs-lookup"><span data-stu-id="c0601-130">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0601-131">-Ämne</span><span class="sxs-lookup"><span data-stu-id="c0601-131">-Topic</span></span>
<span data-ttu-id="c0601-132">Namn på avsnitt</span><span class="sxs-lookup"><span data-stu-id="c0601-132">Topic Name</span></span>

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

### <span data-ttu-id="c0601-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c0601-133">-Confirm</span></span>
<span data-ttu-id="c0601-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c0601-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0601-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0601-135">-WhatIf</span></span>
<span data-ttu-id="c0601-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c0601-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0601-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c0601-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0601-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0601-138">CommonParameters</span></span>
<span data-ttu-id="c0601-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0601-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0601-140">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0601-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0601-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c0601-141">INPUTS</span></span>

### <span data-ttu-id="c0601-142">System. String</span><span class="sxs-lookup"><span data-stu-id="c0601-142">System.String</span></span>

## <span data-ttu-id="c0601-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c0601-143">OUTPUTS</span></span>

### <span data-ttu-id="c0601-144">Microsoft. Azure. commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="c0601-144">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="c0601-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c0601-145">NOTES</span></span>

## <span data-ttu-id="c0601-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c0601-146">RELATED LINKS</span></span>
