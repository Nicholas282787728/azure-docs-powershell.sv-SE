---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
ms.openlocfilehash: a3e057b8fbf6b04f48936b2aa96e9696964e5061
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102710"
---
# <span data-ttu-id="350bc-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="350bc-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="350bc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="350bc-102">SYNOPSIS</span></span>
<span data-ttu-id="350bc-103">Skapar en managedRuleOverride-post för RuleGroupOverrideGroup-posten.</span><span class="sxs-lookup"><span data-stu-id="350bc-103">Creates a managedRuleOverride entry for RuleGroupOverrideGroup entry.</span></span>

## <span data-ttu-id="350bc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="350bc-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId <String> [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="350bc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="350bc-105">DESCRIPTION</span></span>
<span data-ttu-id="350bc-106">Den **nya-AzApplicationGatewayFirewallPolicyManagedRuleOverride** skapar en ruleOverride-post.</span><span class="sxs-lookup"><span data-stu-id="350bc-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleOverride** creates a ruleOverride entry.</span></span>

## <span data-ttu-id="350bc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="350bc-107">EXAMPLES</span></span>

### <span data-ttu-id="350bc-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="350bc-108">Example 1</span></span>
```powershell
PS C:\> ruleOverrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId $ruleId -State Disabled
```

<span data-ttu-id="350bc-109">Skapar en ruleOverride-post med RuleId som $ruleId och State som inaktive rad.</span><span class="sxs-lookup"><span data-stu-id="350bc-109">Creates a ruleOverride Entry with RuleId as $ruleId and State as Disabled.</span></span>

## <span data-ttu-id="350bc-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="350bc-110">PARAMETERS</span></span>

### <span data-ttu-id="350bc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="350bc-111">-DefaultProfile</span></span>
<span data-ttu-id="350bc-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="350bc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="350bc-113">-RuleId</span><span class="sxs-lookup"><span data-stu-id="350bc-113">-RuleId</span></span>
<span data-ttu-id="350bc-114">Ange RuleId i princip posten Åsidosätt.</span><span class="sxs-lookup"><span data-stu-id="350bc-114">Specify the RuleId in override rule entry.</span></span>

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

### <span data-ttu-id="350bc-115">-State</span><span class="sxs-lookup"><span data-stu-id="350bc-115">-State</span></span>
<span data-ttu-id="350bc-116">Ange RuleId i princip posten Åsidosätt.</span><span class="sxs-lookup"><span data-stu-id="350bc-116">Specify the RuleId in override rule entry.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Disabled

Required: False
Position: Named
Default value: Disabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="350bc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="350bc-117">CommonParameters</span></span>
<span data-ttu-id="350bc-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="350bc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="350bc-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="350bc-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="350bc-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="350bc-120">INPUTS</span></span>

### <span data-ttu-id="350bc-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="350bc-121">None</span></span>

## <span data-ttu-id="350bc-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="350bc-122">OUTPUTS</span></span>

### <span data-ttu-id="350bc-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="350bc-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="350bc-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="350bc-124">NOTES</span></span>

## <span data-ttu-id="350bc-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="350bc-125">RELATED LINKS</span></span>
