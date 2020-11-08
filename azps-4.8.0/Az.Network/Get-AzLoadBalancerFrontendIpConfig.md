---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 776ff53573fa68d1757ea7c0422579e253661968
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258306"
---
# <span data-ttu-id="e2606-101">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e2606-101">Get-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="e2606-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e2606-102">SYNOPSIS</span></span>
<span data-ttu-id="e2606-103">Hämtar en klient-IP-konfiguration i en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="e2606-103">Gets a front-end IP configuration in a load balancer.</span></span>

## <span data-ttu-id="e2606-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e2606-104">SYNTAX</span></span>

```
Get-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2606-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e2606-105">DESCRIPTION</span></span>
<span data-ttu-id="e2606-106">Cmdleten **Get-AzLoadBalancerFrontendIpConfig** har en front-IP-konfiguration eller en lista över front-IP-konfigurationer i en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="e2606-106">The **Get-AzLoadBalancerFrontendIpConfig** cmdlet gets a front-end IP configuration or a list of front-end IP configurations in a load balancer.</span></span>

## <span data-ttu-id="e2606-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e2606-107">EXAMPLES</span></span>

### <span data-ttu-id="e2606-108">Exempel 1: Hämta en front-IP-konfiguration i en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="e2606-108">Example 1: Get a front-end IP configuration in a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

<span data-ttu-id="e2606-109">Det första kommandot får belastningsutjämnaren med namnet MyLoadBalancer och lagrar det sedan i variabeln $slb.</span><span class="sxs-lookup"><span data-stu-id="e2606-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="e2606-110">Det andra kommandot får den klient konfiguration för front end som är kopplad till den belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="e2606-110">The second command gets the front end IP configuration associated with that load balancer.</span></span>

## <span data-ttu-id="e2606-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e2606-111">PARAMETERS</span></span>

### <span data-ttu-id="e2606-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2606-112">-DefaultProfile</span></span>
<span data-ttu-id="e2606-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e2606-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2606-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e2606-114">-LoadBalancer</span></span>
<span data-ttu-id="e2606-115">Anger den belastningsutjämnare som är kopplad till den frontend-IP-konfiguration som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="e2606-115">Specifies the load balancer that is associated with the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="e2606-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="e2606-116">-Name</span></span>
<span data-ttu-id="e2606-117">Anger namnet på belastningsutjämnaren som innehåller den frontend-IP-konfiguration som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="e2606-117">Specifies the name of the load balancer that contains the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="e2606-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2606-118">CommonParameters</span></span>
<span data-ttu-id="e2606-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2606-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2606-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2606-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2606-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e2606-121">INPUTS</span></span>

### <span data-ttu-id="e2606-122">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e2606-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e2606-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e2606-123">OUTPUTS</span></span>

### <span data-ttu-id="e2606-124">Microsoft. Azure. commands. Networks. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2606-124">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="e2606-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e2606-125">NOTES</span></span>

## <span data-ttu-id="e2606-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e2606-126">RELATED LINKS</span></span>

[<span data-ttu-id="e2606-127">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e2606-127">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="e2606-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e2606-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="e2606-129">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e2606-129">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="e2606-130">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e2606-130">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="e2606-131">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e2606-131">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


