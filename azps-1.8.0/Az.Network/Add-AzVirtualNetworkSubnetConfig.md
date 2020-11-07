---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 1df94cc14191fcb95e271bf5fef6b1a09fa77060
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748408"
---
# <span data-ttu-id="2977f-101">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2977f-101">Add-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="2977f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2977f-102">SYNOPSIS</span></span>
<span data-ttu-id="2977f-103">Lägger till en under nätverks konfiguration i ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="2977f-103">Adds a subnet configuration to a virtual network.</span></span>

## <span data-ttu-id="2977f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2977f-104">SYNTAX</span></span>

### <span data-ttu-id="2977f-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="2977f-105">SetByResource (Default)</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2977f-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2977f-106">SetByResourceId</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2977f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2977f-107">DESCRIPTION</span></span>
<span data-ttu-id="2977f-108">Cmdleten **Add-AzVirtualNetworkSubnetConfig** lägger till en under nätverks konfiguration i ett befintligt Azure Virtual Network.</span><span class="sxs-lookup"><span data-stu-id="2977f-108">The **Add-AzVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="2977f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2977f-109">EXAMPLES</span></span>

### <span data-ttu-id="2977f-110">1: lägga till ett undernät i ett befintligt virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="2977f-110">1: Add a subnet to an existing virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzVirtualNetwork
```

  <span data-ttu-id="2977f-111">I det här exemplet skapas en resurs grupp först som en behållare för de resurser som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="2977f-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="2977f-112">Därefter skapas en under nätverks konfiguration och används för att skapa ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="2977f-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="2977f-113">Add-AzVirtualNetworkSubnetConfig används sedan för att lägga till ett undernät i det virtuella nätverk i minnet.</span><span class="sxs-lookup"><span data-stu-id="2977f-113">The Add-AzVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="2977f-114">Kommandot Set-AzVirtualNetwork uppdaterar det befintliga virtuella nätverket med det nya under nätet.</span><span class="sxs-lookup"><span data-stu-id="2977f-114">The Set-AzVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

### <span data-ttu-id="2977f-115">2: lägga till en delegering i ett undernät som läggs till i ett befintligt virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="2977f-115">2: Add a delegation to a subnet being added to an existing virtual network</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> Add-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet -AddressPrefix "10.0.2.0/24" -Delegation $delegation | Set-AzVirtualNetwork
```

<span data-ttu-id="2977f-116">I det här exemplet får du först ett befintligt virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="2977f-116">This example first gets an existing vnet.</span></span>
<span data-ttu-id="2977f-117">Därefter skapas ett Delegerings objekt i minnet.</span><span class="sxs-lookup"><span data-stu-id="2977f-117">Then, it creates a delegation object in memory.</span></span>
<span data-ttu-id="2977f-118">Slutligen skapas ett nytt undernät med den delegering som läggs till i VNet.</span><span class="sxs-lookup"><span data-stu-id="2977f-118">Finally, it creates a new subnet with that delegation that is added to the vnet.</span></span> <span data-ttu-id="2977f-119">Den ändrade konfigurationen skickas till servern.</span><span class="sxs-lookup"><span data-stu-id="2977f-119">The modified configuration is then sent to the server.</span></span>

## <span data-ttu-id="2977f-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2977f-120">PARAMETERS</span></span>

### <span data-ttu-id="2977f-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="2977f-121">-AddressPrefix</span></span>
<span data-ttu-id="2977f-122">Anger ett intervall med IP-adresser för en under nätverks konfiguration.</span><span class="sxs-lookup"><span data-stu-id="2977f-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="2977f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2977f-123">-DefaultProfile</span></span>
<span data-ttu-id="2977f-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2977f-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2977f-125">-Delegation</span><span class="sxs-lookup"><span data-stu-id="2977f-125">-Delegation</span></span>
<span data-ttu-id="2977f-126">Lista över tjänster som har behörighet att utföra åtgärder i det här under nätet.</span><span class="sxs-lookup"><span data-stu-id="2977f-126">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="2977f-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="2977f-127">-Name</span></span>
<span data-ttu-id="2977f-128">Anger namnet på den under nätverks konfiguration som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="2977f-128">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="2977f-129">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2977f-129">-NetworkSecurityGroup</span></span>
<span data-ttu-id="2977f-130">Anger ett **NetworkSecurityGroup** -objekt.</span><span class="sxs-lookup"><span data-stu-id="2977f-130">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="2977f-131">Denna cmdlet lägger till en konfiguration för virtuellt nätverk under det objekt som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="2977f-131">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="2977f-132">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="2977f-132">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="2977f-133">Anger ID för en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="2977f-133">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="2977f-134">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="2977f-134">-RouteTable</span></span>
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

### <span data-ttu-id="2977f-135">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="2977f-135">-RouteTableId</span></span>
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

### <span data-ttu-id="2977f-136">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="2977f-136">-ServiceEndpoint</span></span>
<span data-ttu-id="2977f-137">Värde för tjänste slut punkt</span><span class="sxs-lookup"><span data-stu-id="2977f-137">Service Endpoint Value</span></span>

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

### <span data-ttu-id="2977f-138">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2977f-138">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="2977f-139">Principer för tjänste slut punkter</span><span class="sxs-lookup"><span data-stu-id="2977f-139">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="2977f-140">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2977f-140">-VirtualNetwork</span></span>
<span data-ttu-id="2977f-141">Anger det **VirtualNetwork** -objekt som du vill lägga till en under näts konfiguration för.</span><span class="sxs-lookup"><span data-stu-id="2977f-141">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="2977f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2977f-142">CommonParameters</span></span>
<span data-ttu-id="2977f-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2977f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2977f-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2977f-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2977f-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2977f-145">INPUTS</span></span>

### <span data-ttu-id="2977f-146">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2977f-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="2977f-147">System. String</span><span class="sxs-lookup"><span data-stu-id="2977f-147">System.String</span></span>

### <span data-ttu-id="2977f-148">Microsoft. Azure. commands. Networks. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2977f-148">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="2977f-149">Microsoft. Azure. commands. Networks. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="2977f-149">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="2977f-150">System. string []</span><span class="sxs-lookup"><span data-stu-id="2977f-150">System.String[]</span></span>

### <span data-ttu-id="2977f-151">Microsoft. Azure. commands. Network. Models. PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="2977f-151">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="2977f-152">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="2977f-152">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="2977f-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2977f-153">OUTPUTS</span></span>

### <span data-ttu-id="2977f-154">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2977f-154">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="2977f-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2977f-155">NOTES</span></span>

## <span data-ttu-id="2977f-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2977f-156">RELATED LINKS</span></span>

[<span data-ttu-id="2977f-157">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2977f-157">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="2977f-158">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2977f-158">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="2977f-159">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2977f-159">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="2977f-160">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2977f-160">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
