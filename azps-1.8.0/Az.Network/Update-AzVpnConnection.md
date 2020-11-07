---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
ms.openlocfilehash: 5161dfcb843310ad372739438e63adb6c81f1935
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747648"
---
# <span data-ttu-id="681b9-101">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="681b9-101">Update-AzVpnConnection</span></span>

## <span data-ttu-id="681b9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="681b9-102">SYNOPSIS</span></span>
<span data-ttu-id="681b9-103">Uppdaterar en VPN-anslutning.</span><span class="sxs-lookup"><span data-stu-id="681b9-103">Updates a VPN connection.</span></span>

## <span data-ttu-id="681b9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="681b9-104">SYNTAX</span></span>

### <span data-ttu-id="681b9-105">ByVpnConnectionName (standard)</span><span class="sxs-lookup"><span data-stu-id="681b9-105">ByVpnConnectionName (Default)</span></span>
```
Update-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-EnableBgp <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="681b9-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="681b9-106">ByVpnConnectionResourceId</span></span>
```
Update-AzVpnConnection -ResourceId <String> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="681b9-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="681b9-107">ByVpnConnectionObject</span></span>
```
Update-AzVpnConnection -InputObject <PSVpnConnection> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="681b9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="681b9-108">DESCRIPTION</span></span>
<span data-ttu-id="681b9-109">Cmdleten **Update-AzVpnConnection** uppdaterar en VPN-anslutning.</span><span class="sxs-lookup"><span data-stu-id="681b9-109">The **Update-AzVpnConnection** cmdlet updates a VPN connection.</span></span>  
<span data-ttu-id="681b9-110">VPN-anslutning skapar en IPsec-anslutning som ansluter en VPN-gateway till en fjärran sluten kund filial som visas i Azure som en VPN-plats.</span><span class="sxs-lookup"><span data-stu-id="681b9-110">VPN connection creates an IPsec connection that connects a VPN gateway to a remote customer branch represented in Azure as a VPN site.</span></span>

## <span data-ttu-id="681b9-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="681b9-111">EXAMPLES</span></span>

### <span data-ttu-id="681b9-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="681b9-112">Example 1</span></span>

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
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="681b9-113">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav och en VpnSite i västra USA i resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="681b9-113">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="681b9-114">En VPN-gateway skapas därefter i det virtuella navet med två skal enheter.</span><span class="sxs-lookup"><span data-stu-id="681b9-114">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="681b9-115">När gatewayen har skapats är den ansluten till VpnSite med kommandot New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="681b9-115">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="681b9-116">Anslutningen uppdateras då till en ny IpSecPolicy med hjälp av kommandot Set-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="681b9-116">The connection is then updated to have a new IpSecPolicy by using the Set-AzVpnConnection command.</span></span>

### <span data-ttu-id="681b9-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="681b9-117">Example 2</span></span>

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
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="681b9-118">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav och en VpnSite i västra USA i resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="681b9-118">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="681b9-119">En VPN-gateway skapas därefter i det virtuella navet med två skal enheter.</span><span class="sxs-lookup"><span data-stu-id="681b9-119">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="681b9-120">När gatewayen har skapats är den ansluten till VpnSite med kommandot New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="681b9-120">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="681b9-121">Anslutningen uppdateras då och har en ny delad säkerhets nycklar med hjälp av säker sträng konstruktion.</span><span class="sxs-lookup"><span data-stu-id="681b9-121">The connection is then updated to have a new shared key using the secure string construct.</span></span>

## <span data-ttu-id="681b9-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="681b9-122">PARAMETERS</span></span>

### <span data-ttu-id="681b9-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="681b9-123">-AsJob</span></span>
<span data-ttu-id="681b9-124">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="681b9-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="681b9-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="681b9-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="681b9-126">Den bandbredden som ska hanteras av den här anslutningen i Mbps.</span><span class="sxs-lookup"><span data-stu-id="681b9-126">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="681b9-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="681b9-127">-DefaultProfile</span></span>
<span data-ttu-id="681b9-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="681b9-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="681b9-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="681b9-129">-EnableBgp</span></span>
<span data-ttu-id="681b9-130">Aktivera BGP för den här anslutningen</span><span class="sxs-lookup"><span data-stu-id="681b9-130">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="681b9-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="681b9-131">-InputObject</span></span>
<span data-ttu-id="681b9-132">VpnConenction-objekt som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="681b9-132">The VpnConenction object to update.</span></span>

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

### <span data-ttu-id="681b9-133">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="681b9-133">-IpSecPolicy</span></span>
<span data-ttu-id="681b9-134">Den bandbredden som ska hanteras av den här anslutningen i Mbps.</span><span class="sxs-lookup"><span data-stu-id="681b9-134">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="681b9-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="681b9-135">-Name</span></span>
<span data-ttu-id="681b9-136">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="681b9-136">The resource name.</span></span>

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

### <span data-ttu-id="681b9-137">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="681b9-137">-ParentResourceName</span></span>
<span data-ttu-id="681b9-138">Namnet på den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="681b9-138">The parent resource name.</span></span>

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

### <span data-ttu-id="681b9-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="681b9-139">-ResourceGroupName</span></span>
<span data-ttu-id="681b9-140">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="681b9-140">The resource group name.</span></span>

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

### <span data-ttu-id="681b9-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="681b9-141">-ResourceId</span></span>
<span data-ttu-id="681b9-142">Resurs-ID för det VpnConenction-objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="681b9-142">The resource id of the VpnConenction object to delete.</span></span>

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

### <span data-ttu-id="681b9-143">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="681b9-143">-SharedKey</span></span>
<span data-ttu-id="681b9-144">Den delade nycklar som krävs för att konfigurera den här anslutningen.</span><span class="sxs-lookup"><span data-stu-id="681b9-144">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="681b9-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="681b9-145">-Confirm</span></span>
<span data-ttu-id="681b9-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="681b9-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="681b9-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="681b9-147">-WhatIf</span></span>
<span data-ttu-id="681b9-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="681b9-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="681b9-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="681b9-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="681b9-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="681b9-150">CommonParameters</span></span>
<span data-ttu-id="681b9-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="681b9-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="681b9-152">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="681b9-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="681b9-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="681b9-153">INPUTS</span></span>

### <span data-ttu-id="681b9-154">System. String</span><span class="sxs-lookup"><span data-stu-id="681b9-154">System.String</span></span>

### <span data-ttu-id="681b9-155">Microsoft. Azure. commands. Networks. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="681b9-155">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="681b9-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="681b9-156">OUTPUTS</span></span>

### <span data-ttu-id="681b9-157">Microsoft. Azure. commands. Networks. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="681b9-157">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="681b9-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="681b9-158">NOTES</span></span>

## <span data-ttu-id="681b9-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="681b9-159">RELATED LINKS</span></span>

[<span data-ttu-id="681b9-160">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="681b9-160">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="681b9-161">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="681b9-161">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="681b9-162">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="681b9-162">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)
