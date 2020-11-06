---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 37202e0e852f0171ce48c2c3d61d13151b05148c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575202"
---
# <span data-ttu-id="386e9-101">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="386e9-101">New-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="386e9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="386e9-102">SYNOPSIS</span></span>
<span data-ttu-id="386e9-103">Skapar en konfiguration för virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="386e9-103">Creates a virtual network subnet configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="386e9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="386e9-104">SYNTAX</span></span>

### <span data-ttu-id="386e9-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="386e9-105">SetByResource (Default)</span></span>
```
New-AzureRmVirtualNetworkSubnetConfig -Name <String>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-ServiceEndpointPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]>]
 [-Delegation <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="386e9-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="386e9-106">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkSubnetConfig -Name <String>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-ServiceEndpointPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]>]
 [-Delegation <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="386e9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="386e9-107">DESCRIPTION</span></span>
<span data-ttu-id="386e9-108">Cmdleten **New-AzureRmVirtualNetworkSubnetConfig** skapar en konfiguration för virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="386e9-108">**The New-AzureRmVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="386e9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="386e9-109">EXAMPLES</span></span>

### <span data-ttu-id="386e9-110">1: skapa ett virtuellt nätverk med två undernät och en nätverks säkerhets grupp</span><span class="sxs-lookup"><span data-stu-id="386e9-110">1:  Create a virtual network with two subnets and a network security group</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus

$rdpRule = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
   -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 `
   -SourceAddressPrefix Internet -SourcePortRange * `
   -DestinationAddressPrefix * -DestinationPortRange 3389 
    
$networkSecurityGroup = New-AzureRmNetworkSecurityGroup -ResourceGroupName TestResourceGroup `
  -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet `
    -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet `
    -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup

New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup `
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="386e9-111">I det här exemplet skapas två nya maskinvarukonfigurationer med hjälp av New-AzureRmVirtualSubnetConfig cmdlet och sedan används dessa för att skapa ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="386e9-111">This example creates two new subnet configurations using the New-AzureRmVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="386e9-112">New-AzureRmVirtualSubnetConfig mal len skapar bara en i-minnet-representation av under nätet.</span><span class="sxs-lookup"><span data-stu-id="386e9-112">The New-AzureRmVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="386e9-113">I det här exemplet har frontendSubnet CIDR 10.0.1.0/24 och refererar till en nätverks säkerhets grupp som tillåter RDP-åtkomst.</span><span class="sxs-lookup"><span data-stu-id="386e9-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="386e9-114">BackendSubnet har CIDR 10.0.2.0/24 och refererar till samma nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="386e9-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="386e9-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="386e9-115">PARAMETERS</span></span>

### <span data-ttu-id="386e9-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="386e9-116">-AddressPrefix</span></span>
<span data-ttu-id="386e9-117">Anger ett intervall med IP-adresser för en under nätverks konfiguration.</span><span class="sxs-lookup"><span data-stu-id="386e9-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="386e9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="386e9-118">-DefaultProfile</span></span>
<span data-ttu-id="386e9-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="386e9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="386e9-120">-Delegation</span><span class="sxs-lookup"><span data-stu-id="386e9-120">-Delegation</span></span>
<span data-ttu-id="386e9-121">Lista över tjänster som har behörighet att utföra åtgärder i det här under nätet.</span><span class="sxs-lookup"><span data-stu-id="386e9-121">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="386e9-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="386e9-122">-Name</span></span>
<span data-ttu-id="386e9-123">Anger namnet på den nätmask som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="386e9-123">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="386e9-124">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="386e9-124">-NetworkSecurityGroup</span></span>
<span data-ttu-id="386e9-125">Anger ett NetworkSecurityGroup-objekt.</span><span class="sxs-lookup"><span data-stu-id="386e9-125">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="386e9-126">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="386e9-126">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="386e9-127">Anger ID för en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="386e9-127">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="386e9-128">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="386e9-128">-RouteTable</span></span>
<span data-ttu-id="386e9-129">Anger den routningstabell som är associerad med under nätets konfiguration.</span><span class="sxs-lookup"><span data-stu-id="386e9-129">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="386e9-130">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="386e9-130">-RouteTableId</span></span>
<span data-ttu-id="386e9-131">Anger ID för den väg tabell som är associerad med under nätets konfiguration.</span><span class="sxs-lookup"><span data-stu-id="386e9-131">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="386e9-132">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="386e9-132">-ServiceEndpoint</span></span>
<span data-ttu-id="386e9-133">Värde för tjänste slut punkt</span><span class="sxs-lookup"><span data-stu-id="386e9-133">Service Endpoint Value</span></span>

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

### <span data-ttu-id="386e9-134">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="386e9-134">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="386e9-135">Principer för tjänste slut punkter</span><span class="sxs-lookup"><span data-stu-id="386e9-135">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="386e9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="386e9-136">CommonParameters</span></span>
<span data-ttu-id="386e9-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="386e9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="386e9-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="386e9-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="386e9-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="386e9-139">INPUTS</span></span>

### <span data-ttu-id="386e9-140">System. String</span><span class="sxs-lookup"><span data-stu-id="386e9-140">System.String</span></span>

### <span data-ttu-id="386e9-141">Microsoft. Azure. commands. Networks. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="386e9-141">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="386e9-142">Microsoft. Azure. commands. Networks. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="386e9-142">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="386e9-143">System. Collections. Generic. list ' 1 [[system. String, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="386e9-143">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="386e9-144">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSServiceEndpointPolicy, Microsoft. Azure. commands. Network, version = 6.7.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="386e9-144">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="386e9-145">System. Collections. Generic. list ' 1 [[Microsoft.Azure.Commands.Network.Models.PSDelegation, Microsoft. Azure. commands. Network, version = 6.7.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="386e9-145">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSDelegation, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="386e9-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="386e9-146">OUTPUTS</span></span>

### <span data-ttu-id="386e9-147">Microsoft. Azure. commands. Networks. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="386e9-147">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="386e9-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="386e9-148">NOTES</span></span>

## <span data-ttu-id="386e9-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="386e9-149">RELATED LINKS</span></span>

[<span data-ttu-id="386e9-150">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="386e9-150">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="386e9-151">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="386e9-151">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="386e9-152">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="386e9-152">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="386e9-153">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="386e9-153">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


