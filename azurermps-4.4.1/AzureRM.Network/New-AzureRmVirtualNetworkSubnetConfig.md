---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 4211e39555f98fd21a78085f3f49749da60c2b4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574595"
---
# <span data-ttu-id="ce902-101">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ce902-101">New-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="ce902-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ce902-102">SYNOPSIS</span></span>
<span data-ttu-id="ce902-103">Skapar en konfiguration för virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="ce902-103">Creates a virtual network subnet configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce902-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ce902-104">SYNTAX</span></span>

### <span data-ttu-id="ce902-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="ce902-105">SetByResource (Default)</span></span>
```
New-AzureRmVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce902-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ce902-106">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce902-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ce902-107">DESCRIPTION</span></span>
<span data-ttu-id="ce902-108">Cmdleten **New-AzureRmVirtualNetworkSubnetConfig** skapar en konfiguration för virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="ce902-108">**The New-AzureRmVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="ce902-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ce902-109">EXAMPLES</span></span>

### <span data-ttu-id="ce902-110">1: skapa ett virtuellt nätverk med två undernät och en nätverks säkerhets grupp</span><span class="sxs-lookup"><span data-stu-id="ce902-110">1:  Create a virtual network with two subnets and a network security group</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $rdpRule = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
    $networkSecurityGroup = New-AzureRmNetworkSecurityGroup -ResourceGroupName 
    TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup
    $backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup
    New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="ce902-111">I det här exemplet skapas två nya maskinvarukonfigurationer med hjälp av New-AzureRmVirtualSubnetConfig cmdlet och sedan används dessa för att skapa ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="ce902-111">This example creates two new subnet configurations using the New-AzureRmVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="ce902-112">New-AzureRmVirtualSubnetConfig mal len skapar bara en i-minnet-representation av under nätet.</span><span class="sxs-lookup"><span data-stu-id="ce902-112">The New-AzureRmVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="ce902-113">I det här exemplet har frontendSubnet CIDR 10.0.1.0/24 och refererar till en nätverks säkerhets grupp som tillåter RDP-åtkomst.</span><span class="sxs-lookup"><span data-stu-id="ce902-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="ce902-114">BackendSubnet har CIDR 10.0.2.0/24 och refererar till samma nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="ce902-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="ce902-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ce902-115">PARAMETERS</span></span>

### <span data-ttu-id="ce902-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ce902-116">-AddressPrefix</span></span>
<span data-ttu-id="ce902-117">Anger ett intervall med IP-adresser för en under nätverks konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ce902-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="ce902-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="ce902-118">-Name</span></span>
<span data-ttu-id="ce902-119">Anger namnet på den nätmask som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="ce902-119">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="ce902-120">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ce902-120">-NetworkSecurityGroup</span></span>
<span data-ttu-id="ce902-121">Anger ett NetworkSecurityGroup-objekt.</span><span class="sxs-lookup"><span data-stu-id="ce902-121">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="ce902-122">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="ce902-122">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="ce902-123">Anger ID för en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="ce902-123">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="ce902-124">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="ce902-124">-RouteTable</span></span>
<span data-ttu-id="ce902-125">Anger den routningstabell som är associerad med under nätets konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ce902-125">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="ce902-126">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="ce902-126">-RouteTableId</span></span>
<span data-ttu-id="ce902-127">Anger ID för den väg tabell som är associerad med under nätets konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ce902-127">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="ce902-128">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="ce902-128">-ServiceEndpoint</span></span>
<span data-ttu-id="ce902-129">Värde för tjänste slut punkt</span><span class="sxs-lookup"><span data-stu-id="ce902-129">Service Endpoint Value</span></span>

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

### <span data-ttu-id="ce902-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce902-130">-DefaultProfile</span></span>
<span data-ttu-id="ce902-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ce902-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce902-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce902-132">CommonParameters</span></span>
<span data-ttu-id="ce902-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce902-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce902-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce902-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce902-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ce902-135">INPUTS</span></span>

## <span data-ttu-id="ce902-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ce902-136">OUTPUTS</span></span>

### <span data-ttu-id="ce902-137">Microsoft. Azure. commands. Networks. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="ce902-137">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="ce902-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ce902-138">NOTES</span></span>

## <span data-ttu-id="ce902-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ce902-139">RELATED LINKS</span></span>

[<span data-ttu-id="ce902-140">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ce902-140">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="ce902-141">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ce902-141">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="ce902-142">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ce902-142">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="ce902-143">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ce902-143">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


