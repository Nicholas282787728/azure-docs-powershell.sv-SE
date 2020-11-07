---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
ms.openlocfilehash: 2af05b60498fc83b74c00701794dba7f1b59e6a6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931214"
---
# <span data-ttu-id="08db2-101">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="08db2-101">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="08db2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="08db2-102">SYNOPSIS</span></span>
<span data-ttu-id="08db2-103">Tar bort en inkommande NAT-regel från en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="08db2-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08db2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="08db2-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerInboundNatRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08db2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="08db2-105">DESCRIPTION</span></span>
<span data-ttu-id="08db2-106">Cmdleten **Remove-AzureRmLoadBalancerInboundNatRuleConfig** tar bort en inkommande NAT-regel (Network Address Translation) från en Azure belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="08db2-106">The **Remove-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="08db2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="08db2-107">EXAMPLES</span></span>

### <span data-ttu-id="08db2-108">1: ta bort en inkommande NAT-regel från en Azure-belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="08db2-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzureRmLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzureRmLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="08db2-109">Det första kommandot läser in en redan befintlig belastningsutjämnare som heter "mylb" och lagrar den i variabel $load-saldo.</span><span class="sxs-lookup"><span data-stu-id="08db2-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="08db2-110">Det andra kommandot tar bort den inkommande NAT-regeln som är kopplad till den här belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="08db2-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="08db2-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="08db2-111">PARAMETERS</span></span>

### <span data-ttu-id="08db2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08db2-112">-DefaultProfile</span></span>
<span data-ttu-id="08db2-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="08db2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08db2-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="08db2-114">-LoadBalancer</span></span>
<span data-ttu-id="08db2-115">Anger det **Loadbalancer** -objekt som innehåller den inkommande NAT-regelns konfiguration som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="08db2-115">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="08db2-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="08db2-116">-Name</span></span>
<span data-ttu-id="08db2-117">Anger namnet på den inkommande NAT-regelns konfiguration som tas bort med denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08db2-117">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="08db2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08db2-118">CommonParameters</span></span>
<span data-ttu-id="08db2-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08db2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08db2-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08db2-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08db2-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="08db2-121">INPUTS</span></span>

### <span data-ttu-id="08db2-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="08db2-122">PSLoadBalancer</span></span>
<span data-ttu-id="08db2-123">Parametern ' LoadBalancer ' godkänner värdet av typen ' PSLoadBalancer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="08db2-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="08db2-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="08db2-124">OUTPUTS</span></span>

### <span data-ttu-id="08db2-125">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="08db2-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="08db2-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="08db2-126">NOTES</span></span>

## <span data-ttu-id="08db2-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="08db2-127">RELATED LINKS</span></span>

[<span data-ttu-id="08db2-128">Add-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="08db2-128">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="08db2-129">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="08db2-129">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="08db2-130">New-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="08db2-130">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="08db2-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="08db2-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


