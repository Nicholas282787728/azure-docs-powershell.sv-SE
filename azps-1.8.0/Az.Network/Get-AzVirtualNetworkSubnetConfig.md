---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: e5b881547f84714e238f541948602569c773c9c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748192"
---
# <span data-ttu-id="f81b1-101">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f81b1-101">Get-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="f81b1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f81b1-102">SYNOPSIS</span></span>
<span data-ttu-id="f81b1-103">Hämtar ett undernät i ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="f81b1-103">Gets a subnet in a virtual network.</span></span>

## <span data-ttu-id="f81b1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f81b1-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f81b1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f81b1-105">DESCRIPTION</span></span>
<span data-ttu-id="f81b1-106">Cmdleten **Get-AzVirtualNetworkSubnetConfig** hämtar en eller flera konfigurationer i ett Azure-nätverk.</span><span class="sxs-lookup"><span data-stu-id="f81b1-106">The **Get-AzVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="f81b1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f81b1-107">EXAMPLES</span></span>

### <span data-ttu-id="f81b1-108">1: Hämta ett undernät i ett virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="f81b1-108">1: Get a subnet in a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="f81b1-109">I det här exemplet skapas en resurs grupp och ett virtuellt nätverk med ett enda undernät i den resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f81b1-109">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="f81b1-110">Då hämtas data om det under nätet.</span><span class="sxs-lookup"><span data-stu-id="f81b1-110">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="f81b1-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f81b1-111">PARAMETERS</span></span>

### <span data-ttu-id="f81b1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f81b1-112">-DefaultProfile</span></span>
<span data-ttu-id="f81b1-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f81b1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f81b1-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="f81b1-114">-Name</span></span>
<span data-ttu-id="f81b1-115">Anger namnet på den under nätverks konfiguration som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="f81b1-115">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f81b1-116">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f81b1-116">-VirtualNetwork</span></span>
<span data-ttu-id="f81b1-117">Anger det **VirtualNetwork** -objekt som innehåller den under näts konfiguration som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="f81b1-117">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f81b1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f81b1-118">CommonParameters</span></span>
<span data-ttu-id="f81b1-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f81b1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f81b1-120">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f81b1-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f81b1-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f81b1-121">INPUTS</span></span>

### <span data-ttu-id="f81b1-122">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f81b1-122">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="f81b1-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f81b1-123">OUTPUTS</span></span>

### <span data-ttu-id="f81b1-124">Microsoft. Azure. commands. Networks. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="f81b1-124">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="f81b1-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f81b1-125">NOTES</span></span>

## <span data-ttu-id="f81b1-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f81b1-126">RELATED LINKS</span></span>

[<span data-ttu-id="f81b1-127">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f81b1-127">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="f81b1-128">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f81b1-128">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="f81b1-129">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f81b1-129">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="f81b1-130">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f81b1-130">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)


