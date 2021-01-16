---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
ms.openlocfilehash: 3f4faec6b2af39f3386ec39e7df2e5bebcfe4277
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402163"
---
# <span data-ttu-id="06752-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="06752-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="06752-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="06752-102">SYNOPSIS</span></span>
<span data-ttu-id="06752-103">Skapar en ManagedRuleSet för firewallPolicy</span><span class="sxs-lookup"><span data-stu-id="06752-103">Creates a ManagedRuleSet for the firewallPolicy</span></span>

## <span data-ttu-id="06752-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="06752-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType <String> -RuleSetVersion <String>
 [-RuleGroupOverride <PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06752-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="06752-105">DESCRIPTION</span></span>
<span data-ttu-id="06752-106">Den **nya-AzApplicationGatewayFirewallPolicyManagedRuleSet** skapar ett hanterat-regler för en brand Väggs princip.</span><span class="sxs-lookup"><span data-stu-id="06752-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleSet** creates a managed-rules for a firewall policy.</span></span>

## <span data-ttu-id="06752-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="06752-107">EXAMPLES</span></span>

### <span data-ttu-id="06752-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="06752-108">Example 1</span></span>
```powershell
PS C:\> $managedRuleSet = New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType $ruleSetType 
-RuleSetVersion $ruleSetVersion -RuleGroupOverrides $ruleGroupOverride1, $ruleGroupOverride2
```

<span data-ttu-id="06752-109">Skapar en ManagedRuleSet med ruleSetType som $ruleSetType, ruleSetVersion som $ruleSetVersion och RuleGroupOverrides som en lista med hela $ruleGroupOverride 1 $ruleGroupOverride 2 den nya ManagedRuleSet tilldelas till $managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="06752-109">Creates a ManagedRuleSet with ruleSetType as $ruleSetType, ruleSetVersion as $ruleSetVersion and RuleGroupOverrides as a list with entires as $ruleGroupOverride1, $ruleGroupOverride2 The new ManagedRuleSet is assigned to $managedRuleSet</span></span>

## <span data-ttu-id="06752-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="06752-110">PARAMETERS</span></span>

### <span data-ttu-id="06752-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06752-111">-DefaultProfile</span></span>
<span data-ttu-id="06752-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="06752-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06752-113">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="06752-113">-RuleGroupOverride</span></span>
<span data-ttu-id="06752-114">Åsidosättningar för regel grupp.</span><span class="sxs-lookup"><span data-stu-id="06752-114">Rule Group Overrides.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06752-115">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="06752-115">-RuleSetType</span></span>
<span data-ttu-id="06752-116">Ange RuleSetType i en managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="06752-116">Specify the RuleSetType in a managedRuleSet</span></span>

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

### <span data-ttu-id="06752-117">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="06752-117">-RuleSetVersion</span></span>
<span data-ttu-id="06752-118">Ange RuleSetVersion i en managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="06752-118">Specify the RuleSetVersion in a managedRuleSet</span></span>

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

### <span data-ttu-id="06752-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06752-119">CommonParameters</span></span>
<span data-ttu-id="06752-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06752-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06752-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06752-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06752-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="06752-122">INPUTS</span></span>

### <span data-ttu-id="06752-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="06752-123">None</span></span>

## <span data-ttu-id="06752-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="06752-124">OUTPUTS</span></span>

### <span data-ttu-id="06752-125">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="06752-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="06752-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="06752-126">NOTES</span></span>

## <span data-ttu-id="06752-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="06752-127">RELATED LINKS</span></span>
