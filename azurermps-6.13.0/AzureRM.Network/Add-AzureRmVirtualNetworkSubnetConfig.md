---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 1129b24c69dc362ea4d700be28a0823afa860885
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757577"
---
# <span data-ttu-id="33ad3-101">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="33ad3-101">Add-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="33ad3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="33ad3-102">SYNOPSIS</span></span>
<span data-ttu-id="33ad3-103">Lägger till en under nätverks konfiguration i ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="33ad3-103">Adds a subnet configuration to a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33ad3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="33ad3-104">SYNTAX</span></span>

### <span data-ttu-id="33ad3-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="33ad3-105">SetByResource (Default)</span></span>
```
Add-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-ServiceEndpointPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]>]
 [-Delegation <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33ad3-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="33ad3-106">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-ServiceEndpointPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]>]
 [-Delegation <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33ad3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="33ad3-107">DESCRIPTION</span></span>
<span data-ttu-id="33ad3-108">Cmdleten **Add-AzureRmVirtualNetworkSubnetConfig** lägger till en under nätverks konfiguration i ett befintligt Azure Virtual Network.</span><span class="sxs-lookup"><span data-stu-id="33ad3-108">The **Add-AzureRmVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="33ad3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="33ad3-109">EXAMPLES</span></span>

### <span data-ttu-id="33ad3-110">1: lägga till ett undernät i ett befintligt virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="33ad3-110">1: Add a subnet to an existing virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzureRmVirtualNetwork
```

  <span data-ttu-id="33ad3-111">I det här exemplet skapas en resurs grupp först som en behållare för de resurser som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="33ad3-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="33ad3-112">Därefter skapas en under nätverks konfiguration och används för att skapa ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="33ad3-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="33ad3-113">Add-AzureRmVirtualNetworkSubnetConfig används sedan för att lägga till ett undernät i det virtuella nätverk i minnet.</span><span class="sxs-lookup"><span data-stu-id="33ad3-113">The Add-AzureRmVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="33ad3-114">Kommandot Set-AzureRmVirtualNetwork uppdaterar det befintliga virtuella nätverket med det nya under nätet.</span><span class="sxs-lookup"><span data-stu-id="33ad3-114">The Set-AzureRmVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

### <span data-ttu-id="33ad3-115">2: lägga till en delegering i ett undernät som läggs till i ett befintligt virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="33ad3-115">2: Add a delegation to a subnet being added to an existing virtual network</span></span>
```powershell
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $delegation = New-AzureRmDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> Add-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet -AddressPrefix "10.0.2.0/24" -Delegation $delegation | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="33ad3-116">I det här exemplet får du först ett befintligt virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="33ad3-116">This example first gets an existing vnet.</span></span>
<span data-ttu-id="33ad3-117">Därefter skapas ett Delegerings objekt i minnet.</span><span class="sxs-lookup"><span data-stu-id="33ad3-117">Then, it creates a delegation object in memory.</span></span>
<span data-ttu-id="33ad3-118">Slutligen skapas ett nytt undernät med den delegering som läggs till i VNet.</span><span class="sxs-lookup"><span data-stu-id="33ad3-118">Finally, it creates a new subnet with that delegation that is added to the vnet.</span></span> <span data-ttu-id="33ad3-119">Den ändrade konfigurationen skickas till servern.</span><span class="sxs-lookup"><span data-stu-id="33ad3-119">The modified configuration is then sent to the server.</span></span>

## <span data-ttu-id="33ad3-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="33ad3-120">PARAMETERS</span></span>

### <span data-ttu-id="33ad3-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="33ad3-121">-AddressPrefix</span></span>
<span data-ttu-id="33ad3-122">Anger ett intervall med IP-adresser för en under nätverks konfiguration.</span><span class="sxs-lookup"><span data-stu-id="33ad3-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="33ad3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33ad3-123">-DefaultProfile</span></span>
<span data-ttu-id="33ad3-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="33ad3-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33ad3-125">-Delegation</span><span class="sxs-lookup"><span data-stu-id="33ad3-125">-Delegation</span></span>
<span data-ttu-id="33ad3-126">Lista över tjänster som har behörighet att utföra åtgärder i det här under nätet.</span><span class="sxs-lookup"><span data-stu-id="33ad3-126">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="33ad3-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="33ad3-127">-Name</span></span>
<span data-ttu-id="33ad3-128">Anger namnet på den under nätverks konfiguration som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="33ad3-128">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="33ad3-129">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="33ad3-129">-NetworkSecurityGroup</span></span>
<span data-ttu-id="33ad3-130">Anger ett **NetworkSecurityGroup** -objekt.</span><span class="sxs-lookup"><span data-stu-id="33ad3-130">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="33ad3-131">Denna cmdlet lägger till en konfiguration för virtuellt nätverk under det objekt som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="33ad3-131">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="33ad3-132">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="33ad3-132">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="33ad3-133">Anger ID för en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="33ad3-133">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="33ad3-134">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="33ad3-134">-RouteTable</span></span>
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

### <span data-ttu-id="33ad3-135">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="33ad3-135">-RouteTableId</span></span>
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

### <span data-ttu-id="33ad3-136">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="33ad3-136">-ServiceEndpoint</span></span>
<span data-ttu-id="33ad3-137">Värde för tjänste slut punkt</span><span class="sxs-lookup"><span data-stu-id="33ad3-137">Service Endpoint Value</span></span>

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

### <span data-ttu-id="33ad3-138">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="33ad3-138">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="33ad3-139">Principer för tjänste slut punkter</span><span class="sxs-lookup"><span data-stu-id="33ad3-139">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="33ad3-140">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="33ad3-140">-VirtualNetwork</span></span>
<span data-ttu-id="33ad3-141">Anger det **VirtualNetwork** -objekt som du vill lägga till en under näts konfiguration för.</span><span class="sxs-lookup"><span data-stu-id="33ad3-141">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="33ad3-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33ad3-142">CommonParameters</span></span>
<span data-ttu-id="33ad3-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33ad3-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33ad3-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33ad3-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33ad3-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="33ad3-145">INPUTS</span></span>

### <span data-ttu-id="33ad3-146">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="33ad3-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="33ad3-147">System. String</span><span class="sxs-lookup"><span data-stu-id="33ad3-147">System.String</span></span>

### <span data-ttu-id="33ad3-148">Microsoft. Azure. commands. Networks. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="33ad3-148">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="33ad3-149">Microsoft. Azure. commands. Networks. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="33ad3-149">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="33ad3-150">System. Collections. Generic. list ' 1 [[system. String, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="33ad3-150">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="33ad3-151">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSServiceEndpointPolicy, Microsoft. Azure. commands. Network, version = 6.7.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="33ad3-151">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="33ad3-152">System. Collections. Generic. list ' 1 [[Microsoft.Azure.Commands.Network.Models.PSDelegation, Microsoft. Azure. commands. Network, version = 6.7.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="33ad3-152">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSDelegation, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="33ad3-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="33ad3-153">OUTPUTS</span></span>

### <span data-ttu-id="33ad3-154">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="33ad3-154">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="33ad3-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="33ad3-155">NOTES</span></span>

## <span data-ttu-id="33ad3-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="33ad3-156">RELATED LINKS</span></span>

[<span data-ttu-id="33ad3-157">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="33ad3-157">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="33ad3-158">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="33ad3-158">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="33ad3-159">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="33ad3-159">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="33ad3-160">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="33ad3-160">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


