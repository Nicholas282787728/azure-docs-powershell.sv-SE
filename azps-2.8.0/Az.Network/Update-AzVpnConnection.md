---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
ms.openlocfilehash: a0e7775a85196a7a3ba709f284b58e57c46c4cb3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919422"
---
# <span data-ttu-id="cbbc0-101">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="cbbc0-101">Update-AzVpnConnection</span></span>

## <span data-ttu-id="cbbc0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cbbc0-102">SYNOPSIS</span></span>
<span data-ttu-id="cbbc0-103">Uppdaterar en VPN-anslutning.</span><span class="sxs-lookup"><span data-stu-id="cbbc0-103">Updates a VPN connection.</span></span>

## <span data-ttu-id="cbbc0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cbbc0-104">SYNTAX</span></span>

### <span data-ttu-id="cbbc0-105">ByVpnConnectionName (standard)</span><span class="sxs-lookup"><span data-stu-id="cbbc0-105">ByVpnConnectionName (Default)</span></span>
```
Update-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbbc0-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="cbbc0-106">ByVpnConnectionResourceId</span></span>
```
Update-AzVpnConnection -ResourceId <String> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-UsePolicyBasedTrafficSelectors <Boolean>] [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbbc0-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="cbbc0-107">ByVpnConnectionObject</span></span>
```
Update-AzVpnConnection -InputObject <PSVpnConnection> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>]
 [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbbc0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cbbc0-108">DESCRIPTION</span></span>
<span data-ttu-id="cbbc0-109">Cmdleten **Update-AzVpnConnection** uppdaterar en VPN-anslutning.</span><span class="sxs-lookup"><span data-stu-id="cbbc0-109">The **Update-AzVpnConnection** cmdlet updates a VPN connection.</span></span>  
<span data-ttu-id="cbbc0-110">VPN-anslutning skapar en IPsec-anslutning som ansluter en VPN-gateway till en fjärran sluten kund filial som visas i Azure som en VPN-plats.</span><span class="sxs-lookup"><span data-stu-id="cbbc0-110">VPN connection creates an IPsec connection that connects a VPN gateway to a remote customer branch represented in Azure as a VPN site.</span></span>

## <span data-ttu-id="cbbc0-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cbbc0-111">EXAMPLES</span></span>

### <span data-ttu-id="cbbc0-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cbbc0-112">Example 1</span></span>

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

<span data-ttu-id="cbbc0-113">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav och en VpnSite i västra USA i resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="cbbc0-113">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="cbbc0-114">En VPN-gateway skapas därefter i det virtuella navet med två skal enheter.</span><span class="sxs-lookup"><span data-stu-id="cbbc0-114">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="cbbc0-115">När gatewayen har skapats är den ansluten till VpnSite med kommandot New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="cbbc0-115">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="cbbc0-116">Anslutningen uppdateras då till en ny IpSecPolicy med hjälp av kommandot Set-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="cbbc0-116">The connection is then updated to have a new IpSecPolicy by using the Set-AzVpnConnection command.</span></span>

### <span data-ttu-id="cbbc0-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="cbbc0-117">Example 2</span></span>

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

<span data-ttu-id="cbbc0-118">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav och en VpnSite i västra USA i resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="cbbc0-118">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="cbbc0-119">En VPN-gateway skapas därefter i det virtuella navet med två skal enheter.</span><span class="sxs-lookup"><span data-stu-id="cbbc0-119">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="cbbc0-120">När gatewayen har skapats är den ansluten till VpnSite med kommandot New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="cbbc0-120">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="cbbc0-121">Anslutningen uppdateras då och har en ny delad säkerhets nycklar med hjälp av säker sträng konstruktion.</span><span class="sxs-lookup"><span data-stu-id="cbbc0-121">The connection is then updated to have a new shared key using the secure string construct.</span></span>

## <span data-ttu-id="cbbc0-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cbbc0-122">PARAMETERS</span></span>

### <span data-ttu-id="cbbc0-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cbbc0-123">-AsJob</span></span>
<span data-ttu-id="cbbc0-124">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="cbbc0-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cbbc0-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="cbbc0-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="cbbc0-126">Bandbredden som måste hanteras av den här anslutningen i Mbps.</span><span class="sxs-lookup"><span data-stu-id="cbbc0-126">The bandwidth that needs to be handled by this connection in mbps.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbbc0-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbbc0-127">-DefaultProfile</span></span>
<span data-ttu-id="cbbc0-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cbbc0-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbbc0-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="cbbc0-129">-EnableBgp</span></span>
<span data-ttu-id="cbbc0-130">Aktivera BGP för den här anslutningen</span><span class="sxs-lookup"><span data-stu-id="cbbc0-130">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="cbbc0-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cbbc0-131">-InputObject</span></span>
<span data-ttu-id="cbbc0-132">VpnConnection-objekt som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="cbbc0-132">The VpnConnection object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbbc0-133">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="cbbc0-133">-IpSecPolicy</span></span>
<span data-ttu-id="cbbc0-134">Bandbredden som måste hanteras av den här anslutningen i Mbps.</span><span class="sxs-lookup"><span data-stu-id="cbbc0-134">The bandwidth that needs to be handled by this connection in mbps.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbbc0-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="cbbc0-135">-Name</span></span>
<span data-ttu-id="cbbc0-136">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="cbbc0-136">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbbc0-137">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="cbbc0-137">-ParentResourceName</span></span>
<span data-ttu-id="cbbc0-138">Namnet på den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="cbbc0-138">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbbc0-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbbc0-139">-ResourceGroupName</span></span>
<span data-ttu-id="cbbc0-140">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="cbbc0-140">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbbc0-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cbbc0-141">-ResourceId</span></span>
<span data-ttu-id="cbbc0-142">Resurs-ID för det VpnConnection-objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="cbbc0-142">The resource id of the VpnConnection object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionResourceId
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbbc0-143">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="cbbc0-143">-SharedKey</span></span>
<span data-ttu-id="cbbc0-144">Den delade nycklar som krävs för att konfigurera den här anslutningen.</span><span class="sxs-lookup"><span data-stu-id="cbbc0-144">The shared key required to set this connection up.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbbc0-145">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="cbbc0-145">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="cbbc0-146">Använd lokal Azure-IP-adress som käll adress när anslutningen upprättas.</span><span class="sxs-lookup"><span data-stu-id="cbbc0-146">Use local azure ip address as source address while initiating connection.</span></span>

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

### <span data-ttu-id="cbbc0-147">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="cbbc0-147">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="cbbc0-148">Använd principbaserad Traffic Selector för den här anslutningen.</span><span class="sxs-lookup"><span data-stu-id="cbbc0-148">Use policy based traffic selectors for this connection.</span></span>

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

### <span data-ttu-id="cbbc0-149">-VpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="cbbc0-149">-VpnSiteLinkConnection</span></span>
<span data-ttu-id="cbbc0-150">Listan med VpnSiteLinkConnections som den här VpnConnection måste ha.</span><span class="sxs-lookup"><span data-stu-id="cbbc0-150">The list of VpnSiteLinkConnections that this VpnConnection needs to have.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSiteLinkConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbbc0-151">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cbbc0-151">-Confirm</span></span>
<span data-ttu-id="cbbc0-152">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cbbc0-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbbc0-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbbc0-153">-WhatIf</span></span>
<span data-ttu-id="cbbc0-154">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cbbc0-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbbc0-155">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cbbc0-155">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbbc0-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbbc0-156">CommonParameters</span></span>
<span data-ttu-id="cbbc0-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbbc0-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbbc0-158">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cbbc0-158">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbbc0-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cbbc0-159">INPUTS</span></span>

### <span data-ttu-id="cbbc0-160">System. String</span><span class="sxs-lookup"><span data-stu-id="cbbc0-160">System.String</span></span>

### <span data-ttu-id="cbbc0-161">Microsoft. Azure. commands. Networks. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="cbbc0-161">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="cbbc0-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cbbc0-162">OUTPUTS</span></span>

### <span data-ttu-id="cbbc0-163">Microsoft. Azure. commands. Networks. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="cbbc0-163">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="cbbc0-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cbbc0-164">NOTES</span></span>

## <span data-ttu-id="cbbc0-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cbbc0-165">RELATED LINKS</span></span>

[<span data-ttu-id="cbbc0-166">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="cbbc0-166">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="cbbc0-167">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="cbbc0-167">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="cbbc0-168">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="cbbc0-168">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)
