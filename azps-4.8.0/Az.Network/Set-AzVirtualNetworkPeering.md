---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 06DAD751-3A43-4EF6-94C5-AA7AC1A67FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkPeering.md
ms.openlocfilehash: 421358a9241fe41549898547c62404f6ba1162e0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262041"
---
# <span data-ttu-id="b27ba-101">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="b27ba-101">Set-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="b27ba-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b27ba-102">SYNOPSIS</span></span>
<span data-ttu-id="b27ba-103">Konfigurerar en peering med virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="b27ba-103">Configures a virtual network peering.</span></span>

## <span data-ttu-id="b27ba-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b27ba-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkPeering -VirtualNetworkPeering <PSVirtualNetworkPeering> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b27ba-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b27ba-105">DESCRIPTION</span></span>
<span data-ttu-id="b27ba-106">Cmdleten **set-AzVirtualNetworkPeering** konfigurerar en virtuell nätverks-peering.</span><span class="sxs-lookup"><span data-stu-id="b27ba-106">The **Set-AzVirtualNetworkPeering** cmdlet configures a virtual network peering.</span></span>

## <span data-ttu-id="b27ba-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b27ba-107">EXAMPLES</span></span>

### <span data-ttu-id="b27ba-108">Exempel 1: ändra konfiguration av vidarebefordrad trafik för ett virtuellt nätverks-peering</span><span class="sxs-lookup"><span data-stu-id="b27ba-108">Example 1: Change forwarded traffic configuration of a virtual network peering</span></span>
```
# Get the virtual network peering you want to update information for
Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup" -Name "myVnet1ToMyVnet2"

# Change value of AllowForwardedTraffic property
$myVnet1ToMyVnet2.AllowForwardedTraffic = $True

# Update the peering with changes made
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1ToMyVnet2
```

### <span data-ttu-id="b27ba-109">Exempel 2: Ändra virtuell nätverks åtkomst för en virtuell nätverks-peering</span><span class="sxs-lookup"><span data-stu-id="b27ba-109">Example 2: Change virtual network access of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowVirtualNetworkAccess property
$myVnet1TomyVnet2.AllowVirtualNetworkAccess = $False

# Update virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="b27ba-110">Exempel 3: ändra egenskapen för gateway-överföring för ett virtuellt nätverks-peering</span><span class="sxs-lookup"><span data-stu-id="b27ba-110">Example 3: Change gateway transit property configuration of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowGatewayTransit property
$myVnet1TomyVnet2.AllowGatewayTransit = $True

# Update the virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="b27ba-111">Exempel 4: använda Fjärrgateways i virtuellt nätverks-peering</span><span class="sxs-lookup"><span data-stu-id="b27ba-111">Example 4: Use remote gateways in virtual network peering</span></span>
```
# Get the virtual network peering 
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup001" -Name "myVnet1TomyVnet2"

# Change the UseRemoteGateways property
$myVnet1TomyVnet2.UseRemoteGateways = $True

# Update the virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

<span data-ttu-id="b27ba-112">Genom att ändra den här egenskapen till $True kan motpartens VNet-Gateway användas.</span><span class="sxs-lookup"><span data-stu-id="b27ba-112">By changing this property to $True, your peer's VNet gateway can be used.</span></span>
<span data-ttu-id="b27ba-113">Peer VNet måste emellertid ha en konfigurerad gateway och **AllowGatewayTransit** måste ha ett värde för $True.</span><span class="sxs-lookup"><span data-stu-id="b27ba-113">However, the peer VNet must have a gateway configured and **AllowGatewayTransit** must have a value of $True.</span></span>
<span data-ttu-id="b27ba-114">Den här egenskapen kan inte användas om en gateway redan har kon figurer ATS.</span><span class="sxs-lookup"><span data-stu-id="b27ba-114">This property cannot be used if a gateway has already been configured.</span></span>

## <span data-ttu-id="b27ba-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b27ba-115">PARAMETERS</span></span>

### <span data-ttu-id="b27ba-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b27ba-116">-AsJob</span></span>
<span data-ttu-id="b27ba-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b27ba-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b27ba-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b27ba-118">-DefaultProfile</span></span>
<span data-ttu-id="b27ba-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b27ba-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b27ba-120">-VirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="b27ba-120">-VirtualNetworkPeering</span></span>
<span data-ttu-id="b27ba-121">Anger virtuell nätverks-peering.</span><span class="sxs-lookup"><span data-stu-id="b27ba-121">Specifies the virtual network peering.</span></span>

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

### <span data-ttu-id="b27ba-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b27ba-122">CommonParameters</span></span>
<span data-ttu-id="b27ba-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b27ba-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b27ba-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b27ba-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b27ba-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b27ba-125">INPUTS</span></span>

### <span data-ttu-id="b27ba-126">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="b27ba-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="b27ba-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b27ba-127">OUTPUTS</span></span>

### <span data-ttu-id="b27ba-128">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="b27ba-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="b27ba-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b27ba-129">NOTES</span></span>

## <span data-ttu-id="b27ba-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b27ba-130">RELATED LINKS</span></span>

[<span data-ttu-id="b27ba-131">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="b27ba-131">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="b27ba-132">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="b27ba-132">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="b27ba-133">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="b27ba-133">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)
