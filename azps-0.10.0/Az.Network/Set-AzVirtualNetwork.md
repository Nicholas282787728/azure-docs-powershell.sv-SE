---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetwork.md
ms.openlocfilehash: dc780e4b05b2f0ccb92f014f658a9b21aa1bd224
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924145"
---
# <span data-ttu-id="7fb2d-101">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7fb2d-101">Set-AzVirtualNetwork</span></span>

## <span data-ttu-id="7fb2d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7fb2d-102">SYNOPSIS</span></span>
<span data-ttu-id="7fb2d-103">Anger mål tillstånd för ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="7fb2d-103">Sets the goal state for a virtual network.</span></span>

## <span data-ttu-id="7fb2d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7fb2d-104">SYNTAX</span></span>

```
Set-AzVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fb2d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7fb2d-105">DESCRIPTION</span></span>
<span data-ttu-id="7fb2d-106">Cmdleten **set-AzVirtualNetwork** anger mål tillståndet för ett Azure Virtual Network.</span><span class="sxs-lookup"><span data-stu-id="7fb2d-106">The **Set-AzVirtualNetwork** cmdlet sets the goal state for an Azure virtual network.</span></span>

## <span data-ttu-id="7fb2d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7fb2d-107">EXAMPLES</span></span>

### <span data-ttu-id="7fb2d-108">1: skapar ett virtuellt nätverk och tar bort ett av dess undernät</span><span class="sxs-lookup"><span data-stu-id="7fb2d-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="7fb2d-109">I det här exemplet skapas ett virtuellt nätverk med två undernät.</span><span class="sxs-lookup"><span data-stu-id="7fb2d-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="7fb2d-110">Sedan tas den bort från det virtuella nätverkets minnes representation.</span><span class="sxs-lookup"><span data-stu-id="7fb2d-110">Then it removes one subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="7fb2d-111">Set-AzVirtualNetwork cmdlet används sedan för att skriva det ändrade virtuella nätverks tillståndet på tjänstens sida.</span><span class="sxs-lookup"><span data-stu-id="7fb2d-111">The Set-AzVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span>

## <span data-ttu-id="7fb2d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7fb2d-112">PARAMETERS</span></span>

### <span data-ttu-id="7fb2d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7fb2d-113">-AsJob</span></span>
<span data-ttu-id="7fb2d-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="7fb2d-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fb2d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fb2d-115">-DefaultProfile</span></span>
<span data-ttu-id="7fb2d-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7fb2d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fb2d-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7fb2d-117">-VirtualNetwork</span></span>
<span data-ttu-id="7fb2d-118">Anger ett **VirtualNetwork** -objekt som representerar mål tillståndet.</span><span class="sxs-lookup"><span data-stu-id="7fb2d-118">Specifies a **VirtualNetwork** object that represents the goal state.</span></span>

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

### <span data-ttu-id="7fb2d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fb2d-119">CommonParameters</span></span>
<span data-ttu-id="7fb2d-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fb2d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fb2d-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fb2d-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fb2d-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7fb2d-122">INPUTS</span></span>

### <span data-ttu-id="7fb2d-123">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7fb2d-123">PSVirtualNetwork</span></span>
<span data-ttu-id="7fb2d-124">Parametern ' VirtualNetwork ' godkänner värdet av typen ' PSVirtualNetwork ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="7fb2d-124">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="7fb2d-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7fb2d-125">OUTPUTS</span></span>

### <span data-ttu-id="7fb2d-126">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7fb2d-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="7fb2d-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7fb2d-127">NOTES</span></span>

## <span data-ttu-id="7fb2d-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7fb2d-128">RELATED LINKS</span></span>

[<span data-ttu-id="7fb2d-129">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7fb2d-129">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="7fb2d-130">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7fb2d-130">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="7fb2d-131">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7fb2d-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="7fb2d-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7fb2d-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)


