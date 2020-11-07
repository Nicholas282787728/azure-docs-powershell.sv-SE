---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 4e0356f738bcc0abd52f0ec72c4c6766af8be550
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747676"
---
# <span data-ttu-id="38a08-101">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="38a08-101">Set-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="38a08-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="38a08-102">SYNOPSIS</span></span>
<span data-ttu-id="38a08-103">Uppdaterar en under nätverks konfiguration för ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="38a08-103">Updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="38a08-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="38a08-104">SYNTAX</span></span>

### <span data-ttu-id="38a08-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="38a08-105">SetByResource (Default)</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38a08-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="38a08-106">SetByResourceId</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38a08-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="38a08-107">DESCRIPTION</span></span>
<span data-ttu-id="38a08-108">Cmdleten **set-AzVirtualNetworkSubnetConfig** uppdaterar en under nätverks konfiguration för ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="38a08-108">The **Set-AzVirtualNetworkSubnetConfig** cmdlet updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="38a08-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="38a08-109">EXAMPLES</span></span>

### <span data-ttu-id="38a08-110">1: ändra adressprefixet för ett undernät</span><span class="sxs-lookup"><span data-stu-id="38a08-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="38a08-111">I det här exemplet skapas ett virtuellt nätverk med ett undernät.</span><span class="sxs-lookup"><span data-stu-id="38a08-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="38a08-112">Sedan ringer Set-AzVirtualNetworkSubnetConfig för att ändra AddressPrefix för under nätet.</span><span class="sxs-lookup"><span data-stu-id="38a08-112">Then is calls Set-AzVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="38a08-113">Detta påverkar endast det virtuella nätverkets minnes representation.</span><span class="sxs-lookup"><span data-stu-id="38a08-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="38a08-114">Set-AzVirtualNetwork anropas sedan för att ändra det virtuella nätverket i Azure.</span><span class="sxs-lookup"><span data-stu-id="38a08-114">Set-AzVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="38a08-115">2: lägga till en nätverks säkerhets grupp i ett undernät</span><span class="sxs-lookup"><span data-stu-id="38a08-115">2: Add a network security group to a subnet</span></span>
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

<span data-ttu-id="38a08-116">I det här exemplet skapas en resurs grupp med ett virtuellt nätverk som bara innehåller ett undernät.</span><span class="sxs-lookup"><span data-stu-id="38a08-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="38a08-117">Därefter skapas en nätverks säkerhets grupp med en Tillåt-regel för RDP-trafik.</span><span class="sxs-lookup"><span data-stu-id="38a08-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="38a08-118">Set-AzVirtualNetworkSubnetConfig-cmdleten används för att ändra uppslags filen för nät klient delen så att den pekar på den nya nätverks säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="38a08-118">The Set-AzVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="38a08-119">Set-AzVirtualNetwork cmdlet anropas sedan för att skriva tillbaka till tjänsten.</span><span class="sxs-lookup"><span data-stu-id="38a08-119">The Set-AzVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

## <span data-ttu-id="38a08-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="38a08-120">PARAMETERS</span></span>

### <span data-ttu-id="38a08-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="38a08-121">-AddressPrefix</span></span>
<span data-ttu-id="38a08-122">Anger ett intervall med IP-adresser för en under nätverks konfiguration.</span><span class="sxs-lookup"><span data-stu-id="38a08-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="38a08-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38a08-123">-DefaultProfile</span></span>
<span data-ttu-id="38a08-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="38a08-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38a08-125">-Delegation</span><span class="sxs-lookup"><span data-stu-id="38a08-125">-Delegation</span></span>
<span data-ttu-id="38a08-126">Lista över tjänster som har behörighet att utföra åtgärder i det här under nätet.</span><span class="sxs-lookup"><span data-stu-id="38a08-126">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="38a08-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="38a08-127">-Name</span></span>
<span data-ttu-id="38a08-128">Anger namnet på en under nätverks konfiguration som denna cmdlet konfigurerar.</span><span class="sxs-lookup"><span data-stu-id="38a08-128">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

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

### <span data-ttu-id="38a08-129">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="38a08-129">-NetworkSecurityGroup</span></span>
<span data-ttu-id="38a08-130">Anger ett **NetworkSecurityGroup** -objekt.</span><span class="sxs-lookup"><span data-stu-id="38a08-130">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="38a08-131">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="38a08-131">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="38a08-132">Anger ID för en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="38a08-132">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="38a08-133">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="38a08-133">-RouteTable</span></span>
<span data-ttu-id="38a08-134">Anger det väg tabell objekt som är kopplat till nätverks säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="38a08-134">Specifies the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="38a08-135">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="38a08-135">-RouteTableId</span></span>
<span data-ttu-id="38a08-136">Anger ID för det väg objekt som är kopplat till nätverks säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="38a08-136">Specifies the ID of the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="38a08-137">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="38a08-137">-ServiceEndpoint</span></span>
<span data-ttu-id="38a08-138">Värde för tjänste slut punkt</span><span class="sxs-lookup"><span data-stu-id="38a08-138">Service Endpoint Value</span></span>

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

### <span data-ttu-id="38a08-139">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="38a08-139">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="38a08-140">Principer för tjänste slut punkter</span><span class="sxs-lookup"><span data-stu-id="38a08-140">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="38a08-141">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="38a08-141">-VirtualNetwork</span></span>
<span data-ttu-id="38a08-142">Anger det **VirtualNetwork** -objekt som innehåller under nätets konfiguration.</span><span class="sxs-lookup"><span data-stu-id="38a08-142">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

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

### <span data-ttu-id="38a08-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38a08-143">CommonParameters</span></span>
<span data-ttu-id="38a08-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38a08-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38a08-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38a08-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38a08-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="38a08-146">INPUTS</span></span>

### <span data-ttu-id="38a08-147">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="38a08-147">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="38a08-148">System. String</span><span class="sxs-lookup"><span data-stu-id="38a08-148">System.String</span></span>

### <span data-ttu-id="38a08-149">Microsoft. Azure. commands. Networks. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="38a08-149">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="38a08-150">Microsoft. Azure. commands. Networks. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="38a08-150">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="38a08-151">System. string []</span><span class="sxs-lookup"><span data-stu-id="38a08-151">System.String[]</span></span>

### <span data-ttu-id="38a08-152">Microsoft. Azure. commands. Network. Models. PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="38a08-152">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="38a08-153">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="38a08-153">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="38a08-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="38a08-154">OUTPUTS</span></span>

### <span data-ttu-id="38a08-155">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="38a08-155">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="38a08-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="38a08-156">NOTES</span></span>

## <span data-ttu-id="38a08-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="38a08-157">RELATED LINKS</span></span>

[<span data-ttu-id="38a08-158">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="38a08-158">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="38a08-159">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="38a08-159">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="38a08-160">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="38a08-160">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="38a08-161">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="38a08-161">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)
