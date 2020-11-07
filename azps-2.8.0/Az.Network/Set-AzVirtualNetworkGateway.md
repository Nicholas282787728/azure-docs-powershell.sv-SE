---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
ms.openlocfilehash: df3b8df85cd53931de5da7dc710e4558aedcdd48
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919473"
---
# <span data-ttu-id="9e4eb-101">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9e4eb-101">Set-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="9e4eb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9e4eb-102">SYNOPSIS</span></span>
<span data-ttu-id="9e4eb-103">Uppdaterar en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-103">Updates a virtual network gateway.</span></span>

## <span data-ttu-id="9e4eb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9e4eb-104">SYNTAX</span></span>

### <span data-ttu-id="9e4eb-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="9e4eb-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 [-RemoveAadAuthentication] [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e4eb-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e4eb-106">RadiusServerConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e4eb-107">RadiusServerConfigurationUpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="9e4eb-107">RadiusServerConfigurationUpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] -Tag <Hashtable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e4eb-108">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e4eb-108">AadAuthenticationConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -AadTenantUri <String> -AadAudienceId <String> -AadIssuerUri <String> [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e4eb-109">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="9e4eb-109">UpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 [-RemoveAadAuthentication] [-CustomRoute <String[]>] -Tag <Hashtable> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e4eb-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9e4eb-110">DESCRIPTION</span></span>
<span data-ttu-id="9e4eb-111">Cmdleten **set-AzVirtualNetworkGateway** uppdaterar en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-111">The **Set-AzVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="9e4eb-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9e4eb-112">EXAMPLES</span></span>

### <span data-ttu-id="9e4eb-113">Exempel 1: uppdatera ASN för en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="9e4eb-113">Example 1: Update a virtual network gateway's ASN</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="9e4eb-114">Det första kommandot får en virtuell nätverksgateway som heter Gateway01 som tillhör resurs gruppens ResourceGroup001 och lagrar den till variabeln $Gateway det andra kommandot uppdaterar den virtuella nätverksgateway som lagras i variabeln $Gateway.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-114">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="9e4eb-115">Kommandot anger också ASN till 1337.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-115">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="9e4eb-116">Exempel 2: lägga till IPsec-princip till en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="9e4eb-116">Example 2: Add IPsec policy to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="9e4eb-117">Det första kommandot får en virtuell nätverksgateway som heter Gateway01 som tillhör resurs gruppens ResourceGroup001 och lagrar det i variabeln $Gateway det andra kommandot skapar IPsec-principobjektet som enligt angivna IPsec-parametrar.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-117">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="9e4eb-118">Det tredje kommandot uppdaterar den virtuella Nätverksgatewayen som lagras i variabeln $Gateway.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-118">The third command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="9e4eb-119">Kommandot anger även den anpassade IPSec-principen för VPN som anges i $vpnclientipsecpolicy-objekt på virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-119">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

### <span data-ttu-id="9e4eb-120">Exempel 3: lägga till/uppdatera taggar till en befintlig virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="9e4eb-120">Example 3: Add/Update Tags to an existing virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\>Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Tag @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }

Name                   : Gateway001
ResourceGroupName      : ResourceGroup001
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
                         Name          Value
                         ============  ============
                         testtagValue  SomeKeyValue
                         testtagKey    SomeTagKey

IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworks/MyVnet/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/publicIPAddresses/Gateway001Ip"
                             },
                             "Name": "vng1ipConfig",
                             "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/Gateway001IpConfig"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : False
ActiveActive           : False
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
VpnClientConfiguration : null
BgpSettings            : {
                           "Asn": 65515,
                           "BgpPeeringAddress": "1.2.3.4",
                           "PeerWeight": 0
                         }
```

<span data-ttu-id="9e4eb-121">Det första kommandot får en virtuell nätverksgateway med namnet Gateway01 som tillhör resurs gruppens ResourceGroup001 och lagrar det till den variabel som heter $Gateway det andra kommandot uppdaterar den virtuella Nätverksgatewayen Gateway01 med taggarna @ {testtagKey = "SomeTagKey"; testtagValue = "SomeKeyValue"}.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-121">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the tags @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }.</span></span>

### <span data-ttu-id="9e4eb-122">Exempel 4: lägga till/uppdatera AAD-VpnClient för en befintlig virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="9e4eb-122">Example 4: Add/Update AAD authentication configuration for VpnClient of an existing virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\>Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -AadTenantUri "https://login.microsoftonline.com/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4" -AadIssuerUri "https://sts.windows.net/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4/" -AadAudienceId "a21fce82-76af-45e6-8583-a08cb3b956f9"

Name                   : Gateway001
ResourceGroupName      : ResourceGroup001
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
                         Name          Value
                         ============  ============
                         testtagValue  SomeKeyValue
                         testtagKey    SomeTagKey

IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworks/MyVnet/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/publicIPAddresses/Gateway001Ip"
                             },
                             "Name": "vng1ipConfig",
                             "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/Gateway001IpConfig"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : False
ActiveActive           : False
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
vpnClientConfiguration : {
                    "vpnClientProtocols": [
                    "OpenVPN"
                    ],

                    "vpnClientAddressPool": {
                    "addressPrefixes": [
                        "101.10.0.0/16"
                    ]
                    },
                    "vpnClientRootCertificates": "",
                    "vpnClientRevokedCertificates": "",

                    "radiusServerAddress": "",
                    "radiusServerSecret": "",
                    "aadTenantUri": "https://login.microsoftonline.com/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4\",
                    "aadAudienceId": "a21fce82-76af-45e6-8583-a08cb3b956g9\",
                    "aadIssuerUri": "https://sts.windows.net/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4/\"
                },
BgpSettings            : {
                           "Asn": 65515,
                           "BgpPeeringAddress": "1.2.3.4",
                           "PeerWeight": 0
                         }
                         
PS C:\>Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientRootCertificates $rootCert -RemoveAadAuthentication
```

<span data-ttu-id="9e4eb-123">Det första kommandot får en virtuell nätverksgateway med namnet Gateway01 som tillhör resurs gruppens ResourceGroup001 och lagrar det till den variabel som heter $Gateway det andra kommandot uppdaterar den virtuella Nätverksgatewayen Gateway01 med AAD-autentiseringsinställningarna: aadTenantUri, aadAudienceId, aadIssuerUri för VpnClient.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-123">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the AAD authentication configurations params:aadTenantUri, aadAudienceId, aadIssuerUri for VpnClient.</span></span>
<span data-ttu-id="9e4eb-124">Det tredje kommandot tar bort identifieringen av AAD-konfigurationer från VpnClient i virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-124">The third command removes the AAD authentication configuration from VpnClient of virtual network gateway.</span></span>

## <span data-ttu-id="9e4eb-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9e4eb-125">PARAMETERS</span></span>

### <span data-ttu-id="9e4eb-126">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="9e4eb-126">-AadAudienceId</span></span>
<span data-ttu-id="9e4eb-127">P2S AAD: AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-127">P2S AAD authentication option:AadAudienceId.</span></span>

```yaml
Type: System.String
Parameter Sets: AadAuthenticationConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4eb-128">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="9e4eb-128">-AadIssuerUri</span></span>
<span data-ttu-id="9e4eb-129">P2S AAD: AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-129">P2S AAD authentication option:AadIssuerUri.</span></span>

```yaml
Type: System.String
Parameter Sets: AadAuthenticationConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4eb-130">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="9e4eb-130">-AadTenantUri</span></span>
<span data-ttu-id="9e4eb-131">P2S AAD: AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-131">P2S AAD authentication option:AadTenantUri.</span></span>

```yaml
Type: System.String
Parameter Sets: AadAuthenticationConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4eb-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e4eb-132">-AsJob</span></span>
<span data-ttu-id="9e4eb-133">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="9e4eb-133">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9e4eb-134">-ASN</span><span class="sxs-lookup"><span data-stu-id="9e4eb-134">-Asn</span></span>
<span data-ttu-id="9e4eb-135">Anger det autonoma system numret för virtuell nätverksgateway (ASN) som används för att konfigurera BGP-sessioner (Border Gateway Protocol) i IPsec-tunnlar.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-135">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4eb-136">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="9e4eb-136">-CustomRoute</span></span>
<span data-ttu-id="9e4eb-137">Anpassade flöden AddressPool anges av kund</span><span class="sxs-lookup"><span data-stu-id="9e4eb-137">Custom routes AddressPool specified by customer</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4eb-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e4eb-138">-DefaultProfile</span></span>
<span data-ttu-id="9e4eb-139">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e4eb-140">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="9e4eb-140">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="9e4eb-141">Inaktiverar den aktiva aktiva funktionen.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-141">Disables the active-active feature.</span></span>

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

### <span data-ttu-id="9e4eb-142">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="9e4eb-142">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="9e4eb-143">Aktiverar den aktiva aktiva funktionen.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-143">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="9e4eb-144">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="9e4eb-144">-GatewayDefaultSite</span></span>
<span data-ttu-id="9e4eb-145">Anger standard webbplatsen som ska användas för Tvingad tunnel trafik.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-145">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="9e4eb-146">Om en standard webbplats anges routas all Internet trafik från gatewayens virtuella privata nätverk (VPN) till den webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-146">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4eb-147">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="9e4eb-147">-GatewaySku</span></span>
<span data-ttu-id="9e4eb-148">Anger lagerhållnings enhet (SKU) för den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-148">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="9e4eb-149">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="9e4eb-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9e4eb-150">Basisk</span><span class="sxs-lookup"><span data-stu-id="9e4eb-150">Basic</span></span>
- <span data-ttu-id="9e4eb-151">Standar</span><span class="sxs-lookup"><span data-stu-id="9e4eb-151">Standard</span></span>
- <span data-ttu-id="9e4eb-152">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="9e4eb-152">HighPerformance</span></span>
- <span data-ttu-id="9e4eb-153">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="9e4eb-153">VpnGw1</span></span>
- <span data-ttu-id="9e4eb-154">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="9e4eb-154">VpnGw2</span></span>
- <span data-ttu-id="9e4eb-155">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="9e4eb-155">VpnGw3</span></span>
- <span data-ttu-id="9e4eb-156">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="9e4eb-156">VpnGw1AZ</span></span>
- <span data-ttu-id="9e4eb-157">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="9e4eb-157">VpnGw2AZ</span></span>
- <span data-ttu-id="9e4eb-158">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="9e4eb-158">VpnGw3AZ</span></span>
- <span data-ttu-id="9e4eb-159">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="9e4eb-159">ErGw1AZ</span></span>
- <span data-ttu-id="9e4eb-160">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="9e4eb-160">ErGw2AZ</span></span>
- <span data-ttu-id="9e4eb-161">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="9e4eb-161">ErGw3AZ</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw4, VpnGw5, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, VpnGw4AZ, VpnGw5AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4eb-162">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="9e4eb-162">-PeerWeight</span></span>
<span data-ttu-id="9e4eb-163">Anger vikten som har lagts till för vägar som upptäckts via BGP från denna virtuella nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="9e4eb-163">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4eb-164">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="9e4eb-164">-RadiusServerAddress</span></span>
<span data-ttu-id="9e4eb-165">P2S externa RADIUS-serveradress.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-165">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: RadiusServerConfiguration, RadiusServerConfigurationUpdateResourceWithTags
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4eb-166">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="9e4eb-166">-RadiusServerSecret</span></span>
<span data-ttu-id="9e4eb-167">P2S externa RADIUS-server hemlighet.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-167">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RadiusServerConfiguration, RadiusServerConfigurationUpdateResourceWithTags
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4eb-168">-RemoveAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="9e4eb-168">-RemoveAadAuthentication</span></span>
<span data-ttu-id="9e4eb-169">Flagga för att ta bort AAD-inloggningsautentisering för P2S-klient från virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-169">Flag to remove AAD authentication for P2S client from virtual network gateway.</span></span>

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

### <span data-ttu-id="9e4eb-170">-Tagg</span><span class="sxs-lookup"><span data-stu-id="9e4eb-170">-Tag</span></span>
<span data-ttu-id="9e4eb-171">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-171">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: RadiusServerConfigurationUpdateResourceWithTags, UpdateResourceWithTags
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e4eb-172">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9e4eb-172">-VirtualNetworkGateway</span></span>
<span data-ttu-id="9e4eb-173">Anger det virtuella nätverkets gateway-objekt som ska ändras från av.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-173">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="9e4eb-174">Du kan använda Get-AzVirtualNetworkGateway cmdlet för att hämta det virtuella nätverkets gateway-objekt.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-174">You can use the Get-AzVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4eb-175">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="9e4eb-175">-VpnClientAddressPool</span></span>
<span data-ttu-id="9e4eb-176">Anger det adress utrymme som denna cmdlet använder för att tilldela IP-adresser för VPN-klienter från.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-176">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="9e4eb-177">Detta ska inte överlappa virtuella nätverks-eller lokala områden.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-177">This should not overlap with virtual network or on-premise ranges.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4eb-178">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="9e4eb-178">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="9e4eb-179">En lista över IPSec-principer för tunnel protokoll för P2S VPN-klienter.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-179">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4eb-180">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="9e4eb-180">-VpnClientProtocol</span></span>
<span data-ttu-id="9e4eb-181">En lista över protokoll för P2S VPN-klienter</span><span class="sxs-lookup"><span data-stu-id="9e4eb-181">A list of P2S VPN client tunneling protocols</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: SSTP, IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4eb-182">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="9e4eb-182">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="9e4eb-183">Anger en lista över återkallade VPN-klient certifikat.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-183">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="9e4eb-184">En VPN-klient som visar ett certifikat som matchar något av dessa tas bort.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-184">A VPN client presenting a certificate that matches one of these is removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4eb-185">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="9e4eb-185">-VpnClientRootCertificates</span></span>
<span data-ttu-id="9e4eb-186">Anger en lista över de VPN-klient rot certifikat som ska användas för VPN-klientautentisering.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-186">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="9e4eb-187">Anslutning av VPN-klienter måste presentera certifikat som genererats från ett av dessa rot certifikat.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-187">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4eb-188">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9e4eb-188">-Confirm</span></span>
<span data-ttu-id="9e4eb-189">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e4eb-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e4eb-190">-WhatIf</span></span>
<span data-ttu-id="9e4eb-191">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-191">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9e4eb-192">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-192">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e4eb-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e4eb-193">CommonParameters</span></span>
<span data-ttu-id="9e4eb-194">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e4eb-195">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e4eb-195">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e4eb-196">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9e4eb-196">INPUTS</span></span>

### <span data-ttu-id="9e4eb-197">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9e4eb-197">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="9e4eb-198">System. String</span><span class="sxs-lookup"><span data-stu-id="9e4eb-198">System.String</span></span>

### <span data-ttu-id="9e4eb-199">Microsoft. Azure. commands. Networks. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9e4eb-199">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="9e4eb-200">System. string []</span><span class="sxs-lookup"><span data-stu-id="9e4eb-200">System.String[]</span></span>

### <span data-ttu-id="9e4eb-201">Microsoft. Azure. commands. Network. Models. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="9e4eb-201">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="9e4eb-202">Microsoft. Azure. commands. Network. Models. PSVpnClientRevokedCertificate []</span><span class="sxs-lookup"><span data-stu-id="9e4eb-202">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="9e4eb-203">Microsoft. Azure. commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="9e4eb-203">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="9e4eb-204">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="9e4eb-204">System.UInt32</span></span>

### <span data-ttu-id="9e4eb-205">System. Int32</span><span class="sxs-lookup"><span data-stu-id="9e4eb-205">System.Int32</span></span>

### <span data-ttu-id="9e4eb-206">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="9e4eb-206">System.Security.SecureString</span></span>

## <span data-ttu-id="9e4eb-207">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9e4eb-207">OUTPUTS</span></span>

### <span data-ttu-id="9e4eb-208">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9e4eb-208">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="9e4eb-209">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9e4eb-209">NOTES</span></span>
* <span data-ttu-id="9e4eb-210">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="9e4eb-210">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="9e4eb-211">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9e4eb-211">RELATED LINKS</span></span>

[<span data-ttu-id="9e4eb-212">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9e4eb-212">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="9e4eb-213">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9e4eb-213">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="9e4eb-214">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9e4eb-214">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="9e4eb-215">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9e4eb-215">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="9e4eb-216">Ändra storlek – AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9e4eb-216">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)
