---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/update-azurermvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnConnection.md
ms.openlocfilehash: 08b1e18fcd15dfb2667d0aec2410e7e0d7ea7b99
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576860"
---
# <span data-ttu-id="693f7-101">Update-AzureRmVpnConnection</span><span class="sxs-lookup"><span data-stu-id="693f7-101">Update-AzureRmVpnConnection</span></span>

## <span data-ttu-id="693f7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="693f7-102">SYNOPSIS</span></span>
<span data-ttu-id="693f7-103">Uppdaterar ett VpnConnection-objekt till ett mål tillstånd.</span><span class="sxs-lookup"><span data-stu-id="693f7-103">Updates a VpnConnection object to a goal state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="693f7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="693f7-104">SYNTAX</span></span>

### <span data-ttu-id="693f7-105">ByVpnConnectionName (standard)</span><span class="sxs-lookup"><span data-stu-id="693f7-105">ByVpnConnectionName (Default)</span></span>
```
Update-AzureRmVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-EnableBgp <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="693f7-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="693f7-106">ByVpnConnectionResourceId</span></span>
```
Update-AzureRmVpnConnection -ResourceId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="693f7-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="693f7-107">ByVpnConnectionObject</span></span>
```
Update-AzureRmVpnConnection -InputObject <PSVpnConnection> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="693f7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="693f7-108">DESCRIPTION</span></span>
<span data-ttu-id="693f7-109">Skapar en IPSec-anslutning som ansluter en VpnGateway till en fjärrkunds filial som representeras i RM som en VpnSite.</span><span class="sxs-lookup"><span data-stu-id="693f7-109">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="693f7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="693f7-110">EXAMPLES</span></span>

### <span data-ttu-id="693f7-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="693f7-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> $vpnSite = New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> $vpnConnection = New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> $ipsecPolicy = New-AzureRmIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> Update-AzureRmVpnConnection -InputObject $vpnConnection -IpSecPolicy $ipsecPolicy

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

<span data-ttu-id="693f7-112">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav och en VpnSite i västra USA i resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="693f7-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="693f7-113">En VPN-gateway skapas därefter i det virtuella navet med två skal enheter.</span><span class="sxs-lookup"><span data-stu-id="693f7-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="693f7-114">När gatewayen har skapats är den ansluten till VpnSite med kommandot New-AzureRmVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="693f7-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzureRmVpnConnection command.</span></span>

<span data-ttu-id="693f7-115">Anslutningen uppdateras då till en ny IpSecPolicy med hjälp av kommandot Set-AzureRmVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="693f7-115">The connection is then updated to have a new IpSecPolicy by using the Set-AzureRmVpnConnection command.</span></span>

### <span data-ttu-id="693f7-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="693f7-116">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> $vpnSite = New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> $vpnConnection = New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> $Secure_String_Pwd = Read-Host -AsSecureString
PS C:\> Update-AzureRmVpnConnection -InputObject $vpnConnection -SharedKey $Secure_String_Pwd

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

<span data-ttu-id="693f7-117">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav och en VpnSite i västra USA i resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="693f7-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="693f7-118">En VPN-gateway skapas därefter i det virtuella navet med två skal enheter.</span><span class="sxs-lookup"><span data-stu-id="693f7-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="693f7-119">När gatewayen har skapats är den ansluten till VpnSite med kommandot New-AzureRmVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="693f7-119">Once the gateway has been created, it is connected to the VpnSite using the New-AzureRmVpnConnection command.</span></span>

<span data-ttu-id="693f7-120">Anslutningen uppdateras då och har en ny delad säkerhets nycklar med hjälp av säker sträng konstruktion.</span><span class="sxs-lookup"><span data-stu-id="693f7-120">The connection is then updated to have a new shared key using the secure string construct.</span></span>

## <span data-ttu-id="693f7-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="693f7-121">PARAMETERS</span></span>

### <span data-ttu-id="693f7-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="693f7-122">-AsJob</span></span>
<span data-ttu-id="693f7-123">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="693f7-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="693f7-124">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="693f7-124">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="693f7-125">Den bandbredden som ska hanteras av den här anslutningen i Mbps.</span><span class="sxs-lookup"><span data-stu-id="693f7-125">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="693f7-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="693f7-126">-DefaultProfile</span></span>
<span data-ttu-id="693f7-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="693f7-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="693f7-128">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="693f7-128">-EnableBgp</span></span>
<span data-ttu-id="693f7-129">Aktivera BGP för den här anslutningen</span><span class="sxs-lookup"><span data-stu-id="693f7-129">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="693f7-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="693f7-130">-InputObject</span></span>
<span data-ttu-id="693f7-131">VpnConenction-objekt som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="693f7-131">The VpnConenction object to update.</span></span>

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

### <span data-ttu-id="693f7-132">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="693f7-132">-IpSecPolicy</span></span>
<span data-ttu-id="693f7-133">Den bandbredden som ska hanteras av den här anslutningen i Mbps.</span><span class="sxs-lookup"><span data-stu-id="693f7-133">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="693f7-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="693f7-134">-Name</span></span>
<span data-ttu-id="693f7-135">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="693f7-135">The resource name.</span></span>

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

### <span data-ttu-id="693f7-136">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="693f7-136">-ParentResourceName</span></span>
<span data-ttu-id="693f7-137">Namnet på den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="693f7-137">The parent resource name.</span></span>

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

### <span data-ttu-id="693f7-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="693f7-138">-ResourceGroupName</span></span>
<span data-ttu-id="693f7-139">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="693f7-139">The resource group name.</span></span>

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

### <span data-ttu-id="693f7-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="693f7-140">-ResourceId</span></span>
<span data-ttu-id="693f7-141">Resurs-ID för det VpnConenction-objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="693f7-141">The resource id of the VpnConenction object to delete.</span></span>

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

### <span data-ttu-id="693f7-142">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="693f7-142">-SharedKey</span></span>
<span data-ttu-id="693f7-143">Den delade nycklar som krävs för att konfigurera den här anslutningen.</span><span class="sxs-lookup"><span data-stu-id="693f7-143">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="693f7-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="693f7-144">-Confirm</span></span>
<span data-ttu-id="693f7-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="693f7-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="693f7-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="693f7-146">-WhatIf</span></span>
<span data-ttu-id="693f7-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="693f7-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="693f7-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="693f7-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="693f7-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="693f7-149">CommonParameters</span></span>
<span data-ttu-id="693f7-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="693f7-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="693f7-151">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="693f7-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="693f7-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="693f7-152">INPUTS</span></span>

### <span data-ttu-id="693f7-153">System. String</span><span class="sxs-lookup"><span data-stu-id="693f7-153">System.String</span></span>

### <span data-ttu-id="693f7-154">Microsoft. Azure. commands. Networks. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="693f7-154">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="693f7-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="693f7-155">OUTPUTS</span></span>

### <span data-ttu-id="693f7-156">Microsoft. Azure. commands. Networks. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="693f7-156">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="693f7-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="693f7-157">NOTES</span></span>

## <span data-ttu-id="693f7-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="693f7-158">RELATED LINKS</span></span>
