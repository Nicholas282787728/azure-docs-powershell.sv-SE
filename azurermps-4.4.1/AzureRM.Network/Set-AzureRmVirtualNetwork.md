---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
ms.openlocfilehash: a5158b1c2d1439286295a2f84f7273b37d608161
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585403"
---
# <span data-ttu-id="08f71-101">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="08f71-101">Set-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="08f71-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="08f71-102">SYNOPSIS</span></span>
<span data-ttu-id="08f71-103">Anger mål tillstånd för ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="08f71-103">Sets the goal state for a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08f71-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="08f71-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="08f71-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="08f71-105">DESCRIPTION</span></span>
<span data-ttu-id="08f71-106">Cmdleten **set-AzureRmVirtualNetwork** anger mål tillståndet för ett Azure Virtual Network.</span><span class="sxs-lookup"><span data-stu-id="08f71-106">The **Set-AzureRmVirtualNetwork** cmdlet sets the goal state for an Azure virtual network.</span></span>

## <span data-ttu-id="08f71-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="08f71-107">EXAMPLES</span></span>

### <span data-ttu-id="08f71-108">1: skapar ett virtuellt nätverk och tar bort ett av dess undernät</span><span class="sxs-lookup"><span data-stu-id="08f71-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

Remove-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="08f71-109">I det här exemplet skapas ett virtuellt nätverk med två undernät.</span><span class="sxs-lookup"><span data-stu-id="08f71-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="08f71-110">Sedan tas den bort från det virtuella nätverkets minnes representation.</span><span class="sxs-lookup"><span data-stu-id="08f71-110">Then it removes one subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="08f71-111">Set-AzureRmVirtualNetwork cmdlet används sedan för att skriva det ändrade virtuella nätverks tillståndet på tjänstens sida.</span><span class="sxs-lookup"><span data-stu-id="08f71-111">The Set-AzureRmVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span>

## <span data-ttu-id="08f71-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="08f71-112">PARAMETERS</span></span>

### <span data-ttu-id="08f71-113">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="08f71-113">-VirtualNetwork</span></span>
<span data-ttu-id="08f71-114">Anger ett **VirtualNetwork** -objekt som representerar mål tillståndet.</span><span class="sxs-lookup"><span data-stu-id="08f71-114">Specifies a **VirtualNetwork** object that represents the goal state.</span></span>

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

### <span data-ttu-id="08f71-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08f71-115">-DefaultProfile</span></span>
<span data-ttu-id="08f71-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="08f71-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08f71-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08f71-117">CommonParameters</span></span>
<span data-ttu-id="08f71-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08f71-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08f71-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08f71-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08f71-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="08f71-120">INPUTS</span></span>

### <span data-ttu-id="08f71-121">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="08f71-121">PSVirtualNetwork</span></span>
<span data-ttu-id="08f71-122">Parametern ' VirtualNetwork ' godkänner värdet av typen ' PSVirtualNetwork ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="08f71-122">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="08f71-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="08f71-123">OUTPUTS</span></span>

### <span data-ttu-id="08f71-124">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="08f71-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="08f71-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="08f71-125">NOTES</span></span>

## <span data-ttu-id="08f71-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="08f71-126">RELATED LINKS</span></span>

[<span data-ttu-id="08f71-127">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="08f71-127">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="08f71-128">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="08f71-128">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="08f71-129">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="08f71-129">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="08f71-130">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="08f71-130">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)


