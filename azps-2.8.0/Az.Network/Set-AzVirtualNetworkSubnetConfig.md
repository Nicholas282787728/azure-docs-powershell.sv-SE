---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: ecaf236c04c24241cf285e3d8ca379d3bc52645a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919462"
---
# <span data-ttu-id="15356-101">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="15356-101">Set-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="15356-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="15356-102">SYNOPSIS</span></span>
<span data-ttu-id="15356-103">Uppdaterar en under nätverks konfiguration för ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="15356-103">Updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="15356-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="15356-104">SYNTAX</span></span>

### <span data-ttu-id="15356-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="15356-105">SetByResource (Default)</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="15356-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="15356-106">SetByResourceId</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ResourceId <String>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="15356-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="15356-107">DESCRIPTION</span></span>
<span data-ttu-id="15356-108">Cmdleten **set-AzVirtualNetworkSubnetConfig** uppdaterar en under nätverks konfiguration för ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="15356-108">The **Set-AzVirtualNetworkSubnetConfig** cmdlet updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="15356-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="15356-109">EXAMPLES</span></span>

### <span data-ttu-id="15356-110">1: ändra adressprefixet för ett undernät</span><span class="sxs-lookup"><span data-stu-id="15356-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="15356-111">I det här exemplet skapas ett virtuellt nätverk med ett undernät.</span><span class="sxs-lookup"><span data-stu-id="15356-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="15356-112">Sedan ringer Set-AzVirtualNetworkSubnetConfig för att ändra AddressPrefix för under nätet.</span><span class="sxs-lookup"><span data-stu-id="15356-112">Then is calls Set-AzVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="15356-113">Detta påverkar endast det virtuella nätverkets minnes representation.</span><span class="sxs-lookup"><span data-stu-id="15356-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="15356-114">Set-AzVirtualNetwork anropas sedan för att ändra det virtuella nätverket i Azure.</span><span class="sxs-lookup"><span data-stu-id="15356-114">Set-AzVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="15356-115">2: lägga till en nätverks säkerhets grupp i ett undernät</span><span class="sxs-lookup"><span data-stu-id="15356-115">2: Add a network security group to a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

$rdpRule = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow 
    -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName 
    TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix 
    "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="15356-116">I det här exemplet skapas en resurs grupp med ett virtuellt nätverk som bara innehåller ett undernät.</span><span class="sxs-lookup"><span data-stu-id="15356-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="15356-117">Därefter skapas en nätverks säkerhets grupp med en Tillåt-regel för RDP-trafik.</span><span class="sxs-lookup"><span data-stu-id="15356-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="15356-118">Set-AzVirtualNetworkSubnetConfig-cmdleten används för att ändra uppslags filen för nät klient delen så att den pekar på den nya nätverks säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="15356-118">The Set-AzVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="15356-119">Set-AzVirtualNetwork cmdlet anropas sedan för att skriva tillbaka till tjänsten.</span><span class="sxs-lookup"><span data-stu-id="15356-119">The Set-AzVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

### <span data-ttu-id="15356-120">3: ansluta en NAT-gateway till ett undernät</span><span class="sxs-lookup"><span data-stu-id="15356-120">3: Attach a Nat Gateway to a subnet</span></span>
```
$pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" `
   -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"

$natGateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" `
   -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" 

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -InputObject $natGateway 

$virtualNetwork | Set-AzVirtualNetwork
```

## <span data-ttu-id="15356-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="15356-121">PARAMETERS</span></span>

### <span data-ttu-id="15356-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="15356-122">-AddressPrefix</span></span>
<span data-ttu-id="15356-123">Anger ett intervall med IP-adresser för en under nätverks konfiguration.</span><span class="sxs-lookup"><span data-stu-id="15356-123">Specifies a range of IP addresses for a subnet configuration.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15356-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15356-124">-DefaultProfile</span></span>
<span data-ttu-id="15356-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="15356-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15356-126">-Delegation</span><span class="sxs-lookup"><span data-stu-id="15356-126">-Delegation</span></span>
<span data-ttu-id="15356-127">Lista över tjänster som har behörighet att utföra åtgärder i det här under nätet.</span><span class="sxs-lookup"><span data-stu-id="15356-127">List of services that have permission to perform operations on this subnet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSDelegation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15356-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15356-128">-InputObject</span></span>
<span data-ttu-id="15356-129">Anger den NAT-gateway som är associerad med under nätets konfiguration.</span><span class="sxs-lookup"><span data-stu-id="15356-129">Specifies the nat gateway associated with the subnet configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNatGateway
Parameter Sets: SetByResource
Aliases: NatGateway

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15356-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="15356-130">-Name</span></span>
<span data-ttu-id="15356-131">Anger namnet på en under nätverks konfiguration som denna cmdlet konfigurerar.</span><span class="sxs-lookup"><span data-stu-id="15356-131">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

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

### <span data-ttu-id="15356-132">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="15356-132">-NetworkSecurityGroup</span></span>
<span data-ttu-id="15356-133">Anger ett **NetworkSecurityGroup** -objekt.</span><span class="sxs-lookup"><span data-stu-id="15356-133">Specifies a **NetworkSecurityGroup** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15356-134">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="15356-134">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="15356-135">Anger ID för en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="15356-135">Specifies the ID of a network security group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15356-136">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="15356-136">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="15356-137">Konfigurera för att aktivera eller inaktivera nätverks principer för privata slut punkter i under nätet.</span><span class="sxs-lookup"><span data-stu-id="15356-137">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15356-138">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="15356-138">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="15356-139">Konfigurera för att aktivera eller inaktivera nätverks principer för privata länkar i under nätet.</span><span class="sxs-lookup"><span data-stu-id="15356-139">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15356-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="15356-140">-ResourceId</span></span>
<span data-ttu-id="15356-141">Anger ID för NAT-gatewayenheten som är associerad med under nätets konfiguration.</span><span class="sxs-lookup"><span data-stu-id="15356-141">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: NatGatewayId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15356-142">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="15356-142">-RouteTable</span></span>
<span data-ttu-id="15356-143">Anger det väg tabell objekt som är kopplat till nätverks säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="15356-143">Specifies the route table object that is associated with the network security group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15356-144">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="15356-144">-RouteTableId</span></span>
<span data-ttu-id="15356-145">Anger ID för det väg objekt som är kopplat till nätverks säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="15356-145">Specifies the ID of the route table object that is associated with the network security group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15356-146">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="15356-146">-ServiceEndpoint</span></span>
<span data-ttu-id="15356-147">Värde för tjänste slut punkt</span><span class="sxs-lookup"><span data-stu-id="15356-147">Service Endpoint Value</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15356-148">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="15356-148">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="15356-149">Principer för tjänste slut punkter</span><span class="sxs-lookup"><span data-stu-id="15356-149">Service Endpoint Policies</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15356-150">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="15356-150">-VirtualNetwork</span></span>
<span data-ttu-id="15356-151">Anger det **VirtualNetwork** -objekt som innehåller under nätets konfiguration.</span><span class="sxs-lookup"><span data-stu-id="15356-151">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15356-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15356-152">CommonParameters</span></span>
<span data-ttu-id="15356-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15356-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15356-154">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15356-154">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15356-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="15356-155">INPUTS</span></span>

### <span data-ttu-id="15356-156">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="15356-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="15356-157">System. String</span><span class="sxs-lookup"><span data-stu-id="15356-157">System.String</span></span>

### <span data-ttu-id="15356-158">Microsoft. Azure. commands. Networks. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="15356-158">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="15356-159">Microsoft. Azure. commands. Networks. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="15356-159">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="15356-160">System. string []</span><span class="sxs-lookup"><span data-stu-id="15356-160">System.String[]</span></span>

### <span data-ttu-id="15356-161">Microsoft. Azure. commands. Network. Models. PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="15356-161">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="15356-162">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="15356-162">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="15356-163">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="15356-163">OUTPUTS</span></span>

### <span data-ttu-id="15356-164">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="15356-164">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="15356-165">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="15356-165">NOTES</span></span>

## <span data-ttu-id="15356-166">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="15356-166">RELATED LINKS</span></span>

[<span data-ttu-id="15356-167">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="15356-167">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="15356-168">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="15356-168">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="15356-169">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="15356-169">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="15356-170">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="15356-170">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)