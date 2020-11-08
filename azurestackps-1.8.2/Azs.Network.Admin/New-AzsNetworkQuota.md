---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: acda4a136b98a8a83190704a3635bd97ae97a7b2
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100045"
---
# <span data-ttu-id="5f86e-101">New-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="5f86e-101">New-AzsNetworkQuota</span></span>

## <span data-ttu-id="5f86e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5f86e-102">SYNOPSIS</span></span>
<span data-ttu-id="5f86e-103">Skapa eller uppdatera en kvot.</span><span class="sxs-lookup"><span data-stu-id="5f86e-103">Create or update a quota.</span></span>

## <span data-ttu-id="5f86e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5f86e-104">SYNTAX</span></span>

```
New-AzsNetworkQuota [-Name] <String> [[-MaxNicsPerSubscription] <Int64>]
 [[-MaxPublicIpsPerSubscription] <Int64>] [[-MaxVirtualNetworkGatewayConnectionsPerSubscription] <Int64>]
 [[-MaxVnetsPerSubscription] <Int64>] [[-MaxVirtualNetworkGatewaysPerSubscription] <Int64>]
 [[-MaxSecurityGroupsPerSubscription] <Int64>] [[-MaxLoadBalancersPerSubscription] <Int64>]
 [[-Location] <String>] [[-MigrationPhase] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f86e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5f86e-105">DESCRIPTION</span></span>
<span data-ttu-id="5f86e-106">Skapa eller uppdatera en kvot.</span><span class="sxs-lookup"><span data-stu-id="5f86e-106">Create or update a quota.</span></span>

## <span data-ttu-id="5f86e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5f86e-107">EXAMPLES</span></span>

### <span data-ttu-id="5f86e-108">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="5f86e-108">EXAMPLE 1</span></span>
```
New-AzsNetworkQuota -Name NetworkQuotaDefaultValues
```

<span data-ttu-id="5f86e-109">Skapa en ny nätverks kvot med alla standardvärden.</span><span class="sxs-lookup"><span data-stu-id="5f86e-109">Create a new network quota with all the default values.</span></span>

### <span data-ttu-id="5f86e-110">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="5f86e-110">EXAMPLE 2</span></span>
```
New-AzsNetworkQuota -Name NetworkQuota1 -MaxNicsPerSubscription 150 -MaxPublicIpsPerSubscription 150
```

<span data-ttu-id="5f86e-111">Skapa en ny nätverks kvot med icke-standardvärden för kvot.</span><span class="sxs-lookup"><span data-stu-id="5f86e-111">Create a new network quota with non default values for quota.</span></span>

## <span data-ttu-id="5f86e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5f86e-112">PARAMETERS</span></span>

### <span data-ttu-id="5f86e-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="5f86e-113">-Name</span></span>
<span data-ttu-id="5f86e-114">Namn på nätverks kvot resursen.</span><span class="sxs-lookup"><span data-stu-id="5f86e-114">Name of the network quota resource.</span></span>

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

### <span data-ttu-id="5f86e-115">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="5f86e-115">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="5f86e-116">Högsta tillåtna NIC per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="5f86e-116">The maximum NICs allowed per subscription.</span></span>

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

### <span data-ttu-id="5f86e-117">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="5f86e-117">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="5f86e-118">Högsta tillåtna offentliga IP-adresser per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="5f86e-118">The maximum public IP addresses allowed per subscription.</span></span>

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

### <span data-ttu-id="5f86e-119">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="5f86e-119">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="5f86e-120">Det högsta antalet anslutningar för virtuell nätverksgateway som tillåts per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="5f86e-120">The maximum number of virtual network gateway connections allowed per subscription.</span></span>

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

### <span data-ttu-id="5f86e-121">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="5f86e-121">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="5f86e-122">Maxium antal virtuella nätverk som tillåts per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="5f86e-122">The maxium number of virtual networks allowed per subscription.</span></span>

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

### <span data-ttu-id="5f86e-123">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="5f86e-123">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="5f86e-124">Maximalt antal virtuella nätverksgateway per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="5f86e-124">The maximum number of virtual network gateways allowed per subscription.</span></span>

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

### <span data-ttu-id="5f86e-125">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="5f86e-125">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="5f86e-126">Maximalt antal tillåtna säkerhets grupper per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="5f86e-126">The maximum number of security groups allowed per subscription.</span></span>

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

### <span data-ttu-id="5f86e-127">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="5f86e-127">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="5f86e-128">Maximalt antal belastnings utjämningar tillåtna per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="5f86e-128">The maximum number of load balancers allowed per subscription.</span></span>

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

### <span data-ttu-id="5f86e-129">-Plats</span><span class="sxs-lookup"><span data-stu-id="5f86e-129">-Location</span></span>
<span data-ttu-id="5f86e-130">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="5f86e-130">Location of the resource.</span></span>

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

### <span data-ttu-id="5f86e-131">-MigrationPhase</span><span class="sxs-lookup"><span data-stu-id="5f86e-131">-MigrationPhase</span></span>
<span data-ttu-id="5f86e-132">Delstaten som ingen, förbereda, genomföra och avbryta.</span><span class="sxs-lookup"><span data-stu-id="5f86e-132">State of migration such as None, Prepare, Commit, and Abort.</span></span>

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

### <span data-ttu-id="5f86e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f86e-133">-WhatIf</span></span>
<span data-ttu-id="5f86e-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5f86e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f86e-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5f86e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f86e-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5f86e-136">-Confirm</span></span>
<span data-ttu-id="5f86e-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5f86e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f86e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f86e-138">CommonParameters</span></span>
<span data-ttu-id="5f86e-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f86e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f86e-140">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f86e-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f86e-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5f86e-141">INPUTS</span></span>

## <span data-ttu-id="5f86e-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5f86e-142">OUTPUTS</span></span>

### <span data-ttu-id="5f86e-143">Microsoft. AzureStack. Management. Network. admin. Models. quota</span><span class="sxs-lookup"><span data-stu-id="5f86e-143">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="5f86e-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5f86e-144">NOTES</span></span>

## <span data-ttu-id="5f86e-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5f86e-145">RELATED LINKS</span></span>
