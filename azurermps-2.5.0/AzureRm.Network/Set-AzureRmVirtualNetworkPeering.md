---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 06DAD751-3A43-4EF6-94C5-AA7AC1A67FC8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkpeering
schema: 2.0.0
ms.openlocfilehash: d6f258bf15ac89dc0321c61ab592ef9fc6e58a7b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928677"
---
# <span data-ttu-id="577b1-101">Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="577b1-101">Set-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="577b1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="577b1-102">SYNOPSIS</span></span>
<span data-ttu-id="577b1-103">Konfigurerar en peering med virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="577b1-103">Configures a virtual network peering.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="577b1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="577b1-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering <PSVirtualNetworkPeering> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="577b1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="577b1-105">DESCRIPTION</span></span>
<span data-ttu-id="577b1-106">Cmdleten **set-AzureRmVirtualNetworkPeering** konfigurerar en virtuell nätverks-peering.</span><span class="sxs-lookup"><span data-stu-id="577b1-106">The **Set-AzureRmVirtualNetworkPeering** cmdlet configures a virtual network peering.</span></span>

## <span data-ttu-id="577b1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="577b1-107">EXAMPLES</span></span>

### <span data-ttu-id="577b1-108">Exempel 1: ändra konfiguration av vidarebefordrad trafik för ett virtuellt nätverks-peering</span><span class="sxs-lookup"><span data-stu-id="577b1-108">Example 1: Change forwarded traffic configuration of a virtual network peering</span></span>
```
# Get the virtual network peering you want to update information for
Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup" -Name "myVnet1ToMyVnet2"

# Change value of AllowForwardedTraffic property
$myVnet1ToMyVnet2.AllowForwardedTraffic = $True

# Update the peering with changes made
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1ToMyVnet2
```

### <span data-ttu-id="577b1-109">Exempel 2: Ändra virtuell nätverks åtkomst för en virtuell nätverks-peering</span><span class="sxs-lookup"><span data-stu-id="577b1-109">Example 2: Change virtual network access of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowVirtualNetworkAccess property
$myVnet1TomyVnet2.AllowVirtualNetworkAccess = $False

# Update virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="577b1-110">Exempel 3: ändra egenskapen för gateway-överföring för ett virtuellt nätverks-peering</span><span class="sxs-lookup"><span data-stu-id="577b1-110">Example 3: Change gateway transit property configuration of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowGatewayTransit property
$myVnet1TomyVnet2.AllowGatewayTransit = $True

# Update the virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="577b1-111">Exempel 4: använda Fjärrgateways i virtuellt nätverks-peering</span><span class="sxs-lookup"><span data-stu-id="577b1-111">Example 4: Use remote gateways in virtual network peering</span></span>
```
# Get the virtual network peering 
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup001" -Name "myVnet1TomyVnet2"

# Change the UseRemoteGateways property
$myVnet1TomyVnet2.UseRemoteGateways = $True

# Update the virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $LinkToVNet2
```

<span data-ttu-id="577b1-112">Genom att ändra den här egenskapen till $True kan motpartens VNet-Gateway användas.</span><span class="sxs-lookup"><span data-stu-id="577b1-112">By changing this property to $True, your peer's VNet gateway can be used.</span></span>
<span data-ttu-id="577b1-113">Peer VNet måste emellertid ha en konfigurerad gateway och **AllowGatewayTransit** måste ha ett värde för $True.</span><span class="sxs-lookup"><span data-stu-id="577b1-113">However, the peer VNet must have a gateway configured and **AllowGatewayTransit** must have a value of $True.</span></span>

<span data-ttu-id="577b1-114">Den här egenskapen kan inte användas om en gateway redan har kon figurer ATS.</span><span class="sxs-lookup"><span data-stu-id="577b1-114">This property cannot be used if a gateway has already been configured.</span></span>

## <span data-ttu-id="577b1-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="577b1-115">PARAMETERS</span></span>

### <span data-ttu-id="577b1-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="577b1-116">-AsJob</span></span>
<span data-ttu-id="577b1-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="577b1-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="577b1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="577b1-118">-DefaultProfile</span></span>
<span data-ttu-id="577b1-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="577b1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="577b1-120">-VirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="577b1-120">-VirtualNetworkPeering</span></span>
<span data-ttu-id="577b1-121">Anger virtuell nätverks-peering.</span><span class="sxs-lookup"><span data-stu-id="577b1-121">Specifies the virtual network peering.</span></span>

```yaml
Type: PSVirtualNetworkPeering
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="577b1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="577b1-122">CommonParameters</span></span>
<span data-ttu-id="577b1-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="577b1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="577b1-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="577b1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="577b1-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="577b1-125">INPUTS</span></span>

### <span data-ttu-id="577b1-126">PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="577b1-126">PSVirtualNetworkPeering</span></span>
<span data-ttu-id="577b1-127">Parametern ' VirtualNetworkPeering ' godkänner värdet av typen ' PSVirtualNetworkPeering ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="577b1-127">Parameter 'VirtualNetworkPeering' accepts value of type 'PSVirtualNetworkPeering' from the pipeline</span></span>

## <span data-ttu-id="577b1-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="577b1-128">OUTPUTS</span></span>

### <span data-ttu-id="577b1-129">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="577b1-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="577b1-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="577b1-130">NOTES</span></span>

## <span data-ttu-id="577b1-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="577b1-131">RELATED LINKS</span></span>

[<span data-ttu-id="577b1-132">Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="577b1-132">Add-AzureRmVirtualNetworkPeering</span></span>](./Add-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="577b1-133">Get-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="577b1-133">Get-AzureRmVirtualNetworkPeering</span></span>](./Get-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="577b1-134">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="577b1-134">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)


