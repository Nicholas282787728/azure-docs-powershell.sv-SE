---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
ms.openlocfilehash: a35f9b776bcd0f7fcb206103cd20475fb18bd608
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092237"
---
# <span data-ttu-id="998a6-101">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="998a6-101">Update-AzVpnConnection</span></span>

## <span data-ttu-id="998a6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="998a6-102">SYNOPSIS</span></span>
<span data-ttu-id="998a6-103">Uppdaterar en VPN-anslutning.</span><span class="sxs-lookup"><span data-stu-id="998a6-103">Updates a VPN connection.</span></span>

## <span data-ttu-id="998a6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="998a6-104">SYNTAX</span></span>

### <span data-ttu-id="998a6-105">ByVpnConnectionName (standard)</span><span class="sxs-lookup"><span data-stu-id="998a6-105">ByVpnConnectionName (Default)</span></span>
```
Update-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="998a6-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="998a6-106">ByVpnConnectionResourceId</span></span>
```
Update-AzVpnConnection -ResourceId <String> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-UsePolicyBasedTrafficSelectors <Boolean>] [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>]
 [-EnableInternetSecurity <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="998a6-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="998a6-107">ByVpnConnectionObject</span></span>
```
Update-AzVpnConnection -InputObject <PSVpnConnection> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>]
 [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="998a6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="998a6-108">DESCRIPTION</span></span>
<span data-ttu-id="998a6-109">Cmdleten **Update-AzVpnConnection** uppdaterar en VPN-anslutning.</span><span class="sxs-lookup"><span data-stu-id="998a6-109">The **Update-AzVpnConnection** cmdlet updates a VPN connection.</span></span>  
<span data-ttu-id="998a6-110">VPN-anslutning skapar en IPsec-anslutning som ansluter en VPN-gateway till en fjärran sluten kund filial som visas i Azure som en VPN-plats.</span><span class="sxs-lookup"><span data-stu-id="998a6-110">VPN connection creates an IPsec connection that connects a VPN gateway to a remote customer branch represented in Azure as a VPN site.</span></span>

## <span data-ttu-id="998a6-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="998a6-111">EXAMPLES</span></span>

### <span data-ttu-id="998a6-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="998a6-112">Example 1</span></span>

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
PS C:\> $vpnConnection = New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> $ipsecPolicy = New-AzIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> Update-AzVpnConnection -InputObject $vpnConnection -IpSecPolicy $ipsecPolicy

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy}
ConnectionBandwidth       : 20
EnableBgp                 : False
UseLocalAzureIpAddress    : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="998a6-113">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav och en VpnSite i västra USA i resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="998a6-113">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="998a6-114">En VPN-gateway skapas därefter i det virtuella navet med två skal enheter.</span><span class="sxs-lookup"><span data-stu-id="998a6-114">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="998a6-115">När gatewayen har skapats är den ansluten till VpnSite med kommandot New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="998a6-115">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="998a6-116">Anslutningen uppdateras då till en ny IpSecPolicy med hjälp av kommandot Set-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="998a6-116">The connection is then updated to have a new IpSecPolicy by using the Set-AzVpnConnection command.</span></span>

### <span data-ttu-id="998a6-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="998a6-117">Example 2</span></span>

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
PS C:\> $vpnConnection = New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> $Secure_String_Pwd = Read-Host -AsSecureString
PS C:\> Update-AzVpnConnection -InputObject $vpnConnection -SharedKey $Secure_String_Pwd

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy}
ConnectionBandwidth       : 20
EnableBgp                 : False
UseLocalAzureIpAddress    : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="998a6-118">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav och en VpnSite i västra USA i resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="998a6-118">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="998a6-119">En VPN-gateway skapas därefter i det virtuella navet med två skal enheter.</span><span class="sxs-lookup"><span data-stu-id="998a6-119">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="998a6-120">När gatewayen har skapats är den ansluten till VpnSite med kommandot New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="998a6-120">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="998a6-121">Anslutningen uppdateras då och har en ny delad säkerhets nycklar med hjälp av säker sträng konstruktion.</span><span class="sxs-lookup"><span data-stu-id="998a6-121">The connection is then updated to have a new shared key using the secure string construct.</span></span>

## <span data-ttu-id="998a6-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="998a6-122">PARAMETERS</span></span>

### <span data-ttu-id="998a6-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="998a6-123">-AsJob</span></span>
<span data-ttu-id="998a6-124">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="998a6-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="998a6-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="998a6-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="998a6-126">Bandbredden som måste hanteras av den här anslutningen i Mbps.</span><span class="sxs-lookup"><span data-stu-id="998a6-126">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="998a6-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="998a6-127">-DefaultProfile</span></span>
<span data-ttu-id="998a6-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="998a6-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="998a6-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="998a6-129">-EnableBgp</span></span>
<span data-ttu-id="998a6-130">Aktivera BGP för den här anslutningen</span><span class="sxs-lookup"><span data-stu-id="998a6-130">Enable BGP for this connection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="998a6-131">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="998a6-131">-EnableInternetSecurity</span></span>
<span data-ttu-id="998a6-132">Aktivera Internet säkerhet för den här anslutningen</span><span class="sxs-lookup"><span data-stu-id="998a6-132">Enable internet security for this connection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="998a6-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="998a6-133">-InputObject</span></span>
<span data-ttu-id="998a6-134">VpnConnection-objekt som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="998a6-134">The VpnConnection object to update.</span></span>

```yaml
Type: PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="998a6-135">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="998a6-135">-IpSecPolicy</span></span>
<span data-ttu-id="998a6-136">Bandbredden som måste hanteras av den här anslutningen i Mbps.</span><span class="sxs-lookup"><span data-stu-id="998a6-136">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="998a6-137">-Namn</span><span class="sxs-lookup"><span data-stu-id="998a6-137">-Name</span></span>
<span data-ttu-id="998a6-138">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="998a6-138">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="998a6-139">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="998a6-139">-ParentResourceName</span></span>
<span data-ttu-id="998a6-140">Namnet på den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="998a6-140">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="998a6-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="998a6-141">-ResourceGroupName</span></span>
<span data-ttu-id="998a6-142">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="998a6-142">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="998a6-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="998a6-143">-ResourceId</span></span>
<span data-ttu-id="998a6-144">Resurs-ID för det VpnConnection-objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="998a6-144">The resource id of the VpnConnection object to delete.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionResourceId
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="998a6-145">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="998a6-145">-SharedKey</span></span>
<span data-ttu-id="998a6-146">Den delade nycklar som krävs för att konfigurera den här anslutningen.</span><span class="sxs-lookup"><span data-stu-id="998a6-146">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="998a6-147">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="998a6-147">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="998a6-148">Använd lokal Azure-IP-adress som käll adress när anslutningen upprättas.</span><span class="sxs-lookup"><span data-stu-id="998a6-148">Use local azure ip address as source address while initiating connection.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="998a6-149">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="998a6-149">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="998a6-150">Använd principbaserad Traffic Selector för den här anslutningen.</span><span class="sxs-lookup"><span data-stu-id="998a6-150">Use policy based traffic selectors for this connection.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="998a6-151">-VpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="998a6-151">-VpnSiteLinkConnection</span></span>
<span data-ttu-id="998a6-152">Listan med VpnSiteLinkConnections som den här VpnConnection måste ha.</span><span class="sxs-lookup"><span data-stu-id="998a6-152">The list of VpnSiteLinkConnections that this VpnConnection needs to have.</span></span>

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

### <span data-ttu-id="998a6-153">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="998a6-153">-Confirm</span></span>
<span data-ttu-id="998a6-154">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="998a6-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="998a6-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="998a6-155">-WhatIf</span></span>
<span data-ttu-id="998a6-156">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="998a6-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="998a6-157">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="998a6-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="998a6-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="998a6-158">CommonParameters</span></span>
<span data-ttu-id="998a6-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="998a6-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="998a6-160">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="998a6-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="998a6-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="998a6-161">INPUTS</span></span>

### <span data-ttu-id="998a6-162">System. String</span><span class="sxs-lookup"><span data-stu-id="998a6-162">System.String</span></span>

### <span data-ttu-id="998a6-163">Microsoft. Azure. commands. Networks. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="998a6-163">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="998a6-164">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="998a6-164">OUTPUTS</span></span>

### <span data-ttu-id="998a6-165">Microsoft. Azure. commands. Networks. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="998a6-165">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="998a6-166">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="998a6-166">NOTES</span></span>

## <span data-ttu-id="998a6-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="998a6-167">RELATED LINKS</span></span>

[<span data-ttu-id="998a6-168">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="998a6-168">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="998a6-169">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="998a6-169">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="998a6-170">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="998a6-170">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)
