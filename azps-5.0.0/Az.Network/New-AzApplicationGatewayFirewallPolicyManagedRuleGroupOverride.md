---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrulegroupoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
ms.openlocfilehash: 81b09a392464a004030a0798ea211db08a60a9f4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269429"
---
# <span data-ttu-id="c0f83-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="c0f83-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="c0f83-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c0f83-102">SYNOPSIS</span></span>
<span data-ttu-id="c0f83-103">Skapar RuleGroupOverride-post i ManagedRuleSets för brand Väggs principen.</span><span class="sxs-lookup"><span data-stu-id="c0f83-103">Creates RuleGroupOverride entry in ManagedRuleSets for the firewall policy.</span></span>

## <span data-ttu-id="c0f83-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c0f83-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName <String>
 -Rule <PSApplicationGatewayFirewallPolicyManagedRuleOverride[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0f83-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c0f83-105">DESCRIPTION</span></span>
<span data-ttu-id="c0f83-106">**New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** skapar en ruleGroupOverride-post i en managedRuleSet för en brand Väggs princip.</span><span class="sxs-lookup"><span data-stu-id="c0f83-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** creates a ruleGroupOverride entry in a managedRuleSet for a firewall policy.</span></span>

## <span data-ttu-id="c0f83-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c0f83-107">EXAMPLES</span></span>

### <span data-ttu-id="c0f83-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c0f83-108">Example 1</span></span>
```powershell
PS C:\> $overrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName $ruleName -Rules $rule1,$rule2
```

<span data-ttu-id="c0f83-109">Skapar en RuleGroupOverride-post med grupp namnet som $ruleName och regler som $rule 1, $rule 2.</span><span class="sxs-lookup"><span data-stu-id="c0f83-109">Creates a RuleGroupOverride entry with group name as $ruleName and Rules as $rule1, $rule2.</span></span> <span data-ttu-id="c0f83-110">Tilldelar samma $overrideEntry</span><span class="sxs-lookup"><span data-stu-id="c0f83-110">Assigns the same to $overrideEntry</span></span>

## <span data-ttu-id="c0f83-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c0f83-111">PARAMETERS</span></span>

### <span data-ttu-id="c0f83-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0f83-112">-DefaultProfile</span></span>
<span data-ttu-id="c0f83-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c0f83-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0f83-114">-Regel</span><span class="sxs-lookup"><span data-stu-id="c0f83-114">-Rule</span></span>
<span data-ttu-id="c0f83-115">Lista med regler.</span><span class="sxs-lookup"><span data-stu-id="c0f83-115">List of Rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0f83-116">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="c0f83-116">-RuleGroupName</span></span>
<span data-ttu-id="c0f83-117">Ange ruleGroupName i en åsidosättning RuleGroup-post.</span><span class="sxs-lookup"><span data-stu-id="c0f83-117">Specify the ruleGroupName in a override RuleGroup entry.</span></span>

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

### <span data-ttu-id="c0f83-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0f83-118">CommonParameters</span></span>
<span data-ttu-id="c0f83-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0f83-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0f83-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0f83-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0f83-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c0f83-121">INPUTS</span></span>

### <span data-ttu-id="c0f83-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="c0f83-122">None</span></span>

## <span data-ttu-id="c0f83-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c0f83-123">OUTPUTS</span></span>

### <span data-ttu-id="c0f83-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="c0f83-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="c0f83-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c0f83-125">NOTES</span></span>

## <span data-ttu-id="c0f83-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c0f83-126">RELATED LINKS</span></span>
