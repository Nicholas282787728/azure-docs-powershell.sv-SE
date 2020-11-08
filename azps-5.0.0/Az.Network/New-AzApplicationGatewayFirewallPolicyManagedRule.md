---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRule.md
ms.openlocfilehash: 6b709283024a37d85bfac89f7e2fec4448544729
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94262983"
---
# <span data-ttu-id="eb11d-101">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="eb11d-101">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>

## <span data-ttu-id="eb11d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eb11d-102">SYNOPSIS</span></span>
<span data-ttu-id="eb11d-103">Skapa ManagedRules för brand Väggs principen.</span><span class="sxs-lookup"><span data-stu-id="eb11d-103">Create ManagedRules for the firewall policy.</span></span>

## <span data-ttu-id="eb11d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eb11d-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRule
 [-ManagedRuleSet <PSApplicationGatewayFirewallPolicyManagedRuleSet[]>]
 [-Exclusion <PSApplicationGatewayFirewallPolicyExclusion[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb11d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eb11d-105">DESCRIPTION</span></span>
<span data-ttu-id="eb11d-106">Den **nya-AzApplicationGatewayFirewallPolicyManagedRule** skapar ett hanterat-regler för en brand Väggs princip.</span><span class="sxs-lookup"><span data-stu-id="eb11d-106">The **New-AzApplicationGatewayFirewallPolicyManagedRule** creates a managed-rules for a firewall policy.</span></span>

## <span data-ttu-id="eb11d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eb11d-107">EXAMPLES</span></span>

### <span data-ttu-id="eb11d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="eb11d-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallPolicyManagedRule -ManagedRuleSet $managedRuleSet -Exclusion $exclusion1,$exclusion2
```

<span data-ttu-id="eb11d-109">Kommandot skapar hanterade regler en lista med ManagedRuleSet med $managedRuleSet och en undantags lista med poster som $exclusion 1, $exclusion 2.</span><span class="sxs-lookup"><span data-stu-id="eb11d-109">The command creates managed rules a list of ManagedRuleSet with $managedRuleSet and an exclusion list with entries as $exclusion1, $exclusion2.</span></span>

## <span data-ttu-id="eb11d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eb11d-110">PARAMETERS</span></span>

### <span data-ttu-id="eb11d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb11d-111">-DefaultProfile</span></span>
<span data-ttu-id="eb11d-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eb11d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb11d-113">-Uteslutning</span><span class="sxs-lookup"><span data-stu-id="eb11d-113">-Exclusion</span></span>
<span data-ttu-id="eb11d-114">Lista över undantags post.</span><span class="sxs-lookup"><span data-stu-id="eb11d-114">List of Exclusion Entry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExclusion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb11d-115">-ManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="eb11d-115">-ManagedRuleSet</span></span>
<span data-ttu-id="eb11d-116">Lista över hanterade ruleSets.</span><span class="sxs-lookup"><span data-stu-id="eb11d-116">List of Managed ruleSets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleSet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb11d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb11d-117">CommonParameters</span></span>
<span data-ttu-id="eb11d-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb11d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb11d-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eb11d-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb11d-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eb11d-120">INPUTS</span></span>

### <span data-ttu-id="eb11d-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="eb11d-121">None</span></span>

## <span data-ttu-id="eb11d-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eb11d-122">OUTPUTS</span></span>

### <span data-ttu-id="eb11d-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayFirewallPolicyManagedRules</span><span class="sxs-lookup"><span data-stu-id="eb11d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span></span>

## <span data-ttu-id="eb11d-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eb11d-124">NOTES</span></span>

## <span data-ttu-id="eb11d-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eb11d-125">RELATED LINKS</span></span>
