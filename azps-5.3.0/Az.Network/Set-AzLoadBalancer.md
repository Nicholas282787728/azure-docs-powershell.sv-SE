---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
ms.openlocfilehash: 049b99ee0d019ae7f845e5e7578d9982e41a7a4b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98527531"
---
# <span data-ttu-id="300fd-101">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="300fd-101">Set-AzLoadBalancer</span></span>

## <span data-ttu-id="300fd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="300fd-102">SYNOPSIS</span></span>
<span data-ttu-id="300fd-103">Uppdaterar en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="300fd-103">Updates a load balancer.</span></span>

## <span data-ttu-id="300fd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="300fd-104">SYNTAX</span></span>

```
Set-AzLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="300fd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="300fd-105">DESCRIPTION</span></span>
<span data-ttu-id="300fd-106">Cmdleten **set-AzLoadBalancer** uppdaterar en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="300fd-106">The **Set-AzLoadBalancer** cmdlet updates a load balancer.</span></span>

## <span data-ttu-id="300fd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="300fd-107">EXAMPLES</span></span>

### <span data-ttu-id="300fd-108">Exempel 1: ändra en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="300fd-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="300fd-109">Det första kommandot får belastningsutjämnaren med namnet NRPLB och lagrar det sedan i $slb variabel.</span><span class="sxs-lookup"><span data-stu-id="300fd-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="300fd-110">I det andra kommandot används pipeline-operatorn för att överföra belastningsutjämnaren i $slb till Add-AzLoadBalancerInboundNatRuleConfig, som lägger till en inkommande NAT-regel med namnet NewRule.</span><span class="sxs-lookup"><span data-stu-id="300fd-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>
<span data-ttu-id="300fd-111">Det tredje kommandot skickar belastningsutjämnaren till **set-AzLoadBalancer**, som uppdaterar belastningsutjämnaren och sparar den.</span><span class="sxs-lookup"><span data-stu-id="300fd-111">The third command passes the load balancer to **Set-AzLoadBalancer**, which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="300fd-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="300fd-112">PARAMETERS</span></span>

### <span data-ttu-id="300fd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="300fd-113">-AsJob</span></span>
<span data-ttu-id="300fd-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="300fd-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="300fd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="300fd-115">-DefaultProfile</span></span>
<span data-ttu-id="300fd-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="300fd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="300fd-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="300fd-117">-LoadBalancer</span></span>
<span data-ttu-id="300fd-118">Anger ett belastnings Utjämnings objekt som representerar det tillstånd som belastningsutjämnaren ska ställas in på.</span><span class="sxs-lookup"><span data-stu-id="300fd-118">Specifies a load balancer object representing the state to which the load balancer should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="300fd-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="300fd-119">-Confirm</span></span>
<span data-ttu-id="300fd-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="300fd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="300fd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="300fd-121">-WhatIf</span></span>
<span data-ttu-id="300fd-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="300fd-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="300fd-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="300fd-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="300fd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="300fd-124">CommonParameters</span></span>
<span data-ttu-id="300fd-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="300fd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="300fd-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="300fd-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="300fd-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="300fd-127">INPUTS</span></span>

### <span data-ttu-id="300fd-128">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="300fd-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="300fd-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="300fd-129">OUTPUTS</span></span>

### <span data-ttu-id="300fd-130">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="300fd-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="300fd-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="300fd-131">NOTES</span></span>

## <span data-ttu-id="300fd-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="300fd-132">RELATED LINKS</span></span>

[<span data-ttu-id="300fd-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="300fd-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="300fd-134">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="300fd-134">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="300fd-135">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="300fd-135">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)


