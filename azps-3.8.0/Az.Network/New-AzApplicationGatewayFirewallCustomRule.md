---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallcustomrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCustomRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCustomRule.md
ms.openlocfilehash: d8e22f5eb0e504757bd94fa5235d07ad3e3db998
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092556"
---
# <span data-ttu-id="59abd-101">New-AzApplicationGatewayFirewallCustomRule</span><span class="sxs-lookup"><span data-stu-id="59abd-101">New-AzApplicationGatewayFirewallCustomRule</span></span>

## <span data-ttu-id="59abd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="59abd-102">SYNOPSIS</span></span>
<span data-ttu-id="59abd-103">Skapar en ny anpassad regel för brand Väggs principen för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="59abd-103">Creates a new custom rule for the application gateway firewall policy.</span></span>

## <span data-ttu-id="59abd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="59abd-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCustomRule -Name <String> -Priority <Int32> -RuleType <String>
 -MatchCondition <PSApplicationGatewayFirewallCondition[]> -Action <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59abd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="59abd-105">DESCRIPTION</span></span>
<span data-ttu-id="59abd-106">**New-AzApplicationGatewayFirewallCustomRule** skapar en anpassad regel för brand Väggs princip.</span><span class="sxs-lookup"><span data-stu-id="59abd-106">The **New-AzApplicationGatewayFirewallCustomRule** creates a custom rule for firewall policy.</span></span>

## <span data-ttu-id="59abd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="59abd-107">EXAMPLES</span></span>

### <span data-ttu-id="59abd-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="59abd-108">Example 1</span></span>
```powershell
PS C:\> $customRule = New-AzApplicationGatewayFirewallCustomRule -Name example-rule -Priority 1 -RuleType MatchRule -matchConditons $condtion -Action Allow
```

<span data-ttu-id="59abd-109">Kommandot skapar en ny anpassad regel med namnet på exempel regel, prioritet 1 och regel typen MatchRule med villkor som definieras i variabeln condition och åtgärden Tillåt.</span><span class="sxs-lookup"><span data-stu-id="59abd-109">The command creates a new custom rule with name of example-rule, priority 1 and the rule type will be MatchRule with condition defined in the condition variable, the action will the allow.</span></span> <span data-ttu-id="59abd-110">Den nya anpassade regeln sparas i $customRule.</span><span class="sxs-lookup"><span data-stu-id="59abd-110">The new match custom rule is saved in $customRule.</span></span>

## <span data-ttu-id="59abd-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="59abd-111">PARAMETERS</span></span>

### <span data-ttu-id="59abd-112">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="59abd-112">-Action</span></span>
<span data-ttu-id="59abd-113">Typ av åtgärder.</span><span class="sxs-lookup"><span data-stu-id="59abd-113">Type of Actions.</span></span>

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

### <span data-ttu-id="59abd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59abd-114">-DefaultProfile</span></span>
<span data-ttu-id="59abd-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="59abd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59abd-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="59abd-116">-MatchCondition</span></span>
<span data-ttu-id="59abd-117">Lista över matchnings villkor.</span><span class="sxs-lookup"><span data-stu-id="59abd-117">List of match conditions.</span></span>

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

### <span data-ttu-id="59abd-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="59abd-118">-Name</span></span>
<span data-ttu-id="59abd-119">Namnet på regeln.</span><span class="sxs-lookup"><span data-stu-id="59abd-119">The Name of the Rule.</span></span>

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

### <span data-ttu-id="59abd-120">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="59abd-120">-Priority</span></span>
<span data-ttu-id="59abd-121">Beskriver prioriteten för regeln.</span><span class="sxs-lookup"><span data-stu-id="59abd-121">Describes priority of the rule.</span></span>
<span data-ttu-id="59abd-122">Regler med lägre värde utvärderas före regler med högre värde.</span><span class="sxs-lookup"><span data-stu-id="59abd-122">Rules with a lower value will be evaluated before rules with a higher value.</span></span>

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

### <span data-ttu-id="59abd-123">-RuleType</span><span class="sxs-lookup"><span data-stu-id="59abd-123">-RuleType</span></span>
<span data-ttu-id="59abd-124">Beskriver regel typen.</span><span class="sxs-lookup"><span data-stu-id="59abd-124">Describes type of rule.</span></span>

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

### <span data-ttu-id="59abd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59abd-125">CommonParameters</span></span>
<span data-ttu-id="59abd-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59abd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59abd-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59abd-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59abd-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="59abd-128">INPUTS</span></span>

### <span data-ttu-id="59abd-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="59abd-129">None</span></span>

## <span data-ttu-id="59abd-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="59abd-130">OUTPUTS</span></span>

### <span data-ttu-id="59abd-131">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayFirewallCustomRule</span><span class="sxs-lookup"><span data-stu-id="59abd-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule</span></span>

## <span data-ttu-id="59abd-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="59abd-132">NOTES</span></span>

## <span data-ttu-id="59abd-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="59abd-133">RELATED LINKS</span></span>