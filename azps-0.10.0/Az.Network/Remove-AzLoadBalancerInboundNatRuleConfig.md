---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: b135f9a54c084eb7bc5dc4562e16c67e316f8736
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922030"
---
# <span data-ttu-id="9a0d9-101">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9a0d9-101">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="9a0d9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9a0d9-102">SYNOPSIS</span></span>
<span data-ttu-id="9a0d9-103">Tar bort en inkommande NAT-regel från en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="9a0d9-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

## <span data-ttu-id="9a0d9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9a0d9-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a0d9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9a0d9-105">DESCRIPTION</span></span>
<span data-ttu-id="9a0d9-106">Cmdleten **Remove-AzLoadBalancerInboundNatRuleConfig** tar bort en inkommande NAT-regel (Network Address Translation) från en Azure belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="9a0d9-106">The **Remove-AzLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="9a0d9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9a0d9-107">EXAMPLES</span></span>

### <span data-ttu-id="9a0d9-108">1: ta bort en inkommande NAT-regel från en Azure-belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="9a0d9-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="9a0d9-109">Det första kommandot läser in en redan befintlig belastningsutjämnare som heter "mylb" och lagrar den i variabel $load-saldo.</span><span class="sxs-lookup"><span data-stu-id="9a0d9-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="9a0d9-110">Det andra kommandot tar bort den inkommande NAT-regeln som är kopplad till den här belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="9a0d9-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="9a0d9-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9a0d9-111">PARAMETERS</span></span>

### <span data-ttu-id="9a0d9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a0d9-112">-DefaultProfile</span></span>
<span data-ttu-id="9a0d9-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9a0d9-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a0d9-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9a0d9-114">-LoadBalancer</span></span>
<span data-ttu-id="9a0d9-115">Anger det **Loadbalancer** -objekt som innehåller den inkommande NAT-regelns konfiguration som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="9a0d9-115">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9a0d9-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="9a0d9-116">-Name</span></span>
<span data-ttu-id="9a0d9-117">Anger namnet på den inkommande NAT-regelns konfiguration som tas bort med denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a0d9-117">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9a0d9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a0d9-118">CommonParameters</span></span>
<span data-ttu-id="9a0d9-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a0d9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a0d9-120">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a0d9-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a0d9-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9a0d9-121">INPUTS</span></span>

### <span data-ttu-id="9a0d9-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9a0d9-122">PSLoadBalancer</span></span>
<span data-ttu-id="9a0d9-123">Parametern ' LoadBalancer ' godkänner värdet av typen ' PSLoadBalancer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="9a0d9-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="9a0d9-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9a0d9-124">OUTPUTS</span></span>

### <span data-ttu-id="9a0d9-125">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9a0d9-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="9a0d9-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9a0d9-126">NOTES</span></span>

## <span data-ttu-id="9a0d9-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9a0d9-127">RELATED LINKS</span></span>

[<span data-ttu-id="9a0d9-128">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9a0d9-128">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="9a0d9-129">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9a0d9-129">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="9a0d9-130">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9a0d9-130">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="9a0d9-131">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9a0d9-131">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


