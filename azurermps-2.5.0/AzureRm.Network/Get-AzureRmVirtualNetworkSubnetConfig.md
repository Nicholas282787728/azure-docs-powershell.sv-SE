---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworksubnetconfig
schema: 2.0.0
ms.openlocfilehash: ceb009dba1984f69e7da3e04a9ae57a9da14c067
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931261"
---
# <span data-ttu-id="2b6a5-101">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2b6a5-101">Get-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="2b6a5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2b6a5-102">SYNOPSIS</span></span>
<span data-ttu-id="2b6a5-103">Hämtar ett undernät i ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="2b6a5-103">Gets a subnet in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b6a5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2b6a5-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b6a5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2b6a5-105">DESCRIPTION</span></span>
<span data-ttu-id="2b6a5-106">Cmdleten **Get-AzureRmVirtualNetworkSubnetConfig** hämtar en eller flera konfigurationer i ett Azure-nätverk.</span><span class="sxs-lookup"><span data-stu-id="2b6a5-106">The **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="2b6a5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2b6a5-107">EXAMPLES</span></span>

### <span data-ttu-id="2b6a5-108">1: Hämta ett undernät i ett virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="2b6a5-108">1: Get a subnet in a virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="2b6a5-109">I det här exemplet skapas en resurs grupp och ett virtuellt nätverk med ett enda undernät i den resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="2b6a5-109">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="2b6a5-110">Då hämtas data om det under nätet.</span><span class="sxs-lookup"><span data-stu-id="2b6a5-110">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="2b6a5-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2b6a5-111">PARAMETERS</span></span>

### <span data-ttu-id="2b6a5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b6a5-112">-DefaultProfile</span></span>
<span data-ttu-id="2b6a5-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2b6a5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b6a5-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="2b6a5-114">-Name</span></span>
<span data-ttu-id="2b6a5-115">Anger namnet på den under nätverks konfiguration som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="2b6a5-115">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="2b6a5-116">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2b6a5-116">-VirtualNetwork</span></span>
<span data-ttu-id="2b6a5-117">Anger det **VirtualNetwork** -objekt som innehåller den under näts konfiguration som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="2b6a5-117">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="2b6a5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b6a5-118">CommonParameters</span></span>
<span data-ttu-id="2b6a5-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b6a5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b6a5-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b6a5-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b6a5-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2b6a5-121">INPUTS</span></span>

### <span data-ttu-id="2b6a5-122">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2b6a5-122">PSVirtualNetwork</span></span>
<span data-ttu-id="2b6a5-123">Parametern ' VirtualNetwork ' godkänner värdet av typen ' PSVirtualNetwork ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="2b6a5-123">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="2b6a5-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2b6a5-124">OUTPUTS</span></span>

### <span data-ttu-id="2b6a5-125">Microsoft. Azure. commands. Networks. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="2b6a5-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="2b6a5-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2b6a5-126">NOTES</span></span>

## <span data-ttu-id="2b6a5-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2b6a5-127">RELATED LINKS</span></span>

[<span data-ttu-id="2b6a5-128">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2b6a5-128">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="2b6a5-129">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2b6a5-129">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="2b6a5-130">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2b6a5-130">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="2b6a5-131">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2b6a5-131">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


