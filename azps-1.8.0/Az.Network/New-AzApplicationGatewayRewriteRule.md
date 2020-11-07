---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriterule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
ms.openlocfilehash: 9fdbf6f7cd88774c2d14d079201993f6a324ace5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748116"
---
# <span data-ttu-id="3102b-101">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="3102b-101">New-AzApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="3102b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3102b-102">SYNOPSIS</span></span>
<span data-ttu-id="3102b-103">Skapar en Rewrite-regel för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="3102b-103">Creates a rewrite rule for an application gateway.</span></span>

## <span data-ttu-id="3102b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3102b-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRule -Name <String> -ActionSet <PSApplicationGatewayRewriteRuleActionSet>
 [-RuleSequence <Int32>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3102b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3102b-105">DESCRIPTION</span></span>
<span data-ttu-id="3102b-106">Cmdleten **New-AzApplicationGatewayRewriteRule** skapar en ny Skriv regel för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="3102b-106">**The New-AzApplicationGatewayRewriteRule** cmdlet creates a rewrite rule for an Azure application gateway.</span></span>

## <span data-ttu-id="3102b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3102b-107">EXAMPLES</span></span>

### <span data-ttu-id="3102b-108">Exempel 1: skapa en Rewrite-regel för en Programgateway</span><span class="sxs-lookup"><span data-stu-id="3102b-108">Example 1 : Create a rewrite rule for an application gateway</span></span>
```powershell
PS C:\> $rule = New-AzApplicationGatewayRewriteRule -Name rule1 -ActionSet $action -RuleSequence 101 -Condition $condition
```

<span data-ttu-id="3102b-109">Det här kommandot skapar en omskrivnings regel med namnet rule1 och lagrar resultatet i variabeln som heter $rule.</span><span class="sxs-lookup"><span data-stu-id="3102b-109">This command creates a rewrite rule named rule1 and stores the result in the variable named $rule.</span></span>

## <span data-ttu-id="3102b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3102b-110">PARAMETERS</span></span>

### <span data-ttu-id="3102b-111">-ActionSet</span><span class="sxs-lookup"><span data-stu-id="3102b-111">-ActionSet</span></span>
<span data-ttu-id="3102b-112">ActionSet av den omskrivna regeln</span><span class="sxs-lookup"><span data-stu-id="3102b-112">ActionSet of the rewrite rule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3102b-113">-Villkor</span><span class="sxs-lookup"><span data-stu-id="3102b-113">-Condition</span></span>
<span data-ttu-id="3102b-114">Villkor för att den omanvändade regeln ska utföras</span><span class="sxs-lookup"><span data-stu-id="3102b-114">Condition for the rewrite rule to execute</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3102b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3102b-115">-DefaultProfile</span></span>
<span data-ttu-id="3102b-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3102b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3102b-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="3102b-117">-Name</span></span>
<span data-ttu-id="3102b-118">Namnet på RewriteRule</span><span class="sxs-lookup"><span data-stu-id="3102b-118">The name of the RewriteRule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3102b-119">-RuleSequence</span><span class="sxs-lookup"><span data-stu-id="3102b-119">-RuleSequence</span></span>
<span data-ttu-id="3102b-120">Regel ordningen för den här omskrivning-regeln i regeln för att skriva om</span><span class="sxs-lookup"><span data-stu-id="3102b-120">The rule ordering of this rewrite rule in the rewrite rule set</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3102b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3102b-121">CommonParameters</span></span>
<span data-ttu-id="3102b-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3102b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3102b-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3102b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3102b-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3102b-124">INPUTS</span></span>

### <span data-ttu-id="3102b-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="3102b-125">None</span></span>

## <span data-ttu-id="3102b-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3102b-126">OUTPUTS</span></span>

### <span data-ttu-id="3102b-127">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="3102b-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="3102b-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3102b-128">NOTES</span></span>

## <span data-ttu-id="3102b-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3102b-129">RELATED LINKS</span></span>

[<span data-ttu-id="3102b-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3102b-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3102b-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3102b-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3102b-132">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3102b-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3102b-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3102b-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3102b-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3102b-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3102b-135">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="3102b-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="3102b-136">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="3102b-136">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)