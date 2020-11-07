---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 47FE9EF4-6000-4096-8F04-26A0C6661FDB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworksubnetconfig
schema: 2.0.0
ms.openlocfilehash: 4020f6aa32a7dda31f97831badf9f7916f3db10f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931190"
---
# <span data-ttu-id="4fdc1-101">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4fdc1-101">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="4fdc1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4fdc1-102">SYNOPSIS</span></span>
<span data-ttu-id="4fdc1-103">Tar bort en under nätverks konfiguration från ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="4fdc1-103">Removes a subnet configuration from a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fdc1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4fdc1-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fdc1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4fdc1-105">DESCRIPTION</span></span>
<span data-ttu-id="4fdc1-106">Cmdleten **Remove-AzureRmVirtualNetworkSubnetConfig** tar bort ett undernät från ett virtuellt Azure-nätverk.</span><span class="sxs-lookup"><span data-stu-id="4fdc1-106">The **Remove-AzureRmVirtualNetworkSubnetConfig** cmdlet removes a subnet from an Azure virtual network.</span></span>

## <span data-ttu-id="4fdc1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4fdc1-107">EXAMPLES</span></span>

### <span data-ttu-id="4fdc1-108">1: ta bort ett undernät från ett virtuellt nätverk och uppdatera det virtuella nätverket</span><span class="sxs-lookup"><span data-stu-id="4fdc1-108">1: Remove a subnet from a virtual network and update the virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet 
    $frontendSubnet,$backendSubnet

Remove-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork 
    $virtualNetwork
    $virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="4fdc1-109">I det här exemplet skapas en resurs grupp och ett virtuellt nätverk med två undernät.</span><span class="sxs-lookup"><span data-stu-id="4fdc1-109">This example creates a resource group and a virtual network with two subnets.</span></span> <span data-ttu-id="4fdc1-110">Därefter används kommandot Remove-AzureRmVirtualNetworkSubnetConfig för att ta bort backend-undernätet från det virtuella nätverkets minnes representation.</span><span class="sxs-lookup"><span data-stu-id="4fdc1-110">It then uses the Remove-AzureRmVirtualNetworkSubnetConfig command to remove the backend subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="4fdc1-111">Set-AzureRmVirtualNetwork anropas sedan för att ändra det virtuella nätverket på Server sidan.</span><span class="sxs-lookup"><span data-stu-id="4fdc1-111">Set-AzureRmVirtualNetwork is then called to modify the virtual network on the server side.</span></span>

## <span data-ttu-id="4fdc1-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4fdc1-112">PARAMETERS</span></span>

### <span data-ttu-id="4fdc1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fdc1-113">-DefaultProfile</span></span>
<span data-ttu-id="4fdc1-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4fdc1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fdc1-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="4fdc1-115">-Name</span></span>
<span data-ttu-id="4fdc1-116">Anger namnet på den Subnet-konfiguration som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="4fdc1-116">Specifies the name of the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="4fdc1-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4fdc1-117">-VirtualNetwork</span></span>
<span data-ttu-id="4fdc1-118">Anger det **VirtualNetwork** -objekt som innehåller den nätmask som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="4fdc1-118">Specifies the **VirtualNetwork** object that contains the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="4fdc1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fdc1-119">CommonParameters</span></span>
<span data-ttu-id="4fdc1-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fdc1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fdc1-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fdc1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fdc1-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4fdc1-122">INPUTS</span></span>

### <span data-ttu-id="4fdc1-123">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4fdc1-123">PSVirtualNetwork</span></span>
<span data-ttu-id="4fdc1-124">Parametern ' VirtualNetwork ' godkänner värdet av typen ' PSVirtualNetwork ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="4fdc1-124">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="4fdc1-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4fdc1-125">OUTPUTS</span></span>

### <span data-ttu-id="4fdc1-126">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4fdc1-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="4fdc1-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4fdc1-127">NOTES</span></span>

## <span data-ttu-id="4fdc1-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4fdc1-128">RELATED LINKS</span></span>

[<span data-ttu-id="4fdc1-129">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4fdc1-129">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="4fdc1-130">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4fdc1-130">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="4fdc1-131">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4fdc1-131">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="4fdc1-132">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4fdc1-132">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


