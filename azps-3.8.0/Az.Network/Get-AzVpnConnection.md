---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnConnection.md
ms.openlocfilehash: c52aec45b71510c508ad56359b0ea87c98bef4dc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092585"
---
# <span data-ttu-id="466bc-101">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="466bc-101">Get-AzVpnConnection</span></span>

## <span data-ttu-id="466bc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="466bc-102">SYNOPSIS</span></span>
<span data-ttu-id="466bc-103">Får en VPN-anslutning med namn eller visar alla VPN-anslutningar som är anslutna till en VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="466bc-103">Gets a vpn connection by name or lists all vpn connections connected to a VpnGateway.</span></span>

## <span data-ttu-id="466bc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="466bc-104">SYNTAX</span></span>

### <span data-ttu-id="466bc-105">ByVpnGatewayName (standard)</span><span class="sxs-lookup"><span data-stu-id="466bc-105">ByVpnGatewayName (Default)</span></span>
```
Get-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="466bc-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="466bc-106">ByVpnGatewayObject</span></span>
```
Get-AzVpnConnection -ParentObject <PSVpnGateway> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="466bc-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="466bc-107">ByVpnGatewayResourceId</span></span>
```
Get-AzVpnConnection -ParentResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="466bc-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="466bc-108">DESCRIPTION</span></span>
<span data-ttu-id="466bc-109">Får en VPN-anslutning med namn eller visar alla VPN-anslutningar som är anslutna till en VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="466bc-109">Gets a vpn connection by name or lists all vpn connections connected to a VpnGateway.</span></span>

## <span data-ttu-id="466bc-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="466bc-110">EXAMPLES</span></span>

### <span data-ttu-id="466bc-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="466bc-111">Example 1</span></span>

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

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Get-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection"

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
Etag                      : W/"xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="466bc-112">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav och en VpnSite i västra USA i resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="466bc-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="466bc-113">En VPN-gateway skapas därefter i det virtuella navet med två skal enheter.</span><span class="sxs-lookup"><span data-stu-id="466bc-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="466bc-114">När gatewayen har skapats är den ansluten till VpnSite med kommandot New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="466bc-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="466bc-115">Då får anslutningen hjälp av anslutnings namnet.</span><span class="sxs-lookup"><span data-stu-id="466bc-115">Then it gets the connection using the connection name.</span></span>

### <span data-ttu-id="466bc-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="466bc-116">Example 2</span></span>

```powershell
PS C:\> Get-AzVpnConnection -ResourceGroupName ps9361 -ParentResourceName testvpngw -Name test*

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
Etag                      : W/"xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection1

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
Etag                      : W/"xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection2
```

<span data-ttu-id="466bc-117">Denna cmdlet får alla anslutningar som börjar med "test".</span><span class="sxs-lookup"><span data-stu-id="466bc-117">This cmdlet gets all connections that start with "test".</span></span>

## <span data-ttu-id="466bc-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="466bc-118">PARAMETERS</span></span>

### <span data-ttu-id="466bc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="466bc-119">-DefaultProfile</span></span>
<span data-ttu-id="466bc-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="466bc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="466bc-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="466bc-121">-Name</span></span>
<span data-ttu-id="466bc-122">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="466bc-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="466bc-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="466bc-123">-ParentObject</span></span>
<span data-ttu-id="466bc-124">Den överordnade VpnGateway för den här anslutningen.</span><span class="sxs-lookup"><span data-stu-id="466bc-124">The parent VpnGateway for this connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: ParentVpnGateway, VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="466bc-125">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="466bc-125">-ParentResourceId</span></span>
<span data-ttu-id="466bc-126">Resurs-ID för den överordnade VpnGateway för den här anslutningen.</span><span class="sxs-lookup"><span data-stu-id="466bc-126">The resource id of the parent VpnGateway for this connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: ParentVpnGatewayId, VpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="466bc-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="466bc-127">-ParentResourceName</span></span>
<span data-ttu-id="466bc-128">Namnet på den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="466bc-128">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="466bc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="466bc-129">-ResourceGroupName</span></span>
<span data-ttu-id="466bc-130">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="466bc-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="466bc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="466bc-131">CommonParameters</span></span>
<span data-ttu-id="466bc-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="466bc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="466bc-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="466bc-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="466bc-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="466bc-134">INPUTS</span></span>

### <span data-ttu-id="466bc-135">Microsoft. Azure. commands. Networks. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="466bc-135">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="466bc-136">System. String</span><span class="sxs-lookup"><span data-stu-id="466bc-136">System.String</span></span>

## <span data-ttu-id="466bc-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="466bc-137">OUTPUTS</span></span>

### <span data-ttu-id="466bc-138">Microsoft. Azure. commands. Networks. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="466bc-138">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="466bc-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="466bc-139">NOTES</span></span>

## <span data-ttu-id="466bc-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="466bc-140">RELATED LINKS</span></span>

[<span data-ttu-id="466bc-141">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="466bc-141">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="466bc-142">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="466bc-142">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="466bc-143">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="466bc-143">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)