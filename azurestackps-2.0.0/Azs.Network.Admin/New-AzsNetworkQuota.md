---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/new-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: 554ebe0e6c4ef8a4b0d262071595c0dc6336f482
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923109"
---
# <span data-ttu-id="99ce3-101">New-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="99ce3-101">New-AzsNetworkQuota</span></span>

## <span data-ttu-id="99ce3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="99ce3-102">SYNOPSIS</span></span>
<span data-ttu-id="99ce3-103">Skapa eller uppdatera en kvot.</span><span class="sxs-lookup"><span data-stu-id="99ce3-103">Create or update a quota.</span></span>

## <span data-ttu-id="99ce3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="99ce3-104">SYNTAX</span></span>

### <span data-ttu-id="99ce3-105">CreateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="99ce3-105">CreateExpanded (Default)</span></span>
```
New-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-MaxNicsPerSubscription <Int64>]
 [-MaxPublicIpsPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="99ce3-106">Göra</span><span class="sxs-lookup"><span data-stu-id="99ce3-106">Create</span></span>
```
New-AzsNetworkQuota -Name <String> -Quota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="99ce3-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="99ce3-107">CreateViaIdentity</span></span>
```
New-AzsNetworkQuota -InputObject <INetworkAdminIdentity> -Quota <IQuota> [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="99ce3-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="99ce3-108">CreateViaIdentityExpanded</span></span>
```
New-AzsNetworkQuota -InputObject <INetworkAdminIdentity> [-MaxLoadBalancersPerSubscription <Int64>]
 [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxSecurityGroupsPerSubscription <Int64>] [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="99ce3-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="99ce3-109">DESCRIPTION</span></span>
<span data-ttu-id="99ce3-110">Skapa eller uppdatera en kvot.</span><span class="sxs-lookup"><span data-stu-id="99ce3-110">Create or update a quota.</span></span>

## <span data-ttu-id="99ce3-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="99ce3-111">EXAMPLES</span></span>

### <span data-ttu-id="99ce3-112">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="99ce3-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsNetworkQuota -Name NetworkQuotaDefaultValues
```

<span data-ttu-id="99ce3-113">Skapa en ny nätverks kvot med alla standardvärden.</span><span class="sxs-lookup"><span data-stu-id="99ce3-113">Create a new network quota with all the default values.</span></span>

### <span data-ttu-id="99ce3-114">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="99ce3-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
New-AzsNetworkQuota -Name NetworkQuota1 -MaxNicsPerSubscription 150 -MaxPublicIpsPerSubscription 150
```
<span data-ttu-id="99ce3-115">Skapa en ny nätverks kvot med icke-standardvärden för kvot.</span><span class="sxs-lookup"><span data-stu-id="99ce3-115">Create a new network quota with non default values for quota.</span></span>



## <span data-ttu-id="99ce3-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="99ce3-116">PARAMETERS</span></span>

### <span data-ttu-id="99ce3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99ce3-117">-DefaultProfile</span></span>
<span data-ttu-id="99ce3-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="99ce3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99ce3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99ce3-119">-InputObject</span></span>
<span data-ttu-id="99ce3-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="99ce3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: CreateViaIdentity, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="99ce3-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="99ce3-121">-Location</span></span>
<span data-ttu-id="99ce3-122">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="99ce3-122">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="99ce3-123">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="99ce3-123">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="99ce3-124">Maximalt antal belastningsutjämnaren som ett klient abonnemang kan etablera.</span><span class="sxs-lookup"><span data-stu-id="99ce3-124">Maximum number of load balancers a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="99ce3-125">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="99ce3-125">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="99ce3-126">Maximalt antal nätverkskort ett klient organisations abonnemang kan etablera.</span><span class="sxs-lookup"><span data-stu-id="99ce3-126">Maximum number of NICs a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="99ce3-127">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="99ce3-127">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="99ce3-128">Maximalt antal offentliga IP-adresser ett klient organisations abonnemang kan etablera.</span><span class="sxs-lookup"><span data-stu-id="99ce3-128">Maximum number of public IP addresses a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="99ce3-129">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="99ce3-129">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="99ce3-130">Maximalt antal säkerhets grupper som ett klient organisations abonnemang kan etablera.</span><span class="sxs-lookup"><span data-stu-id="99ce3-130">Maximum number of security groups a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="99ce3-131">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="99ce3-131">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="99ce3-132">Maximalt antal virtuella Nätverksgatewayen som ett klient abonnemang kan etablera.</span><span class="sxs-lookup"><span data-stu-id="99ce3-132">Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="99ce3-133">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="99ce3-133">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="99ce3-134">Maximalt antal virtuella nätverks-gateways som ett klient organisations abonnemang kan etablera.</span><span class="sxs-lookup"><span data-stu-id="99ce3-134">Maximum number of virtual network gateways a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="99ce3-135">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="99ce3-135">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="99ce3-136">Maximalt antal virtuella nätverk som en klient organisations prenumeration kan etablera.</span><span class="sxs-lookup"><span data-stu-id="99ce3-136">Maximum number of virtual networks a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="99ce3-137">-Namn</span><span class="sxs-lookup"><span data-stu-id="99ce3-137">-Name</span></span>
<span data-ttu-id="99ce3-138">Namnet på resursen.</span><span class="sxs-lookup"><span data-stu-id="99ce3-138">Name of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="99ce3-139">-Kvot</span><span class="sxs-lookup"><span data-stu-id="99ce3-139">-Quota</span></span>
<span data-ttu-id="99ce3-140">Nätverks kvot resurs.</span><span class="sxs-lookup"><span data-stu-id="99ce3-140">Network quota resource.</span></span>
<span data-ttu-id="99ce3-141">Om du vill skapa läser du avsnittet anteckningar för kvot egenskaper och skapar en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="99ce3-141">To construct, see NOTES section for QUOTA properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="99ce3-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="99ce3-142">-SubscriptionId</span></span>
<span data-ttu-id="99ce3-143">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="99ce3-143">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="99ce3-144">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="99ce3-144">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="99ce3-145">-Tagg</span><span class="sxs-lookup"><span data-stu-id="99ce3-145">-Tag</span></span>
<span data-ttu-id="99ce3-146">Lista över värde par för nycklar.</span><span class="sxs-lookup"><span data-stu-id="99ce3-146">List of key value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="99ce3-147">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="99ce3-147">-Confirm</span></span>
<span data-ttu-id="99ce3-148">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="99ce3-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99ce3-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99ce3-149">-WhatIf</span></span>
<span data-ttu-id="99ce3-150">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="99ce3-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99ce3-151">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="99ce3-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99ce3-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99ce3-152">CommonParameters</span></span>
<span data-ttu-id="99ce3-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99ce3-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99ce3-154">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99ce3-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99ce3-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="99ce3-155">INPUTS</span></span>

### <span data-ttu-id="99ce3-156">Microsoft. Azure. PowerShell. cmdletar. NetworkAdmin. Models. Api20150615. IQuota</span><span class="sxs-lookup"><span data-stu-id="99ce3-156">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>

### <span data-ttu-id="99ce3-157">Microsoft. Azure. PowerShell. cmdletar. NetworkAdmin. Models. INetworkAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="99ce3-157">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="99ce3-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="99ce3-158">OUTPUTS</span></span>

### <span data-ttu-id="99ce3-159">Microsoft. Azure. PowerShell. cmdletar. NetworkAdmin. Models. Api20150615. IQuota</span><span class="sxs-lookup"><span data-stu-id="99ce3-159">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>



## <span data-ttu-id="99ce3-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="99ce3-160">NOTES</span></span>

<span data-ttu-id="99ce3-161">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="99ce3-161">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="99ce3-162">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="99ce3-162">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="99ce3-163">INPUTOBJECT <INetworkAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="99ce3-163">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="99ce3-164">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="99ce3-164">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="99ce3-165">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="99ce3-165">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="99ce3-166">`[ResourceName <String>]`: Namnet på resursen.</span><span class="sxs-lookup"><span data-stu-id="99ce3-166">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="99ce3-167">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="99ce3-167">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="99ce3-168">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="99ce3-168">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="99ce3-169">KVOT <IQuota> : nätverks kvot resurs.</span><span class="sxs-lookup"><span data-stu-id="99ce3-169">QUOTA <IQuota>: Network quota resource.</span></span>
  - <span data-ttu-id="99ce3-170">`[Tag <IResourceTags>]`: Lista med värde par för nycklar.</span><span class="sxs-lookup"><span data-stu-id="99ce3-170">`[Tag <IResourceTags>]`: List of key value pairs.</span></span>
    - <span data-ttu-id="99ce3-171">`[(Any) <String>]`: Detta indikerar att en egenskap kan läggas till i det här objektet.</span><span class="sxs-lookup"><span data-stu-id="99ce3-171">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="99ce3-172">`[MaxLoadBalancersPerSubscription <Int64?>]`: Det högsta antalet belastningsutjämnare som ett klient abonnemang kan etablera.</span><span class="sxs-lookup"><span data-stu-id="99ce3-172">`[MaxLoadBalancersPerSubscription <Int64?>]`: Maximum number of load balancers a tenant subscription can provision.</span></span>
  - <span data-ttu-id="99ce3-173">`[MaxNicsPerSubscription <Int64?>]`: Maximalt antal nätverkskort ett klient organisations abonnemang kan etablera.</span><span class="sxs-lookup"><span data-stu-id="99ce3-173">`[MaxNicsPerSubscription <Int64?>]`: Maximum number of NICs a tenant subscription can provision.</span></span>
  - <span data-ttu-id="99ce3-174">`[MaxPublicIpsPerSubscription <Int64?>]`: Det högsta antalet offentliga IP-adresser som ett klient organisations abonnemang kan etablera.</span><span class="sxs-lookup"><span data-stu-id="99ce3-174">`[MaxPublicIpsPerSubscription <Int64?>]`: Maximum number of public IP addresses a tenant subscription can provision.</span></span>
  - <span data-ttu-id="99ce3-175">`[MaxSecurityGroupsPerSubscription <Int64?>]`: Maximalt antal säkerhets grupper ett klient organisations abonnemang kan etablera.</span><span class="sxs-lookup"><span data-stu-id="99ce3-175">`[MaxSecurityGroupsPerSubscription <Int64?>]`: Maximum number of security groups a tenant subscription can provision.</span></span>
  - <span data-ttu-id="99ce3-176">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: Högsta antal anslutningar för virtuella nätverk som ett klient abonnemang kan etablera.</span><span class="sxs-lookup"><span data-stu-id="99ce3-176">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>
  - <span data-ttu-id="99ce3-177">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Det högsta antalet virtuella nätverks-gateways som ett klient organisations abonnemang kan etablera.</span><span class="sxs-lookup"><span data-stu-id="99ce3-177">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Maximum number of virtual network gateways a tenant subscription can provision.</span></span>
  - <span data-ttu-id="99ce3-178">`[MaxVnetsPerSubscription <Int64?>]`: Maximalt antal virtuella nätverk ett klient organisations abonnemang kan etablera.</span><span class="sxs-lookup"><span data-stu-id="99ce3-178">`[MaxVnetsPerSubscription <Int64?>]`: Maximum number of virtual networks a tenant subscription can provision.</span></span>

## <span data-ttu-id="99ce3-179">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="99ce3-179">RELATED LINKS</span></span>
