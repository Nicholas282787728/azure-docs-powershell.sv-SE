---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1FDA90C0-D01F-45E1-9149-16AD04046271
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
ms.openlocfilehash: fbfa70146a5eb70d118e6cd1859f968c576d8a0f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931309"
---
# <span data-ttu-id="b93ca-101">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b93ca-101">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="b93ca-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b93ca-102">SYNOPSIS</span></span>
<span data-ttu-id="b93ca-103">Hämtar en inkommande NAT-regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="b93ca-103">Gets an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b93ca-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b93ca-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerInboundNatRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b93ca-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b93ca-105">DESCRIPTION</span></span>
<span data-ttu-id="b93ca-106">Cmdleten **Get-AzureRmLoadBalancerInboundNatRuleConfig** får en eller flera inkommande NAT-regler (Network Address Translation) i en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="b93ca-106">The **Get-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet gets one or more inbound network address translation (NAT) rules in an Azure load balancer.</span></span>

## <span data-ttu-id="b93ca-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b93ca-107">EXAMPLES</span></span>

### <span data-ttu-id="b93ca-108">Exempel 1: skaffa en inkommande NAT-regel</span><span class="sxs-lookup"><span data-stu-id="b93ca-108">Example 1: Get an inbound NAT rule configuration</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule1" -LoadBalancer $slb
```

<span data-ttu-id="b93ca-109">Det första kommandot får belastningsutjämnaren med namnet MyLoadBalancer och lagrar det i variabeln $slb.</span><span class="sxs-lookup"><span data-stu-id="b93ca-109">The first command gets the load balancer named MyLoadBalancer, and stores it in the variable $slb.</span></span>

<span data-ttu-id="b93ca-110">Det andra kommandot hämtar den associerade NAT-regeln med namnet MyInboundNatRule1 från belastningsutjämnaren i $slb.</span><span class="sxs-lookup"><span data-stu-id="b93ca-110">The second command gets the associated NAT rule named MyInboundNatRule1 from the load balancer in $slb.</span></span>

## <span data-ttu-id="b93ca-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b93ca-111">PARAMETERS</span></span>

### <span data-ttu-id="b93ca-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b93ca-112">-DefaultProfile</span></span>
<span data-ttu-id="b93ca-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b93ca-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b93ca-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b93ca-114">-LoadBalancer</span></span>
<span data-ttu-id="b93ca-115">Anger den belastnings utjämning som är kopplad till den inkommande NAT-regelns konfiguration för att få.</span><span class="sxs-lookup"><span data-stu-id="b93ca-115">Specifies the load balancer that is associated with the inbound NAT rule configuration to get.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b93ca-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="b93ca-116">-Name</span></span>
<span data-ttu-id="b93ca-117">Anger namnet på den inkommande NAT-regelns konfiguration för att få.</span><span class="sxs-lookup"><span data-stu-id="b93ca-117">Specifies the name of the inbound NAT rule configuration to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b93ca-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b93ca-118">CommonParameters</span></span>
<span data-ttu-id="b93ca-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b93ca-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b93ca-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b93ca-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b93ca-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b93ca-121">INPUTS</span></span>

### <span data-ttu-id="b93ca-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b93ca-122">PSLoadBalancer</span></span>
<span data-ttu-id="b93ca-123">Parametern ' LoadBalancer ' godkänner värdet av typen ' PSLoadBalancer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="b93ca-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="b93ca-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b93ca-124">OUTPUTS</span></span>

### <span data-ttu-id="b93ca-125">Microsoft. Azure. commands. Networks. Models. PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="b93ca-125">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="b93ca-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b93ca-126">NOTES</span></span>

## <span data-ttu-id="b93ca-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b93ca-127">RELATED LINKS</span></span>

[<span data-ttu-id="b93ca-128">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b93ca-128">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="b93ca-129">New-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b93ca-129">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="b93ca-130">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b93ca-130">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="b93ca-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b93ca-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


