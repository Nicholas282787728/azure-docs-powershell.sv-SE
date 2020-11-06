---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualHubVnetConnection.md
ms.openlocfilehash: 8aeb992b08e2749168ef3da2db6c264158c6a9ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575211"
---
# <span data-ttu-id="bed5f-101">Get-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="bed5f-101">Get-AzureRmVirtualHubVnetConnection</span></span>

## <span data-ttu-id="bed5f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bed5f-102">SYNOPSIS</span></span>
<span data-ttu-id="bed5f-103">Hämtar en virtuell nätverks anslutning i ett virtuellt nav eller visar alla virtuella nätverks anslutningar i ett virtuellt nav.</span><span class="sxs-lookup"><span data-stu-id="bed5f-103">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bed5f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bed5f-104">SYNTAX</span></span>

### <span data-ttu-id="bed5f-105">ByVirtualHubName (standard)</span><span class="sxs-lookup"><span data-stu-id="bed5f-105">ByVirtualHubName (Default)</span></span>
```
Get-AzureRmVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bed5f-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="bed5f-106">ByVirtualHubObject</span></span>
```
Get-AzureRmVirtualHubVnetConnection -ParentObject <PSVirtualHub> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bed5f-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="bed5f-107">ByVirtualHubResourceId</span></span>
```
Get-AzureRmVirtualHubVnetConnection -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bed5f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bed5f-108">DESCRIPTION</span></span>
<span data-ttu-id="bed5f-109">Hämtar en virtuell nätverks anslutning i ett virtuellt nav eller visar alla virtuella nätverks anslutningar i ett virtuellt nav.</span><span class="sxs-lookup"><span data-stu-id="bed5f-109">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

## <span data-ttu-id="bed5f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bed5f-110">EXAMPLES</span></span>

### <span data-ttu-id="bed5f-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bed5f-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzureRmVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzureRmVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

PS C:\> Get-AzureRmVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
```

<span data-ttu-id="bed5f-112">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav i den här resurs gruppen i Azure.</span><span class="sxs-lookup"><span data-stu-id="bed5f-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="bed5f-113">En virtuell nätverks anslutning skapas därefter som kommer att vara peer för det virtuella nätverket till det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="bed5f-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="bed5f-114">När du har skapat navets virtuella nätverks anslutning får du den virtuella nav-anslutningen med dess resurs grupp namn, hubbens namn och anslutnings namnet.</span><span class="sxs-lookup"><span data-stu-id="bed5f-114">After the hub virtual network connection is created, it gets the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="bed5f-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="bed5f-115">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzureRmVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzureRmVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Get-AzureRmVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
```

<span data-ttu-id="bed5f-116">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav i den här resurs gruppen i Azure.</span><span class="sxs-lookup"><span data-stu-id="bed5f-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="bed5f-117">En virtuell nätverks anslutning skapas därefter som kommer att vara peer för det virtuella nätverket till det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="bed5f-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="bed5f-118">När den virtuella nav-nätverksanslutningen har skapats visas en lista med alla virtuella hubbar för navet med dess resurs grupp namn och hubbens namn.</span><span class="sxs-lookup"><span data-stu-id="bed5f-118">After the hub virtual network connection is created, it lists all the hub virtual network connection using its resource group name and the hub name.</span></span>

## <span data-ttu-id="bed5f-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bed5f-119">PARAMETERS</span></span>

### <span data-ttu-id="bed5f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bed5f-120">-DefaultProfile</span></span>
<span data-ttu-id="bed5f-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bed5f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bed5f-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="bed5f-122">-Name</span></span>
<span data-ttu-id="bed5f-123">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="bed5f-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bed5f-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="bed5f-124">-ParentObject</span></span>
<span data-ttu-id="bed5f-125">Den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="bed5f-125">The parent resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bed5f-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="bed5f-126">-ParentResourceId</span></span>
<span data-ttu-id="bed5f-127">Överordnat resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="bed5f-127">The parent resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bed5f-128">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="bed5f-128">-ParentResourceName</span></span>
<span data-ttu-id="bed5f-129">Namnet på den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="bed5f-129">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bed5f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bed5f-130">-ResourceGroupName</span></span>
<span data-ttu-id="bed5f-131">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="bed5f-131">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bed5f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bed5f-132">CommonParameters</span></span>
<span data-ttu-id="bed5f-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bed5f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bed5f-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bed5f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bed5f-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bed5f-135">INPUTS</span></span>

### <span data-ttu-id="bed5f-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="bed5f-136">None</span></span>

## <span data-ttu-id="bed5f-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bed5f-137">OUTPUTS</span></span>

### <span data-ttu-id="bed5f-138">Microsoft. Azure. commands. Networks. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="bed5f-138">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="bed5f-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bed5f-139">NOTES</span></span>

## <span data-ttu-id="bed5f-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bed5f-140">RELATED LINKS</span></span>
