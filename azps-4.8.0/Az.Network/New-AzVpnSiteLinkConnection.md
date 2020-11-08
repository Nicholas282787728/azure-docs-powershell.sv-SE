---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsitelinkconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLinkConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLinkConnection.md
ms.openlocfilehash: 31679702c1499ac91f41b14057e1bc13ef2dfc32
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262077"
---
# <span data-ttu-id="63370-101">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="63370-101">New-AzVpnSiteLinkConnection</span></span>

## <span data-ttu-id="63370-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="63370-102">SYNOPSIS</span></span>
<span data-ttu-id="63370-103">Skapar ett Azure VpnSiteLinkConnection-objekt.</span><span class="sxs-lookup"><span data-stu-id="63370-103">Creates an Azure VpnSiteLinkConnection object.</span></span>

## <span data-ttu-id="63370-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="63370-104">SYNTAX</span></span>

```
New-AzVpnSiteLinkConnection -Name <String> -VpnSiteLink <PSVpnSiteLink> [-SharedKey <SecureString>]
 [-ConnectionBandwidth <UInt32>] [-RoutingWeight <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63370-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="63370-105">DESCRIPTION</span></span>
<span data-ttu-id="63370-106">Skapar ett Azure VpnSiteLinkConnection-objekt.</span><span class="sxs-lookup"><span data-stu-id="63370-106">Creates an Azure VpnSiteLinkConnection object.</span></span>

## <span data-ttu-id="63370-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="63370-107">EXAMPLES</span></span>

### <span data-ttu-id="63370-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="63370-108">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink)


PS C:\> $vpnSiteLinkConnection = New-AzVpnSiteLinkConnection -Name "testLinkConnection1" -VpnSiteLink $vpnSite.VpnSiteLinks[0] -ConnectionBandwidth 100

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite -VpnSiteLinkConnection @($vpnSiteLinkConnection)
```

<span data-ttu-id="63370-109">Ovanstående skapar en resurs grupp, virtuellt WAN, virtuellt nätverk, virtuellt nav och en VpnSite med 1 VpnSiteLinks i västra USA i resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="63370-109">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>
<span data-ttu-id="63370-110">En VPN-gateway skapas därefter i det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="63370-110">A VPN gateway will be created thereafter in the Virtual Hub.</span></span>
<span data-ttu-id="63370-111">När gatewayen har skapats är den ansluten till VpnSite med hjälp av kommandot New-AzVpnConnection med 1 VpnSiteLinkConnections till VpnSiteLink för VpnSite.</span><span class="sxs-lookup"><span data-stu-id="63370-111">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command with 1 VpnSiteLinkConnections to the VpnSiteLink of the VpnSite.</span></span>

## <span data-ttu-id="63370-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="63370-112">PARAMETERS</span></span>

### <span data-ttu-id="63370-113">-ConnectionBandwidth</span><span class="sxs-lookup"><span data-stu-id="63370-113">-ConnectionBandwidth</span></span>
<span data-ttu-id="63370-114">Bandbredden som måste hanteras av den här länk anslutningen i Mbps.</span><span class="sxs-lookup"><span data-stu-id="63370-114">The bandwidth that needs to be handled by this link connection in mbps.</span></span>

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

### <span data-ttu-id="63370-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63370-115">-DefaultProfile</span></span>
<span data-ttu-id="63370-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="63370-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63370-117">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="63370-117">-EnableBgp</span></span>
<span data-ttu-id="63370-118">Aktivera BGP för denna länk anslutning</span><span class="sxs-lookup"><span data-stu-id="63370-118">Enable BGP for this link connection</span></span>

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

### <span data-ttu-id="63370-119">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="63370-119">-IpSecPolicy</span></span>
<span data-ttu-id="63370-120">IpSec-princip som ska användas för den här länken.</span><span class="sxs-lookup"><span data-stu-id="63370-120">IpSec Policy to be considered for this link connection.</span></span>

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

### <span data-ttu-id="63370-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="63370-121">-Name</span></span>
<span data-ttu-id="63370-122">Namn</span><span class="sxs-lookup"><span data-stu-id="63370-122">Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63370-123">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="63370-123">-RoutingWeight</span></span>
<span data-ttu-id="63370-124">Vägs vikt</span><span class="sxs-lookup"><span data-stu-id="63370-124">Routing Weight</span></span>

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

### <span data-ttu-id="63370-125">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="63370-125">-SharedKey</span></span>
<span data-ttu-id="63370-126">Den delade knapp som krävs för att konfigurera länken.</span><span class="sxs-lookup"><span data-stu-id="63370-126">The shared key required to set this link connection up.</span></span>

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

### <span data-ttu-id="63370-127">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="63370-127">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="63370-128">Använd lokal Azure-IP-adress som käll-IP för den här länken.</span><span class="sxs-lookup"><span data-stu-id="63370-128">Use local azure ip address as source ip for this link connection.</span></span>

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

### <span data-ttu-id="63370-129">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="63370-129">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="63370-130">Använd principbaserad trafikväljaren för den här länk anslutningen.</span><span class="sxs-lookup"><span data-stu-id="63370-130">Use policy based traffic selectors for this link connection.</span></span>

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

### <span data-ttu-id="63370-131">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="63370-131">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="63370-132">Gateway-anslutnings protokoll: IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="63370-132">Gateway connection protocol:IKEv1/IKEv2</span></span>

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

### <span data-ttu-id="63370-133">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="63370-133">-VpnSiteLink</span></span>
<span data-ttu-id="63370-134">Länken VPN-plats att ansluta till.</span><span class="sxs-lookup"><span data-stu-id="63370-134">The vpn site link object to connect to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63370-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63370-135">CommonParameters</span></span>
<span data-ttu-id="63370-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63370-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63370-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63370-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63370-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="63370-138">INPUTS</span></span>

### <span data-ttu-id="63370-139">Microsoft. Azure. commands. Networks. Models. PSVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="63370-139">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span></span>

## <span data-ttu-id="63370-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="63370-140">OUTPUTS</span></span>

### <span data-ttu-id="63370-141">Microsoft. Azure. commands. Networks. Models. PSVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="63370-141">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLinkConnection</span></span>

## <span data-ttu-id="63370-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="63370-142">NOTES</span></span>

## <span data-ttu-id="63370-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="63370-143">RELATED LINKS</span></span>

[<span data-ttu-id="63370-144">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="63370-144">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)