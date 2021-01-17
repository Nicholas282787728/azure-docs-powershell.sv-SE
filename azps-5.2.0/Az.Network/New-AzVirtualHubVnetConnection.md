---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
ms.openlocfilehash: f4087782e247e574cd49634e148b6852e9fb8dc6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415064"
---
# <span data-ttu-id="c7b03-101">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="c7b03-101">New-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="c7b03-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c7b03-102">SYNOPSIS</span></span>
<span data-ttu-id="c7b03-103">New-AzVirtualHubVnetConnection cmdlet skapar en HubVirtualNetworkConnection-resurs som peererar ett virtuellt nätverk med det virtuella Azure-navet.</span><span class="sxs-lookup"><span data-stu-id="c7b03-103">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="c7b03-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c7b03-104">SYNTAX</span></span>

### <span data-ttu-id="c7b03-105">ByVirtualHubNameByRemoteVirtualNetworkObject (standard)</span><span class="sxs-lookup"><span data-stu-id="c7b03-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Default)</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7b03-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="c7b03-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7b03-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="c7b03-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7b03-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="c7b03-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c7b03-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="c7b03-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7b03-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="c7b03-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c7b03-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c7b03-111">DESCRIPTION</span></span>
<span data-ttu-id="c7b03-112">New-AzVirtualHubVnetConnection cmdlet skapar en HubVirtualNetworkConnection-resurs som peererar ett virtuellt nätverk med det virtuella Azure-navet.</span><span class="sxs-lookup"><span data-stu-id="c7b03-112">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="c7b03-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c7b03-113">EXAMPLES</span></span>

### <span data-ttu-id="c7b03-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c7b03-114">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
EnableInternetSecurity : False
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

<span data-ttu-id="c7b03-115">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav i den här resurs gruppen i Azure.</span><span class="sxs-lookup"><span data-stu-id="c7b03-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="c7b03-116">En virtuell nätverks anslutning skapas därefter som kommer att vara peer för det virtuella nätverket till det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="c7b03-116">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

### <span data-ttu-id="c7b03-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="c7b03-117">Example 2</span></span>

<span data-ttu-id="c7b03-118">New-AzVirtualHubVnetConnection cmdlet skapar en HubVirtualNetworkConnection-resurs som peererar ett virtuellt nätverk med det virtuella Azure-navet.</span><span class="sxs-lookup"><span data-stu-id="c7b03-118">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span> <span data-ttu-id="c7b03-119">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="c7b03-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVirtualHubVnetConnection -EnableInternetSecurity -Name 'testvnetconnection' -ParentResourceName 'westushub' -RemoteVirtualNetwork <PSVirtualNetwork> -ResourceGroupName 'testRG'
```


### <span data-ttu-id="c7b03-120">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="c7b03-120">Example 3</span></span>
```powershell
PS C:\> $rgName = "testRg"
PS C:\> $virtualHubName = "testHub"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName $rgName -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $rt1 = Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "defaultRouteTable"
PS C:\> $rt2 = Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "noneRouteTable"
PS C:\> $route1 = New-AzStaticRoute -Name "route1" -AddressPrefix @("10.20.0.0/16", "10.30.0.0/16")-NextHopIpAddress "10.90.0.5"
PS C:\> $routingconfig = New-AzRoutingConfiguration -AssociatedRouteTable $rt1.Id -Label @("testLabel") -Id @($rt2.Id) -StaticRoute @($route1)

AssociatedRouteTable  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/defaultRouteTable"
PropagatedRouteTables : {
                          "Labels": [
                            "testLabel"
                          ],
                          "Ids": [
                            {
                              "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/noneRouteTable"
                            }
                          ]
                        }
VnetRoutes            : {
                          "StaticRoutes": [
                            {
                              "Name": "route1",
                              "AddressPrefixes": [
                                "10.20.0.0/16",
                                "10.30.0.0/16"
                              ],
                              "NextHopIpAddress": "10.90.0.5"
                            }
                          ]
                        }
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork -RoutingConfiguration $routingconfig
```
<span data-ttu-id="c7b03-121">Ovanstående skapar en ny konfigurering av Routning och skapar statiska vägar i konfigurationen för routning med nästa hopp som angiven IP-adress.</span><span class="sxs-lookup"><span data-stu-id="c7b03-121">The above will create a new routing configuration and create static routes in the routing config with the next hop as a specified IP address.</span></span> <span data-ttu-id="c7b03-122">Denna konfiguration av routning kan sedan överföras till kommandot New-AzVirtualHubVnetConnection som parametern-RoutingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c7b03-122">This routing configuration can then be passed into  the New-AzVirtualHubVnetConnection command as the parameter -RoutingConfiguration.</span></span>

## <span data-ttu-id="c7b03-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c7b03-123">PARAMETERS</span></span>

### <span data-ttu-id="c7b03-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c7b03-124">-AsJob</span></span>
<span data-ttu-id="c7b03-125">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="c7b03-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c7b03-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7b03-126">-DefaultProfile</span></span>
<span data-ttu-id="c7b03-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c7b03-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7b03-128">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="c7b03-128">-EnableInternetSecurity</span></span>
<span data-ttu-id="c7b03-129">Aktivera Internet säkerhet för den här anslutningen</span><span class="sxs-lookup"><span data-stu-id="c7b03-129">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="c7b03-130">-EnableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="c7b03-130">-EnableInternetSecurityFlag</span></span>
<span data-ttu-id="c7b03-131">Aktivera Internet säkerhet för den här anslutningen</span><span class="sxs-lookup"><span data-stu-id="c7b03-131">Enable internet security for this connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7b03-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="c7b03-132">-Name</span></span>
<span data-ttu-id="c7b03-133">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="c7b03-133">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7b03-134">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c7b03-134">-ParentObject</span></span>
<span data-ttu-id="c7b03-135">Den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="c7b03-135">The parent resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkResourceId
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7b03-136">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c7b03-136">-ParentResourceId</span></span>
<span data-ttu-id="c7b03-137">Den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="c7b03-137">The parent resource.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceIdByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7b03-138">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="c7b03-138">-ParentResourceName</span></span>
<span data-ttu-id="c7b03-139">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="c7b03-139">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7b03-140">-RemoteVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c7b03-140">-RemoteVirtualNetwork</span></span>
<span data-ttu-id="c7b03-141">Det virtuella fjärrnätverk som den här nav-nätverks anslutningen är ansluten till.</span><span class="sxs-lookup"><span data-stu-id="c7b03-141">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7b03-142">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="c7b03-142">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="c7b03-143">Det virtuella fjärrnätverk som den här nav-nätverks anslutningen är ansluten till.</span><span class="sxs-lookup"><span data-stu-id="c7b03-143">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkResourceId, ByVirtualHubObjectByRemoteVirtualNetworkResourceId, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7b03-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7b03-144">-ResourceGroupName</span></span>
<span data-ttu-id="c7b03-145">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="c7b03-145">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7b03-146">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7b03-146">-RoutingConfiguration</span></span>
<span data-ttu-id="c7b03-147">Dirigerings konfiguration för den här anslutningen</span><span class="sxs-lookup"><span data-stu-id="c7b03-147">Routing configuration for this connection</span></span>

```yaml
Type: PSRoutingConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7b03-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c7b03-148">-Confirm</span></span>
<span data-ttu-id="c7b03-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c7b03-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7b03-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7b03-150">-WhatIf</span></span>
<span data-ttu-id="c7b03-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c7b03-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7b03-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c7b03-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7b03-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7b03-153">CommonParameters</span></span>
<span data-ttu-id="c7b03-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7b03-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7b03-155">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7b03-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7b03-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c7b03-156">INPUTS</span></span>

### <span data-ttu-id="c7b03-157">Microsoft. Azure. commands. Networks. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="c7b03-157">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="c7b03-158">System. String</span><span class="sxs-lookup"><span data-stu-id="c7b03-158">System.String</span></span>

## <span data-ttu-id="c7b03-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c7b03-159">OUTPUTS</span></span>

### <span data-ttu-id="c7b03-160">Microsoft. Azure. commands. Networks. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="c7b03-160">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="c7b03-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c7b03-161">NOTES</span></span>

## <span data-ttu-id="c7b03-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c7b03-162">RELATED LINKS</span></span>

[<span data-ttu-id="c7b03-163">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="c7b03-163">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="c7b03-164">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="c7b03-164">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="c7b03-165">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7b03-165">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
