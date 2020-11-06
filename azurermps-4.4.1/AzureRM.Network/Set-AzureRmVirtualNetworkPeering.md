---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 06DAD751-3A43-4EF6-94C5-AA7AC1A67FC8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: aaaca86109331543d8e1b292e0e04ea7b5cbb5f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574568"
---
# <span data-ttu-id="51476-101">Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="51476-101">Set-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="51476-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="51476-102">SYNOPSIS</span></span>
<span data-ttu-id="51476-103">Konfigurerar en peering med virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="51476-103">Configures a virtual network peering.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51476-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="51476-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering <PSVirtualNetworkPeering>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51476-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="51476-105">DESCRIPTION</span></span>
<span data-ttu-id="51476-106">Cmdleten **set-AzureRmVirtualNetworkPeering** konfigurerar en virtuell nätverks-peering.</span><span class="sxs-lookup"><span data-stu-id="51476-106">The **Set-AzureRmVirtualNetworkPeering** cmdlet configures a virtual network peering.</span></span>

## <span data-ttu-id="51476-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="51476-107">EXAMPLES</span></span>

### <span data-ttu-id="51476-108">Exempel 1: ändra konfiguration av vidarebefordrad trafik för ett virtuellt nätverks-peering</span><span class="sxs-lookup"><span data-stu-id="51476-108">Example 1: Change forwarded traffic configuration of a virtual network peering</span></span>
```
# Get the virtual network peering you want to update information for
Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup" -Name "myVnet1ToMyVnet2"

# Change value of AllowForwardedTraffic property
$myVnet1ToMyVnet2.AllowForwardedTraffic = $True

# Update the peering with changes made
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1ToMyVnet2
```

### <span data-ttu-id="51476-109">Exempel 2: Ändra virtuell nätverks åtkomst för en virtuell nätverks-peering</span><span class="sxs-lookup"><span data-stu-id="51476-109">Example 2: Change virtual network access of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowVirtualNetworkAccess property
$myVnet1TomyVnet2.AllowVirtualNetworkAccess = $False

# Update virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="51476-110">Exempel 3: ändra egenskapen för gateway-överföring för ett virtuellt nätverks-peering</span><span class="sxs-lookup"><span data-stu-id="51476-110">Example 3: Change gateway transit property configuration of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowGatewayTransit property
$myVnet1TomyVnet2.AllowGatewayTransit = $True

# Update the virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="51476-111">Exempel 4: använda Fjärrgateways i virtuellt nätverks-peering</span><span class="sxs-lookup"><span data-stu-id="51476-111">Example 4: Use remote gateways in virtual network peering</span></span>
```
# Get the virtual network peering 
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup001" -Name "myVnet1TomyVnet2"

# Change the UseRemoteGateways property
$myVnet1TomyVnet2.UseRemoteGateways = $True

# Update the virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $LinkToVNet2
```

<span data-ttu-id="51476-112">Genom att ändra den här egenskapen till $True kan motpartens VNet-Gateway användas.</span><span class="sxs-lookup"><span data-stu-id="51476-112">By changing this property to $True, your peer's VNet gateway can be used.</span></span>
<span data-ttu-id="51476-113">Peer VNet måste emellertid ha en konfigurerad gateway och **AllowGatewayTransit** måste ha ett värde för $True.</span><span class="sxs-lookup"><span data-stu-id="51476-113">However, the peer VNet must have a gateway configured and **AllowGatewayTransit** must have a value of $True.</span></span>

<span data-ttu-id="51476-114">Den här egenskapen kan inte användas om en gateway redan har kon figurer ATS.</span><span class="sxs-lookup"><span data-stu-id="51476-114">This property cannot be used if a gateway has already been configured.</span></span>

## <span data-ttu-id="51476-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="51476-115">PARAMETERS</span></span>

### <span data-ttu-id="51476-116">-VirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="51476-116">-VirtualNetworkPeering</span></span>
<span data-ttu-id="51476-117">Anger virtuell nätverks-peering.</span><span class="sxs-lookup"><span data-stu-id="51476-117">Specifies the virtual network peering.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51476-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51476-118">-DefaultProfile</span></span>
<span data-ttu-id="51476-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="51476-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51476-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51476-120">CommonParameters</span></span>
<span data-ttu-id="51476-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51476-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51476-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51476-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51476-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="51476-123">INPUTS</span></span>

### <span data-ttu-id="51476-124">PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="51476-124">PSVirtualNetworkPeering</span></span>
<span data-ttu-id="51476-125">Parametern ' VirtualNetworkPeering ' godkänner värdet av typen ' PSVirtualNetworkPeering ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="51476-125">Parameter 'VirtualNetworkPeering' accepts value of type 'PSVirtualNetworkPeering' from the pipeline</span></span>

## <span data-ttu-id="51476-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="51476-126">OUTPUTS</span></span>

### <span data-ttu-id="51476-127">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="51476-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="51476-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="51476-128">NOTES</span></span>

## <span data-ttu-id="51476-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="51476-129">RELATED LINKS</span></span>

[<span data-ttu-id="51476-130">Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="51476-130">Add-AzureRmVirtualNetworkPeering</span></span>](./Add-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="51476-131">Get-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="51476-131">Get-AzureRmVirtualNetworkPeering</span></span>](./Get-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="51476-132">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="51476-132">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)


