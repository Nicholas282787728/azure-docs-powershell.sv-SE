---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 4e8aeb73c694229e290ee96fa11d3de71bb510ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576145"
---
# <span data-ttu-id="4cdb4-101">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4cdb4-101">Set-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="4cdb4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4cdb4-102">SYNOPSIS</span></span>
<span data-ttu-id="4cdb4-103">Konfigurerar mål tillstånd för en under nätverks konfiguration i ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="4cdb4-103">Configures the goal state for a subnet configuration in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cdb4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4cdb4-104">SYNTAX</span></span>

### <span data-ttu-id="4cdb4-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="4cdb4-105">SetByResource (Default)</span></span>
```
Set-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-ServiceEndpointPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]>]
 [-Delegation <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4cdb4-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4cdb4-106">SetByResourceId</span></span>
```
Set-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-ServiceEndpointPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]>]
 [-Delegation <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4cdb4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4cdb4-107">DESCRIPTION</span></span>
<span data-ttu-id="4cdb4-108">Cmdleten **set-AzureRmVirtualNetworkSubnetConfig** konfigurerar mål tillståndet för en under nätverks konfiguration i ett Azure Virtual Network.</span><span class="sxs-lookup"><span data-stu-id="4cdb4-108">The **Set-AzureRmVirtualNetworkSubnetConfig** cmdlet configures the goal state for a subnet configuration in an Azure virtual network.</span></span>

## <span data-ttu-id="4cdb4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4cdb4-109">EXAMPLES</span></span>

### <span data-ttu-id="4cdb4-110">1: ändra adressprefixet för ett undernät</span><span class="sxs-lookup"><span data-stu-id="4cdb4-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="4cdb4-111">I det här exemplet skapas ett virtuellt nätverk med ett undernät.</span><span class="sxs-lookup"><span data-stu-id="4cdb4-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="4cdb4-112">Sedan ringer Set-AzureRmVirtualNetworkSubnetConfig för att ändra AddressPrefix för under nätet.</span><span class="sxs-lookup"><span data-stu-id="4cdb4-112">Then is calls Set-AzureRmVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="4cdb4-113">Detta påverkar endast det virtuella nätverkets minnes representation.</span><span class="sxs-lookup"><span data-stu-id="4cdb4-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="4cdb4-114">Set-AzureRmVirtualNetwork anropas sedan för att ändra det virtuella nätverket i Azure.</span><span class="sxs-lookup"><span data-stu-id="4cdb4-114">Set-AzureRmVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="4cdb4-115">2: lägga till en nätverks säkerhets grupp i ett undernät</span><span class="sxs-lookup"><span data-stu-id="4cdb4-115">2: Add a network security group to a subnet</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

$rdpRule = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow 
    -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$networkSecurityGroup = New-AzureRmNetworkSecurityGroup -ResourceGroupName 
    TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

Set-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix 
    "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="4cdb4-116">I det här exemplet skapas en resurs grupp med ett virtuellt nätverk som bara innehåller ett undernät.</span><span class="sxs-lookup"><span data-stu-id="4cdb4-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="4cdb4-117">Därefter skapas en nätverks säkerhets grupp med en Tillåt-regel för RDP-trafik.</span><span class="sxs-lookup"><span data-stu-id="4cdb4-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="4cdb4-118">Set-AzureRmVirtualNetworkSubnetConfig-cmdleten används för att ändra uppslags filen för nät klient delen så att den pekar på den nya nätverks säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="4cdb4-118">The Set-AzureRmVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="4cdb4-119">Set-AzureRmVirtualNetwork cmdlet anropas sedan för att skriva tillbaka till tjänsten.</span><span class="sxs-lookup"><span data-stu-id="4cdb4-119">The Set-AzureRmVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

## <span data-ttu-id="4cdb4-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4cdb4-120">PARAMETERS</span></span>

### <span data-ttu-id="4cdb4-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4cdb4-121">-AddressPrefix</span></span>
<span data-ttu-id="4cdb4-122">Anger ett intervall med IP-adresser för en under nätverks konfiguration.</span><span class="sxs-lookup"><span data-stu-id="4cdb4-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cdb4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cdb4-123">-DefaultProfile</span></span>
<span data-ttu-id="4cdb4-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4cdb4-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cdb4-125">-Delegation</span><span class="sxs-lookup"><span data-stu-id="4cdb4-125">-Delegation</span></span>
<span data-ttu-id="4cdb4-126">Lista över tjänster som har behörighet att utföra åtgärder i det här under nätet.</span><span class="sxs-lookup"><span data-stu-id="4cdb4-126">List of services that have permission to perform operations on this subnet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cdb4-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="4cdb4-127">-Name</span></span>
<span data-ttu-id="4cdb4-128">Anger namnet på en under nätverks konfiguration som denna cmdlet konfigurerar.</span><span class="sxs-lookup"><span data-stu-id="4cdb4-128">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

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

### <span data-ttu-id="4cdb4-129">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4cdb4-129">-NetworkSecurityGroup</span></span>
<span data-ttu-id="4cdb4-130">Anger ett **NetworkSecurityGroup** -objekt.</span><span class="sxs-lookup"><span data-stu-id="4cdb4-130">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="4cdb4-131">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="4cdb4-131">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="4cdb4-132">Anger ID för en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="4cdb4-132">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="4cdb4-133">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="4cdb4-133">-RouteTable</span></span>
<span data-ttu-id="4cdb4-134">Anger det väg tabell objekt som är kopplat till nätverks säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="4cdb4-134">Specifies the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="4cdb4-135">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="4cdb4-135">-RouteTableId</span></span>
<span data-ttu-id="4cdb4-136">Anger ID för det väg objekt som är kopplat till nätverks säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="4cdb4-136">Specifies the ID of the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="4cdb4-137">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="4cdb4-137">-ServiceEndpoint</span></span>
<span data-ttu-id="4cdb4-138">Värde för tjänste slut punkt</span><span class="sxs-lookup"><span data-stu-id="4cdb4-138">Service Endpoint Value</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cdb4-139">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4cdb4-139">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="4cdb4-140">Principer för tjänste slut punkter</span><span class="sxs-lookup"><span data-stu-id="4cdb4-140">Service Endpoint Policies</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cdb4-141">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4cdb4-141">-VirtualNetwork</span></span>
<span data-ttu-id="4cdb4-142">Anger det **VirtualNetwork** -objekt som innehåller under nätets konfiguration.</span><span class="sxs-lookup"><span data-stu-id="4cdb4-142">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

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

### <span data-ttu-id="4cdb4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cdb4-143">CommonParameters</span></span>
<span data-ttu-id="4cdb4-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cdb4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cdb4-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cdb4-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cdb4-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4cdb4-146">INPUTS</span></span>

### <span data-ttu-id="4cdb4-147">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4cdb4-147">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="4cdb4-148">System. String</span><span class="sxs-lookup"><span data-stu-id="4cdb4-148">System.String</span></span>

### <span data-ttu-id="4cdb4-149">Microsoft. Azure. commands. Networks. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4cdb4-149">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="4cdb4-150">Microsoft. Azure. commands. Networks. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="4cdb4-150">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="4cdb4-151">System. Collections. Generic. list ' 1 [[system. String, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="4cdb4-151">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="4cdb4-152">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSServiceEndpointPolicy, Microsoft. Azure. commands. Network, version = 6.7.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4cdb4-152">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="4cdb4-153">System. Collections. Generic. list ' 1 [[Microsoft.Azure.Commands.Network.Models.PSDelegation, Microsoft. Azure. commands. Network, version = 6.7.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4cdb4-153">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSDelegation, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4cdb4-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4cdb4-154">OUTPUTS</span></span>

### <span data-ttu-id="4cdb4-155">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4cdb4-155">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="4cdb4-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4cdb4-156">NOTES</span></span>

## <span data-ttu-id="4cdb4-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4cdb4-157">RELATED LINKS</span></span>

[<span data-ttu-id="4cdb4-158">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4cdb4-158">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="4cdb4-159">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4cdb4-159">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="4cdb4-160">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4cdb4-160">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="4cdb4-161">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4cdb4-161">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)


