---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F421174A-B138-45EB-AF84-CB3CE5870F27
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 2a9fca5faf7ba024a5d5c891aa1c74ba002ac053
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576909"
---
# <span data-ttu-id="720c3-101">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="720c3-101">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="720c3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="720c3-102">SYNOPSIS</span></span>
<span data-ttu-id="720c3-103">Hämtar en konfiguration för en server dels adresspool för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="720c3-103">Gets a backend address pool configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="720c3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="720c3-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="720c3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="720c3-105">DESCRIPTION</span></span>
<span data-ttu-id="720c3-106">Cmdleten **Get-AzureRmLoadBalancerBackendAddressPoolConfig** har en enskild server grupp eller en lista över Server grupper i en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="720c3-106">The **Get-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet gets a single backend address pool or a list of backend address pools within a load balancer.</span></span>

## <span data-ttu-id="720c3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="720c3-107">EXAMPLES</span></span>

### <span data-ttu-id="720c3-108">Exempel 1: Hämta Server delens adresspool</span><span class="sxs-lookup"><span data-stu-id="720c3-108">Example 1: Get the backend address pool</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" -LoadBalancer $loadbalancer
```

<span data-ttu-id="720c3-109">Det första kommandot får en befintlig belastningsutjämnare med namnet MyLoadBalancer i resurs gruppen med namnet MyResourceGroup och lagrar den sedan i $loadbalancer variabel.</span><span class="sxs-lookup"><span data-stu-id="720c3-109">The first command gets an existing load balancer named MyLoadBalancer in the resource group named MyResourceGroup, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="720c3-110">Med det andra kommandot hämtas den associerade server delens konfiguration med namnet BackendAddressPool02 för belastningsutjämnaren i $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="720c3-110">The second command gets the associated backend address pool configuration named BackendAddressPool02 for the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="720c3-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="720c3-111">PARAMETERS</span></span>

### <span data-ttu-id="720c3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="720c3-112">-DefaultProfile</span></span>
<span data-ttu-id="720c3-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="720c3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="720c3-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="720c3-114">-LoadBalancer</span></span>
<span data-ttu-id="720c3-115">Anger den belastnings utjämning som är kopplad till den server dels adresspoolen som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="720c3-115">Specifies the load balancer that is associated with the backend address pool to get.</span></span>

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

### <span data-ttu-id="720c3-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="720c3-116">-Name</span></span>
<span data-ttu-id="720c3-117">Anger namnet på belastningsutjämnaren som innehåller Server delens adresspool som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="720c3-117">Specifies the name of the load balancer that contains the backend address pool to get.</span></span>

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

### <span data-ttu-id="720c3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="720c3-118">CommonParameters</span></span>
<span data-ttu-id="720c3-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="720c3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="720c3-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="720c3-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="720c3-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="720c3-121">INPUTS</span></span>

### <span data-ttu-id="720c3-122">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="720c3-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="720c3-123">Parametrar: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="720c3-123">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="720c3-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="720c3-124">OUTPUTS</span></span>

### <span data-ttu-id="720c3-125">Microsoft. Azure. commands. Networks. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="720c3-125">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="720c3-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="720c3-126">NOTES</span></span>

## <span data-ttu-id="720c3-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="720c3-127">RELATED LINKS</span></span>

[<span data-ttu-id="720c3-128">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="720c3-128">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="720c3-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="720c3-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="720c3-130">New-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="720c3-130">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="720c3-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="720c3-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


