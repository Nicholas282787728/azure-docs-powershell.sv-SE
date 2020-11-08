---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 444db99b21289f3c46c2f73a726e44dad8635d39
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102165"
---
# <span data-ttu-id="8c20a-101">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8c20a-101">Get-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="8c20a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8c20a-102">SYNOPSIS</span></span>
<span data-ttu-id="8c20a-103">Hämtar en eller flera inkommande konfigurationer för NAT-pool från en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="8c20a-103">Gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="8c20a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8c20a-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c20a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8c20a-105">DESCRIPTION</span></span>
<span data-ttu-id="8c20a-106">Cmdleten **Get-AzLoadBalancerInboundNatPoolConfig** hämtar en eller flera inkommande konfigurationer för NAT-pooler från en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="8c20a-106">The **Get-AzLoadBalancerInboundNatPoolConfig** cmdlet gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="8c20a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8c20a-107">EXAMPLES</span></span>

### <span data-ttu-id="8c20a-108">1: få</span><span class="sxs-lookup"><span data-stu-id="8c20a-108">1: Get</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Get-AzLoadBalancerInboundNatPoolConfig -Name myInboundNatPool
```

## <span data-ttu-id="8c20a-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8c20a-109">PARAMETERS</span></span>

### <span data-ttu-id="8c20a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c20a-110">-DefaultProfile</span></span>
<span data-ttu-id="8c20a-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8c20a-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c20a-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8c20a-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="8c20a-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="8c20a-113">-Name</span></span>
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

### <span data-ttu-id="8c20a-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c20a-114">CommonParameters</span></span>
<span data-ttu-id="8c20a-115">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c20a-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c20a-116">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c20a-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c20a-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8c20a-117">INPUTS</span></span>

### <span data-ttu-id="8c20a-118">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8c20a-118">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="8c20a-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8c20a-119">OUTPUTS</span></span>

### <span data-ttu-id="8c20a-120">Microsoft. Azure. commands. Networks. Models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="8c20a-120">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="8c20a-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8c20a-121">NOTES</span></span>

## <span data-ttu-id="8c20a-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8c20a-122">RELATED LINKS</span></span>

[<span data-ttu-id="8c20a-123">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8c20a-123">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="8c20a-124">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8c20a-124">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="8c20a-125">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8c20a-125">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="8c20a-126">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8c20a-126">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
