---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2CF11FC-520C-4C14-9A1B-13F06B250B5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 87329e4864e4fd91d1a8aec09183fe02d8c498ff
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091053"
---
# <span data-ttu-id="7eef1-101">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7eef1-101">Get-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="7eef1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7eef1-102">SYNOPSIS</span></span>
<span data-ttu-id="7eef1-103">Hämtar regel konfigurationen för en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="7eef1-103">Gets the rule configuration for a load balancer.</span></span>

## <span data-ttu-id="7eef1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7eef1-104">SYNTAX</span></span>

```
Get-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7eef1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7eef1-105">DESCRIPTION</span></span>
<span data-ttu-id="7eef1-106">Cmdleten **Get-AzLoadBalancerRuleConfig** hämtar en eller flera regler för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="7eef1-106">The **Get-AzLoadBalancerRuleConfig** cmdlet gets one or more rule configurations for a load balancer.</span></span>

## <span data-ttu-id="7eef1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7eef1-107">EXAMPLES</span></span>

### <span data-ttu-id="7eef1-108">Exempel 1: Hämta regel konfigurationen för en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="7eef1-108">Example 1: Get the rule configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerRuleConfig -Name "MyLBrulename" -LoadBalancer $slb
```

<span data-ttu-id="7eef1-109">Det första kommandot får belastningsutjämnaren med namnet MyLoadBalancer och lagrar det sedan i variabeln $slb.</span><span class="sxs-lookup"><span data-stu-id="7eef1-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="7eef1-110">Det andra kommandot hämtar den associerade regel konfigurationen med namnet MyLBrulename från belastningsutjämnaren i $slb.</span><span class="sxs-lookup"><span data-stu-id="7eef1-110">The second command gets the associated rule configuration named MyLBrulename from the load balancer in $slb.</span></span>

## <span data-ttu-id="7eef1-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7eef1-111">PARAMETERS</span></span>

### <span data-ttu-id="7eef1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eef1-112">-DefaultProfile</span></span>
<span data-ttu-id="7eef1-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7eef1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7eef1-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7eef1-114">-LoadBalancer</span></span>
<span data-ttu-id="7eef1-115">Anger den belastningsutjämnare som är associerad med den regel konfiguration som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="7eef1-115">Specifies the load balancer that is associated with the rule configuration to get.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7eef1-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="7eef1-116">-Name</span></span>
<span data-ttu-id="7eef1-117">Anger namnet på den regel konfiguration som ska visas.</span><span class="sxs-lookup"><span data-stu-id="7eef1-117">Specifies the name of the rule configuration to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eef1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eef1-118">CommonParameters</span></span>
<span data-ttu-id="7eef1-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7eef1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eef1-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7eef1-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eef1-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7eef1-121">INPUTS</span></span>

### <span data-ttu-id="7eef1-122">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7eef1-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="7eef1-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7eef1-123">OUTPUTS</span></span>

### <span data-ttu-id="7eef1-124">Microsoft. Azure. commands. Networks. Models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="7eef1-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="7eef1-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7eef1-125">NOTES</span></span>

## <span data-ttu-id="7eef1-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7eef1-126">RELATED LINKS</span></span>

[<span data-ttu-id="7eef1-127">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7eef1-127">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="7eef1-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7eef1-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="7eef1-129">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7eef1-129">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="7eef1-130">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7eef1-130">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)

