---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: e106656124aea48dff6c7fd7183027e183dce93b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398675"
---
# <span data-ttu-id="73cbb-101">New-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="73cbb-101">New-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="73cbb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="73cbb-102">SYNOPSIS</span></span>
<span data-ttu-id="73cbb-103">Skapar en adresspool för backend-adresser på en Loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="73cbb-103">Creates a backend address pool on a loadbalancer.</span></span> 

## <span data-ttu-id="73cbb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="73cbb-104">SYNTAX</span></span>

### <span data-ttu-id="73cbb-105">CreateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="73cbb-105">CreateByNameParameterSet</span></span>
```
New-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> -Name <String>
 [-LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73cbb-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73cbb-106">CreateByParentObjectParameterSet</span></span>
```
New-AzLoadBalancerBackendAddressPool -LoadBalancer <PSLoadBalancer> -Name <String>
 [-LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73cbb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="73cbb-107">DESCRIPTION</span></span>
<span data-ttu-id="73cbb-108">Skapar en adresspool för backend-adresser på en Loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="73cbb-108">Creates a backend address pool on a loadbalancer.</span></span> <span data-ttu-id="73cbb-109">Möjliggör specifiying en matris med PSLoadBalancerBackendAddress.</span><span class="sxs-lookup"><span data-stu-id="73cbb-109">Allows for specifiying a array of PSLoadBalancerBackendAddress.</span></span> 
## <span data-ttu-id="73cbb-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="73cbb-110">EXAMPLES</span></span>

### <span data-ttu-id="73cbb-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="73cbb-111">Example 1</span></span>
```powershell
## create by passing loadbalancer without Ips
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
PS C:\> $ip1 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ip2 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.6" -Name "TestVNetRef2" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ips = @($ip1, $ip2)

PS C:\> $lb | New-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="73cbb-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="73cbb-112">Example 2</span></span>
```powershell
## create by passing loadbalancer with ips
PS C:\> $lb | New-AzLoadBalancerBackendAddressPool -Name $backendPool7 -LoadBalancerBackendAddress $ips
```

### <span data-ttu-id="73cbb-113">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="73cbb-113">Example 3</span></span>
```powershell
## create by name without ips
PS C:\> New-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool3
```

### <span data-ttu-id="73cbb-114">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="73cbb-114">Example 4</span></span>
```powershell
## create by name with ips
PS C:\> New-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool3 -LoadBalancerBackendAddress $ips
```

## <span data-ttu-id="73cbb-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="73cbb-115">PARAMETERS</span></span>

### <span data-ttu-id="73cbb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73cbb-116">-DefaultProfile</span></span>
<span data-ttu-id="73cbb-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="73cbb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73cbb-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="73cbb-118">-LoadBalancer</span></span>
<span data-ttu-id="73cbb-119">Resursen för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="73cbb-119">The load balancer resource.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73cbb-120">-LoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="73cbb-120">-LoadBalancerBackendAddress</span></span>
<span data-ttu-id="73cbb-121">Server delens adresser.</span><span class="sxs-lookup"><span data-stu-id="73cbb-121">The backend addresses.</span></span>

```yaml
Type: PSLoadBalancerBackendAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73cbb-122">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="73cbb-122">-LoadBalancerName</span></span>
<span data-ttu-id="73cbb-123">Namnet på belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="73cbb-123">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73cbb-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="73cbb-124">-Name</span></span>
<span data-ttu-id="73cbb-125">Namnet på backend-poolen.</span><span class="sxs-lookup"><span data-stu-id="73cbb-125">The name of the backend pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73cbb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73cbb-126">-ResourceGroupName</span></span>
<span data-ttu-id="73cbb-127">Belastnings utjämningens resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="73cbb-127">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73cbb-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="73cbb-128">-Confirm</span></span>
<span data-ttu-id="73cbb-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="73cbb-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73cbb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73cbb-130">-WhatIf</span></span>
<span data-ttu-id="73cbb-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="73cbb-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73cbb-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="73cbb-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73cbb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73cbb-133">CommonParameters</span></span>
<span data-ttu-id="73cbb-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73cbb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73cbb-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="73cbb-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73cbb-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="73cbb-136">INPUTS</span></span>

### <span data-ttu-id="73cbb-137">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="73cbb-137">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="73cbb-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="73cbb-138">OUTPUTS</span></span>

### <span data-ttu-id="73cbb-139">Microsoft. Azure. commands. Networks. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="73cbb-139">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="73cbb-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="73cbb-140">NOTES</span></span>

## <span data-ttu-id="73cbb-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="73cbb-141">RELATED LINKS</span></span>
