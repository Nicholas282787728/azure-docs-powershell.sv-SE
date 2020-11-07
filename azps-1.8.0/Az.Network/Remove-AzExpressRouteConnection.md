---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteConnection.md
ms.openlocfilehash: 7200f03ef931d86eff79a551fc414d3f9bc38e0b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747904"
---
# <span data-ttu-id="4da0b-101">Remove-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="4da0b-101">Remove-AzExpressRouteConnection</span></span>

## <span data-ttu-id="4da0b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4da0b-102">SYNOPSIS</span></span>
<span data-ttu-id="4da0b-103">Tar bort en ExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="4da0b-103">Removes a ExpressRouteConnection.</span></span>

## <span data-ttu-id="4da0b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4da0b-104">SYNTAX</span></span>

### <span data-ttu-id="4da0b-105">ByExpressRouteConnectionName (standard)</span><span class="sxs-lookup"><span data-stu-id="4da0b-105">ByExpressRouteConnectionName (Default)</span></span>
```
Remove-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4da0b-106">ByExpressRouteConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="4da0b-106">ByExpressRouteConnectionResourceId</span></span>
```
Remove-AzExpressRouteConnection -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4da0b-107">ByExpressRouteConnectionObject</span><span class="sxs-lookup"><span data-stu-id="4da0b-107">ByExpressRouteConnectionObject</span></span>
```
Remove-AzExpressRouteConnection -InputObject <PSExpressRouteConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4da0b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4da0b-108">DESCRIPTION</span></span>
<span data-ttu-id="4da0b-109">Tar bort en ExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="4da0b-109">Removes a ExpressRouteConnection.</span></span>

## <span data-ttu-id="4da0b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4da0b-110">EXAMPLES</span></span>

### <span data-ttu-id="4da0b-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4da0b-111">Example 1</span></span>
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
PS C:\> Remove-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection"
```

<span data-ttu-id="4da0b-112">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav i västra USA i resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="4da0b-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="4da0b-113">En ExpressRoute gateway kommer att skapas därefter i det virtuella navet med två skal enheter.</span><span class="sxs-lookup"><span data-stu-id="4da0b-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="4da0b-114">När gatewayen har skapats är den ansluten till ExpressRouteSite med kommandot New-AzExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="4da0b-114">Once the gateway has been created, it is connected to the ExpressRouteSite using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="4da0b-115">Därefter tas anslutningen bort med anslutnings namnet.</span><span class="sxs-lookup"><span data-stu-id="4da0b-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="4da0b-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="4da0b-116">Example 2</span></span>

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
PS C:\> Get-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection" | Remove-AzExpressRouteConnection
```

<span data-ttu-id="4da0b-117">Samma som exempel 1 men tar nu bort anslutningen med piped-objektet från get-AzExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="4da0b-117">Same as example 1, but it now removes the connection using the piped object from Get-AzExpressRouteConnection.</span></span>

## <span data-ttu-id="4da0b-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4da0b-118">PARAMETERS</span></span>

### <span data-ttu-id="4da0b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4da0b-119">-DefaultProfile</span></span>
<span data-ttu-id="4da0b-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4da0b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4da0b-121">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="4da0b-121">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="4da0b-122">Namnet på den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="4da0b-122">The parent resource name.</span></span>

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

### <span data-ttu-id="4da0b-123">-Force</span><span class="sxs-lookup"><span data-stu-id="4da0b-123">-Force</span></span>
<span data-ttu-id="4da0b-124">Fråga inte efter bekräftelse om du vill overrite en resurs</span><span class="sxs-lookup"><span data-stu-id="4da0b-124">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="4da0b-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4da0b-125">-InputObject</span></span>
<span data-ttu-id="4da0b-126">ExpressRouteConenction-objekt som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="4da0b-126">The ExpressRouteConenction object to update.</span></span>

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

### <span data-ttu-id="4da0b-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="4da0b-127">-Name</span></span>
<span data-ttu-id="4da0b-128">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="4da0b-128">The resource name.</span></span>

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

### <span data-ttu-id="4da0b-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4da0b-129">-PassThru</span></span>
<span data-ttu-id="4da0b-130">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="4da0b-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4da0b-131">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="4da0b-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4da0b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4da0b-132">-ResourceGroupName</span></span>
<span data-ttu-id="4da0b-133">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="4da0b-133">The resource group name.</span></span>

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

### <span data-ttu-id="4da0b-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4da0b-134">-ResourceId</span></span>
<span data-ttu-id="4da0b-135">Resurs-ID för det ExpressRouteConenction-objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="4da0b-135">The resource id of the ExpressRouteConenction object to delete.</span></span>

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

### <span data-ttu-id="4da0b-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4da0b-136">-Confirm</span></span>
<span data-ttu-id="4da0b-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4da0b-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4da0b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4da0b-138">-WhatIf</span></span>
<span data-ttu-id="4da0b-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4da0b-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4da0b-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4da0b-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4da0b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4da0b-141">CommonParameters</span></span>
<span data-ttu-id="4da0b-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4da0b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4da0b-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4da0b-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4da0b-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4da0b-144">INPUTS</span></span>

### <span data-ttu-id="4da0b-145">System. String</span><span class="sxs-lookup"><span data-stu-id="4da0b-145">System.String</span></span>

### <span data-ttu-id="4da0b-146">Microsoft. Azure. commands. Networks. Models. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="4da0b-146">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="4da0b-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4da0b-147">OUTPUTS</span></span>

### <span data-ttu-id="4da0b-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4da0b-148">System.Boolean</span></span>

## <span data-ttu-id="4da0b-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4da0b-149">NOTES</span></span>

## <span data-ttu-id="4da0b-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4da0b-150">RELATED LINKS</span></span>
