---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1FDA90C0-D01F-45E1-9149-16AD04046271
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: e28ebc04277e3c9031c9c287aa02f7eea32867a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918745"
---
# <span data-ttu-id="90cec-101">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="90cec-101">Get-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="90cec-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="90cec-102">SYNOPSIS</span></span>
<span data-ttu-id="90cec-103">Hämtar en inkommande NAT-regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="90cec-103">Gets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="90cec-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="90cec-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90cec-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="90cec-105">DESCRIPTION</span></span>
<span data-ttu-id="90cec-106">Cmdleten **Get-AzLoadBalancerInboundNatRuleConfig** får en eller flera inkommande NAT-regler (Network Address Translation) i en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="90cec-106">The **Get-AzLoadBalancerInboundNatRuleConfig** cmdlet gets one or more inbound network address translation (NAT) rules in an Azure load balancer.</span></span>

## <span data-ttu-id="90cec-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="90cec-107">EXAMPLES</span></span>

### <span data-ttu-id="90cec-108">Exempel 1: skaffa en inkommande NAT-regel</span><span class="sxs-lookup"><span data-stu-id="90cec-108">Example 1: Get an inbound NAT rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule1" -LoadBalancer $slb
```

<span data-ttu-id="90cec-109">Det första kommandot får belastningsutjämnaren med namnet MyLoadBalancer och lagrar det i variabeln $slb.</span><span class="sxs-lookup"><span data-stu-id="90cec-109">The first command gets the load balancer named MyLoadBalancer, and stores it in the variable $slb.</span></span>
<span data-ttu-id="90cec-110">Det andra kommandot hämtar den associerade NAT-regeln med namnet MyInboundNatRule1 från belastningsutjämnaren i $slb.</span><span class="sxs-lookup"><span data-stu-id="90cec-110">The second command gets the associated NAT rule named MyInboundNatRule1 from the load balancer in $slb.</span></span>

## <span data-ttu-id="90cec-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="90cec-111">PARAMETERS</span></span>

### <span data-ttu-id="90cec-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90cec-112">-DefaultProfile</span></span>
<span data-ttu-id="90cec-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="90cec-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90cec-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="90cec-114">-LoadBalancer</span></span>
<span data-ttu-id="90cec-115">Anger den belastnings utjämning som är kopplad till den inkommande NAT-regelns konfiguration för att få.</span><span class="sxs-lookup"><span data-stu-id="90cec-115">Specifies the load balancer that is associated with the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="90cec-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="90cec-116">-Name</span></span>
<span data-ttu-id="90cec-117">Anger namnet på den inkommande NAT-regelns konfiguration för att få.</span><span class="sxs-lookup"><span data-stu-id="90cec-117">Specifies the name of the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="90cec-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90cec-118">CommonParameters</span></span>
<span data-ttu-id="90cec-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90cec-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90cec-120">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90cec-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90cec-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="90cec-121">INPUTS</span></span>

### <span data-ttu-id="90cec-122">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="90cec-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="90cec-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="90cec-123">OUTPUTS</span></span>

### <span data-ttu-id="90cec-124">Microsoft. Azure. commands. Networks. Models. PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="90cec-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="90cec-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="90cec-125">NOTES</span></span>

## <span data-ttu-id="90cec-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="90cec-126">RELATED LINKS</span></span>

[<span data-ttu-id="90cec-127">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="90cec-127">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="90cec-128">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="90cec-128">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="90cec-129">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="90cec-129">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="90cec-130">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="90cec-130">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)

