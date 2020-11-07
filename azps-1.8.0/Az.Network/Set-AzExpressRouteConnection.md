---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteConnection.md
ms.openlocfilehash: 70f349fbb6a97009db4ba11e8de945b0700e3c2f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747748"
---
# <span data-ttu-id="fa064-101">Set-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="fa064-101">Set-AzExpressRouteConnection</span></span>

## <span data-ttu-id="fa064-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fa064-102">SYNOPSIS</span></span>
<span data-ttu-id="fa064-103">Uppdaterar en Express vägs anslutning som skapas mellan en snabb cirkulations gateway och en lokal ExpressRoute-krets med peering.</span><span class="sxs-lookup"><span data-stu-id="fa064-103">Updates an express route connection created between an express route gateway and on-premise express route circuit peering.</span></span>

## <span data-ttu-id="fa064-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fa064-104">SYNTAX</span></span>

### <span data-ttu-id="fa064-105">ByExpressRouteConnectionName (standard)</span><span class="sxs-lookup"><span data-stu-id="fa064-105">ByExpressRouteConnectionName (Default)</span></span>
```
Set-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa064-106">ByExpressRouteConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="fa064-106">ByExpressRouteConnectionResourceId</span></span>
```
Set-AzExpressRouteConnection -ResourceId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa064-107">ByExpressRouteConnectionObject</span><span class="sxs-lookup"><span data-stu-id="fa064-107">ByExpressRouteConnectionObject</span></span>
```
Set-AzExpressRouteConnection -InputObject <PSExpressRouteConnection> [-AuthorizationKey <String>]
 [-RoutingWeight <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fa064-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fa064-108">DESCRIPTION</span></span>
<span data-ttu-id="fa064-109">Cmdleten **set-AzExpressRouteConnection** uppdaterar en Express-vägs anslutning som skapas mellan en ExpressRoute-gateway och lokal ExpressRoute-kretsen.</span><span class="sxs-lookup"><span data-stu-id="fa064-109">The **Set-AzExpressRouteConnection** cmdlet updates an express route connection created between an express route gateway and on-premise express route circuit peering.</span></span>

## <span data-ttu-id="fa064-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fa064-110">EXAMPLES</span></span>

### <span data-ttu-id="fa064-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fa064-111">Example 1</span></span>

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
PS C:\> Set-AzExpressRouteConnection -InputObject $ExpressRouteConnection -RoutingWeight 30

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 30
ProvisioningState                  : Succeeded
Name                               : testConnection
Etag                               : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection
```

<span data-ttu-id="fa064-112">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav och en ExpressRouteSite i västra USA i resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="fa064-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a ExpressRouteSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="fa064-113">En ExpressRoute gateway kommer att skapas därefter i det virtuella navet med två skal enheter.</span><span class="sxs-lookup"><span data-stu-id="fa064-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="fa064-114">När gatewayen har skapats är den ansluten till den lokala ExpressRoute-kretsen med kommandot New-AzExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="fa064-114">Once the gateway has been created, it is connected to the on premise ExpressRoute circuit peering using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="fa064-115">Anslutningen uppdateras då till en annan RoutingWeight med hjälp av kommandot Set-AzExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="fa064-115">The connection is then updated to have a different RoutingWeight by using the Set-AzExpressRouteConnection command.</span></span>

## <span data-ttu-id="fa064-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fa064-116">PARAMETERS</span></span>

### <span data-ttu-id="fa064-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa064-117">-AsJob</span></span>
<span data-ttu-id="fa064-118">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="fa064-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fa064-119">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="fa064-119">-AuthorizationKey</span></span>
<span data-ttu-id="fa064-120">Den auktoriseringsregel som ska användas för att skapa ExpressRoute Gateway-anslutning.</span><span class="sxs-lookup"><span data-stu-id="fa064-120">The authorization key to be used to create the ExpressRoute gateway connection.</span></span>

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

### <span data-ttu-id="fa064-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa064-121">-DefaultProfile</span></span>
<span data-ttu-id="fa064-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fa064-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa064-123">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="fa064-123">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="fa064-124">Namnet på den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="fa064-124">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa064-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa064-125">-InputObject</span></span>
<span data-ttu-id="fa064-126">ExpressRouteConenction-objekt som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="fa064-126">The ExpressRouteConenction object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection
Parameter Sets: ByExpressRouteConnectionObject
Aliases: ExpressRouteConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa064-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="fa064-127">-Name</span></span>
<span data-ttu-id="fa064-128">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="fa064-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionName
Aliases: ResourceName, ExpressRouteConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa064-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa064-129">-ResourceGroupName</span></span>
<span data-ttu-id="fa064-130">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="fa064-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa064-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa064-131">-ResourceId</span></span>
<span data-ttu-id="fa064-132">Resurs-ID för det ExpressRouteConenction-objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="fa064-132">The resource id of the ExpressRouteConenction object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionResourceId
Aliases: ExpressRouteConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa064-133">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="fa064-133">-RoutingWeight</span></span>
<span data-ttu-id="fa064-134">Den vikt som måste kopplas till den här anslutningen för paket dirigering.</span><span class="sxs-lookup"><span data-stu-id="fa064-134">The weight that needs to be assigned to this connection for packet routing.</span></span>

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

### <span data-ttu-id="fa064-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fa064-135">-Confirm</span></span>
<span data-ttu-id="fa064-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fa064-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa064-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa064-137">-WhatIf</span></span>
<span data-ttu-id="fa064-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fa064-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa064-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fa064-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa064-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa064-140">CommonParameters</span></span>
<span data-ttu-id="fa064-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa064-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa064-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa064-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa064-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fa064-143">INPUTS</span></span>

### <span data-ttu-id="fa064-144">System. String</span><span class="sxs-lookup"><span data-stu-id="fa064-144">System.String</span></span>

### <span data-ttu-id="fa064-145">Microsoft. Azure. commands. Networks. Models. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="fa064-145">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="fa064-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fa064-146">OUTPUTS</span></span>

### <span data-ttu-id="fa064-147">Microsoft. Azure. commands. Networks. Models. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="fa064-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="fa064-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fa064-148">NOTES</span></span>

## <span data-ttu-id="fa064-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fa064-149">RELATED LINKS</span></span>
