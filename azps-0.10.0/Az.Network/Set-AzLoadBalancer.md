---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancer.md
ms.openlocfilehash: 17af7cc61ec3d254133dd0563e8ea09fc0e3043f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924222"
---
# <span data-ttu-id="180df-101">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="180df-101">Set-AzLoadBalancer</span></span>

## <span data-ttu-id="180df-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="180df-102">SYNOPSIS</span></span>
<span data-ttu-id="180df-103">Anger mål tillstånd för en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="180df-103">Sets the goal state for a load balancer.</span></span>

## <span data-ttu-id="180df-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="180df-104">SYNTAX</span></span>

```
Set-AzLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="180df-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="180df-105">DESCRIPTION</span></span>
<span data-ttu-id="180df-106">Cmdleten **set-AzLoadBalancer** anger mål tillståndet för en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="180df-106">The **Set-AzLoadBalancer** cmdlet sets the goal state for an Azure load balancer.</span></span>

## <span data-ttu-id="180df-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="180df-107">EXAMPLES</span></span>

### <span data-ttu-id="180df-108">Exempel 1: ändra en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="180df-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="180df-109">Det första kommandot får belastningsutjämnaren med namnet NRPLB och lagrar det sedan i $slb variabel.</span><span class="sxs-lookup"><span data-stu-id="180df-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="180df-110">I det andra kommandot används pipeline-operatorn för att överföra belastningsutjämnaren i $slb till Add-AzLoadBalancerInboundNatRuleConfig, som lägger till en inkommande NAT-regel med namnet NewRule.</span><span class="sxs-lookup"><span data-stu-id="180df-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>

<span data-ttu-id="180df-111">Det tredje kommandot skickar belastningsutjämnaren till **set-AzLoadBalancer** , som uppdaterar belastningsutjämnaren och sparar den.</span><span class="sxs-lookup"><span data-stu-id="180df-111">The third command passes the load balancer to **Set-AzLoadBalancer** , which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="180df-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="180df-112">PARAMETERS</span></span>

### <span data-ttu-id="180df-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="180df-113">-AsJob</span></span>
<span data-ttu-id="180df-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="180df-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="180df-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="180df-115">-DefaultProfile</span></span>
<span data-ttu-id="180df-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="180df-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="180df-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="180df-117">-LoadBalancer</span></span>
<span data-ttu-id="180df-118">Anger en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="180df-118">Specifies a load balancer.</span></span>
<span data-ttu-id="180df-119">Denna cmdlet anger mål tillståndet för belastningsutjämnaren som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="180df-119">This cmdlet sets the goal state for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="180df-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="180df-120">CommonParameters</span></span>
<span data-ttu-id="180df-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="180df-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="180df-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="180df-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="180df-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="180df-123">INPUTS</span></span>

### <span data-ttu-id="180df-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="180df-124">PSLoadBalancer</span></span>
<span data-ttu-id="180df-125">Parametern ' LoadBalancer ' godkänner värdet av typen ' PSLoadBalancer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="180df-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="180df-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="180df-126">OUTPUTS</span></span>

### <span data-ttu-id="180df-127">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="180df-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="180df-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="180df-128">NOTES</span></span>

## <span data-ttu-id="180df-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="180df-129">RELATED LINKS</span></span>

[<span data-ttu-id="180df-130">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="180df-130">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="180df-131">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="180df-131">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="180df-132">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="180df-132">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)


