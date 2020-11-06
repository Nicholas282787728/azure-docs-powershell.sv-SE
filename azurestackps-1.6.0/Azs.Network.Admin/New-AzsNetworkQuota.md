---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: afc762c4b7d932f682f77e2df6586c773e0f22e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572240"
---
# <span data-ttu-id="27312-101">New-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="27312-101">New-AzsNetworkQuota</span></span>

## <span data-ttu-id="27312-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="27312-102">SYNOPSIS</span></span>
<span data-ttu-id="27312-103">Skapa eller uppdatera en kvot.</span><span class="sxs-lookup"><span data-stu-id="27312-103">Create or update a quota.</span></span>

## <span data-ttu-id="27312-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="27312-104">SYNTAX</span></span>

```
New-AzsNetworkQuota [-Name] <String> [[-MaxNicsPerSubscription] <Int64>]
 [[-MaxPublicIpsPerSubscription] <Int64>] [[-MaxVirtualNetworkGatewayConnectionsPerSubscription] <Int64>]
 [[-MaxVnetsPerSubscription] <Int64>] [[-MaxVirtualNetworkGatewaysPerSubscription] <Int64>]
 [[-MaxSecurityGroupsPerSubscription] <Int64>] [[-MaxLoadBalancersPerSubscription] <Int64>]
 [[-Location] <String>] [[-MigrationPhase] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27312-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="27312-105">DESCRIPTION</span></span>
<span data-ttu-id="27312-106">Skapa eller uppdatera en kvot.</span><span class="sxs-lookup"><span data-stu-id="27312-106">Create or update a quota.</span></span>

## <span data-ttu-id="27312-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="27312-107">EXAMPLES</span></span>

### <span data-ttu-id="27312-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="27312-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsNetworkQuota -Name NetworkQuotaDefaultValues
```

<span data-ttu-id="27312-109">Skapa en ny nätverks kvot med alla standardvärden.</span><span class="sxs-lookup"><span data-stu-id="27312-109">Create a new network quota with all the default values.</span></span>

### <span data-ttu-id="27312-110">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="27312-110">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
New-AzsNetworkQuota -Name NetworkQuota1 -MaxNicsPerSubscription 150 -MaxPublicIpsPerSubscription 150
```

<span data-ttu-id="27312-111">Skapa en ny nätverks kvot med icke-standardvärden för kvot.</span><span class="sxs-lookup"><span data-stu-id="27312-111">Create a new network quota with non default values for quota.</span></span>

## <span data-ttu-id="27312-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="27312-112">PARAMETERS</span></span>

### <span data-ttu-id="27312-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="27312-113">-Location</span></span>
<span data-ttu-id="27312-114">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="27312-114">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27312-115">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="27312-115">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="27312-116">Maximalt antal belastnings utjämningar tillåtna per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="27312-116">The maximum number of load balancers allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27312-117">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="27312-117">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="27312-118">Högsta tillåtna NIC per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="27312-118">The maximum NICs allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27312-119">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="27312-119">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="27312-120">Högsta tillåtna offentliga IP-adresser per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="27312-120">The maximum public IP addresses allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27312-121">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="27312-121">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="27312-122">Maximalt antal tillåtna säkerhets grupper per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="27312-122">The maximum number of security groups allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27312-123">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="27312-123">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="27312-124">Det högsta antalet anslutningar för virtuell nätverksgateway som tillåts per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="27312-124">The maximum number of virtual network gateway connections allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27312-125">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="27312-125">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="27312-126">Maximalt antal virtuella nätverksgateway per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="27312-126">The maximum number of virtual network gateways allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27312-127">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="27312-127">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="27312-128">Maxium antal virtuella nätverk som tillåts per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="27312-128">The maxium number of virtual networks allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27312-129">-MigrationPhase</span><span class="sxs-lookup"><span data-stu-id="27312-129">-MigrationPhase</span></span>
<span data-ttu-id="27312-130">Inaktuella.</span><span class="sxs-lookup"><span data-stu-id="27312-130">Deprecated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: Prepare
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27312-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="27312-131">-Name</span></span>
<span data-ttu-id="27312-132">Namn på nätverks kvot resursen.</span><span class="sxs-lookup"><span data-stu-id="27312-132">Name of the network quota resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27312-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="27312-133">-Confirm</span></span>
<span data-ttu-id="27312-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="27312-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27312-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27312-135">-WhatIf</span></span>
<span data-ttu-id="27312-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="27312-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27312-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="27312-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27312-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27312-138">CommonParameters</span></span>
<span data-ttu-id="27312-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27312-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27312-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27312-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27312-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="27312-141">INPUTS</span></span>

## <span data-ttu-id="27312-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="27312-142">OUTPUTS</span></span>

### <span data-ttu-id="27312-143">Microsoft. AzureStack. Management. Network. admin. Models. quota</span><span class="sxs-lookup"><span data-stu-id="27312-143">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="27312-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="27312-144">NOTES</span></span>

## <span data-ttu-id="27312-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="27312-145">RELATED LINKS</span></span>

