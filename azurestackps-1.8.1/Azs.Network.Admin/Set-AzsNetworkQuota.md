---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8d20f84d91c110ae1f4e55508b33f758fc0d5583
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921818"
---
# <span data-ttu-id="a9629-101">Set-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="a9629-101">Set-AzsNetworkQuota</span></span>

## <span data-ttu-id="a9629-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a9629-102">SYNOPSIS</span></span>
<span data-ttu-id="a9629-103">Skapa eller uppdatera en kvot.</span><span class="sxs-lookup"><span data-stu-id="a9629-103">Create or update a quota.</span></span>

## <span data-ttu-id="a9629-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a9629-104">SYNTAX</span></span>

### <span data-ttu-id="a9629-105">Kvoter (standard)</span><span class="sxs-lookup"><span data-stu-id="a9629-105">Quotas (Default)</span></span>
```
Set-AzsNetworkQuota -Name <String> [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9629-106">ID</span><span class="sxs-lookup"><span data-stu-id="a9629-106">ResourceId</span></span>
```
Set-AzsNetworkQuota [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9629-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="a9629-107">InputObject</span></span>
```
Set-AzsNetworkQuota [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] -InputObject <Quota> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9629-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a9629-108">DESCRIPTION</span></span>
<span data-ttu-id="a9629-109">Skapa eller uppdatera en kvot.</span><span class="sxs-lookup"><span data-stu-id="a9629-109">Create or update a quota.</span></span>

## <span data-ttu-id="a9629-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a9629-110">EXAMPLES</span></span>

### <span data-ttu-id="a9629-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="a9629-111">EXAMPLE 1</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxVnetsPerSubscription 20
```

<span data-ttu-id="a9629-112">Uppdatera en nätverks kvot efter namn.</span><span class="sxs-lookup"><span data-stu-id="a9629-112">Update a network quota by name.</span></span>

### <span data-ttu-id="a9629-113">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="a9629-113">EXAMPLE 2</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxPublicIpsPerSubscription 75 -MaxNicsPerSubscription 100
```

<span data-ttu-id="a9629-114">Uppdatera en nätverks kvot efter namn.</span><span class="sxs-lookup"><span data-stu-id="a9629-114">Update a network quota by name.</span></span>

## <span data-ttu-id="a9629-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a9629-115">PARAMETERS</span></span>

### <span data-ttu-id="a9629-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="a9629-116">-Name</span></span>
<span data-ttu-id="a9629-117">Namnet på resursen.</span><span class="sxs-lookup"><span data-stu-id="a9629-117">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Quotas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9629-118">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a9629-118">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="a9629-119">Högsta tillåtna NIC per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="a9629-119">The maximum NICs allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9629-120">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a9629-120">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="a9629-121">Högsta tillåtna offentliga IP-adresser per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="a9629-121">The maximum public IP addresses allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9629-122">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a9629-122">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="a9629-123">Det högsta antalet anslutningar för virtuell nätverksgateway som tillåts per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="a9629-123">The maximum number of virtual network gateway connections allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9629-124">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a9629-124">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="a9629-125">Maxium antal virtuella nätverk som tillåts per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="a9629-125">The maxium number of virtual networks allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9629-126">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a9629-126">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="a9629-127">Maximalt antal virtuella nätverksgateway per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="a9629-127">The maximum number of virtual network gateways allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9629-128">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a9629-128">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="a9629-129">Maximalt antal tillåtna säkerhets grupper per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="a9629-129">The maximum number of security groups allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9629-130">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a9629-130">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="a9629-131">Maximalt antal belastnings utjämningar tillåtna per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="a9629-131">The maximum number of load balancers allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9629-132">-Plats</span><span class="sxs-lookup"><span data-stu-id="a9629-132">-Location</span></span>
<span data-ttu-id="a9629-133">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="a9629-133">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Quotas
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9629-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9629-134">-ResourceId</span></span>
<span data-ttu-id="a9629-135">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="a9629-135">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9629-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9629-136">-InputObject</span></span>
<span data-ttu-id="a9629-137">Posbbily ändrade nätverks kvot som returnerats av Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="a9629-137">Posbbily modified network quota returned by Get-AzsNetworkQuota</span></span>

```yaml
Type: Quota
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9629-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9629-138">-WhatIf</span></span>
<span data-ttu-id="a9629-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a9629-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9629-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a9629-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9629-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a9629-141">-Confirm</span></span>
<span data-ttu-id="a9629-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a9629-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9629-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9629-143">CommonParameters</span></span>
<span data-ttu-id="a9629-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9629-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9629-145">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9629-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9629-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a9629-146">INPUTS</span></span>

## <span data-ttu-id="a9629-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a9629-147">OUTPUTS</span></span>

### <span data-ttu-id="a9629-148">Microsoft. AzureStack. Management. Network. admin. Models. quota</span><span class="sxs-lookup"><span data-stu-id="a9629-148">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="a9629-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a9629-149">NOTES</span></span>

## <span data-ttu-id="a9629-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a9629-150">RELATED LINKS</span></span>
