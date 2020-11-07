---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 13901193-8C68-4969-ADCD-2E82EA714354
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: 1a27b43a7767fab6fee7cc89098ef045dde8529c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755490"
---
# <span data-ttu-id="51705-101">Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="51705-101">Add-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="51705-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="51705-102">SYNOPSIS</span></span>
<span data-ttu-id="51705-103">Skapar en peering mellan två virtuella nätverk.</span><span class="sxs-lookup"><span data-stu-id="51705-103">Creates a peering between two virtual networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51705-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="51705-104">SYNTAX</span></span>

```
Add-AzureRmVirtualNetworkPeering -Name <String> -VirtualNetwork <PSVirtualNetwork>
 -RemoteVirtualNetworkId <String> [-BlockVirtualNetworkAccess] [-AllowForwardedTraffic] [-AllowGatewayTransit]
 [-UseRemoteGateways] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51705-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="51705-105">DESCRIPTION</span></span>
<span data-ttu-id="51705-106">Cmdleten **Add-AzureRmVirtualNetworkPeering** skapar en peering mellan två virtuella nätverk.</span><span class="sxs-lookup"><span data-stu-id="51705-106">The **Add-AzureRmVirtualNetworkPeering** cmdlet creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="51705-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="51705-107">EXAMPLES</span></span>

### <span data-ttu-id="51705-108">Exempel 1: skapa en peering mellan två virtuella nätverk i samma region</span><span class="sxs-lookup"><span data-stu-id="51705-108">Example 1: Create a peering between two virtual networks in the same region</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'
$location='eastus'

# Create a resource group.
New-AzureRmResourceGroup -Name $rgName  -Location $location

# Create virtual network 1.
$vnet1 = New-AzureRmVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location $location

# Create virtual network 2.
$vnet2 = New-AzureRmVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location $location

# Peer VNet1 to VNet2.
Add-AzureRmVirtualNetworkPeering -Name myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzureRmVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="51705-109">Observera att en peering-länk måste skapas från vnet1 till vnet2 och tvärtom för att peering ska fungera.</span><span class="sxs-lookup"><span data-stu-id="51705-109">Note that a peering link must be created from vnet1 to vnet2 and vice versa in order for peering to work.</span></span>

### <span data-ttu-id="51705-110">Exempel 2: skapa en peering mellan två virtuella nätverk i olika regioner</span><span class="sxs-lookup"><span data-stu-id="51705-110">Example 2: Create a peering between two virtual networks in different regions</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'

# Create a resource group.
New-AzureRmResourceGroup -Name $rgName  -Location westcentralus

# Create virtual network 1.
$vnet1 = New-AzureRmVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location westcentralus

# Create virtual network 2.
$vnet2 = New-AzureRmVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location candacentral

# Peer VNet1 to VNet2.
Add-AzureRmVirtualNetworkPeering -Name myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzureRmVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="51705-111">Här står ' myVnet1 ' i US West Central med "myVnet2" i Canada Central.</span><span class="sxs-lookup"><span data-stu-id="51705-111">Here 'myVnet1' in US West Central is peered with 'myVnet2' in Canada Central.</span></span>

## <span data-ttu-id="51705-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="51705-112">PARAMETERS</span></span>

### <span data-ttu-id="51705-113">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="51705-113">-AllowForwardedTraffic</span></span>
<span data-ttu-id="51705-114">Visar att denna cmdlet tillåter den vidarebefordrade trafiken från de virtuella datorerna i det virtuella fjärrnätverket.</span><span class="sxs-lookup"><span data-stu-id="51705-114">Indicates that this cmdlet allows the forwarded traffic from the virtual machines in the remote virtual network.</span></span>

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

### <span data-ttu-id="51705-115">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="51705-115">-AllowGatewayTransit</span></span>
<span data-ttu-id="51705-116">Flagga för att tillåta att gatewayLinks används i det virtuella fjärrnätverkets länk till det här virtuella nätverket</span><span class="sxs-lookup"><span data-stu-id="51705-116">Flag to allow gatewayLinks be used in remote virtual network's link to this virtual network</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: AlloowGatewayTransit

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51705-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51705-117">-AsJob</span></span>
<span data-ttu-id="51705-118">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="51705-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="51705-119">-BlockVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="51705-119">-BlockVirtualNetworkAccess</span></span>
<span data-ttu-id="51705-120">Anger att denna cmdlet blockerar de virtuella datorerna i det länkade virtuella nätverks utrymmet för att komma åt alla virtuella datorer i lokalt virtuellt nätverks utrymme.</span><span class="sxs-lookup"><span data-stu-id="51705-120">Indicates that this cmdlet blocks the virtual machines in the linked virtual network space to access all the virtual machines in local virtual network space.</span></span>

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

### <span data-ttu-id="51705-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51705-121">-DefaultProfile</span></span>
<span data-ttu-id="51705-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="51705-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51705-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="51705-123">-Name</span></span>
<span data-ttu-id="51705-124">Anger namnet på den virtuella nätverks-peering.</span><span class="sxs-lookup"><span data-stu-id="51705-124">Specifies the name of the virtual network peering.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51705-125">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="51705-125">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="51705-126">Anger ID för det virtuella fjärrnätverket.</span><span class="sxs-lookup"><span data-stu-id="51705-126">Specifies the ID of the remote virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51705-127">-UseRemoteGateways</span><span class="sxs-lookup"><span data-stu-id="51705-127">-UseRemoteGateways</span></span>
<span data-ttu-id="51705-128">Anger att denna cmdlet tillåter Fjärrgateways i det här virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="51705-128">Indicates that this cmdlet allows remote gateways on this virtual network.</span></span>

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

### <span data-ttu-id="51705-129">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="51705-129">-VirtualNetwork</span></span>
<span data-ttu-id="51705-130">Anger det överordnade virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="51705-130">Specifies the parent virtual network.</span></span>

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

### <span data-ttu-id="51705-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51705-131">CommonParameters</span></span>
<span data-ttu-id="51705-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51705-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51705-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51705-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51705-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="51705-134">INPUTS</span></span>

### <span data-ttu-id="51705-135">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="51705-135">String</span></span>
<span data-ttu-id="51705-136">Parametern ' RemoteVirtualNetworkId ' godkänner värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="51705-136">Parameter 'RemoteVirtualNetworkId' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="51705-137">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="51705-137">PSVirtualNetwork</span></span>
<span data-ttu-id="51705-138">Parametern ' VirtualNetwork ' godkänner värdet av typen ' PSVirtualNetwork ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="51705-138">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="51705-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="51705-139">OUTPUTS</span></span>

### <span data-ttu-id="51705-140">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="51705-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="51705-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="51705-141">NOTES</span></span>

## <span data-ttu-id="51705-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="51705-142">RELATED LINKS</span></span>

[<span data-ttu-id="51705-143">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="51705-143">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="51705-144">Get-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="51705-144">Get-AzureRmVirtualNetworkPeering</span></span>](./Get-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="51705-145">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="51705-145">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="51705-146">Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="51705-146">Set-AzureRmVirtualNetworkPeering</span></span>](./Set-AzureRmVirtualNetworkPeering.md)


