---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2867f0c438f1f8752137f680365ecade255d291
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571576"
---
# <span data-ttu-id="9fa70-101">Set-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="9fa70-101">Set-AzsNetworkQuota</span></span>

## <span data-ttu-id="9fa70-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9fa70-102">SYNOPSIS</span></span>
<span data-ttu-id="9fa70-103">Skapa eller uppdatera en kvot.</span><span class="sxs-lookup"><span data-stu-id="9fa70-103">Create or update a quota.</span></span>

## <span data-ttu-id="9fa70-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9fa70-104">SYNTAX</span></span>

### <span data-ttu-id="9fa70-105">Kvoter (standard)</span><span class="sxs-lookup"><span data-stu-id="9fa70-105">Quotas (Default)</span></span>
```
Set-AzsNetworkQuota -Name <String> [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fa70-106">ID</span><span class="sxs-lookup"><span data-stu-id="9fa70-106">ResourceId</span></span>
```
Set-AzsNetworkQuota [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fa70-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="9fa70-107">InputObject</span></span>
```
Set-AzsNetworkQuota [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] -InputObject <Quota> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fa70-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9fa70-108">DESCRIPTION</span></span>
<span data-ttu-id="9fa70-109">Skapa eller uppdatera en kvot.</span><span class="sxs-lookup"><span data-stu-id="9fa70-109">Create or update a quota.</span></span>

## <span data-ttu-id="9fa70-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9fa70-110">EXAMPLES</span></span>

### <span data-ttu-id="9fa70-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9fa70-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxVnetsPerSubscription 20
```

<span data-ttu-id="9fa70-112">Uppdatera en nätverks kvot efter namn.</span><span class="sxs-lookup"><span data-stu-id="9fa70-112">Update a network quota by name.</span></span>

### <span data-ttu-id="9fa70-113">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="9fa70-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxPublicIpsPerSubscription 75 -MaxNicsPerSubscription 100
```

<span data-ttu-id="9fa70-114">Uppdatera en nätverks kvot efter namn.</span><span class="sxs-lookup"><span data-stu-id="9fa70-114">Update a network quota by name.</span></span>

## <span data-ttu-id="9fa70-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9fa70-115">PARAMETERS</span></span>

### <span data-ttu-id="9fa70-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9fa70-116">-InputObject</span></span>
<span data-ttu-id="9fa70-117">Posbbily ändrade nätverks kvot som returnerats av Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="9fa70-117">Posbbily modified network quota returned by Get-AzsNetworkQuota</span></span>

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

### <span data-ttu-id="9fa70-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="9fa70-118">-Location</span></span>
<span data-ttu-id="9fa70-119">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="9fa70-119">Location of the resource.</span></span>

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

### <span data-ttu-id="9fa70-120">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="9fa70-120">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="9fa70-121">Maximalt antal belastnings utjämningar tillåtna per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="9fa70-121">The maximum number of load balancers allowed per subscription.</span></span>

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

### <span data-ttu-id="9fa70-122">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="9fa70-122">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="9fa70-123">Högsta tillåtna NIC per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="9fa70-123">The maximum NICs allowed per subscription.</span></span>

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

### <span data-ttu-id="9fa70-124">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="9fa70-124">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="9fa70-125">Högsta tillåtna offentliga IP-adresser per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="9fa70-125">The maximum public IP addresses allowed per subscription.</span></span>

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

### <span data-ttu-id="9fa70-126">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="9fa70-126">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="9fa70-127">Maximalt antal tillåtna säkerhets grupper per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="9fa70-127">The maximum number of security groups allowed per subscription.</span></span>

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

### <span data-ttu-id="9fa70-128">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="9fa70-128">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="9fa70-129">Det högsta antalet anslutningar för virtuell nätverksgateway som tillåts per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="9fa70-129">The maximum number of virtual network gateway connections allowed per subscription.</span></span>

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

### <span data-ttu-id="9fa70-130">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="9fa70-130">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="9fa70-131">Maximalt antal virtuella nätverksgateway per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="9fa70-131">The maximum number of virtual network gateways allowed per subscription.</span></span>

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

### <span data-ttu-id="9fa70-132">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="9fa70-132">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="9fa70-133">Maxium antal virtuella nätverk som tillåts per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="9fa70-133">The maxium number of virtual networks allowed per subscription.</span></span>

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

### <span data-ttu-id="9fa70-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="9fa70-134">-Name</span></span>
<span data-ttu-id="9fa70-135">Namnet på resursen.</span><span class="sxs-lookup"><span data-stu-id="9fa70-135">Name of the resource.</span></span>

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

### <span data-ttu-id="9fa70-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9fa70-136">-ResourceId</span></span>
<span data-ttu-id="9fa70-137">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="9fa70-137">The resource id.</span></span>

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

### <span data-ttu-id="9fa70-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9fa70-138">-Confirm</span></span>
<span data-ttu-id="9fa70-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9fa70-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fa70-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fa70-140">-WhatIf</span></span>
<span data-ttu-id="9fa70-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9fa70-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fa70-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9fa70-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fa70-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fa70-143">CommonParameters</span></span>
<span data-ttu-id="9fa70-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fa70-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fa70-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fa70-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fa70-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9fa70-146">INPUTS</span></span>

## <span data-ttu-id="9fa70-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9fa70-147">OUTPUTS</span></span>

### <span data-ttu-id="9fa70-148">Microsoft. AzureStack. Management. Network. admin. Models. quota</span><span class="sxs-lookup"><span data-stu-id="9fa70-148">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="9fa70-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9fa70-149">NOTES</span></span>

## <span data-ttu-id="9fa70-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9fa70-150">RELATED LINKS</span></span>

