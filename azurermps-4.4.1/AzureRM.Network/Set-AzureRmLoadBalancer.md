---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancer.md
ms.openlocfilehash: be09bb6592ebf950c2fb3de6b4a512235fd0feab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756579"
---
# <span data-ttu-id="261df-101">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="261df-101">Set-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="261df-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="261df-102">SYNOPSIS</span></span>
<span data-ttu-id="261df-103">Anger mål tillstånd för en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="261df-103">Sets the goal state for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="261df-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="261df-104">SYNTAX</span></span>

```
Set-AzureRmLoadBalancer -LoadBalancer <PSLoadBalancer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="261df-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="261df-105">DESCRIPTION</span></span>
<span data-ttu-id="261df-106">Cmdleten **set-AzureRmLoadBalancer** anger mål tillståndet för en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="261df-106">The **Set-AzureRmLoadBalancer** cmdlet sets the goal state for an Azure load balancer.</span></span>

## <span data-ttu-id="261df-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="261df-107">EXAMPLES</span></span>

### <span data-ttu-id="261df-108">Exempel 1: ändra en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="261df-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzureRmLoadBalancer
```

<span data-ttu-id="261df-109">Det första kommandot får belastningsutjämnaren med namnet NRPLB och lagrar det sedan i $slb variabel.</span><span class="sxs-lookup"><span data-stu-id="261df-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="261df-110">I det andra kommandot används pipeline-operatorn för att överföra belastningsutjämnaren i $slb till Add-AzureRmLoadBalancerInboundNatRuleConfig, som lägger till en inkommande NAT-regel med namnet NewRule.</span><span class="sxs-lookup"><span data-stu-id="261df-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>

<span data-ttu-id="261df-111">Det tredje kommandot skickar belastningsutjämnaren till **set-AzureRmLoadBalancer** , som uppdaterar belastningsutjämnaren och sparar den.</span><span class="sxs-lookup"><span data-stu-id="261df-111">The third command passes the load balancer to **Set-AzureRmLoadBalancer** , which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="261df-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="261df-112">PARAMETERS</span></span>

### <span data-ttu-id="261df-113">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="261df-113">-LoadBalancer</span></span>
<span data-ttu-id="261df-114">Anger en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="261df-114">Specifies a load balancer.</span></span>
<span data-ttu-id="261df-115">Denna cmdlet anger mål tillståndet för belastningsutjämnaren som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="261df-115">This cmdlet sets the goal state for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="261df-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="261df-116">-DefaultProfile</span></span>
<span data-ttu-id="261df-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="261df-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="261df-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="261df-118">CommonParameters</span></span>
<span data-ttu-id="261df-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="261df-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="261df-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="261df-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="261df-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="261df-121">INPUTS</span></span>

### <span data-ttu-id="261df-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="261df-122">PSLoadBalancer</span></span>
<span data-ttu-id="261df-123">Parametern ' LoadBalancer ' godkänner värdet av typen ' PSLoadBalancer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="261df-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="261df-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="261df-124">OUTPUTS</span></span>

### <span data-ttu-id="261df-125">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="261df-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="261df-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="261df-126">NOTES</span></span>

## <span data-ttu-id="261df-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="261df-127">RELATED LINKS</span></span>

[<span data-ttu-id="261df-128">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="261df-128">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="261df-129">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="261df-129">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="261df-130">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="261df-130">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)


