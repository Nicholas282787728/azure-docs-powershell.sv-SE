---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteConnection.md
ms.openlocfilehash: 72aa8af012addf4fa309adc7c63467ecaf667fff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918302"
---
# <span data-ttu-id="d76fc-101">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="d76fc-101">New-AzExpressRouteConnection</span></span>

## <span data-ttu-id="d76fc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d76fc-102">SYNOPSIS</span></span>
<span data-ttu-id="d76fc-103">Skapar en ExpressRoute-anslutning som ansluter en ExpressRoute Gateway till en lokal ExpressRoute-krets</span><span class="sxs-lookup"><span data-stu-id="d76fc-103">Creates an ExpressRoute connection that connects an ExpressRoute gateway to an on premise ExpressRoute circuit</span></span>

## <span data-ttu-id="d76fc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d76fc-104">SYNTAX</span></span>

### <span data-ttu-id="d76fc-105">ByExpressRouteGatewayName (standard)</span><span class="sxs-lookup"><span data-stu-id="d76fc-105">ByExpressRouteGatewayName (Default)</span></span>
```
New-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 -ExpressRouteCircuitPeeringId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d76fc-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="d76fc-106">ByExpressRouteGatewayObject</span></span>
```
New-AzExpressRouteConnection -ExpressRouteGatewayObject <PSExpressRouteGateway> -Name <String>
 -ExpressRouteCircuitPeeringId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d76fc-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="d76fc-107">ByExpressRouteGatewayResourceId</span></span>
```
New-AzExpressRouteConnection -ParentResourceId <String> -Name <String> -ExpressRouteCircuitPeeringId <String>
 [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d76fc-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d76fc-108">DESCRIPTION</span></span>
<span data-ttu-id="d76fc-109">Skapar en ExpressRoute-anslutning mellan en lokal ExpressRoute-krets med BGP-peering till ExpressRoute gateway i ett virtuellt nav.</span><span class="sxs-lookup"><span data-stu-id="d76fc-109">Creates an ExpressRoute connection between an on-premise ExpressRoute circuit BGP peering to the ExpressRoute gateway inside a Virtual hub.</span></span>

## <span data-ttu-id="d76fc-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d76fc-110">EXAMPLES</span></span>

### <span data-ttu-id="d76fc-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d76fc-111">Example 1</span></span>

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
```

<span data-ttu-id="d76fc-112">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav, ExpressRoute och en ExpressRoute-krets med privat peering i västra centrala USA i resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="d76fc-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub, Express Route gateway and an ExpressRoute circuit with private peering in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="d76fc-113">När gatewayen har skapats är den ansluten till ExpressRoute-kretsen med kommandot New-AzExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="d76fc-113">Once the gateway has been created, it is connected to the ExpressRoute Circuit Peering using the New-AzExpressRouteConnection command.</span></span>

## <span data-ttu-id="d76fc-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d76fc-114">PARAMETERS</span></span>

### <span data-ttu-id="d76fc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d76fc-115">-AsJob</span></span>
<span data-ttu-id="d76fc-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d76fc-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d76fc-117">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="d76fc-117">-AuthorizationKey</span></span>
<span data-ttu-id="d76fc-118">En nyckeln från ExpressRoute-kretsen för att kunna skapa en anslutning till en gateway i ett annat abonnemang.</span><span class="sxs-lookup"><span data-stu-id="d76fc-118">A key obtained from the ExpressRoute circuit owner to be able to create a connection with a gateway in a different subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d76fc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d76fc-119">-DefaultProfile</span></span>
<span data-ttu-id="d76fc-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d76fc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d76fc-121">-ExpressRouteCircuitPeeringId</span><span class="sxs-lookup"><span data-stu-id="d76fc-121">-ExpressRouteCircuitPeeringId</span></span>
<span data-ttu-id="d76fc-122">Resurs-ID för den ExpressRoute-krets som den här ExpressRoute-anslutningen för snabb vägen ska skapas till.</span><span class="sxs-lookup"><span data-stu-id="d76fc-122">The resource id of the Express Route Circuit Peering to which this Express Route gateway connection is to be created to.</span></span>

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

### <span data-ttu-id="d76fc-123">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="d76fc-123">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="d76fc-124">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="d76fc-124">The resource group name.</span></span>

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

### <span data-ttu-id="d76fc-125">-ExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="d76fc-125">-ExpressRouteGatewayObject</span></span>
<span data-ttu-id="d76fc-126">Den överordnade ExpressRouteGateway för den här anslutningen.</span><span class="sxs-lookup"><span data-stu-id="d76fc-126">The parent ExpressRouteGateway for this connection.</span></span>

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

### <span data-ttu-id="d76fc-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="d76fc-127">-Name</span></span>
<span data-ttu-id="d76fc-128">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="d76fc-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, ExpressRouteConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d76fc-129">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d76fc-129">-ParentResourceId</span></span>
<span data-ttu-id="d76fc-130">Resurs-ID för den överordnade ExpressRouteGateway för den här anslutningen.</span><span class="sxs-lookup"><span data-stu-id="d76fc-130">The resource id of the parent ExpressRouteGateway for this connection.</span></span>

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

### <span data-ttu-id="d76fc-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d76fc-131">-ResourceGroupName</span></span>
<span data-ttu-id="d76fc-132">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="d76fc-132">The resource group name.</span></span>

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

### <span data-ttu-id="d76fc-133">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="d76fc-133">-RoutingWeight</span></span>
<span data-ttu-id="d76fc-134">Den vikt för paket dirigering som måste tilldelas den här anslutningen.</span><span class="sxs-lookup"><span data-stu-id="d76fc-134">The weight for packet routing that needs to be assigned to this connection.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d76fc-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d76fc-135">-Confirm</span></span>
<span data-ttu-id="d76fc-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d76fc-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d76fc-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d76fc-137">-WhatIf</span></span>
<span data-ttu-id="d76fc-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d76fc-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d76fc-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d76fc-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d76fc-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d76fc-140">CommonParameters</span></span>
<span data-ttu-id="d76fc-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d76fc-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d76fc-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d76fc-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d76fc-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d76fc-143">INPUTS</span></span>

### <span data-ttu-id="d76fc-144">Microsoft. Azure. commands. Networks. Models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="d76fc-144">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="d76fc-145">System. String</span><span class="sxs-lookup"><span data-stu-id="d76fc-145">System.String</span></span>

## <span data-ttu-id="d76fc-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d76fc-146">OUTPUTS</span></span>

### <span data-ttu-id="d76fc-147">Microsoft. Azure. commands. Networks. Models. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="d76fc-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="d76fc-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d76fc-148">NOTES</span></span>

## <span data-ttu-id="d76fc-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d76fc-149">RELATED LINKS</span></span>
