---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancer.md
ms.openlocfilehash: 463b9cf07bbb04273e1653f4d84805de3802b616
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575614"
---
# <span data-ttu-id="aad9e-101">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="aad9e-101">Set-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="aad9e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aad9e-102">SYNOPSIS</span></span>
<span data-ttu-id="aad9e-103">Anger mål tillstånd för en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="aad9e-103">Sets the goal state for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aad9e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aad9e-104">SYNTAX</span></span>

```
Set-AzureRmLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aad9e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aad9e-105">DESCRIPTION</span></span>
<span data-ttu-id="aad9e-106">Cmdleten **set-AzureRmLoadBalancer** anger mål tillståndet för en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="aad9e-106">The **Set-AzureRmLoadBalancer** cmdlet sets the goal state for an Azure load balancer.</span></span>

## <span data-ttu-id="aad9e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aad9e-107">EXAMPLES</span></span>

### <span data-ttu-id="aad9e-108">Exempel 1: ändra en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="aad9e-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzureRmLoadBalancer
```

<span data-ttu-id="aad9e-109">Det första kommandot får belastningsutjämnaren med namnet NRPLB och lagrar det sedan i $slb variabel.</span><span class="sxs-lookup"><span data-stu-id="aad9e-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="aad9e-110">I det andra kommandot används pipeline-operatorn för att överföra belastningsutjämnaren i $slb till Add-AzureRmLoadBalancerInboundNatRuleConfig, som lägger till en inkommande NAT-regel med namnet NewRule.</span><span class="sxs-lookup"><span data-stu-id="aad9e-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>

<span data-ttu-id="aad9e-111">Det tredje kommandot skickar belastningsutjämnaren till **set-AzureRmLoadBalancer** , som uppdaterar belastningsutjämnaren och sparar den.</span><span class="sxs-lookup"><span data-stu-id="aad9e-111">The third command passes the load balancer to **Set-AzureRmLoadBalancer** , which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="aad9e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aad9e-112">PARAMETERS</span></span>

### <span data-ttu-id="aad9e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aad9e-113">-AsJob</span></span>
<span data-ttu-id="aad9e-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="aad9e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aad9e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aad9e-115">-DefaultProfile</span></span>
<span data-ttu-id="aad9e-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="aad9e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aad9e-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="aad9e-117">-LoadBalancer</span></span>
<span data-ttu-id="aad9e-118">Anger en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="aad9e-118">Specifies a load balancer.</span></span>
<span data-ttu-id="aad9e-119">Denna cmdlet anger mål tillståndet för belastningsutjämnaren som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="aad9e-119">This cmdlet sets the goal state for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="aad9e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aad9e-120">CommonParameters</span></span>
<span data-ttu-id="aad9e-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aad9e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aad9e-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aad9e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aad9e-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aad9e-123">INPUTS</span></span>

### <span data-ttu-id="aad9e-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="aad9e-124">PSLoadBalancer</span></span>
<span data-ttu-id="aad9e-125">Parametern ' LoadBalancer ' godkänner värdet av typen ' PSLoadBalancer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="aad9e-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="aad9e-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aad9e-126">OUTPUTS</span></span>

### <span data-ttu-id="aad9e-127">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="aad9e-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="aad9e-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aad9e-128">NOTES</span></span>

## <span data-ttu-id="aad9e-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aad9e-129">RELATED LINKS</span></span>

[<span data-ttu-id="aad9e-130">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="aad9e-130">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="aad9e-131">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="aad9e-131">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="aad9e-132">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="aad9e-132">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)


