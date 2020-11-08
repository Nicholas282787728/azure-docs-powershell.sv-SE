---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 688168317a622cb0375bb111050f3e54696047ff
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258770"
---
# <span data-ttu-id="409f8-101">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="409f8-101">Get-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="409f8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="409f8-102">SYNOPSIS</span></span>
<span data-ttu-id="409f8-103">Hämtar en virtuell nätverks anslutning i ett virtuellt nav eller visar alla virtuella nätverks anslutningar i ett virtuellt nav.</span><span class="sxs-lookup"><span data-stu-id="409f8-103">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

## <span data-ttu-id="409f8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="409f8-104">SYNTAX</span></span>

### <span data-ttu-id="409f8-105">ByVirtualHubName (standard)</span><span class="sxs-lookup"><span data-stu-id="409f8-105">ByVirtualHubName (Default)</span></span>
```
Get-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="409f8-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="409f8-106">ByVirtualHubObject</span></span>
```
Get-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="409f8-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="409f8-107">ByVirtualHubResourceId</span></span>
```
Get-AzVirtualHubVnetConnection -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="409f8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="409f8-108">DESCRIPTION</span></span>
<span data-ttu-id="409f8-109">Hämtar en virtuell nätverks anslutning i ett virtuellt nav eller visar alla virtuella nätverks anslutningar i ett virtuellt nav.</span><span class="sxs-lookup"><span data-stu-id="409f8-109">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

## <span data-ttu-id="409f8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="409f8-110">EXAMPLES</span></span>

### <span data-ttu-id="409f8-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="409f8-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
RoutingConfiguration : {
                            "AssociatedRouteTable": {
                                "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                            },
                            "PropagatedRouteTables": {
                                "Labels": [],
                                "Ids": [
                                    {
                                        "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                    }
                                ]
                            },
                            "VnetRoutes": {
                                "StaticRoutes": []
                            }
                        }
```

<span data-ttu-id="409f8-112">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav i den här resurs gruppen i Azure.</span><span class="sxs-lookup"><span data-stu-id="409f8-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="409f8-113">En virtuell nätverks anslutning skapas därefter som kommer att vara peer för det virtuella nätverket till det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="409f8-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="409f8-114">När du har skapat navets virtuella nätverks anslutning får du den virtuella nav-anslutningen med dess resurs grupp namn, hubbens namn och anslutnings namnet.</span><span class="sxs-lookup"><span data-stu-id="409f8-114">After the hub virtual network connection is created, it gets the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="409f8-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="409f8-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
RoutingConfiguration : {
                            "AssociatedRouteTable": {
                                "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                            },
                            "PropagatedRouteTables": {
                                "Labels": [],
                                "Ids": [
                                    {
                                        "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                    }
                                ]
                            },
                            "VnetRoutes": {
                                "StaticRoutes": []
                            }
                        }
```

<span data-ttu-id="409f8-116">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav i den här resurs gruppen i Azure.</span><span class="sxs-lookup"><span data-stu-id="409f8-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="409f8-117">En virtuell nätverks anslutning skapas därefter som kommer att vara peer för det virtuella nätverket till det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="409f8-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="409f8-118">När den virtuella nav-nätverksanslutningen har skapats visas en lista med alla virtuella hubbar för navet med dess resurs grupp namn och hubbens namn.</span><span class="sxs-lookup"><span data-stu-id="409f8-118">After the hub virtual network connection is created, it lists all the hub virtual network connection using its resource group name and the hub name.</span></span>

### <span data-ttu-id="409f8-119">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="409f8-119">Example 3</span></span>

```powershell
PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name test*

Name                 : testvnetconnection1
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection1
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
RoutingConfiguration : {
                            "AssociatedRouteTable": {
                                "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                            },
                            "PropagatedRouteTables": {
                                "Labels": [],
                                "Ids": [
                                    {
                                        "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                    }
                                ]
                            },
                            "VnetRoutes": {
                                "StaticRoutes": []
                            }
                        }

Name                 : testvnetconnection2
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection2
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
RoutingConfiguration : {
                            "AssociatedRouteTable": {
                                "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                            },
                            "PropagatedRouteTables": {
                                "Labels": [],
                                "Ids": [
                                    {
                                        "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                    }
                                ]
                            },
                            "VnetRoutes": {
                                "StaticRoutes": []
                            }
                        }
```

<span data-ttu-id="409f8-120">Denna cmdlet visar alla virtuella Hubbs nätverks anslutningar som börjar med "test" med dess resurs grupp namn och hubbens namn.</span><span class="sxs-lookup"><span data-stu-id="409f8-120">This cmdlet lists all the hub virtual network connections starting with "test" using its resource group name and the hub name.</span></span>

## <span data-ttu-id="409f8-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="409f8-121">PARAMETERS</span></span>

### <span data-ttu-id="409f8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="409f8-122">-DefaultProfile</span></span>
<span data-ttu-id="409f8-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="409f8-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="409f8-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="409f8-124">-Name</span></span>
<span data-ttu-id="409f8-125">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="409f8-125">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="409f8-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="409f8-126">-ParentObject</span></span>
<span data-ttu-id="409f8-127">Den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="409f8-127">The parent resource.</span></span>

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

### <span data-ttu-id="409f8-128">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="409f8-128">-ParentResourceId</span></span>
<span data-ttu-id="409f8-129">Överordnat resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="409f8-129">The parent resource id.</span></span>

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

### <span data-ttu-id="409f8-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="409f8-130">-ParentResourceName</span></span>
<span data-ttu-id="409f8-131">Namnet på den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="409f8-131">The parent resource name.</span></span>

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

### <span data-ttu-id="409f8-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="409f8-132">-ResourceGroupName</span></span>
<span data-ttu-id="409f8-133">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="409f8-133">The resource group name.</span></span>

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

### <span data-ttu-id="409f8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="409f8-134">CommonParameters</span></span>
<span data-ttu-id="409f8-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="409f8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="409f8-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="409f8-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="409f8-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="409f8-137">INPUTS</span></span>

### <span data-ttu-id="409f8-138">Microsoft. Azure. commands. Networks. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="409f8-138">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="409f8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="409f8-139">System.String</span></span>

## <span data-ttu-id="409f8-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="409f8-140">OUTPUTS</span></span>

### <span data-ttu-id="409f8-141">Microsoft. Azure. commands. Networks. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="409f8-141">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="409f8-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="409f8-142">NOTES</span></span>

## <span data-ttu-id="409f8-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="409f8-143">RELATED LINKS</span></span>

[<span data-ttu-id="409f8-144">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="409f8-144">New-AzVirtualHubVnetConnection</span></span>](./New-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="409f8-145">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="409f8-145">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)
