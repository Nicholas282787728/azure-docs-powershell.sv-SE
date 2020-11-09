---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: dcc5e688838508e6917a6732b24d7de3b27b2737
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322482"
---
# <span data-ttu-id="d80bf-101">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d80bf-101">Get-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="d80bf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d80bf-102">SYNOPSIS</span></span>
<span data-ttu-id="d80bf-103">Hämtar ett undernät i ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="d80bf-103">Gets a subnet in a virtual network.</span></span>

## <span data-ttu-id="d80bf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d80bf-104">SYNTAX</span></span>

### <span data-ttu-id="d80bf-105">GetByVirtualNetwork (standard)</span><span class="sxs-lookup"><span data-stu-id="d80bf-105">GetByVirtualNetwork (Default)</span></span>
```
Get-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d80bf-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d80bf-106">GetByResourceId</span></span>
```
Get-AzVirtualNetworkSubnetConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d80bf-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d80bf-107">DESCRIPTION</span></span>
<span data-ttu-id="d80bf-108">Cmdleten **Get-AzVirtualNetworkSubnetConfig** hämtar en eller flera konfigurationer i ett Azure-nätverk.</span><span class="sxs-lookup"><span data-stu-id="d80bf-108">The **Get-AzVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="d80bf-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d80bf-109">EXAMPLES</span></span>

### <span data-ttu-id="d80bf-110">1: Hämta ett undernät i ett virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="d80bf-110">1: Get a subnet in a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="d80bf-111">I det här exemplet skapas en resurs grupp och ett virtuellt nätverk med ett enda undernät i den resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d80bf-111">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="d80bf-112">Då hämtas data om det under nätet.</span><span class="sxs-lookup"><span data-stu-id="d80bf-112">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="d80bf-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d80bf-113">PARAMETERS</span></span>

### <span data-ttu-id="d80bf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d80bf-114">-DefaultProfile</span></span>
<span data-ttu-id="d80bf-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d80bf-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d80bf-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="d80bf-116">-Name</span></span>
<span data-ttu-id="d80bf-117">Anger namnet på den under nätverks konfiguration som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="d80bf-117">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByVirtualNetwork
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d80bf-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d80bf-118">-ResourceId</span></span>
<span data-ttu-id="d80bf-119">Anger resurs-ID för det undernät som denna cmdlet hämtar.</span><span class="sxs-lookup"><span data-stu-id="d80bf-119">Specifies the resource id of the subnet that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d80bf-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d80bf-120">-VirtualNetwork</span></span>
<span data-ttu-id="d80bf-121">Anger det **VirtualNetwork** -objekt som innehåller den under näts konfiguration som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="d80bf-121">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: GetByVirtualNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d80bf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d80bf-122">CommonParameters</span></span>
<span data-ttu-id="d80bf-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d80bf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d80bf-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d80bf-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d80bf-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d80bf-125">INPUTS</span></span>

### <span data-ttu-id="d80bf-126">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d80bf-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="d80bf-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d80bf-127">System.String</span></span>

## <span data-ttu-id="d80bf-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d80bf-128">OUTPUTS</span></span>

### <span data-ttu-id="d80bf-129">Microsoft. Azure. commands. Networks. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="d80bf-129">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="d80bf-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d80bf-130">NOTES</span></span>

## <span data-ttu-id="d80bf-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d80bf-131">RELATED LINKS</span></span>

[<span data-ttu-id="d80bf-132">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d80bf-132">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="d80bf-133">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d80bf-133">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="d80bf-134">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d80bf-134">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="d80bf-135">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d80bf-135">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
