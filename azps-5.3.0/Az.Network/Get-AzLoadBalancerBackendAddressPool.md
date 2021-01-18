---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 5d1c561af678086671927d3782a1fafbd9de503b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520920"
---
# <span data-ttu-id="76c3a-101">Get-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="76c3a-101">Get-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="76c3a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="76c3a-102">SYNOPSIS</span></span>
<span data-ttu-id="76c3a-103">Get-AzLoadBalancerBackendAddressPool hämtar en eller flera backend-adresspooler associerade med en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="76c3a-103">Get-AzLoadBalancerBackendAddressPool retrieves one or more backend address pools associated with a load balancer.</span></span> 

## <span data-ttu-id="76c3a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="76c3a-104">SYNTAX</span></span>

### <span data-ttu-id="76c3a-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="76c3a-105">GetByNameParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76c3a-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="76c3a-106">GetByParentObjectParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76c3a-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="76c3a-107">GetByResourceIdParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="76c3a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="76c3a-108">DESCRIPTION</span></span>
<span data-ttu-id="76c3a-109">Get-AzLoadBalancerBackendAddressPool hämtar en eller flera backend-adresspooler associerade med en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="76c3a-109">Get-AzLoadBalancerBackendAddressPool retrieves one or more backend address pools associated with a load balancer.</span></span>

## <span data-ttu-id="76c3a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="76c3a-110">EXAMPLES</span></span>

### <span data-ttu-id="76c3a-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="76c3a-111">Example 1</span></span>
```powershell
## Get single backend under loadbalancer
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
```

```powershell
## Get all backends under loadbalancer
PS C:\> $lb | Get-AzLoadBalancerBackendAddressPool
```
### <span data-ttu-id="76c3a-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="76c3a-112">Example 2</span></span>
```powershell
#Get specific backend from loadbalancer
PS C:\> $lb | Get-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="76c3a-113">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="76c3a-113">Example 3</span></span>
```powershell
#Get a backend by resource Id
PS C:\> Get-AzLoadBalancerBackendAddressPool -ResourceId $backendPool1.Id
```

## <span data-ttu-id="76c3a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="76c3a-114">PARAMETERS</span></span>

### <span data-ttu-id="76c3a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76c3a-115">-DefaultProfile</span></span>
<span data-ttu-id="76c3a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="76c3a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76c3a-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="76c3a-117">-LoadBalancer</span></span>
<span data-ttu-id="76c3a-118">{{Fill LoadBalancer Description}}</span><span class="sxs-lookup"><span data-stu-id="76c3a-118">{{ Fill LoadBalancer Description }}</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76c3a-119">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="76c3a-119">-LoadBalancerName</span></span>
<span data-ttu-id="76c3a-120">Namnet på belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="76c3a-120">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76c3a-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="76c3a-121">-Name</span></span>
<span data-ttu-id="76c3a-122">Namnet på backend-adresspoolen.</span><span class="sxs-lookup"><span data-stu-id="76c3a-122">The name of the backend address pool.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76c3a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76c3a-123">-ResourceGroupName</span></span>
<span data-ttu-id="76c3a-124">Belastnings utjämningens resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="76c3a-124">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76c3a-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76c3a-125">-ResourceId</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76c3a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76c3a-126">CommonParameters</span></span>
<span data-ttu-id="76c3a-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76c3a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76c3a-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76c3a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76c3a-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="76c3a-129">INPUTS</span></span>

### <span data-ttu-id="76c3a-130">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="76c3a-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="76c3a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="76c3a-131">System.String</span></span>

## <span data-ttu-id="76c3a-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="76c3a-132">OUTPUTS</span></span>

### <span data-ttu-id="76c3a-133">Microsoft. Azure. commands. Networks. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="76c3a-133">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="76c3a-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="76c3a-134">NOTES</span></span>

## <span data-ttu-id="76c3a-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="76c3a-135">RELATED LINKS</span></span>
