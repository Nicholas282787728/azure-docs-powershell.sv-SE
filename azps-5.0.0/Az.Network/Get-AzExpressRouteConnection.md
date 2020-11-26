---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteConnection.md
ms.openlocfilehash: 10514c693ff349550ee2c751f2a3091a7211a41e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271813"
---
# <span data-ttu-id="fe5be-101">Get-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="fe5be-101">Get-AzExpressRouteConnection</span></span>

## <span data-ttu-id="fe5be-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fe5be-102">SYNOPSIS</span></span>
<span data-ttu-id="fe5be-103">Hämtar en ExpressRoute-anslutning med namn eller visar alla ExpressRoute-anslutningar som är anslutna till en ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="fe5be-103">Gets a ExpressRoute connection by name or lists all ExpressRoute connections connected to a ExpressRouteGateway.</span></span>

## <span data-ttu-id="fe5be-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fe5be-104">SYNTAX</span></span>

### <span data-ttu-id="fe5be-105">ByExpressRouteGatewayName (standard)</span><span class="sxs-lookup"><span data-stu-id="fe5be-105">ByExpressRouteGatewayName (Default)</span></span>
```
Get-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe5be-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="fe5be-106">ByExpressRouteGatewayObject</span></span>
```
Get-AzExpressRouteConnection -ExpressRouteGatewayObject <PSExpressRouteGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe5be-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="fe5be-107">ByExpressRouteGatewayResourceId</span></span>
```
Get-AzExpressRouteConnection -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe5be-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fe5be-108">DESCRIPTION</span></span>
<span data-ttu-id="fe5be-109">Hämtar en ExpressRoute-anslutning med namn eller visar alla ExpressRoute-anslutningar som är anslutna till en ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="fe5be-109">Gets an ExpressRoute connection by name or lists all ExpressRoute connections connected to a ExpressRouteGateway.</span></span>

## <span data-ttu-id="fe5be-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fe5be-110">EXAMPLES</span></span>

### <span data-ttu-id="fe5be-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fe5be-111">Example 1</span></span>

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
PS C:\> Get-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection"

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection
Etag                               : W/"00000000-0000-0000-0000-000000000000"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection
EnableInternetSecurity             : False
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

<span data-ttu-id="fe5be-112">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav och en ExpressRouteSite i västra USA i resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="fe5be-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a ExpressRouteSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="fe5be-113">En ExpressRoute gateway kommer att skapas därefter i det virtuella navet med två skal enheter.</span><span class="sxs-lookup"><span data-stu-id="fe5be-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="fe5be-114">När gatewayen har skapats är den ansluten till den lokala ExpressRoute-kretsen med kommandot New-AzExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="fe5be-114">Once the gateway has been created, it is connected to the on premise ExpressRoute circuit using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="fe5be-115">Då får anslutningen hjälp av anslutnings namnet.</span><span class="sxs-lookup"><span data-stu-id="fe5be-115">Then it gets the connection using the connection name.</span></span>

### <span data-ttu-id="fe5be-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="fe5be-116">Example 2</span></span>

```powershell
PS C:\> Get-AzExpressRouteConnection -ResourceGroupName ps9361 -ParentResourceName testExpressRoutegw -Name test*

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection1
Etag                               : W/"00000000-0000-0000-0000-000000000000"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection1
EnableInternetSecurity             : False
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

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection2
Etag                               : W/"00000000-0000-0000-0000-000000000000"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection2
EnableInternetSecurity             : False
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

<span data-ttu-id="fe5be-117">Det här kommandot får alla anslutningar i ExpressRoute "testExpressRoutegw" som börjar med "test"</span><span class="sxs-lookup"><span data-stu-id="fe5be-117">This command will get all Connections in ExpressRoute "testExpressRoutegw" that start with "test"</span></span>

## <span data-ttu-id="fe5be-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fe5be-118">PARAMETERS</span></span>

### <span data-ttu-id="fe5be-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe5be-119">-DefaultProfile</span></span>
<span data-ttu-id="fe5be-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fe5be-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe5be-121">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="fe5be-121">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="fe5be-122">Namnet på den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="fe5be-122">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe5be-123">-ExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="fe5be-123">-ExpressRouteGatewayObject</span></span>
<span data-ttu-id="fe5be-124">Den överordnade ExpressRouteGateway för den här anslutningen.</span><span class="sxs-lookup"><span data-stu-id="fe5be-124">The parent ExpressRouteGateway for this connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway
Parameter Sets: ByExpressRouteGatewayObject
Aliases: ExpressRouteGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe5be-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="fe5be-125">-Name</span></span>
<span data-ttu-id="fe5be-126">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="fe5be-126">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, ExpressRouteConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="fe5be-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="fe5be-127">-ParentResourceId</span></span>
<span data-ttu-id="fe5be-128">Resurs-ID för den överordnade ExpressRouteGateway för den här anslutningen.</span><span class="sxs-lookup"><span data-stu-id="fe5be-128">The resource id of the parent ExpressRouteGateway for this connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: ExpressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe5be-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe5be-129">-ResourceGroupName</span></span>
<span data-ttu-id="fe5be-130">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="fe5be-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe5be-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe5be-131">CommonParameters</span></span>
<span data-ttu-id="fe5be-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe5be-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe5be-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe5be-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe5be-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fe5be-134">INPUTS</span></span>

### <span data-ttu-id="fe5be-135">System. String</span><span class="sxs-lookup"><span data-stu-id="fe5be-135">System.String</span></span>

## <span data-ttu-id="fe5be-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fe5be-136">OUTPUTS</span></span>

### <span data-ttu-id="fe5be-137">Microsoft. Azure. commands. Networks. Models. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="fe5be-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="fe5be-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fe5be-138">NOTES</span></span>

## <span data-ttu-id="fe5be-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fe5be-139">RELATED LINKS</span></span>