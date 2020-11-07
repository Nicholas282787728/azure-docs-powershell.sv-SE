---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworksubnetconfig
schema: 2.0.0
ms.openlocfilehash: b13a06fbc2bd7f071888dcd0504d3e1963cbedd8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930870"
---
# <span data-ttu-id="efddf-101">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="efddf-101">Set-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="efddf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="efddf-102">SYNOPSIS</span></span>
<span data-ttu-id="efddf-103">Konfigurerar mål tillstånd för en under nätverks konfiguration i ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="efddf-103">Configures the goal state for a subnet configuration in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="efddf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="efddf-104">SYNTAX</span></span>

### <span data-ttu-id="efddf-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="efddf-105">SetByResource (Default)</span></span>
```
Set-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="efddf-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="efddf-106">SetByResourceId</span></span>
```
Set-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efddf-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="efddf-107">DESCRIPTION</span></span>
<span data-ttu-id="efddf-108">Cmdleten **set-AzureRmVirtualNetworkSubnetConfig** konfigurerar mål tillståndet för en under nätverks konfiguration i ett Azure Virtual Network.</span><span class="sxs-lookup"><span data-stu-id="efddf-108">The **Set-AzureRmVirtualNetworkSubnetConfig** cmdlet configures the goal state for a subnet configuration in an Azure virtual network.</span></span>

## <span data-ttu-id="efddf-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="efddf-109">EXAMPLES</span></span>

### <span data-ttu-id="efddf-110">1: ändra adressprefixet för ett undernät</span><span class="sxs-lookup"><span data-stu-id="efddf-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="efddf-111">I det här exemplet skapas ett virtuellt nätverk med ett undernät.</span><span class="sxs-lookup"><span data-stu-id="efddf-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="efddf-112">Sedan ringer Set-AzureRmVirtualNetworkSubnetConfig för att ändra AddressPrefix för under nätet.</span><span class="sxs-lookup"><span data-stu-id="efddf-112">Then is calls Set-AzureRmVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="efddf-113">Detta påverkar endast det virtuella nätverkets minnes representation.</span><span class="sxs-lookup"><span data-stu-id="efddf-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="efddf-114">Set-AzureRmVirtualNetwork anropas sedan för att ändra det virtuella nätverket i Azure.</span><span class="sxs-lookup"><span data-stu-id="efddf-114">Set-AzureRmVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="efddf-115">2: lägga till en nätverks säkerhets grupp i ett undernät</span><span class="sxs-lookup"><span data-stu-id="efddf-115">2: Add a network security group to a subnet</span></span>
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

<span data-ttu-id="efddf-116">I det här exemplet skapas en resurs grupp med ett virtuellt nätverk som bara innehåller ett undernät.</span><span class="sxs-lookup"><span data-stu-id="efddf-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="efddf-117">Därefter skapas en nätverks säkerhets grupp med en Tillåt-regel för RDP-trafik.</span><span class="sxs-lookup"><span data-stu-id="efddf-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="efddf-118">Set-AzureRmVirtualNetworkSubnetConfig-cmdleten används för att ändra uppslags filen för nät klient delen så att den pekar på den nya nätverks säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="efddf-118">The Set-AzureRmVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="efddf-119">Set-AzureRmVirtualNetwork cmdlet anropas sedan för att skriva tillbaka till tjänsten.</span><span class="sxs-lookup"><span data-stu-id="efddf-119">The Set-AzureRmVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

## <span data-ttu-id="efddf-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="efddf-120">PARAMETERS</span></span>

### <span data-ttu-id="efddf-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="efddf-121">-AddressPrefix</span></span>
<span data-ttu-id="efddf-122">Anger ett intervall med IP-adresser för en under nätverks konfiguration.</span><span class="sxs-lookup"><span data-stu-id="efddf-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="efddf-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efddf-123">-DefaultProfile</span></span>
<span data-ttu-id="efddf-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="efddf-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efddf-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="efddf-125">-Name</span></span>
<span data-ttu-id="efddf-126">Anger namnet på en under nätverks konfiguration som denna cmdlet konfigurerar.</span><span class="sxs-lookup"><span data-stu-id="efddf-126">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

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

### <span data-ttu-id="efddf-127">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="efddf-127">-NetworkSecurityGroup</span></span>
<span data-ttu-id="efddf-128">Anger ett **NetworkSecurityGroup** -objekt.</span><span class="sxs-lookup"><span data-stu-id="efddf-128">Specifies a **NetworkSecurityGroup** object.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efddf-129">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="efddf-129">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="efddf-130">Anger ID för en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="efddf-130">Specifies the ID of a network security group.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efddf-131">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="efddf-131">-RouteTable</span></span>
<span data-ttu-id="efddf-132">Anger det väg tabell objekt som är kopplat till nätverks säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="efddf-132">Specifies the route table object that is associated with the network security group.</span></span>

```yaml
Type: PSRouteTable
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efddf-133">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="efddf-133">-RouteTableId</span></span>
<span data-ttu-id="efddf-134">Anger ID för det väg objekt som är kopplat till nätverks säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="efddf-134">Specifies the ID of the route table object that is associated with the network security group.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efddf-135">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="efddf-135">-ServiceEndpoint</span></span>
<span data-ttu-id="efddf-136">Värde för tjänste slut punkt</span><span class="sxs-lookup"><span data-stu-id="efddf-136">Service Endpoint Value</span></span>

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

### <span data-ttu-id="efddf-137">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="efddf-137">-VirtualNetwork</span></span>
<span data-ttu-id="efddf-138">Anger det **VirtualNetwork** -objekt som innehåller under nätets konfiguration.</span><span class="sxs-lookup"><span data-stu-id="efddf-138">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="efddf-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efddf-139">CommonParameters</span></span>
<span data-ttu-id="efddf-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efddf-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efddf-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efddf-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efddf-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="efddf-142">INPUTS</span></span>

### <span data-ttu-id="efddf-143">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="efddf-143">PSVirtualNetwork</span></span>
<span data-ttu-id="efddf-144">Parametern ' VirtualNetwork ' godkänner värdet av typen ' PSVirtualNetwork ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="efddf-144">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="efddf-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="efddf-145">OUTPUTS</span></span>

### <span data-ttu-id="efddf-146">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="efddf-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="efddf-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="efddf-147">NOTES</span></span>

## <span data-ttu-id="efddf-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="efddf-148">RELATED LINKS</span></span>

[<span data-ttu-id="efddf-149">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="efddf-149">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="efddf-150">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="efddf-150">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="efddf-151">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="efddf-151">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="efddf-152">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="efddf-152">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)


