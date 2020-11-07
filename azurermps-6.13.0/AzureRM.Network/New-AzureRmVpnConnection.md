---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnConnection.md
ms.openlocfilehash: 8b7d0845e6a8fce2d6c496573a493dfd187c34af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757569"
---
# <span data-ttu-id="41c44-101">New-AzureRmVpnConnection</span><span class="sxs-lookup"><span data-stu-id="41c44-101">New-AzureRmVpnConnection</span></span>

## <span data-ttu-id="41c44-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="41c44-102">SYNOPSIS</span></span>
<span data-ttu-id="41c44-103">Skapar en IPSec-anslutning som ansluter en VpnGateway till en fjärrkunds filial som representeras i RM som en VpnSite.</span><span class="sxs-lookup"><span data-stu-id="41c44-103">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41c44-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="41c44-104">SYNTAX</span></span>

### <span data-ttu-id="41c44-105">ByVpnGatewayNameByVpnSiteObject (standard)</span><span class="sxs-lookup"><span data-stu-id="41c44-105">ByVpnGatewayNameByVpnSiteObject (Default)</span></span>
```
New-AzureRmVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -VpnSite <PSVpnSite> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41c44-106">ByVpnGatewayNameByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="41c44-106">ByVpnGatewayNameByVpnSiteResourceId</span></span>
```
New-AzureRmVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -VpnSiteId <String> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41c44-107">ByVpnGatewayObjectByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="41c44-107">ByVpnGatewayObjectByVpnSiteObject</span></span>
```
New-AzureRmVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSite <PSVpnSite>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41c44-108">ByVpnGatewayObjectByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="41c44-108">ByVpnGatewayObjectByVpnSiteResourceId</span></span>
```
New-AzureRmVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSiteId <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41c44-109">ByVpnGatewayResourceIdByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="41c44-109">ByVpnGatewayResourceIdByVpnSiteObject</span></span>
```
New-AzureRmVpnConnection -ParentResourceId <String> -Name <String> -VpnSite <PSVpnSite>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41c44-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="41c44-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span></span>
```
New-AzureRmVpnConnection -ParentResourceId <String> -Name <String> -VpnSiteId <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41c44-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="41c44-111">DESCRIPTION</span></span>
<span data-ttu-id="41c44-112">Skapar en IPSec-anslutning som ansluter en VpnGateway till en fjärrkunds filial som representeras i RM som en VpnSite.</span><span class="sxs-lookup"><span data-stu-id="41c44-112">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="41c44-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="41c44-113">EXAMPLES</span></span>

### <span data-ttu-id="41c44-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="41c44-114">Example 1</span></span>

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

PS C:\> New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite -ConnectionBandwidth 20

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="41c44-115">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav och en VpnSite i västra USA i resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="41c44-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="41c44-116">En VPN-gateway skapas därefter i det virtuella navet med två skal enheter.</span><span class="sxs-lookup"><span data-stu-id="41c44-116">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="41c44-117">När gatewayen har skapats är den ansluten till VpnSite med kommandot New-AzureRmVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="41c44-117">Once the gateway has been created, it is connected to the VpnSite using the New-AzureRmVpnConnection command.</span></span>

## <span data-ttu-id="41c44-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="41c44-118">PARAMETERS</span></span>

### <span data-ttu-id="41c44-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41c44-119">-AsJob</span></span>
<span data-ttu-id="41c44-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="41c44-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="41c44-121">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="41c44-121">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="41c44-122">Den bandbredden som ska hanteras av den här anslutningen i Mbps.</span><span class="sxs-lookup"><span data-stu-id="41c44-122">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="41c44-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41c44-123">-DefaultProfile</span></span>
<span data-ttu-id="41c44-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="41c44-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41c44-125">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="41c44-125">-EnableBgp</span></span>
<span data-ttu-id="41c44-126">Aktivera BGP för den här anslutningen</span><span class="sxs-lookup"><span data-stu-id="41c44-126">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="41c44-127">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="41c44-127">-IpSecPolicy</span></span>
<span data-ttu-id="41c44-128">Den bandbredden som ska hanteras av den här anslutningen i Mbps.</span><span class="sxs-lookup"><span data-stu-id="41c44-128">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="41c44-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="41c44-129">-Name</span></span>
<span data-ttu-id="41c44-130">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="41c44-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41c44-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="41c44-131">-ParentObject</span></span>
<span data-ttu-id="41c44-132">Den överordnade VpnGateway för den här anslutningen.</span><span class="sxs-lookup"><span data-stu-id="41c44-132">The parent VpnGateway for this connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObjectByVpnSiteObject, ByVpnGatewayObjectByVpnSiteResourceId
Aliases: ParentVpnGateway, VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41c44-133">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="41c44-133">-ParentResourceId</span></span>
<span data-ttu-id="41c44-134">Resurs-ID för den överordnade VpnGateway för den här anslutningen.</span><span class="sxs-lookup"><span data-stu-id="41c44-134">The resource id of the parent VpnGateway for this connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceIdByVpnSiteObject, ByVpnGatewayResourceIdByVpnSiteResourceId
Aliases: ParentVpnGatewayId, VpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41c44-135">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="41c44-135">-ParentResourceName</span></span>
<span data-ttu-id="41c44-136">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="41c44-136">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayNameByVpnSiteResourceId
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41c44-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41c44-137">-ResourceGroupName</span></span>
<span data-ttu-id="41c44-138">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="41c44-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayNameByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41c44-139">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="41c44-139">-SharedKey</span></span>
<span data-ttu-id="41c44-140">Den delade nycklar som krävs för att konfigurera den här anslutningen.</span><span class="sxs-lookup"><span data-stu-id="41c44-140">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="41c44-141">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="41c44-141">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="41c44-142">Gateway-anslutnings protokoll: IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="41c44-142">Gateway connection protocol:IKEv1/IKEv2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IKEv1, IKEv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41c44-143">-VpnSite</span><span class="sxs-lookup"><span data-stu-id="41c44-143">-VpnSite</span></span>
<span data-ttu-id="41c44-144">VPN-webbplatsen som den här nav-nätverks anslutningen är ansluten till.</span><span class="sxs-lookup"><span data-stu-id="41c44-144">The remote vpn site to which this hub virtual network connection is connected.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSite
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayObjectByVpnSiteObject, ByVpnGatewayResourceIdByVpnSiteObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41c44-145">-VpnSiteId</span><span class="sxs-lookup"><span data-stu-id="41c44-145">-VpnSiteId</span></span>
<span data-ttu-id="41c44-146">VPN-webbplatsen som den här nav-nätverks anslutningen är ansluten till.</span><span class="sxs-lookup"><span data-stu-id="41c44-146">The remote vpn site to which this hub virtual network connection is connected.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNameByVpnSiteResourceId, ByVpnGatewayObjectByVpnSiteResourceId, ByVpnGatewayResourceIdByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41c44-147">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="41c44-147">-Confirm</span></span>
<span data-ttu-id="41c44-148">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="41c44-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41c44-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41c44-149">-WhatIf</span></span>
<span data-ttu-id="41c44-150">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="41c44-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41c44-151">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="41c44-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41c44-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41c44-152">CommonParameters</span></span>
<span data-ttu-id="41c44-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41c44-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41c44-154">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41c44-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41c44-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="41c44-155">INPUTS</span></span>

### <span data-ttu-id="41c44-156">Microsoft. Azure. commands. Networks. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="41c44-156">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="41c44-157">System. String</span><span class="sxs-lookup"><span data-stu-id="41c44-157">System.String</span></span>

## <span data-ttu-id="41c44-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="41c44-158">OUTPUTS</span></span>

### <span data-ttu-id="41c44-159">Microsoft. Azure. commands. Networks. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="41c44-159">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="41c44-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="41c44-160">NOTES</span></span>

## <span data-ttu-id="41c44-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="41c44-161">RELATED LINKS</span></span>
