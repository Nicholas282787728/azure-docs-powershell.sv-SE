---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F421174A-B138-45EB-AF84-CB3CE5870F27
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 9c2341494f1508563523a181532ce98347051ac3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922278"
---
# <span data-ttu-id="f0ff1-101">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f0ff1-101">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="f0ff1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f0ff1-102">SYNOPSIS</span></span>
<span data-ttu-id="f0ff1-103">Hämtar en konfiguration för en server dels adresspool för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="f0ff1-103">Gets a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="f0ff1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f0ff1-104">SYNTAX</span></span>

```
Get-AzLoadBalancerBackendAddressPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0ff1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f0ff1-105">DESCRIPTION</span></span>
<span data-ttu-id="f0ff1-106">Cmdleten **Get-AzLoadBalancerBackendAddressPoolConfig** har en enskild server grupp eller en lista över Server grupper i en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="f0ff1-106">The **Get-AzLoadBalancerBackendAddressPoolConfig** cmdlet gets a single backend address pool or a list of backend address pools within a load balancer.</span></span>

## <span data-ttu-id="f0ff1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f0ff1-107">EXAMPLES</span></span>

### <span data-ttu-id="f0ff1-108">Exempel 1: Hämta Server delens adresspool</span><span class="sxs-lookup"><span data-stu-id="f0ff1-108">Example 1: Get the backend address pool</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" -LoadBalancer $loadbalancer
```

<span data-ttu-id="f0ff1-109">Det första kommandot får en befintlig belastningsutjämnare med namnet MyLoadBalancer i resurs gruppen med namnet MyResourceGroup och lagrar den sedan i $loadbalancer variabel.</span><span class="sxs-lookup"><span data-stu-id="f0ff1-109">The first command gets an existing load balancer named MyLoadBalancer in the resource group named MyResourceGroup, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="f0ff1-110">Med det andra kommandot hämtas den associerade server delens konfiguration med namnet BackendAddressPool02 för belastningsutjämnaren i $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="f0ff1-110">The second command gets the associated backend address pool configuration named BackendAddressPool02 for the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="f0ff1-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f0ff1-111">PARAMETERS</span></span>

### <span data-ttu-id="f0ff1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0ff1-112">-DefaultProfile</span></span>
<span data-ttu-id="f0ff1-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f0ff1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0ff1-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f0ff1-114">-LoadBalancer</span></span>
<span data-ttu-id="f0ff1-115">Anger den belastnings utjämning som är kopplad till den server dels adresspoolen som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="f0ff1-115">Specifies the load balancer that is associated with the backend address pool to get.</span></span>

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

### <span data-ttu-id="f0ff1-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="f0ff1-116">-Name</span></span>
<span data-ttu-id="f0ff1-117">Anger namnet på belastningsutjämnaren som innehåller Server delens adresspool som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="f0ff1-117">Specifies the name of the load balancer that contains the backend address pool to get.</span></span>

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

### <span data-ttu-id="f0ff1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0ff1-118">CommonParameters</span></span>
<span data-ttu-id="f0ff1-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0ff1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0ff1-120">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0ff1-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0ff1-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f0ff1-121">INPUTS</span></span>

### <span data-ttu-id="f0ff1-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f0ff1-122">PSLoadBalancer</span></span>
<span data-ttu-id="f0ff1-123">Parametern ' LoadBalancer ' godkänner värdet av typen ' PSLoadBalancer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="f0ff1-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="f0ff1-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f0ff1-124">OUTPUTS</span></span>

### <span data-ttu-id="f0ff1-125">Microsoft. Azure. commands. Networks. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f0ff1-125">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="f0ff1-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f0ff1-126">NOTES</span></span>

## <span data-ttu-id="f0ff1-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f0ff1-127">RELATED LINKS</span></span>

[<span data-ttu-id="f0ff1-128">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f0ff1-128">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="f0ff1-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f0ff1-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="f0ff1-130">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f0ff1-130">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="f0ff1-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f0ff1-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


