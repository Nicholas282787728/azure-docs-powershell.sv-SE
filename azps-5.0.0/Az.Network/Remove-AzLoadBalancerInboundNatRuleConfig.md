---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 76cf9e2624c812d99702823b303e4e6427845670
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269304"
---
# <span data-ttu-id="44d99-101">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="44d99-101">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="44d99-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="44d99-102">SYNOPSIS</span></span>
<span data-ttu-id="44d99-103">Tar bort en inkommande NAT-regel från en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="44d99-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

## <span data-ttu-id="44d99-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="44d99-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44d99-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="44d99-105">DESCRIPTION</span></span>
<span data-ttu-id="44d99-106">Cmdleten **Remove-AzLoadBalancerInboundNatRuleConfig** tar bort en inkommande NAT-regel (Network Address Translation) från en Azure belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="44d99-106">The **Remove-AzLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="44d99-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="44d99-107">EXAMPLES</span></span>

### <span data-ttu-id="44d99-108">1: ta bort en inkommande NAT-regel från en Azure-belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="44d99-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="44d99-109">Det första kommandot läser in en redan befintlig belastningsutjämnare som heter "mylb" och lagrar den i variabel $load-saldo.</span><span class="sxs-lookup"><span data-stu-id="44d99-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="44d99-110">Det andra kommandot tar bort den inkommande NAT-regeln som är kopplad till den här belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="44d99-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="44d99-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="44d99-111">PARAMETERS</span></span>

### <span data-ttu-id="44d99-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44d99-112">-DefaultProfile</span></span>
<span data-ttu-id="44d99-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="44d99-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44d99-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="44d99-114">-LoadBalancer</span></span>
<span data-ttu-id="44d99-115">Anger det **Loadbalancer** -objekt som innehåller den inkommande NAT-regelns konfiguration som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="44d99-115">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="44d99-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="44d99-116">-Name</span></span>
<span data-ttu-id="44d99-117">Anger namnet på den inkommande NAT-regelns konfiguration som tas bort med denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44d99-117">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="44d99-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="44d99-118">-Confirm</span></span>
<span data-ttu-id="44d99-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="44d99-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44d99-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44d99-120">-WhatIf</span></span>
<span data-ttu-id="44d99-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="44d99-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="44d99-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="44d99-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44d99-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44d99-123">CommonParameters</span></span>
<span data-ttu-id="44d99-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44d99-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44d99-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44d99-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44d99-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="44d99-126">INPUTS</span></span>

### <span data-ttu-id="44d99-127">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="44d99-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="44d99-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="44d99-128">OUTPUTS</span></span>

### <span data-ttu-id="44d99-129">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="44d99-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="44d99-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="44d99-130">NOTES</span></span>

## <span data-ttu-id="44d99-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="44d99-131">RELATED LINKS</span></span>

[<span data-ttu-id="44d99-132">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="44d99-132">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="44d99-133">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="44d99-133">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="44d99-134">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="44d99-134">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="44d99-135">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="44d99-135">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


