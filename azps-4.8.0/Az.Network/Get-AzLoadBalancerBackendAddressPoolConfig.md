---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F421174A-B138-45EB-AF84-CB3CE5870F27
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: f6acd469c49df7e67e8aa9bf00faf4952a33eb79
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261860"
---
# <span data-ttu-id="085c2-101">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="085c2-101">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="085c2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="085c2-102">SYNOPSIS</span></span>
<span data-ttu-id="085c2-103">Hämtar en konfiguration för en server dels adresspool för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="085c2-103">Gets a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="085c2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="085c2-104">SYNTAX</span></span>

```
Get-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="085c2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="085c2-105">DESCRIPTION</span></span>
<span data-ttu-id="085c2-106">Cmdleten **Get-AzLoadBalancerBackendAddressPoolConfig** har en enskild server grupp eller en lista över Server grupper i en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="085c2-106">The **Get-AzLoadBalancerBackendAddressPoolConfig** cmdlet gets a single backend address pool or a list of backend address pools within a load balancer.</span></span>

## <span data-ttu-id="085c2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="085c2-107">EXAMPLES</span></span>

### <span data-ttu-id="085c2-108">Exempel 1: Hämta Server delens adresspool</span><span class="sxs-lookup"><span data-stu-id="085c2-108">Example 1: Get the backend address pool</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" -LoadBalancer $loadbalancer
```

<span data-ttu-id="085c2-109">Det första kommandot får en befintlig belastningsutjämnare med namnet MyLoadBalancer i resurs gruppen med namnet MyResourceGroup och lagrar den sedan i $loadbalancer variabel.</span><span class="sxs-lookup"><span data-stu-id="085c2-109">The first command gets an existing load balancer named MyLoadBalancer in the resource group named MyResourceGroup, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="085c2-110">Med det andra kommandot hämtas den associerade server delens konfiguration med namnet BackendAddressPool02 för belastningsutjämnaren i $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="085c2-110">The second command gets the associated backend address pool configuration named BackendAddressPool02 for the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="085c2-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="085c2-111">PARAMETERS</span></span>

### <span data-ttu-id="085c2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="085c2-112">-DefaultProfile</span></span>
<span data-ttu-id="085c2-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="085c2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="085c2-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="085c2-114">-LoadBalancer</span></span>
<span data-ttu-id="085c2-115">Anger den belastnings utjämning som är kopplad till den server dels adresspoolen som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="085c2-115">Specifies the load balancer that is associated with the backend address pool to get.</span></span>

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

### <span data-ttu-id="085c2-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="085c2-116">-Name</span></span>
<span data-ttu-id="085c2-117">Anger namnet på belastningsutjämnaren som innehåller Server delens adresspool som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="085c2-117">Specifies the name of the load balancer that contains the backend address pool to get.</span></span>

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

### <span data-ttu-id="085c2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="085c2-118">CommonParameters</span></span>
<span data-ttu-id="085c2-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="085c2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="085c2-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="085c2-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="085c2-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="085c2-121">INPUTS</span></span>

### <span data-ttu-id="085c2-122">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="085c2-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="085c2-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="085c2-123">OUTPUTS</span></span>

### <span data-ttu-id="085c2-124">Microsoft. Azure. commands. Networks. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="085c2-124">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="085c2-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="085c2-125">NOTES</span></span>

## <span data-ttu-id="085c2-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="085c2-126">RELATED LINKS</span></span>

[<span data-ttu-id="085c2-127">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="085c2-127">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="085c2-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="085c2-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="085c2-129">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="085c2-129">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="085c2-130">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="085c2-130">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)

