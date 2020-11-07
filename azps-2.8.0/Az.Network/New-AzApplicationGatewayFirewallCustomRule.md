---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallcustomrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCustomRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCustomRule.md
ms.openlocfilehash: 1f8e165d8353c046749bd2ea0eb749a75fb2d6c7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918675"
---
# <span data-ttu-id="efc39-101">New-AzApplicationGatewayFirewallCustomRule</span><span class="sxs-lookup"><span data-stu-id="efc39-101">New-AzApplicationGatewayFirewallCustomRule</span></span>

## <span data-ttu-id="efc39-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="efc39-102">SYNOPSIS</span></span>
<span data-ttu-id="efc39-103">Skapar en ny anpassad regel för brand Väggs principen för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="efc39-103">Creates a new custom rule for the application gateway firewall policy.</span></span>

## <span data-ttu-id="efc39-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="efc39-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCustomRule -Name <String> -Priority <Int32> -RuleType <String>
 -MatchCondition <PSApplicationGatewayFirewallCondition[]> -Action <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efc39-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="efc39-105">DESCRIPTION</span></span>
<span data-ttu-id="efc39-106">**New-AzApplicationGatewayFirewallCustomRule** skapar en anpassad regel för brand Väggs princip.</span><span class="sxs-lookup"><span data-stu-id="efc39-106">The **New-AzApplicationGatewayFirewallCustomRule** creates a custom rule for firewall policy.</span></span>

## <span data-ttu-id="efc39-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="efc39-107">EXAMPLES</span></span>

### <span data-ttu-id="efc39-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="efc39-108">Example 1</span></span>
```powershell
PS C:\> $customRule = New-AzApplicationGatewayFirewallCustomRule -Name example-rule -Priority 1 -RuleType MatchRule -matchConditons $condtion -Action Allow
```

<span data-ttu-id="efc39-109">Kommandot skapar en ny anpassad regel med namnet på exempel regel, prioritet 1 och regel typen MatchRule med villkor som definieras i variabeln condition och åtgärden Tillåt.</span><span class="sxs-lookup"><span data-stu-id="efc39-109">The command creates a new custom rule with name of example-rule, priority 1 and the rule type will be MatchRule with condition defined in the condition variable, the action will the allow.</span></span> <span data-ttu-id="efc39-110">Den nya anpassade regeln sparas i $customRule.</span><span class="sxs-lookup"><span data-stu-id="efc39-110">The new match custom rule is saved in $customRule.</span></span>

## <span data-ttu-id="efc39-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="efc39-111">PARAMETERS</span></span>

### <span data-ttu-id="efc39-112">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="efc39-112">-Action</span></span>
<span data-ttu-id="efc39-113">Typ av åtgärder.</span><span class="sxs-lookup"><span data-stu-id="efc39-113">Type of Actions.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efc39-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efc39-114">-DefaultProfile</span></span>
<span data-ttu-id="efc39-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="efc39-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efc39-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="efc39-116">-MatchCondition</span></span>
<span data-ttu-id="efc39-117">Lista över matchnings villkor.</span><span class="sxs-lookup"><span data-stu-id="efc39-117">List of match conditions.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efc39-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="efc39-118">-Name</span></span>
<span data-ttu-id="efc39-119">Namnet på regeln.</span><span class="sxs-lookup"><span data-stu-id="efc39-119">The Name of the Rule.</span></span>

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

### <span data-ttu-id="efc39-120">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="efc39-120">-Priority</span></span>
<span data-ttu-id="efc39-121">Beskriver prioriteten för regeln.</span><span class="sxs-lookup"><span data-stu-id="efc39-121">Describes priority of the rule.</span></span>
<span data-ttu-id="efc39-122">Regler med lägre värde utvärderas före regler med högre värde.</span><span class="sxs-lookup"><span data-stu-id="efc39-122">Rules with a lower value will be evaluated before rules with a higher value.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efc39-123">-RuleType</span><span class="sxs-lookup"><span data-stu-id="efc39-123">-RuleType</span></span>
<span data-ttu-id="efc39-124">Beskriver regel typen.</span><span class="sxs-lookup"><span data-stu-id="efc39-124">Describes type of rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MatchRule

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efc39-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efc39-125">CommonParameters</span></span>
<span data-ttu-id="efc39-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efc39-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efc39-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efc39-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efc39-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="efc39-128">INPUTS</span></span>

### <span data-ttu-id="efc39-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="efc39-129">None</span></span>

## <span data-ttu-id="efc39-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="efc39-130">OUTPUTS</span></span>

### <span data-ttu-id="efc39-131">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayFirewallCustomRule</span><span class="sxs-lookup"><span data-stu-id="efc39-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule</span></span>

## <span data-ttu-id="efc39-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="efc39-132">NOTES</span></span>

## <span data-ttu-id="efc39-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="efc39-133">RELATED LINKS</span></span>
