---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B2CF11FC-520C-4C14-9A1B-13F06B250B5D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerruleconfig
schema: 2.0.0
ms.openlocfilehash: bd834351322f3141685538ea80a89e689d70c74f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931302"
---
# <span data-ttu-id="a1c74-101">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a1c74-101">Get-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="a1c74-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a1c74-102">SYNOPSIS</span></span>
<span data-ttu-id="a1c74-103">Hämtar regel konfigurationen för en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="a1c74-103">Gets the rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1c74-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a1c74-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1c74-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a1c74-105">DESCRIPTION</span></span>
<span data-ttu-id="a1c74-106">Cmdleten **Get-AzureRmLoadBalancerRuleConfig** hämtar en eller flera regler för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="a1c74-106">The **Get-AzureRmLoadBalancerRuleConfig** cmdlet gets one or more rule configurations for a load balancer.</span></span>

## <span data-ttu-id="a1c74-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a1c74-107">EXAMPLES</span></span>

### <span data-ttu-id="a1c74-108">Exempel 1: Hämta regel konfigurationen för en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="a1c74-108">Example 1: Get the rule configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerRuleConfig -Name "MyLBrulename" -LoadBalancer $slb
```

<span data-ttu-id="a1c74-109">Det första kommandot får belastningsutjämnaren med namnet MyLoadBalancer och lagrar det sedan i variabeln $slb.</span><span class="sxs-lookup"><span data-stu-id="a1c74-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="a1c74-110">Det andra kommandot hämtar den associerade regel konfigurationen med namnet MyLBrulename från belastningsutjämnaren i $slb.</span><span class="sxs-lookup"><span data-stu-id="a1c74-110">The second command gets the associated rule configuration named MyLBrulename from the load balancer in $slb.</span></span>

## <span data-ttu-id="a1c74-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a1c74-111">PARAMETERS</span></span>

### <span data-ttu-id="a1c74-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1c74-112">-DefaultProfile</span></span>
<span data-ttu-id="a1c74-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a1c74-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1c74-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a1c74-114">-LoadBalancer</span></span>
<span data-ttu-id="a1c74-115">Anger den belastningsutjämnare som är associerad med den regel konfiguration som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="a1c74-115">Specifies the load balancer that is associated with the rule configuration to get.</span></span>

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

### <span data-ttu-id="a1c74-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="a1c74-116">-Name</span></span>
<span data-ttu-id="a1c74-117">Anger namnet på den regel konfiguration som ska visas.</span><span class="sxs-lookup"><span data-stu-id="a1c74-117">Specifies the name of the rule configuration to get.</span></span>

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

### <span data-ttu-id="a1c74-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1c74-118">CommonParameters</span></span>
<span data-ttu-id="a1c74-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1c74-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1c74-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1c74-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1c74-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a1c74-121">INPUTS</span></span>

### <span data-ttu-id="a1c74-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a1c74-122">PSLoadBalancer</span></span>
<span data-ttu-id="a1c74-123">Parametern ' LoadBalancer ' godkänner värdet av typen ' PSLoadBalancer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="a1c74-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="a1c74-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a1c74-124">OUTPUTS</span></span>

### <span data-ttu-id="a1c74-125">Microsoft. Azure. commands. Networks. Models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="a1c74-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="a1c74-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a1c74-126">NOTES</span></span>

## <span data-ttu-id="a1c74-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a1c74-127">RELATED LINKS</span></span>

[<span data-ttu-id="a1c74-128">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a1c74-128">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="a1c74-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a1c74-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="a1c74-130">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a1c74-130">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="a1c74-131">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a1c74-131">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


