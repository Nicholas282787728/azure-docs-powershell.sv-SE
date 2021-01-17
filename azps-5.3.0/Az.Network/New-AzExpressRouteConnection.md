---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteConnection.md
ms.openlocfilehash: 565e79420821e8d8764b5e461e33d275247ddb3c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98425352"
---
# <span data-ttu-id="a3faf-101">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="a3faf-101">New-AzExpressRouteConnection</span></span>

## <span data-ttu-id="a3faf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a3faf-102">SYNOPSIS</span></span>
<span data-ttu-id="a3faf-103">Skapar en ExpressRoute-anslutning som ansluter en ExpressRoute Gateway till en lokal ExpressRoute-krets</span><span class="sxs-lookup"><span data-stu-id="a3faf-103">Creates an ExpressRoute connection that connects an ExpressRoute gateway to an on premise ExpressRoute circuit</span></span>

## <span data-ttu-id="a3faf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a3faf-104">SYNTAX</span></span>

### <span data-ttu-id="a3faf-105">ByExpressRouteGatewayName (standard)</span><span class="sxs-lookup"><span data-stu-id="a3faf-105">ByExpressRouteGatewayName (Default)</span></span>
```
New-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 -ExpressRouteCircuitPeeringId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3faf-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="a3faf-106">ByExpressRouteGatewayObject</span></span>
```
New-AzExpressRouteConnection -ExpressRouteGatewayObject <PSExpressRouteGateway> -Name <String>
 -ExpressRouteCircuitPeeringId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3faf-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="a3faf-107">ByExpressRouteGatewayResourceId</span></span>
```
New-AzExpressRouteConnection -ParentResourceId <String> -Name <String> -ExpressRouteCircuitPeeringId <String>
 [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3faf-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a3faf-108">DESCRIPTION</span></span>
<span data-ttu-id="a3faf-109">Skapar en ExpressRoute-anslutning mellan en lokal ExpressRoute-krets med BGP-peering till ExpressRoute gateway i ett virtuellt nav.</span><span class="sxs-lookup"><span data-stu-id="a3faf-109">Creates an ExpressRoute connection between an on-premise ExpressRoute circuit BGP peering to the ExpressRoute gateway inside a Virtual hub.</span></span>

## <span data-ttu-id="a3faf-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a3faf-110">EXAMPLES</span></span>

### <span data-ttu-id="a3faf-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a3faf-111">Example 1</span></span>

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

<span data-ttu-id="a3faf-112">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav, ExpressRoute och en ExpressRoute-krets med privat peering i västra centrala USA i resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="a3faf-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub, Express Route gateway and an ExpressRoute circuit with private peering in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="a3faf-113">När gatewayen har skapats är den ansluten till ExpressRoute-kretsen med kommandot New-AzExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="a3faf-113">Once the gateway has been created, it is connected to the ExpressRoute Circuit Peering using the New-AzExpressRouteConnection command.</span></span>

## <span data-ttu-id="a3faf-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a3faf-114">PARAMETERS</span></span>

### <span data-ttu-id="a3faf-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3faf-115">-AsJob</span></span>
<span data-ttu-id="a3faf-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a3faf-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a3faf-117">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="a3faf-117">-AuthorizationKey</span></span>
<span data-ttu-id="a3faf-118">En nyckeln från ExpressRoute-kretsen för att kunna skapa en anslutning till en gateway i ett annat abonnemang.</span><span class="sxs-lookup"><span data-stu-id="a3faf-118">A key obtained from the ExpressRoute circuit owner to be able to create a connection with a gateway in a different subscription.</span></span>

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

### <span data-ttu-id="a3faf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3faf-119">-DefaultProfile</span></span>
<span data-ttu-id="a3faf-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a3faf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3faf-121">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="a3faf-121">-EnableInternetSecurity</span></span>
<span data-ttu-id="a3faf-122">Aktivera Internet säkerhet för denna ExpressRoute Gateway-anslutning</span><span class="sxs-lookup"><span data-stu-id="a3faf-122">Enable internet security for this ExpressRoute Gateway connection</span></span>

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

### <span data-ttu-id="a3faf-123">-ExpressRouteCircuitPeeringId</span><span class="sxs-lookup"><span data-stu-id="a3faf-123">-ExpressRouteCircuitPeeringId</span></span>
<span data-ttu-id="a3faf-124">Resurs-ID för den ExpressRoute-krets som den här ExpressRoute-anslutningen för snabb vägen ska skapas till.</span><span class="sxs-lookup"><span data-stu-id="a3faf-124">The resource id of the Express Route Circuit Peering to which this Express Route gateway connection is to be created to.</span></span>

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

### <span data-ttu-id="a3faf-125">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="a3faf-125">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="a3faf-126">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="a3faf-126">The resource group name.</span></span>

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

### <span data-ttu-id="a3faf-127">-ExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="a3faf-127">-ExpressRouteGatewayObject</span></span>
<span data-ttu-id="a3faf-128">Den överordnade ExpressRouteGateway för den här anslutningen.</span><span class="sxs-lookup"><span data-stu-id="a3faf-128">The parent ExpressRouteGateway for this connection.</span></span>

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

### <span data-ttu-id="a3faf-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="a3faf-129">-Name</span></span>
<span data-ttu-id="a3faf-130">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="a3faf-130">The resource name.</span></span>

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

### <span data-ttu-id="a3faf-131">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a3faf-131">-ParentResourceId</span></span>
<span data-ttu-id="a3faf-132">Resurs-ID för den överordnade ExpressRouteGateway för den här anslutningen.</span><span class="sxs-lookup"><span data-stu-id="a3faf-132">The resource id of the parent ExpressRouteGateway for this connection.</span></span>

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

### <span data-ttu-id="a3faf-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3faf-133">-ResourceGroupName</span></span>
<span data-ttu-id="a3faf-134">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="a3faf-134">The resource group name.</span></span>

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

### <span data-ttu-id="a3faf-135">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3faf-135">-RoutingConfiguration</span></span>
<span data-ttu-id="a3faf-136">Dirigerings konfiguration för den här anslutningen</span><span class="sxs-lookup"><span data-stu-id="a3faf-136">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="a3faf-137">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="a3faf-137">-RoutingWeight</span></span>
<span data-ttu-id="a3faf-138">Den vikt för paket dirigering som måste tilldelas den här anslutningen.</span><span class="sxs-lookup"><span data-stu-id="a3faf-138">The weight for packet routing that needs to be assigned to this connection.</span></span>

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

### <span data-ttu-id="a3faf-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a3faf-139">-Confirm</span></span>
<span data-ttu-id="a3faf-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a3faf-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3faf-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3faf-141">-WhatIf</span></span>
<span data-ttu-id="a3faf-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a3faf-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3faf-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a3faf-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3faf-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3faf-144">CommonParameters</span></span>
<span data-ttu-id="a3faf-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3faf-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3faf-146">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3faf-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3faf-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a3faf-147">INPUTS</span></span>

### <span data-ttu-id="a3faf-148">Microsoft. Azure. commands. Networks. Models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="a3faf-148">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="a3faf-149">System. String</span><span class="sxs-lookup"><span data-stu-id="a3faf-149">System.String</span></span>

## <span data-ttu-id="a3faf-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a3faf-150">OUTPUTS</span></span>

### <span data-ttu-id="a3faf-151">Microsoft. Azure. commands. Networks. Models. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="a3faf-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="a3faf-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a3faf-152">NOTES</span></span>

## <span data-ttu-id="a3faf-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a3faf-153">RELATED LINKS</span></span>

[<span data-ttu-id="a3faf-154">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3faf-154">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
