---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47FE9EF4-6000-4096-8F04-26A0C6661FDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 7d90ffff788239996f7b79f7e56493611db86e04
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091697"
---
# <span data-ttu-id="9c81e-101">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9c81e-101">Remove-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="9c81e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9c81e-102">SYNOPSIS</span></span>
<span data-ttu-id="9c81e-103">Tar bort en under nätverks konfiguration från ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="9c81e-103">Removes a subnet configuration from a virtual network.</span></span>

## <span data-ttu-id="9c81e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9c81e-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c81e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9c81e-105">DESCRIPTION</span></span>
<span data-ttu-id="9c81e-106">Cmdleten **Remove-AzVirtualNetworkSubnetConfig** tar bort ett undernät från ett virtuellt Azure-nätverk.</span><span class="sxs-lookup"><span data-stu-id="9c81e-106">The **Remove-AzVirtualNetworkSubnetConfig** cmdlet removes a subnet from an Azure virtual network.</span></span>

## <span data-ttu-id="9c81e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9c81e-107">EXAMPLES</span></span>

### <span data-ttu-id="9c81e-108">1: ta bort ett undernät från ett virtuellt nätverk och uppdatera det virtuella nätverket</span><span class="sxs-lookup"><span data-stu-id="9c81e-108">1: Remove a subnet from a virtual network and update the virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet 
    $frontendSubnet,$backendSubnet

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork 
    $virtualNetwork
    $virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="9c81e-109">I det här exemplet skapas en resurs grupp och ett virtuellt nätverk med två undernät.</span><span class="sxs-lookup"><span data-stu-id="9c81e-109">This example creates a resource group and a virtual network with two subnets.</span></span> <span data-ttu-id="9c81e-110">Därefter används kommandot Remove-AzVirtualNetworkSubnetConfig för att ta bort backend-undernätet från det virtuella nätverkets minnes representation.</span><span class="sxs-lookup"><span data-stu-id="9c81e-110">It then uses the Remove-AzVirtualNetworkSubnetConfig command to remove the backend subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="9c81e-111">Set-AzVirtualNetwork anropas sedan för att ändra det virtuella nätverket på Server sidan.</span><span class="sxs-lookup"><span data-stu-id="9c81e-111">Set-AzVirtualNetwork is then called to modify the virtual network on the server side.</span></span>

## <span data-ttu-id="9c81e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9c81e-112">PARAMETERS</span></span>

### <span data-ttu-id="9c81e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c81e-113">-DefaultProfile</span></span>
<span data-ttu-id="9c81e-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9c81e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c81e-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="9c81e-115">-Name</span></span>
<span data-ttu-id="9c81e-116">Anger namnet på den Subnet-konfiguration som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="9c81e-116">Specifies the name of the subnet configuration to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c81e-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9c81e-117">-VirtualNetwork</span></span>
<span data-ttu-id="9c81e-118">Anger det **VirtualNetwork** -objekt som innehåller den nätmask som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="9c81e-118">Specifies the **VirtualNetwork** object that contains the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="9c81e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c81e-119">CommonParameters</span></span>
<span data-ttu-id="9c81e-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c81e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c81e-121">Mer information finns i [about_CommonParameters] ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c81e-121">For more information, see [about_CommonParameters] (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c81e-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9c81e-122">INPUTS</span></span>

### <span data-ttu-id="9c81e-123">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9c81e-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="9c81e-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9c81e-124">OUTPUTS</span></span>

### <span data-ttu-id="9c81e-125">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9c81e-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="9c81e-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9c81e-126">NOTES</span></span>

## <span data-ttu-id="9c81e-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9c81e-127">RELATED LINKS</span></span>

[<span data-ttu-id="9c81e-128">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9c81e-128">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="9c81e-129">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9c81e-129">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="9c81e-130">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9c81e-130">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="9c81e-131">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9c81e-131">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)


