---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1FDA90C0-D01F-45E1-9149-16AD04046271
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 378d9521e309629bdb9e6ee58cfc1cd06fd9ef7b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574803"
---
# <span data-ttu-id="95abd-101">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="95abd-101">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="95abd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="95abd-102">SYNOPSIS</span></span>
<span data-ttu-id="95abd-103">Hämtar en inkommande NAT-regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="95abd-103">Gets an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95abd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="95abd-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95abd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="95abd-105">DESCRIPTION</span></span>
<span data-ttu-id="95abd-106">Cmdleten **Get-AzureRmLoadBalancerInboundNatRuleConfig** får en eller flera inkommande NAT-regler (Network Address Translation) i en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="95abd-106">The **Get-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet gets one or more inbound network address translation (NAT) rules in an Azure load balancer.</span></span>

## <span data-ttu-id="95abd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="95abd-107">EXAMPLES</span></span>

### <span data-ttu-id="95abd-108">Exempel 1: skaffa en inkommande NAT-regel</span><span class="sxs-lookup"><span data-stu-id="95abd-108">Example 1: Get an inbound NAT rule configuration</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule1" -LoadBalancer $slb
```

<span data-ttu-id="95abd-109">Det första kommandot får belastningsutjämnaren med namnet MyLoadBalancer och lagrar det i variabeln $slb.</span><span class="sxs-lookup"><span data-stu-id="95abd-109">The first command gets the load balancer named MyLoadBalancer, and stores it in the variable $slb.</span></span>
<span data-ttu-id="95abd-110">Det andra kommandot hämtar den associerade NAT-regeln med namnet MyInboundNatRule1 från belastningsutjämnaren i $slb.</span><span class="sxs-lookup"><span data-stu-id="95abd-110">The second command gets the associated NAT rule named MyInboundNatRule1 from the load balancer in $slb.</span></span>

## <span data-ttu-id="95abd-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="95abd-111">PARAMETERS</span></span>

### <span data-ttu-id="95abd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95abd-112">-DefaultProfile</span></span>
<span data-ttu-id="95abd-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="95abd-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95abd-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="95abd-114">-LoadBalancer</span></span>
<span data-ttu-id="95abd-115">Anger den belastnings utjämning som är kopplad till den inkommande NAT-regelns konfiguration för att få.</span><span class="sxs-lookup"><span data-stu-id="95abd-115">Specifies the load balancer that is associated with the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="95abd-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="95abd-116">-Name</span></span>
<span data-ttu-id="95abd-117">Anger namnet på den inkommande NAT-regelns konfiguration för att få.</span><span class="sxs-lookup"><span data-stu-id="95abd-117">Specifies the name of the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="95abd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95abd-118">CommonParameters</span></span>
<span data-ttu-id="95abd-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95abd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95abd-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95abd-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95abd-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="95abd-121">INPUTS</span></span>

### <span data-ttu-id="95abd-122">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="95abd-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="95abd-123">Parametrar: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="95abd-123">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="95abd-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="95abd-124">OUTPUTS</span></span>

### <span data-ttu-id="95abd-125">Microsoft. Azure. commands. Networks. Models. PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="95abd-125">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="95abd-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="95abd-126">NOTES</span></span>

## <span data-ttu-id="95abd-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="95abd-127">RELATED LINKS</span></span>

[<span data-ttu-id="95abd-128">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="95abd-128">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="95abd-129">New-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="95abd-129">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="95abd-130">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="95abd-130">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="95abd-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="95abd-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


