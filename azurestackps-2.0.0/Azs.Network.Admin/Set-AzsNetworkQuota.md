---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/set-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: c2cc0e7a22d7e581eece9004950b54bc0151fad3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923098"
---
# <span data-ttu-id="75887-101">Set-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="75887-101">Set-AzsNetworkQuota</span></span>

## <span data-ttu-id="75887-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="75887-102">SYNOPSIS</span></span>
<span data-ttu-id="75887-103">Skapa eller uppdatera en kvot.</span><span class="sxs-lookup"><span data-stu-id="75887-103">Create or update a quota.</span></span>

## <span data-ttu-id="75887-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="75887-104">SYNTAX</span></span>

### <span data-ttu-id="75887-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="75887-105">UpdateExpanded (Default)</span></span>
```
Set-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-MaxNicsPerSubscription <Int64>]
 [-MaxPublicIpsPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="75887-106">Uppdatera</span><span class="sxs-lookup"><span data-stu-id="75887-106">Update</span></span>
```
Set-AzsNetworkQuota -Name <String> -Quota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="75887-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="75887-107">DESCRIPTION</span></span>
<span data-ttu-id="75887-108">Skapa eller uppdatera en kvot.</span><span class="sxs-lookup"><span data-stu-id="75887-108">Create or update a quota.</span></span>

## <span data-ttu-id="75887-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="75887-109">EXAMPLES</span></span>

### <span data-ttu-id="75887-110">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="75887-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxVnetsPerSubscription 20
```

<span data-ttu-id="75887-111">Uppdatera en nätverks kvot efter namn.</span><span class="sxs-lookup"><span data-stu-id="75887-111">Update a network quota by name.</span></span>

### <span data-ttu-id="75887-112">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="75887-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxPublicIpsPerSubscription 75 -MaxNicsPerSubscription 100
```

<span data-ttu-id="75887-113">Uppdatera en nätverks kvot efter namn.</span><span class="sxs-lookup"><span data-stu-id="75887-113">Update a network quota by name.</span></span>

## <span data-ttu-id="75887-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="75887-114">PARAMETERS</span></span>

### <span data-ttu-id="75887-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75887-115">-DefaultProfile</span></span>
<span data-ttu-id="75887-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="75887-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="75887-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="75887-117">-Location</span></span>
<span data-ttu-id="75887-118">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="75887-118">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="75887-119">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="75887-119">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="75887-120">Maximalt antal belastningsutjämnaren som ett klient abonnemang kan etablera.</span><span class="sxs-lookup"><span data-stu-id="75887-120">Maximum number of load balancers a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="75887-121">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="75887-121">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="75887-122">Maximalt antal nätverkskort ett klient organisations abonnemang kan etablera.</span><span class="sxs-lookup"><span data-stu-id="75887-122">Maximum number of NICs a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="75887-123">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="75887-123">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="75887-124">Maximalt antal offentliga IP-adresser ett klient organisations abonnemang kan etablera.</span><span class="sxs-lookup"><span data-stu-id="75887-124">Maximum number of public IP addresses a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="75887-125">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="75887-125">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="75887-126">Maximalt antal säkerhets grupper som ett klient organisations abonnemang kan etablera.</span><span class="sxs-lookup"><span data-stu-id="75887-126">Maximum number of security groups a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="75887-127">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="75887-127">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="75887-128">Maximalt antal virtuella Nätverksgatewayen som ett klient abonnemang kan etablera.</span><span class="sxs-lookup"><span data-stu-id="75887-128">Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="75887-129">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="75887-129">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="75887-130">Maximalt antal virtuella nätverks-gateways som ett klient organisations abonnemang kan etablera.</span><span class="sxs-lookup"><span data-stu-id="75887-130">Maximum number of virtual network gateways a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="75887-131">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="75887-131">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="75887-132">Maximalt antal virtuella nätverk som en klient organisations prenumeration kan etablera.</span><span class="sxs-lookup"><span data-stu-id="75887-132">Maximum number of virtual networks a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="75887-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="75887-133">-Name</span></span>
<span data-ttu-id="75887-134">Namnet på resursen.</span><span class="sxs-lookup"><span data-stu-id="75887-134">Name of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="75887-135">-Kvot</span><span class="sxs-lookup"><span data-stu-id="75887-135">-Quota</span></span>
<span data-ttu-id="75887-136">Nätverks kvot resurs.</span><span class="sxs-lookup"><span data-stu-id="75887-136">Network quota resource.</span></span>
<span data-ttu-id="75887-137">Om du vill skapa läser du avsnittet anteckningar för kvot egenskaper och skapar en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="75887-137">To construct, see NOTES section for QUOTA properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="75887-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="75887-138">-SubscriptionId</span></span>
<span data-ttu-id="75887-139">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="75887-139">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="75887-140">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="75887-140">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="75887-141">-Tagg</span><span class="sxs-lookup"><span data-stu-id="75887-141">-Tag</span></span>
<span data-ttu-id="75887-142">Lista över värde par för nycklar.</span><span class="sxs-lookup"><span data-stu-id="75887-142">List of key value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="75887-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="75887-143">-Confirm</span></span>
<span data-ttu-id="75887-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="75887-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="75887-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75887-145">-WhatIf</span></span>
<span data-ttu-id="75887-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="75887-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75887-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="75887-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="75887-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75887-148">CommonParameters</span></span>
<span data-ttu-id="75887-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75887-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75887-150">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75887-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75887-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="75887-151">INPUTS</span></span>

### <span data-ttu-id="75887-152">Microsoft. Azure. PowerShell. cmdletar. NetworkAdmin. Models. Api20150615. IQuota</span><span class="sxs-lookup"><span data-stu-id="75887-152">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>

## <span data-ttu-id="75887-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="75887-153">OUTPUTS</span></span>

### <span data-ttu-id="75887-154">Microsoft. Azure. PowerShell. cmdletar. NetworkAdmin. Models. Api20150615. IQuota</span><span class="sxs-lookup"><span data-stu-id="75887-154">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>



## <span data-ttu-id="75887-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="75887-155">NOTES</span></span>

<span data-ttu-id="75887-156">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="75887-156">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="75887-157">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="75887-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="75887-158">KVOT <IQuota> : nätverks kvot resurs.</span><span class="sxs-lookup"><span data-stu-id="75887-158">QUOTA <IQuota>: Network quota resource.</span></span>
  - <span data-ttu-id="75887-159">`[Tag <IResourceTags>]`: Lista med värde par för nycklar.</span><span class="sxs-lookup"><span data-stu-id="75887-159">`[Tag <IResourceTags>]`: List of key value pairs.</span></span>
    - <span data-ttu-id="75887-160">`[(Any) <String>]`: Detta indikerar att en egenskap kan läggas till i det här objektet.</span><span class="sxs-lookup"><span data-stu-id="75887-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="75887-161">`[MaxLoadBalancersPerSubscription <Int64?>]`: Det högsta antalet belastningsutjämnare som ett klient abonnemang kan etablera.</span><span class="sxs-lookup"><span data-stu-id="75887-161">`[MaxLoadBalancersPerSubscription <Int64?>]`: Maximum number of load balancers a tenant subscription can provision.</span></span>
  - <span data-ttu-id="75887-162">`[MaxNicsPerSubscription <Int64?>]`: Maximalt antal nätverkskort ett klient organisations abonnemang kan etablera.</span><span class="sxs-lookup"><span data-stu-id="75887-162">`[MaxNicsPerSubscription <Int64?>]`: Maximum number of NICs a tenant subscription can provision.</span></span>
  - <span data-ttu-id="75887-163">`[MaxPublicIpsPerSubscription <Int64?>]`: Det högsta antalet offentliga IP-adresser som ett klient organisations abonnemang kan etablera.</span><span class="sxs-lookup"><span data-stu-id="75887-163">`[MaxPublicIpsPerSubscription <Int64?>]`: Maximum number of public IP addresses a tenant subscription can provision.</span></span>
  - <span data-ttu-id="75887-164">`[MaxSecurityGroupsPerSubscription <Int64?>]`: Maximalt antal säkerhets grupper ett klient organisations abonnemang kan etablera.</span><span class="sxs-lookup"><span data-stu-id="75887-164">`[MaxSecurityGroupsPerSubscription <Int64?>]`: Maximum number of security groups a tenant subscription can provision.</span></span>
  - <span data-ttu-id="75887-165">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: Högsta antal anslutningar för virtuella nätverk som ett klient abonnemang kan etablera.</span><span class="sxs-lookup"><span data-stu-id="75887-165">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>
  - <span data-ttu-id="75887-166">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Det högsta antalet virtuella nätverks-gateways som ett klient organisations abonnemang kan etablera.</span><span class="sxs-lookup"><span data-stu-id="75887-166">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Maximum number of virtual network gateways a tenant subscription can provision.</span></span>
  - <span data-ttu-id="75887-167">`[MaxVnetsPerSubscription <Int64?>]`: Maximalt antal virtuella nätverk ett klient organisations abonnemang kan etablera.</span><span class="sxs-lookup"><span data-stu-id="75887-167">`[MaxVnetsPerSubscription <Int64?>]`: Maximum number of virtual networks a tenant subscription can provision.</span></span>

## <span data-ttu-id="75887-168">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="75887-168">RELATED LINKS</span></span>

