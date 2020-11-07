---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: d76803df11ff3f89e20ca7d849577ca51331416c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578879"
---
# <span data-ttu-id="cfba1-101">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cfba1-101">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="cfba1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cfba1-102">SYNOPSIS</span></span>
<span data-ttu-id="cfba1-103">Tar bort en inkommande NAT-regel från en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="cfba1-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfba1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cfba1-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfba1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cfba1-105">DESCRIPTION</span></span>
<span data-ttu-id="cfba1-106">Cmdleten **Remove-AzureRmLoadBalancerInboundNatRuleConfig** tar bort en inkommande NAT-regel (Network Address Translation) från en Azure belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="cfba1-106">The **Remove-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="cfba1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cfba1-107">EXAMPLES</span></span>

### <span data-ttu-id="cfba1-108">1: ta bort en inkommande NAT-regel från en Azure-belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="cfba1-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzureRmLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzureRmLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="cfba1-109">Det första kommandot läser in en redan befintlig belastningsutjämnare som heter "mylb" och lagrar den i variabel $load-saldo.</span><span class="sxs-lookup"><span data-stu-id="cfba1-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="cfba1-110">Det andra kommandot tar bort den inkommande NAT-regeln som är kopplad till den här belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="cfba1-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="cfba1-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cfba1-111">PARAMETERS</span></span>

### <span data-ttu-id="cfba1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfba1-112">-DefaultProfile</span></span>
<span data-ttu-id="cfba1-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cfba1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfba1-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cfba1-114">-LoadBalancer</span></span>
<span data-ttu-id="cfba1-115">Anger det **Loadbalancer** -objekt som innehåller den inkommande NAT-regelns konfiguration som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="cfba1-115">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cfba1-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="cfba1-116">-Name</span></span>
<span data-ttu-id="cfba1-117">Anger namnet på den inkommande NAT-regelns konfiguration som tas bort med denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfba1-117">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cfba1-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cfba1-118">-Confirm</span></span>
<span data-ttu-id="cfba1-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cfba1-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfba1-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfba1-120">-WhatIf</span></span>
<span data-ttu-id="cfba1-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cfba1-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cfba1-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cfba1-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfba1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfba1-123">CommonParameters</span></span>
<span data-ttu-id="cfba1-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfba1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfba1-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfba1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfba1-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cfba1-126">INPUTS</span></span>

### <span data-ttu-id="cfba1-127">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cfba1-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="cfba1-128">Parametrar: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cfba1-128">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="cfba1-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cfba1-129">OUTPUTS</span></span>

### <span data-ttu-id="cfba1-130">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cfba1-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="cfba1-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cfba1-131">NOTES</span></span>

## <span data-ttu-id="cfba1-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cfba1-132">RELATED LINKS</span></span>

[<span data-ttu-id="cfba1-133">Add-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cfba1-133">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="cfba1-134">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cfba1-134">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="cfba1-135">New-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cfba1-135">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="cfba1-136">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cfba1-136">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)

