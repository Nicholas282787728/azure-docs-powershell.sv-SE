---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworksubnetconfig
schema: 2.0.0
ms.openlocfilehash: ede9f044698fe90c7d4394c4852cd20e96d7518d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930945"
---
# <span data-ttu-id="797d4-101">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="797d4-101">New-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="797d4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="797d4-102">SYNOPSIS</span></span>
<span data-ttu-id="797d4-103">Skapar en konfiguration för virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="797d4-103">Creates a virtual network subnet configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="797d4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="797d4-104">SYNTAX</span></span>

### <span data-ttu-id="797d4-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="797d4-105">SetByResource (Default)</span></span>
```
New-AzureRmVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="797d4-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="797d4-106">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="797d4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="797d4-107">DESCRIPTION</span></span>
<span data-ttu-id="797d4-108">Cmdleten **New-AzureRmVirtualNetworkSubnetConfig** skapar en konfiguration för virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="797d4-108">**The New-AzureRmVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="797d4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="797d4-109">EXAMPLES</span></span>

### <span data-ttu-id="797d4-110">1: skapa ett virtuellt nätverk med två undernät och en nätverks säkerhets grupp</span><span class="sxs-lookup"><span data-stu-id="797d4-110">1:  Create a virtual network with two subnets and a network security group</span></span>
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

<span data-ttu-id="797d4-111">I det här exemplet skapas två nya maskinvarukonfigurationer med hjälp av New-AzureRmVirtualSubnetConfig cmdlet och sedan används dessa för att skapa ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="797d4-111">This example creates two new subnet configurations using the New-AzureRmVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="797d4-112">New-AzureRmVirtualSubnetConfig mal len skapar bara en i-minnet-representation av under nätet.</span><span class="sxs-lookup"><span data-stu-id="797d4-112">The New-AzureRmVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="797d4-113">I det här exemplet har frontendSubnet CIDR 10.0.1.0/24 och refererar till en nätverks säkerhets grupp som tillåter RDP-åtkomst.</span><span class="sxs-lookup"><span data-stu-id="797d4-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="797d4-114">BackendSubnet har CIDR 10.0.2.0/24 och refererar till samma nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="797d4-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="797d4-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="797d4-115">PARAMETERS</span></span>

### <span data-ttu-id="797d4-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="797d4-116">-AddressPrefix</span></span>
<span data-ttu-id="797d4-117">Anger ett intervall med IP-adresser för en under nätverks konfiguration.</span><span class="sxs-lookup"><span data-stu-id="797d4-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="797d4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="797d4-118">-DefaultProfile</span></span>
<span data-ttu-id="797d4-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="797d4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="797d4-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="797d4-120">-Name</span></span>
<span data-ttu-id="797d4-121">Anger namnet på den nätmask som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="797d4-121">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="797d4-122">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="797d4-122">-NetworkSecurityGroup</span></span>
<span data-ttu-id="797d4-123">Anger ett NetworkSecurityGroup-objekt.</span><span class="sxs-lookup"><span data-stu-id="797d4-123">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="797d4-124">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="797d4-124">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="797d4-125">Anger ID för en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="797d4-125">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="797d4-126">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="797d4-126">-RouteTable</span></span>
<span data-ttu-id="797d4-127">Anger den routningstabell som är associerad med under nätets konfiguration.</span><span class="sxs-lookup"><span data-stu-id="797d4-127">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="797d4-128">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="797d4-128">-RouteTableId</span></span>
<span data-ttu-id="797d4-129">Anger ID för den väg tabell som är associerad med under nätets konfiguration.</span><span class="sxs-lookup"><span data-stu-id="797d4-129">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="797d4-130">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="797d4-130">-ServiceEndpoint</span></span>
<span data-ttu-id="797d4-131">Värde för tjänste slut punkt</span><span class="sxs-lookup"><span data-stu-id="797d4-131">Service Endpoint Value</span></span>

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

### <span data-ttu-id="797d4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="797d4-132">CommonParameters</span></span>
<span data-ttu-id="797d4-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="797d4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="797d4-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="797d4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="797d4-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="797d4-135">INPUTS</span></span>

## <span data-ttu-id="797d4-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="797d4-136">OUTPUTS</span></span>

### <span data-ttu-id="797d4-137">Microsoft. Azure. commands. Networks. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="797d4-137">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="797d4-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="797d4-138">NOTES</span></span>

## <span data-ttu-id="797d4-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="797d4-139">RELATED LINKS</span></span>

[<span data-ttu-id="797d4-140">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="797d4-140">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="797d4-141">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="797d4-141">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="797d4-142">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="797d4-142">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="797d4-143">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="797d4-143">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


