---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 9b5718dc7d0931a5a99e8f76ce4376b0753bc571
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756922"
---
# <span data-ttu-id="2c738-101">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2c738-101">Add-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="2c738-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2c738-102">SYNOPSIS</span></span>
<span data-ttu-id="2c738-103">Lägger till en under nätverks konfiguration i ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="2c738-103">Adds a subnet configuration to a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c738-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2c738-104">SYNTAX</span></span>

### <span data-ttu-id="2c738-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="2c738-105">SetByResource (Default)</span></span>
```
Add-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c738-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2c738-106">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c738-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2c738-107">DESCRIPTION</span></span>
<span data-ttu-id="2c738-108">Cmdleten **Add-AzureRmVirtualNetworkSubnetConfig** lägger till en under nätverks konfiguration i ett befintligt Azure Virtual Network.</span><span class="sxs-lookup"><span data-stu-id="2c738-108">The **Add-AzureRmVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="2c738-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2c738-109">EXAMPLES</span></span>

### <span data-ttu-id="2c738-110">1: lägga till ett undernät i ett befintligt virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="2c738-110">1: Add a subnet to an existing virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzureRmVirtualNetwork
```

  <span data-ttu-id="2c738-111">I det här exemplet skapas en resurs grupp först som en behållare för de resurser som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="2c738-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="2c738-112">Därefter skapas en under nätverks konfiguration och används för att skapa ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="2c738-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="2c738-113">Add-AzureRmVirtualNetworkSubnetConfig används sedan för att lägga till ett undernät i det virtuella nätverk i minnet.</span><span class="sxs-lookup"><span data-stu-id="2c738-113">The Add-AzureRmVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="2c738-114">Kommandot Set-AzureRmVirtualNetwork uppdaterar det befintliga virtuella nätverket med det nya under nätet.</span><span class="sxs-lookup"><span data-stu-id="2c738-114">The Set-AzureRmVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

## <span data-ttu-id="2c738-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2c738-115">PARAMETERS</span></span>

### <span data-ttu-id="2c738-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="2c738-116">-AddressPrefix</span></span>
<span data-ttu-id="2c738-117">Anger ett intervall med IP-adresser för en under nätverks konfiguration.</span><span class="sxs-lookup"><span data-stu-id="2c738-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="2c738-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="2c738-118">-Name</span></span>
<span data-ttu-id="2c738-119">Anger namnet på den under nätverks konfiguration som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="2c738-119">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="2c738-120">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2c738-120">-NetworkSecurityGroup</span></span>
<span data-ttu-id="2c738-121">Anger ett **NetworkSecurityGroup** -objekt.</span><span class="sxs-lookup"><span data-stu-id="2c738-121">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="2c738-122">Denna cmdlet lägger till en konfiguration för virtuellt nätverk under det objekt som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="2c738-122">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="2c738-123">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="2c738-123">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="2c738-124">Anger ID för en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="2c738-124">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="2c738-125">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="2c738-125">-RouteTable</span></span>
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

### <span data-ttu-id="2c738-126">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="2c738-126">-RouteTableId</span></span>
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

### <span data-ttu-id="2c738-127">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="2c738-127">-ServiceEndpoint</span></span>
<span data-ttu-id="2c738-128">Värde för tjänste slut punkt</span><span class="sxs-lookup"><span data-stu-id="2c738-128">Service Endpoint Value</span></span>

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

### <span data-ttu-id="2c738-129">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2c738-129">-VirtualNetwork</span></span>
<span data-ttu-id="2c738-130">Anger det **VirtualNetwork** -objekt som du vill lägga till en under näts konfiguration för.</span><span class="sxs-lookup"><span data-stu-id="2c738-130">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="2c738-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c738-131">-DefaultProfile</span></span>
<span data-ttu-id="2c738-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2c738-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c738-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c738-133">CommonParameters</span></span>
<span data-ttu-id="2c738-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c738-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c738-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c738-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c738-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2c738-136">INPUTS</span></span>

### <span data-ttu-id="2c738-137">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2c738-137">PSVirtualNetwork</span></span>
<span data-ttu-id="2c738-138">Parametern ' VirtualNetwork ' godkänner värdet av typen ' PSVirtualNetwork ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="2c738-138">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="2c738-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2c738-139">OUTPUTS</span></span>

### <span data-ttu-id="2c738-140">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2c738-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="2c738-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2c738-141">NOTES</span></span>

## <span data-ttu-id="2c738-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2c738-142">RELATED LINKS</span></span>

[<span data-ttu-id="2c738-143">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2c738-143">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="2c738-144">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2c738-144">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="2c738-145">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2c738-145">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="2c738-146">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2c738-146">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


