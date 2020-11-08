---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnConnection.md
ms.openlocfilehash: 3b7bf41818ded2b866ea72a81ff1c17ccc365358
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261848"
---
# <span data-ttu-id="1699a-101">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="1699a-101">New-AzVpnConnection</span></span>

## <span data-ttu-id="1699a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1699a-102">SYNOPSIS</span></span>
<span data-ttu-id="1699a-103">Skapar en IPSec-anslutning som ansluter en VpnGateway till en fjärrkunds filial som representeras i RM som en VpnSite.</span><span class="sxs-lookup"><span data-stu-id="1699a-103">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="1699a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1699a-104">SYNTAX</span></span>

### <span data-ttu-id="1699a-105">ByVpnGatewayNameByVpnSiteObject (standard)</span><span class="sxs-lookup"><span data-stu-id="1699a-105">ByVpnGatewayNameByVpnSiteObject (Default)</span></span>
```
New-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -VpnSite <PSVpnSite> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress]
 [-UsePolicyBasedTrafficSelectors] [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1699a-106">ByVpnGatewayNameByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="1699a-106">ByVpnGatewayNameByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> -VpnSiteId <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1699a-107">ByVpnGatewayObjectByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="1699a-107">ByVpnGatewayObjectByVpnSiteObject</span></span>
```
New-AzVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSite <PSVpnSite>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1699a-108">ByVpnGatewayObjectByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="1699a-108">ByVpnGatewayObjectByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSiteId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1699a-109">ByVpnGatewayResourceIdByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="1699a-109">ByVpnGatewayResourceIdByVpnSiteObject</span></span>
```
New-AzVpnConnection -ParentResourceId <String> -Name <String> -VpnSite <PSVpnSite> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1699a-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="1699a-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ParentResourceId <String> -Name <String> -VpnSiteId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1699a-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1699a-111">DESCRIPTION</span></span>
<span data-ttu-id="1699a-112">Skapar en IPSec-anslutning som ansluter en VpnGateway till en fjärrkunds filial som representeras i RM som en VpnSite.</span><span class="sxs-lookup"><span data-stu-id="1699a-112">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="1699a-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1699a-113">EXAMPLES</span></span>

### <span data-ttu-id="1699a-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1699a-114">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite -ConnectionBandwidth 20

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
UseLocalAzureIpAddress    : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
RoutingConfiguration      : {
                                "AssociatedRouteTable": {
                                    "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                }
                                "PropagatedRouteTables": {
                                    "Labels": [],
                                    "Ids": [
                                    {
                                    "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                    }
                                ]
                                },
                                "VnetRoutes": {
                                    "StaticRoutes": []
                                }
                            }
```

<span data-ttu-id="1699a-115">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav och en VpnSite i västra USA i resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="1699a-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="1699a-116">En VPN-gateway skapas därefter i det virtuella navet med två skal enheter.</span><span class="sxs-lookup"><span data-stu-id="1699a-116">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="1699a-117">När gatewayen har skapats är den ansluten till VpnSite med kommandot New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="1699a-117">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

### <span data-ttu-id="1699a-118">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="1699a-118">Example 2</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink1 = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSiteLink2 = New-AzVpnSiteLink -Name "testVpnSiteLink2" -IpAddress "15.25.35.55" -LinkProviderName "SomeTelecomProvider2" -LinkSpeedInMbps "100"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink1, $vpnSiteLink2)


PS C:\> $vpnSiteLinkConnection1 = New-AzVpnSiteLinkConnection -Name "testLinkConnection1" -VpnSiteLink $vpnSite.VpnSiteLinks[0] -ConnectionBandwidth 100
PS C:\> $vpnSiteLinkConnection2 = New-AzVpnSiteLinkConnection -Name "testLinkConnection2" -VpnSiteLink $vpnSite.VpnSiteLinks[1] -ConnectionBandwidth 10

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite -VpnSiteLinkConnection @($vpnSiteLinkConnection1, $vpnSiteLinkConnection2)
```

<span data-ttu-id="1699a-119">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav och en VpnSite med 1 VpnSiteLinks i västra USA i resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="1699a-119">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>
<span data-ttu-id="1699a-120">En VPN-gateway skapas därefter i det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="1699a-120">A VPN gateway will be created thereafter in the Virtual Hub.</span></span>
<span data-ttu-id="1699a-121">När gatewayen har skapats är den ansluten till VpnSite med hjälp av kommandot New-AzVpnConnection med 1 VpnSiteLinkConnections till VpnSiteLink för VpnSite.</span><span class="sxs-lookup"><span data-stu-id="1699a-121">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command with 1 VpnSiteLinkConnections to the VpnSiteLink of the VpnSite.</span></span>

## <span data-ttu-id="1699a-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1699a-122">PARAMETERS</span></span>

### <span data-ttu-id="1699a-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1699a-123">-AsJob</span></span>
<span data-ttu-id="1699a-124">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="1699a-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1699a-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="1699a-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="1699a-126">Bandbredden som måste hanteras av den här anslutningen i Mbps.</span><span class="sxs-lookup"><span data-stu-id="1699a-126">The bandwidth that needs to be handled by this connection in mbps.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1699a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1699a-127">-DefaultProfile</span></span>
<span data-ttu-id="1699a-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1699a-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1699a-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="1699a-129">-EnableBgp</span></span>
<span data-ttu-id="1699a-130">Aktivera BGP för den här anslutningen</span><span class="sxs-lookup"><span data-stu-id="1699a-130">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="1699a-131">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="1699a-131">-EnableInternetSecurity</span></span>
<span data-ttu-id="1699a-132">Aktivera Internet säkerhet för den här anslutningen</span><span class="sxs-lookup"><span data-stu-id="1699a-132">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="1699a-133">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="1699a-133">-IpSecPolicy</span></span>
<span data-ttu-id="1699a-134">Bandbredden som måste hanteras av den här anslutningen i Mbps.</span><span class="sxs-lookup"><span data-stu-id="1699a-134">The bandwidth that needs to be handled by this connection in mbps.</span></span>

```yaml
Type: PSIpsecPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1699a-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="1699a-135">-Name</span></span>
<span data-ttu-id="1699a-136">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="1699a-136">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1699a-137">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1699a-137">-ParentObject</span></span>
<span data-ttu-id="1699a-138">Den överordnade VpnGateway för den här anslutningen.</span><span class="sxs-lookup"><span data-stu-id="1699a-138">The parent VpnGateway for this connection.</span></span>

```yaml
Type: PSVpnGateway
Parameter Sets: ByVpnGatewayObjectByVpnSiteObject, ByVpnGatewayObjectByVpnSiteResourceId
Aliases: ParentVpnGateway, VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1699a-139">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="1699a-139">-ParentResourceId</span></span>
<span data-ttu-id="1699a-140">Resurs-ID för den överordnade VpnGateway för den här anslutningen.</span><span class="sxs-lookup"><span data-stu-id="1699a-140">The resource id of the parent VpnGateway for this connection.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayResourceIdByVpnSiteObject, ByVpnGatewayResourceIdByVpnSiteResourceId
Aliases: ParentVpnGatewayId, VpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1699a-141">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="1699a-141">-ParentResourceName</span></span>
<span data-ttu-id="1699a-142">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="1699a-142">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayNameByVpnSiteResourceId
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1699a-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1699a-143">-ResourceGroupName</span></span>
<span data-ttu-id="1699a-144">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="1699a-144">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayNameByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1699a-145">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="1699a-145">-RoutingConfiguration</span></span>
<span data-ttu-id="1699a-146">Dirigerings konfiguration för den här anslutningen</span><span class="sxs-lookup"><span data-stu-id="1699a-146">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="1699a-147">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="1699a-147">-SharedKey</span></span>
<span data-ttu-id="1699a-148">Den delade nycklar som krävs för att konfigurera den här anslutningen.</span><span class="sxs-lookup"><span data-stu-id="1699a-148">The shared key required to set this connection up.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1699a-149">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="1699a-149">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="1699a-150">Använd lokal Azure-IP-adress som käll adress när anslutningen upprättas.</span><span class="sxs-lookup"><span data-stu-id="1699a-150">Use local azure ip address as source address while initiating connection.</span></span>

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

### <span data-ttu-id="1699a-151">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="1699a-151">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="1699a-152">Använd principbaserad Traffic Selector för den här anslutningen.</span><span class="sxs-lookup"><span data-stu-id="1699a-152">Use policy based traffic selectors for this connection.</span></span>

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

### <span data-ttu-id="1699a-153">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="1699a-153">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="1699a-154">Gateway-anslutnings protokoll: IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="1699a-154">Gateway connection protocol:IKEv1/IKEv2</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: IKEv1, IKEv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1699a-155">-VpnSite</span><span class="sxs-lookup"><span data-stu-id="1699a-155">-VpnSite</span></span>
<span data-ttu-id="1699a-156">VPN-webbplatsen som den här nav-nätverks anslutningen är ansluten till.</span><span class="sxs-lookup"><span data-stu-id="1699a-156">The remote vpn site to which this hub virtual network connection is connected.</span></span>

```yaml
Type: PSVpnSite
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayObjectByVpnSiteObject, ByVpnGatewayResourceIdByVpnSiteObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1699a-157">-VpnSiteId</span><span class="sxs-lookup"><span data-stu-id="1699a-157">-VpnSiteId</span></span>
<span data-ttu-id="1699a-158">VPN-webbplatsen som den här nav-nätverks anslutningen är ansluten till.</span><span class="sxs-lookup"><span data-stu-id="1699a-158">The remote vpn site to which this hub virtual network connection is connected.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayNameByVpnSiteResourceId, ByVpnGatewayObjectByVpnSiteResourceId, ByVpnGatewayResourceIdByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1699a-159">-VpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="1699a-159">-VpnSiteLinkConnection</span></span>
<span data-ttu-id="1699a-160">Listan med VpnSiteLinkConnections som denna VpnConnection har.</span><span class="sxs-lookup"><span data-stu-id="1699a-160">The list of VpnSiteLinkConnections that this VpnConnection have.</span></span>

```yaml
Type: PSVpnSiteLinkConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1699a-161">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1699a-161">-Confirm</span></span>
<span data-ttu-id="1699a-162">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1699a-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1699a-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1699a-163">-WhatIf</span></span>
<span data-ttu-id="1699a-164">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1699a-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1699a-165">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1699a-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1699a-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1699a-166">CommonParameters</span></span>
<span data-ttu-id="1699a-167">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1699a-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1699a-168">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1699a-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1699a-169">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1699a-169">INPUTS</span></span>

### <span data-ttu-id="1699a-170">Microsoft. Azure. commands. Networks. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="1699a-170">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="1699a-171">System. String</span><span class="sxs-lookup"><span data-stu-id="1699a-171">System.String</span></span>

## <span data-ttu-id="1699a-172">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1699a-172">OUTPUTS</span></span>

### <span data-ttu-id="1699a-173">Microsoft. Azure. commands. Networks. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="1699a-173">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="1699a-174">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1699a-174">NOTES</span></span>

## <span data-ttu-id="1699a-175">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1699a-175">RELATED LINKS</span></span>

[<span data-ttu-id="1699a-176">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="1699a-176">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="1699a-177">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="1699a-177">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="1699a-178">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="1699a-178">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)

[<span data-ttu-id="1699a-179">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="1699a-179">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
