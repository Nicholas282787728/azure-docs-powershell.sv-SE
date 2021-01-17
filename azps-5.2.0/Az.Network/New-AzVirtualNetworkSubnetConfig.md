---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 7afedb15ea5e7b5e2968dbb425a662f7de7e2ac1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412323"
---
# <span data-ttu-id="01322-101">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="01322-101">New-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="01322-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="01322-102">SYNOPSIS</span></span>
<span data-ttu-id="01322-103">Skapar en konfiguration för virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="01322-103">Creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="01322-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="01322-104">SYNTAX</span></span>

### <span data-ttu-id="01322-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="01322-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="01322-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="01322-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ResourceId <String>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-PrivateEndpointNetworkPoliciesFlag <String>] [-PrivateLinkServiceNetworkPoliciesFlag <String>]
 [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01322-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="01322-107">DESCRIPTION</span></span>
<span data-ttu-id="01322-108">Cmdleten **New-AzVirtualNetworkSubnetConfig** skapar en konfiguration för virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="01322-108">**The New-AzVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="01322-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="01322-109">EXAMPLES</span></span>

### <span data-ttu-id="01322-110">Exempel 1: skapa ett virtuellt nätverk med två undernät och en nätverks säkerhets grupp</span><span class="sxs-lookup"><span data-stu-id="01322-110">Example 1: Create a virtual network with two subnets and a network security group</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$rdpRule = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
   -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 `
   -SourceAddressPrefix Internet -SourcePortRange * `
   -DestinationAddressPrefix * -DestinationPortRange 3389 
    
$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName TestResourceGroup `
  -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet `
    -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet `
    -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup

$pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" `
   -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"

$natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" `
   -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip

$natGatewaySubnet = New-AzVirtualNetworkSubnetConfig -Name natGatewaySubnet `
   -AddressPrefix "10.0.3.0/24" -InputObject $natGateway

New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup `
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet,$natGatewaySubnet
```

<span data-ttu-id="01322-111">I det här exemplet skapas två nya maskinvarukonfigurationer med hjälp av New-AzVirtualSubnetConfig cmdlet och sedan används dessa för att skapa ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="01322-111">This example creates two new subnet configurations using the New-AzVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="01322-112">New-AzVirtualSubnetConfig mal len skapar bara en i-minnet-representation av under nätet.</span><span class="sxs-lookup"><span data-stu-id="01322-112">The New-AzVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="01322-113">I det här exemplet har frontendSubnet CIDR 10.0.1.0/24 och refererar till en nätverks säkerhets grupp som tillåter RDP-åtkomst.</span><span class="sxs-lookup"><span data-stu-id="01322-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="01322-114">BackendSubnet har CIDR 10.0.2.0/24 och refererar till samma nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="01322-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="01322-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="01322-115">PARAMETERS</span></span>

### <span data-ttu-id="01322-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="01322-116">-AddressPrefix</span></span>
<span data-ttu-id="01322-117">Anger ett intervall med IP-adresser för en under nätverks konfiguration.</span><span class="sxs-lookup"><span data-stu-id="01322-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="01322-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01322-118">-DefaultProfile</span></span>
<span data-ttu-id="01322-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="01322-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01322-120">-Delegation</span><span class="sxs-lookup"><span data-stu-id="01322-120">-Delegation</span></span>
<span data-ttu-id="01322-121">Lista över tjänster som har behörighet att utföra åtgärder i det här under nätet.</span><span class="sxs-lookup"><span data-stu-id="01322-121">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="01322-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01322-122">-InputObject</span></span>
<span data-ttu-id="01322-123">Anger den NAT-gateway som är associerad med under nätets konfiguration</span><span class="sxs-lookup"><span data-stu-id="01322-123">Specifies the nat gateway associated with the subnet configuration</span></span>

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

### <span data-ttu-id="01322-124">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="01322-124">-IpAllocation</span></span>
<span data-ttu-id="01322-125">Anger IpAllocations för ett undernät.</span><span class="sxs-lookup"><span data-stu-id="01322-125">Specifies IpAllocations for a subnet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpAllocation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01322-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="01322-126">-Name</span></span>
<span data-ttu-id="01322-127">Anger namnet på den nätmask som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="01322-127">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="01322-128">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="01322-128">-NetworkSecurityGroup</span></span>
<span data-ttu-id="01322-129">Anger ett NetworkSecurityGroup-objekt.</span><span class="sxs-lookup"><span data-stu-id="01322-129">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="01322-130">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="01322-130">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="01322-131">Anger ID för en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="01322-131">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="01322-132">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="01322-132">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="01322-133">Konfigurera för att aktivera eller inaktivera nätverks principer för privata slut punkter i under nätet.</span><span class="sxs-lookup"><span data-stu-id="01322-133">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="01322-134">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="01322-134">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="01322-135">Konfigurera för att aktivera eller inaktivera nätverks principer för privata länkar i under nätet.</span><span class="sxs-lookup"><span data-stu-id="01322-135">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="01322-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01322-136">-ResourceId</span></span>
<span data-ttu-id="01322-137">Anger ID för NAT-gatewayenheten som är associerad med under nätets konfiguration.</span><span class="sxs-lookup"><span data-stu-id="01322-137">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="01322-138">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="01322-138">-RouteTable</span></span>
<span data-ttu-id="01322-139">Anger den routningstabell som är associerad med under nätets konfiguration.</span><span class="sxs-lookup"><span data-stu-id="01322-139">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="01322-140">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="01322-140">-RouteTableId</span></span>
<span data-ttu-id="01322-141">Anger ID för den väg tabell som är associerad med under nätets konfiguration.</span><span class="sxs-lookup"><span data-stu-id="01322-141">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="01322-142">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="01322-142">-ServiceEndpoint</span></span>
<span data-ttu-id="01322-143">Värde för tjänste slut punkt</span><span class="sxs-lookup"><span data-stu-id="01322-143">Service Endpoint Value</span></span>

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

### <span data-ttu-id="01322-144">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="01322-144">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="01322-145">Principer för tjänste slut punkter</span><span class="sxs-lookup"><span data-stu-id="01322-145">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="01322-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01322-146">CommonParameters</span></span>
<span data-ttu-id="01322-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01322-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01322-148">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="01322-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01322-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="01322-149">INPUTS</span></span>

### <span data-ttu-id="01322-150">System. String</span><span class="sxs-lookup"><span data-stu-id="01322-150">System.String</span></span>

### <span data-ttu-id="01322-151">Microsoft. Azure. commands. Networks. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="01322-151">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="01322-152">Microsoft. Azure. commands. Networks. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="01322-152">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="01322-153">Microsoft. Azure. commands. Networks. Models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="01322-153">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

### <span data-ttu-id="01322-154">System. string []</span><span class="sxs-lookup"><span data-stu-id="01322-154">System.String[]</span></span>

### <span data-ttu-id="01322-155">Microsoft. Azure. commands. Network. Models. PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="01322-155">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="01322-156">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="01322-156">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="01322-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="01322-157">OUTPUTS</span></span>

### <span data-ttu-id="01322-158">Microsoft. Azure. commands. Networks. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="01322-158">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="01322-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="01322-159">NOTES</span></span>

## <span data-ttu-id="01322-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="01322-160">RELATED LINKS</span></span>

[<span data-ttu-id="01322-161">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="01322-161">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="01322-162">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="01322-162">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="01322-163">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="01322-163">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="01322-164">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="01322-164">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
