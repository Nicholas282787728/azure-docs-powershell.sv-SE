---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnConnection.md
ms.openlocfilehash: 870caec4cad2bd4d64c00a2b0bf3423f080b98ba
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93925998"
---
# <span data-ttu-id="596be-101">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="596be-101">New-AzVpnConnection</span></span>

## <span data-ttu-id="596be-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="596be-102">SYNOPSIS</span></span>
<span data-ttu-id="596be-103">Skapar en IPSec-anslutning som ansluter en VpnGateway till en fjärrkunds filial som representeras i RM som en VpnSite.</span><span class="sxs-lookup"><span data-stu-id="596be-103">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="596be-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="596be-104">SYNTAX</span></span>

### <span data-ttu-id="596be-105">ByVpnGatewayNameByVpnSiteObject (standard)</span><span class="sxs-lookup"><span data-stu-id="596be-105">ByVpnGatewayNameByVpnSiteObject (Default)</span></span>
```
New-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -VpnSite <PSVpnSite> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress]
 [-UsePolicyBasedTrafficSelectors] [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>]
 [-EnableInternetSecurity] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="596be-106">ByVpnGatewayNameByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="596be-106">ByVpnGatewayNameByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> -VpnSiteId <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="596be-107">ByVpnGatewayObjectByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="596be-107">ByVpnGatewayObjectByVpnSiteObject</span></span>
```
New-AzVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSite <PSVpnSite>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="596be-108">ByVpnGatewayObjectByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="596be-108">ByVpnGatewayObjectByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSiteId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="596be-109">ByVpnGatewayResourceIdByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="596be-109">ByVpnGatewayResourceIdByVpnSiteObject</span></span>
```
New-AzVpnConnection -ParentResourceId <String> -Name <String> -VpnSite <PSVpnSite> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="596be-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="596be-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ParentResourceId <String> -Name <String> -VpnSiteId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="596be-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="596be-111">DESCRIPTION</span></span>
<span data-ttu-id="596be-112">Skapar en IPSec-anslutning som ansluter en VpnGateway till en fjärrkunds filial som representeras i RM som en VpnSite.</span><span class="sxs-lookup"><span data-stu-id="596be-112">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="596be-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="596be-113">EXAMPLES</span></span>

### <span data-ttu-id="596be-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="596be-114">Example 1</span></span>

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
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="596be-115">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav och en VpnSite i västra USA i resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="596be-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="596be-116">En VPN-gateway skapas därefter i det virtuella navet med två skal enheter.</span><span class="sxs-lookup"><span data-stu-id="596be-116">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="596be-117">När gatewayen har skapats är den ansluten till VpnSite med kommandot New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="596be-117">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

### <span data-ttu-id="596be-118">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="596be-118">Example 2</span></span>
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

<span data-ttu-id="596be-119">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav och en VpnSite med 1 VpnSiteLinks i västra USA i resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="596be-119">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>
<span data-ttu-id="596be-120">En VPN-gateway skapas därefter i det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="596be-120">A VPN gateway will be created thereafter in the Virtual Hub.</span></span>
<span data-ttu-id="596be-121">När gatewayen har skapats är den ansluten till VpnSite med hjälp av kommandot New-AzVpnConnection med 1 VpnSiteLinkConnections till VpnSiteLink för VpnSite.</span><span class="sxs-lookup"><span data-stu-id="596be-121">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command with 1 VpnSiteLinkConnections to the VpnSiteLink of the VpnSite.</span></span>

## <span data-ttu-id="596be-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="596be-122">PARAMETERS</span></span>

### <span data-ttu-id="596be-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="596be-123">-AsJob</span></span>
<span data-ttu-id="596be-124">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="596be-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="596be-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="596be-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="596be-126">Bandbredden som måste hanteras av den här anslutningen i Mbps.</span><span class="sxs-lookup"><span data-stu-id="596be-126">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="596be-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="596be-127">-DefaultProfile</span></span>
<span data-ttu-id="596be-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="596be-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="596be-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="596be-129">-EnableBgp</span></span>
<span data-ttu-id="596be-130">Aktivera BGP för den här anslutningen</span><span class="sxs-lookup"><span data-stu-id="596be-130">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="596be-131">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="596be-131">-EnableInternetSecurity</span></span>
<span data-ttu-id="596be-132">Aktivera Internet säkerhet för den här anslutningen</span><span class="sxs-lookup"><span data-stu-id="596be-132">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="596be-133">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="596be-133">-IpSecPolicy</span></span>
<span data-ttu-id="596be-134">Bandbredden som måste hanteras av den här anslutningen i Mbps.</span><span class="sxs-lookup"><span data-stu-id="596be-134">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="596be-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="596be-135">-Name</span></span>
<span data-ttu-id="596be-136">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="596be-136">The resource name.</span></span>

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

### <span data-ttu-id="596be-137">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="596be-137">-ParentObject</span></span>
<span data-ttu-id="596be-138">Den överordnade VpnGateway för den här anslutningen.</span><span class="sxs-lookup"><span data-stu-id="596be-138">The parent VpnGateway for this connection.</span></span>

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

### <span data-ttu-id="596be-139">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="596be-139">-ParentResourceId</span></span>
<span data-ttu-id="596be-140">Resurs-ID för den överordnade VpnGateway för den här anslutningen.</span><span class="sxs-lookup"><span data-stu-id="596be-140">The resource id of the parent VpnGateway for this connection.</span></span>

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

### <span data-ttu-id="596be-141">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="596be-141">-ParentResourceName</span></span>
<span data-ttu-id="596be-142">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="596be-142">The resource group name.</span></span>

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

### <span data-ttu-id="596be-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="596be-143">-ResourceGroupName</span></span>
<span data-ttu-id="596be-144">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="596be-144">The resource group name.</span></span>

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

### <span data-ttu-id="596be-145">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="596be-145">-SharedKey</span></span>
<span data-ttu-id="596be-146">Den delade nycklar som krävs för att konfigurera den här anslutningen.</span><span class="sxs-lookup"><span data-stu-id="596be-146">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="596be-147">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="596be-147">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="596be-148">Använd lokal Azure-IP-adress som käll adress när anslutningen upprättas.</span><span class="sxs-lookup"><span data-stu-id="596be-148">Use local azure ip address as source address while initiating connection.</span></span>

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

### <span data-ttu-id="596be-149">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="596be-149">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="596be-150">Använd principbaserad Traffic Selector för den här anslutningen.</span><span class="sxs-lookup"><span data-stu-id="596be-150">Use policy based traffic selectors for this connection.</span></span>

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

### <span data-ttu-id="596be-151">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="596be-151">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="596be-152">Gateway-anslutnings protokoll: IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="596be-152">Gateway connection protocol:IKEv1/IKEv2</span></span>

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

### <span data-ttu-id="596be-153">-VpnSite</span><span class="sxs-lookup"><span data-stu-id="596be-153">-VpnSite</span></span>
<span data-ttu-id="596be-154">VPN-webbplatsen som den här nav-nätverks anslutningen är ansluten till.</span><span class="sxs-lookup"><span data-stu-id="596be-154">The remote vpn site to which this hub virtual network connection is connected.</span></span>

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

### <span data-ttu-id="596be-155">-VpnSiteId</span><span class="sxs-lookup"><span data-stu-id="596be-155">-VpnSiteId</span></span>
<span data-ttu-id="596be-156">VPN-webbplatsen som den här nav-nätverks anslutningen är ansluten till.</span><span class="sxs-lookup"><span data-stu-id="596be-156">The remote vpn site to which this hub virtual network connection is connected.</span></span>

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

### <span data-ttu-id="596be-157">-VpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="596be-157">-VpnSiteLinkConnection</span></span>
<span data-ttu-id="596be-158">Listan med VpnSiteLinkConnections som denna VpnConnection har.</span><span class="sxs-lookup"><span data-stu-id="596be-158">The list of VpnSiteLinkConnections that this VpnConnection have.</span></span>

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

### <span data-ttu-id="596be-159">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="596be-159">-Confirm</span></span>
<span data-ttu-id="596be-160">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="596be-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="596be-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="596be-161">-WhatIf</span></span>
<span data-ttu-id="596be-162">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="596be-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="596be-163">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="596be-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="596be-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="596be-164">CommonParameters</span></span>
<span data-ttu-id="596be-165">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="596be-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="596be-166">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="596be-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="596be-167">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="596be-167">INPUTS</span></span>

### <span data-ttu-id="596be-168">Microsoft. Azure. commands. Networks. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="596be-168">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="596be-169">System. String</span><span class="sxs-lookup"><span data-stu-id="596be-169">System.String</span></span>

## <span data-ttu-id="596be-170">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="596be-170">OUTPUTS</span></span>

### <span data-ttu-id="596be-171">Microsoft. Azure. commands. Networks. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="596be-171">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="596be-172">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="596be-172">NOTES</span></span>

## <span data-ttu-id="596be-173">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="596be-173">RELATED LINKS</span></span>

[<span data-ttu-id="596be-174">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="596be-174">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="596be-175">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="596be-175">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="596be-176">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="596be-176">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)
