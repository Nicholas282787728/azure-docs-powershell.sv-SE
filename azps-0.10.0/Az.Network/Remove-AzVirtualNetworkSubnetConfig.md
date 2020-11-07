---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47FE9EF4-6000-4096-8F04-26A0C6661FDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 5f05672c5fd3f0866652507fd0f61f7a8b6e0fcc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924318"
---
# <span data-ttu-id="1dd89-101">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1dd89-101">Remove-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="1dd89-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1dd89-102">SYNOPSIS</span></span>
<span data-ttu-id="1dd89-103">Tar bort en under nätverks konfiguration från ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="1dd89-103">Removes a subnet configuration from a virtual network.</span></span>

## <span data-ttu-id="1dd89-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1dd89-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1dd89-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1dd89-105">DESCRIPTION</span></span>
<span data-ttu-id="1dd89-106">Cmdleten **Remove-AzVirtualNetworkSubnetConfig** tar bort ett undernät från ett virtuellt Azure-nätverk.</span><span class="sxs-lookup"><span data-stu-id="1dd89-106">The **Remove-AzVirtualNetworkSubnetConfig** cmdlet removes a subnet from an Azure virtual network.</span></span>

## <span data-ttu-id="1dd89-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1dd89-107">EXAMPLES</span></span>

### <span data-ttu-id="1dd89-108">1: ta bort ett undernät från ett virtuellt nätverk och uppdatera det virtuella nätverket</span><span class="sxs-lookup"><span data-stu-id="1dd89-108">1: Remove a subnet from a virtual network and update the virtual network</span></span>
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

<span data-ttu-id="1dd89-109">I det här exemplet skapas en resurs grupp och ett virtuellt nätverk med två undernät.</span><span class="sxs-lookup"><span data-stu-id="1dd89-109">This example creates a resource group and a virtual network with two subnets.</span></span> <span data-ttu-id="1dd89-110">Därefter används kommandot Remove-AzVirtualNetworkSubnetConfig för att ta bort backend-undernätet från det virtuella nätverkets minnes representation.</span><span class="sxs-lookup"><span data-stu-id="1dd89-110">It then uses the Remove-AzVirtualNetworkSubnetConfig command to remove the backend subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="1dd89-111">Set-AzVirtualNetwork anropas sedan för att ändra det virtuella nätverket på Server sidan.</span><span class="sxs-lookup"><span data-stu-id="1dd89-111">Set-AzVirtualNetwork is then called to modify the virtual network on the server side.</span></span>

## <span data-ttu-id="1dd89-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1dd89-112">PARAMETERS</span></span>

### <span data-ttu-id="1dd89-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dd89-113">-DefaultProfile</span></span>
<span data-ttu-id="1dd89-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1dd89-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1dd89-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="1dd89-115">-Name</span></span>
<span data-ttu-id="1dd89-116">Anger namnet på den Subnet-konfiguration som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="1dd89-116">Specifies the name of the subnet configuration to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dd89-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1dd89-117">-VirtualNetwork</span></span>
<span data-ttu-id="1dd89-118">Anger det **VirtualNetwork** -objekt som innehåller den nätmask som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="1dd89-118">Specifies the **VirtualNetwork** object that contains the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="1dd89-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dd89-119">CommonParameters</span></span>
<span data-ttu-id="1dd89-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dd89-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dd89-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dd89-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dd89-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1dd89-122">INPUTS</span></span>

### <span data-ttu-id="1dd89-123">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1dd89-123">PSVirtualNetwork</span></span>
<span data-ttu-id="1dd89-124">Parametern ' VirtualNetwork ' godkänner värdet av typen ' PSVirtualNetwork ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="1dd89-124">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="1dd89-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1dd89-125">OUTPUTS</span></span>

### <span data-ttu-id="1dd89-126">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1dd89-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="1dd89-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1dd89-127">NOTES</span></span>

## <span data-ttu-id="1dd89-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1dd89-128">RELATED LINKS</span></span>

[<span data-ttu-id="1dd89-129">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1dd89-129">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="1dd89-130">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1dd89-130">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="1dd89-131">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1dd89-131">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="1dd89-132">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1dd89-132">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)


