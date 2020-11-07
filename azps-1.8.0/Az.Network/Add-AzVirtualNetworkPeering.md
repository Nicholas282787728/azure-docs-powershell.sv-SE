---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13901193-8C68-4969-ADCD-2E82EA714354
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkPeering.md
ms.openlocfilehash: 3e4457945e6dfc003c2031d292556e90a7c245ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748412"
---
# <span data-ttu-id="0d34d-101">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="0d34d-101">Add-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="0d34d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0d34d-102">SYNOPSIS</span></span>
<span data-ttu-id="0d34d-103">Skapar en peering mellan två virtuella nätverk.</span><span class="sxs-lookup"><span data-stu-id="0d34d-103">Creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="0d34d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0d34d-104">SYNTAX</span></span>

```
Add-AzVirtualNetworkPeering -Name <String> -VirtualNetwork <PSVirtualNetwork> -RemoteVirtualNetworkId <String>
 [-BlockVirtualNetworkAccess] [-AllowForwardedTraffic] [-AllowGatewayTransit] [-UseRemoteGateways] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d34d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0d34d-105">DESCRIPTION</span></span>
<span data-ttu-id="0d34d-106">Cmdleten **Add-AzVirtualNetworkPeering** skapar en peering mellan två virtuella nätverk.</span><span class="sxs-lookup"><span data-stu-id="0d34d-106">The **Add-AzVirtualNetworkPeering** cmdlet creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="0d34d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0d34d-107">EXAMPLES</span></span>

### <span data-ttu-id="0d34d-108">Exempel 1: skapa en peering mellan två virtuella nätverk i samma region</span><span class="sxs-lookup"><span data-stu-id="0d34d-108">Example 1: Create a peering between two virtual networks in the same region</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'
$location='eastus'

# Create a resource group.
New-AzResourceGroup -Name $rgName  -Location $location

# Create virtual network 1.
$vnet1 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location $location

# Create virtual network 2.
$vnet2 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location $location

# Peer VNet1 to VNet2.
Add-AzVirtualNetworkPeering -Name 'myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="0d34d-109">Observera att en peering-länk måste skapas från vnet1 till vnet2 och tvärtom för att peering ska fungera.</span><span class="sxs-lookup"><span data-stu-id="0d34d-109">Note that a peering link must be created from vnet1 to vnet2 and vice versa in order for peering to work.</span></span>

### <span data-ttu-id="0d34d-110">Exempel 2: skapa en peering mellan två virtuella nätverk i olika regioner</span><span class="sxs-lookup"><span data-stu-id="0d34d-110">Example 2: Create a peering between two virtual networks in different regions</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'

# Create a resource group.
New-AzResourceGroup -Name $rgName  -Location westcentralus

# Create virtual network 1.
$vnet1 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location westcentralus

# Create virtual network 2.
$vnet2 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location candacentral

# Peer VNet1 to VNet2.
Add-AzVirtualNetworkPeering -Name 'myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="0d34d-111">Här står ' myVnet1 ' i US West Central med "myVnet2" i Canada Central.</span><span class="sxs-lookup"><span data-stu-id="0d34d-111">Here 'myVnet1' in US West Central is peered with 'myVnet2' in Canada Central.</span></span>

## <span data-ttu-id="0d34d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0d34d-112">PARAMETERS</span></span>

### <span data-ttu-id="0d34d-113">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="0d34d-113">-AllowForwardedTraffic</span></span>
<span data-ttu-id="0d34d-114">Visar att denna cmdlet tillåter den vidarebefordrade trafiken från de virtuella datorerna i det virtuella fjärrnätverket.</span><span class="sxs-lookup"><span data-stu-id="0d34d-114">Indicates that this cmdlet allows the forwarded traffic from the virtual machines in the remote virtual network.</span></span>

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

### <span data-ttu-id="0d34d-115">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="0d34d-115">-AllowGatewayTransit</span></span>
<span data-ttu-id="0d34d-116">Flagga för att tillåta att gatewayLinks används i det virtuella fjärrnätverkets länk till det här virtuella nätverket</span><span class="sxs-lookup"><span data-stu-id="0d34d-116">Flag to allow gatewayLinks be used in remote virtual network's link to this virtual network</span></span>

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

### <span data-ttu-id="0d34d-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0d34d-117">-AsJob</span></span>
<span data-ttu-id="0d34d-118">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="0d34d-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0d34d-119">-BlockVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="0d34d-119">-BlockVirtualNetworkAccess</span></span>
<span data-ttu-id="0d34d-120">Anger att denna cmdlet blockerar de virtuella datorerna i det länkade virtuella nätverks utrymmet för att komma åt alla virtuella datorer i lokalt virtuellt nätverks utrymme.</span><span class="sxs-lookup"><span data-stu-id="0d34d-120">Indicates that this cmdlet blocks the virtual machines in the linked virtual network space to access all the virtual machines in local virtual network space.</span></span>

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

### <span data-ttu-id="0d34d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d34d-121">-DefaultProfile</span></span>
<span data-ttu-id="0d34d-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0d34d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d34d-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="0d34d-123">-Name</span></span>
<span data-ttu-id="0d34d-124">Anger namnet på den virtuella nätverks-peering.</span><span class="sxs-lookup"><span data-stu-id="0d34d-124">Specifies the name of the virtual network peering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d34d-125">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="0d34d-125">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="0d34d-126">Anger ID för det virtuella fjärrnätverket.</span><span class="sxs-lookup"><span data-stu-id="0d34d-126">Specifies the ID of the remote virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d34d-127">-UseRemoteGateways</span><span class="sxs-lookup"><span data-stu-id="0d34d-127">-UseRemoteGateways</span></span>
<span data-ttu-id="0d34d-128">Anger att denna cmdlet tillåter Fjärrgateways i det här virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="0d34d-128">Indicates that this cmdlet allows remote gateways on this virtual network.</span></span>

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

### <span data-ttu-id="0d34d-129">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0d34d-129">-VirtualNetwork</span></span>
<span data-ttu-id="0d34d-130">Anger det överordnade virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="0d34d-130">Specifies the parent virtual network.</span></span>

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

### <span data-ttu-id="0d34d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d34d-131">CommonParameters</span></span>
<span data-ttu-id="0d34d-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d34d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d34d-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d34d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d34d-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0d34d-134">INPUTS</span></span>

### <span data-ttu-id="0d34d-135">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0d34d-135">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="0d34d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="0d34d-136">System.String</span></span>

## <span data-ttu-id="0d34d-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0d34d-137">OUTPUTS</span></span>

### <span data-ttu-id="0d34d-138">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="0d34d-138">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="0d34d-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0d34d-139">NOTES</span></span>

## <span data-ttu-id="0d34d-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0d34d-140">RELATED LINKS</span></span>

[<span data-ttu-id="0d34d-141">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0d34d-141">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="0d34d-142">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="0d34d-142">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="0d34d-143">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="0d34d-143">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="0d34d-144">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="0d34d-144">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)