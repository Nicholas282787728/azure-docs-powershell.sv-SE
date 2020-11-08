---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteConnection.md
ms.openlocfilehash: 565e79420821e8d8764b5e461e33d275247ddb3c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271768"
---
# <span data-ttu-id="62e52-101">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="62e52-101">New-AzExpressRouteConnection</span></span>

## <span data-ttu-id="62e52-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="62e52-102">SYNOPSIS</span></span>
<span data-ttu-id="62e52-103">Skapar en ExpressRoute-anslutning som ansluter en ExpressRoute Gateway till en lokal ExpressRoute-krets</span><span class="sxs-lookup"><span data-stu-id="62e52-103">Creates an ExpressRoute connection that connects an ExpressRoute gateway to an on premise ExpressRoute circuit</span></span>

## <span data-ttu-id="62e52-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="62e52-104">SYNTAX</span></span>

### <span data-ttu-id="62e52-105">ByExpressRouteGatewayName (standard)</span><span class="sxs-lookup"><span data-stu-id="62e52-105">ByExpressRouteGatewayName (Default)</span></span>
```
New-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 -ExpressRouteCircuitPeeringId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62e52-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="62e52-106">ByExpressRouteGatewayObject</span></span>
```
New-AzExpressRouteConnection -ExpressRouteGatewayObject <PSExpressRouteGateway> -Name <String>
 -ExpressRouteCircuitPeeringId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62e52-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="62e52-107">ByExpressRouteGatewayResourceId</span></span>
```
New-AzExpressRouteConnection -ParentResourceId <String> -Name <String> -ExpressRouteCircuitPeeringId <String>
 [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62e52-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="62e52-108">DESCRIPTION</span></span>
<span data-ttu-id="62e52-109">Skapar en ExpressRoute-anslutning mellan en lokal ExpressRoute-krets med BGP-peering till ExpressRoute gateway i ett virtuellt nav.</span><span class="sxs-lookup"><span data-stu-id="62e52-109">Creates an ExpressRoute connection between an on-premise ExpressRoute circuit BGP peering to the ExpressRoute gateway inside a Virtual hub.</span></span>

## <span data-ttu-id="62e52-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="62e52-110">EXAMPLES</span></span>

### <span data-ttu-id="62e52-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="62e52-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> $ExpressRouteGateway = Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw"
PS C:\> $ExpressRouteCircuit = New-AzExpressRouteCircuit -ResourceGroupName "testRG" -Name "testExpressRouteCircuit" -Location "West Central US" -SkuTier Premium -SkuFamily MeteredData -ServiceProviderName "Equinix" -PeeringLocation "Silicon Valley" -BandwidthInMbps 200
PS C:\> Add-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ExpressRouteCircuit -PeeringType AzurePrivatePeering -PeerASN 100 -PrimaryPeerAddressPrefix "123.0.0.0/30" -SecondaryPeerAddressPrefix "123.0.0.4/30" -VlanId 300
PS C:\> $ExpressRouteCircuit = Set-AzExpressRouteCircuit -ExpressRouteCircuit $ExpressRouteCircuit
PS C:\> $ExpressRouteCircuitPeeringId = $ExpressRouteCircuit.Peerings[0].Id
PS C:\> New-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection" -ExpressRouteCircuitPeeringId $ExpressRouteCircuitPeeringId -RoutingWeight 20
ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection
Etag                               : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection
RoutingConfiguration               : {
                                       "AssociatedRouteTable": {
                                         "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                       },
                                       "PropagatedRouteTables": {
                                         "Labels": [],
                                         "Ids": [
                                           {
                                             "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                           }
                                         ]
                                       },
                                       "VnetRoutes": {
                                         "StaticRoutes": []
                                       }
                                     }
```

<span data-ttu-id="62e52-112">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav, ExpressRoute och en ExpressRoute-krets med privat peering i västra centrala USA i resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="62e52-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub, Express Route gateway and an ExpressRoute circuit with private peering in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="62e52-113">När gatewayen har skapats är den ansluten till ExpressRoute-kretsen med kommandot New-AzExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="62e52-113">Once the gateway has been created, it is connected to the ExpressRoute Circuit Peering using the New-AzExpressRouteConnection command.</span></span>

## <span data-ttu-id="62e52-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="62e52-114">PARAMETERS</span></span>

### <span data-ttu-id="62e52-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="62e52-115">-AsJob</span></span>
<span data-ttu-id="62e52-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="62e52-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e52-117">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="62e52-117">-AuthorizationKey</span></span>
<span data-ttu-id="62e52-118">En nyckeln från ExpressRoute-kretsen för att kunna skapa en anslutning till en gateway i ett annat abonnemang.</span><span class="sxs-lookup"><span data-stu-id="62e52-118">A key obtained from the ExpressRoute circuit owner to be able to create a connection with a gateway in a different subscription.</span></span>

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

### <span data-ttu-id="62e52-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62e52-119">-DefaultProfile</span></span>
<span data-ttu-id="62e52-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="62e52-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62e52-121">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="62e52-121">-EnableInternetSecurity</span></span>
<span data-ttu-id="62e52-122">Aktivera Internet säkerhet för denna ExpressRoute Gateway-anslutning</span><span class="sxs-lookup"><span data-stu-id="62e52-122">Enable internet security for this ExpressRoute Gateway connection</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e52-123">-ExpressRouteCircuitPeeringId</span><span class="sxs-lookup"><span data-stu-id="62e52-123">-ExpressRouteCircuitPeeringId</span></span>
<span data-ttu-id="62e52-124">Resurs-ID för den ExpressRoute-krets som den här ExpressRoute-anslutningen för snabb vägen ska skapas till.</span><span class="sxs-lookup"><span data-stu-id="62e52-124">The resource id of the Express Route Circuit Peering to which this Express Route gateway connection is to be created to.</span></span>

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

### <span data-ttu-id="62e52-125">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="62e52-125">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="62e52-126">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="62e52-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e52-127">-ExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="62e52-127">-ExpressRouteGatewayObject</span></span>
<span data-ttu-id="62e52-128">Den överordnade ExpressRouteGateway för den här anslutningen.</span><span class="sxs-lookup"><span data-stu-id="62e52-128">The parent ExpressRouteGateway for this connection.</span></span>

```yaml
Type: PSExpressRouteGateway
Parameter Sets: ByExpressRouteGatewayObject
Aliases: ExpressRouteGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62e52-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="62e52-129">-Name</span></span>
<span data-ttu-id="62e52-130">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="62e52-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, ExpressRouteConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e52-131">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="62e52-131">-ParentResourceId</span></span>
<span data-ttu-id="62e52-132">Resurs-ID för den överordnade ExpressRouteGateway för den här anslutningen.</span><span class="sxs-lookup"><span data-stu-id="62e52-132">The resource id of the parent ExpressRouteGateway for this connection.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: ExpressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62e52-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62e52-133">-ResourceGroupName</span></span>
<span data-ttu-id="62e52-134">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="62e52-134">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e52-135">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="62e52-135">-RoutingConfiguration</span></span>
<span data-ttu-id="62e52-136">Dirigerings konfiguration för den här anslutningen</span><span class="sxs-lookup"><span data-stu-id="62e52-136">Routing configuration for this connection</span></span>

```yaml
Type: PSRoutingConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e52-137">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="62e52-137">-RoutingWeight</span></span>
<span data-ttu-id="62e52-138">Den vikt för paket dirigering som måste tilldelas den här anslutningen.</span><span class="sxs-lookup"><span data-stu-id="62e52-138">The weight for packet routing that needs to be assigned to this connection.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e52-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="62e52-139">-Confirm</span></span>
<span data-ttu-id="62e52-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="62e52-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62e52-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62e52-141">-WhatIf</span></span>
<span data-ttu-id="62e52-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="62e52-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62e52-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="62e52-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62e52-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62e52-144">CommonParameters</span></span>
<span data-ttu-id="62e52-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62e52-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62e52-146">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62e52-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62e52-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="62e52-147">INPUTS</span></span>

### <span data-ttu-id="62e52-148">Microsoft. Azure. commands. Networks. Models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="62e52-148">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="62e52-149">System. String</span><span class="sxs-lookup"><span data-stu-id="62e52-149">System.String</span></span>

## <span data-ttu-id="62e52-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="62e52-150">OUTPUTS</span></span>

### <span data-ttu-id="62e52-151">Microsoft. Azure. commands. Networks. Models. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="62e52-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="62e52-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="62e52-152">NOTES</span></span>

## <span data-ttu-id="62e52-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="62e52-153">RELATED LINKS</span></span>

[<span data-ttu-id="62e52-154">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="62e52-154">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
