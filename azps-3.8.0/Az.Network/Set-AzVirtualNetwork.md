---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
ms.openlocfilehash: 822b982b2c1714e2c0331cc9b64fe2c1753044f7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93928038"
---
# <span data-ttu-id="bda7c-101">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bda7c-101">Set-AzVirtualNetwork</span></span>

## <span data-ttu-id="bda7c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bda7c-102">SYNOPSIS</span></span>
<span data-ttu-id="bda7c-103">Uppdaterar ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="bda7c-103">Updates a virtual network.</span></span>

## <span data-ttu-id="bda7c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bda7c-104">SYNTAX</span></span>

```
Set-AzVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bda7c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bda7c-105">DESCRIPTION</span></span>
<span data-ttu-id="bda7c-106">Cmdleten **set-AzVirtualNetwork** uppdaterar ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="bda7c-106">The **Set-AzVirtualNetwork** cmdlet updates a virtual network.</span></span>

## <span data-ttu-id="bda7c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bda7c-107">EXAMPLES</span></span>

### <span data-ttu-id="bda7c-108">1: skapar ett virtuellt nätverk och tar bort ett av dess undernät</span><span class="sxs-lookup"><span data-stu-id="bda7c-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" ## Create resource group
$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24" ## Create backend subnet

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet ## Create virtual network

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork ## Remove subnet from in memory representation of virtual network

$virtualNetwork | Set-AzVirtualNetwork ## Remove subnet from virtual network
```

<span data-ttu-id="bda7c-109">I det här exemplet skapas ett virtuellt nätverk med namnet TestResourceGroup med två undernät: frontendSubnet och backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="bda7c-109">This example creates a virtual network called TestResourceGroup with two subnets: frontendSubnet and backendSubnet.</span></span> <span data-ttu-id="bda7c-110">Sedan tas den bort från backendSubnet i minnet för det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="bda7c-110">Then it removes backendSubnet subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="bda7c-111">Set-AzVirtualNetwork cmdlet används sedan för att skriva det ändrade virtuella nätverks tillståndet på tjänstens sida.</span><span class="sxs-lookup"><span data-stu-id="bda7c-111">The Set-AzVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span> <span data-ttu-id="bda7c-112">När Set-AzVirtualNetwork cmdlet körs tas backendSubnet bort.</span><span class="sxs-lookup"><span data-stu-id="bda7c-112">When the Set-AzVirtualNetwork cmdlet is executed, the backendSubnet is removed.</span></span>

## <span data-ttu-id="bda7c-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bda7c-113">PARAMETERS</span></span>

### <span data-ttu-id="bda7c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bda7c-114">-AsJob</span></span>
<span data-ttu-id="bda7c-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="bda7c-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bda7c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bda7c-116">-DefaultProfile</span></span>
<span data-ttu-id="bda7c-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bda7c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bda7c-118">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bda7c-118">-VirtualNetwork</span></span>
<span data-ttu-id="bda7c-119">Anger ett virtuellt nätverks objekt som representerar tillståndet som det virtuella nätverket ska ställas in i.</span><span class="sxs-lookup"><span data-stu-id="bda7c-119">Specifies a virtual network object representing the state to which the virtual network should be set.</span></span>

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

### <span data-ttu-id="bda7c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bda7c-120">CommonParameters</span></span>
<span data-ttu-id="bda7c-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bda7c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bda7c-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bda7c-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bda7c-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bda7c-123">INPUTS</span></span>

### <span data-ttu-id="bda7c-124">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bda7c-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="bda7c-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bda7c-125">OUTPUTS</span></span>

### <span data-ttu-id="bda7c-126">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bda7c-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="bda7c-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bda7c-127">NOTES</span></span>

## <span data-ttu-id="bda7c-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bda7c-128">RELATED LINKS</span></span>

[<span data-ttu-id="bda7c-129">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bda7c-129">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="bda7c-130">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bda7c-130">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="bda7c-131">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bda7c-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="bda7c-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bda7c-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)


