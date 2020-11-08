---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
ms.openlocfilehash: 9a18a995c79e744d4da366c59b621c1313048913
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261783"
---
# <span data-ttu-id="3d476-101">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3d476-101">Set-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="3d476-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3d476-102">SYNOPSIS</span></span>
<span data-ttu-id="3d476-103">Uppdaterar en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="3d476-103">Updates a virtual network gateway.</span></span>

## <span data-ttu-id="3d476-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3d476-104">SYNTAX</span></span>

### <span data-ttu-id="3d476-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="3d476-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3d476-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d476-106">RadiusServerConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-RemoveAadAuthentication] [-CustomRoute <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d476-107">RadiusServerConfigurationUpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="3d476-107">RadiusServerConfigurationUpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-RemoveAadAuthentication] [-CustomRoute <String[]>] -Tag <Hashtable>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d476-108">MultipleRadiusServersConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d476-108">MultipleRadiusServersConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] -RadiusServerList <PSRadiusServer[]>
 [-RemoveAadAuthentication] [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d476-109">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d476-109">AadAuthenticationConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] -AadTenantUri <String>
 -AadAudienceId <String> -AadIssuerUri <String> [-RemoveAadAuthentication] [-CustomRoute <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d476-110">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="3d476-110">UpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] -Tag <Hashtable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d476-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3d476-111">DESCRIPTION</span></span>
<span data-ttu-id="3d476-112">Cmdleten **set-AzVirtualNetworkGateway** uppdaterar en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="3d476-112">The **Set-AzVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="3d476-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3d476-113">EXAMPLES</span></span>

### <span data-ttu-id="3d476-114">Exempel 1: uppdatera ASN för en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="3d476-114">Example 1: Update a virtual network gateway's ASN</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="3d476-115">Det första kommandot får en virtuell nätverksgateway som heter Gateway01 som tillhör resurs gruppens ResourceGroup001 och lagrar den till variabeln $Gateway det andra kommandot uppdaterar den virtuella nätverksgateway som lagras i variabeln $Gateway.</span><span class="sxs-lookup"><span data-stu-id="3d476-115">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="3d476-116">Kommandot anger också ASN till 1337.</span><span class="sxs-lookup"><span data-stu-id="3d476-116">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="3d476-117">Exempel 2: lägga till IPsec-princip till en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="3d476-117">Example 2: Add IPsec policy to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="3d476-118">Det första kommandot får en virtuell nätverksgateway som heter Gateway01 som tillhör resurs gruppens ResourceGroup001 och lagrar det i variabeln $Gateway det andra kommandot skapar IPsec-principobjektet som enligt angivna IPsec-parametrar.</span><span class="sxs-lookup"><span data-stu-id="3d476-118">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="3d476-119">Det tredje kommandot uppdaterar den virtuella Nätverksgatewayen som lagras i variabeln $Gateway.</span><span class="sxs-lookup"><span data-stu-id="3d476-119">The third command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="3d476-120">Kommandot anger även den anpassade IPSec-principen för VPN som anges i $vpnclientipsecpolicy-objekt på virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="3d476-120">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

### <span data-ttu-id="3d476-121">Exempel 3: lägga till/uppdatera taggar till en befintlig virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="3d476-121">Example 3: Add/Update Tags to an existing virtual network gateway</span></span>
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

<span data-ttu-id="3d476-122">Det första kommandot får en virtuell nätverksgateway med namnet Gateway01 som tillhör resurs gruppens ResourceGroup001 och lagrar det till den variabel som heter $Gateway det andra kommandot uppdaterar den virtuella Nätverksgatewayen Gateway01 med taggarna @ {testtagKey = "SomeTagKey"; testtagValue = "SomeKeyValue"}.</span><span class="sxs-lookup"><span data-stu-id="3d476-122">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the tags @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }.</span></span>

### <span data-ttu-id="3d476-123">Exempel 4: lägga till/uppdatera AAD-VpnClient för en befintlig virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="3d476-123">Example 4: Add/Update AAD authentication configuration for VpnClient of an existing virtual network gateway</span></span>
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

<span data-ttu-id="3d476-124">Det första kommandot får en virtuell nätverksgateway med namnet Gateway01 som tillhör resurs gruppens ResourceGroup001 och lagrar det till den variabel som heter $Gateway det andra kommandot uppdaterar den virtuella Nätverksgatewayen Gateway01 med AAD-autentiseringsinställningarna: aadTenantUri, aadAudienceId, aadIssuerUri för VpnClient.</span><span class="sxs-lookup"><span data-stu-id="3d476-124">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the AAD authentication configurations params:aadTenantUri, aadAudienceId, aadIssuerUri for VpnClient.</span></span>
<span data-ttu-id="3d476-125">Det tredje kommandot tar bort identifieringen av AAD-konfigurationer från VpnClient i virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="3d476-125">The third command removes the AAD authentication configuration from VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="3d476-126">Exempel 5: lägga till/uppdatera IpConfigurationBgpPeeringAddresses till en befintlig virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="3d476-126">Example 5: Add/Update IpConfigurationBgpPeeringAddresses to an existing virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\>$ipconfigurationId1 = '/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/default'
PS C:\>$addresslist1 = @('169.254.21.25')
PS C:\>$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
PS C:\>Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -IpConfigurationBgpPeeringAddresses $gw1ipconfBgp1

Name                   : Gateway001
ResourceGroupName      : ResourceGroup001
Location               : westcentralus
Id                     : /subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001
Etag                   : W/"a08f13d3-6106-44e0-9127-e35e6f9793d5"
ResourceGuid           : 30993429-a1ed-42ca-9862-9156b013626e
ProvisioningState      : Succeeded
Tags                   :
IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworks/newApipaNet/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/publicIPAddresses/newapipaip"
                             },
                             "Name": "default",
                             "Etag": "W/\"a08f13d3-6106-44e0-9127-e35e6f9793d5\"",
                             "Id": "/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/default"
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
                           "BgpPeeringAddress": "10.1.255.30",
                           "PeerWeight": 0,
                           "BgpPeeringAddresses": [
                             {
                               "IpconfigurationId": "/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/default",
                               "DefaultBgpIpAddresses": [
                                 "10.1.255.30"
                               ],
                               "CustomBgpIpAddresses": [
                                 "169.254.21.55"
                               ],
                               "TunnelIpAddresses": [
                                 "13.78.146.151"
                               ]
                             }
                           ]
                         }
```

<span data-ttu-id="3d476-127">Det första kommandot får en virtuell nätverksgateway med namnet Gateway01 som tillhör resurs gruppens ResourceGroup001 och lagrar det i variabeln $Gateway det andra kommandot tilldelar värdet för ID-numret för virtuell nätverksgateway Gateway01 till variabelt ipconfigurationId1.</span><span class="sxs-lookup"><span data-stu-id="3d476-127">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command assigns the value of virtual network gateway Gateway01 IpConfiguration Id into variable ipconfigurationId1.</span></span>
<span data-ttu-id="3d476-128">Det tredje kommandot tilldelar adress listan till addresslist1.</span><span class="sxs-lookup"><span data-stu-id="3d476-128">The third command assigns the address list into addresslist1.</span></span>
<span data-ttu-id="3d476-129">Det fjärde kommandot har skapat ett PSIpConfigurationBgpPeeringAddress-objekt.</span><span class="sxs-lookup"><span data-stu-id="3d476-129">The fourth command created a PSIpConfigurationBgpPeeringAddress object.</span></span>
<span data-ttu-id="3d476-130">Det femte kommandot ange den här nya PSIpConfigurationBgpPeeringAddress till IpConfigurationBgpPeeringAddresses och uppdatera gatewayen.</span><span class="sxs-lookup"><span data-stu-id="3d476-130">The fifth command set this new created PSIpConfigurationBgpPeeringAddress to IpConfigurationBgpPeeringAddresses and update the gateway.</span></span>

## <span data-ttu-id="3d476-131">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3d476-131">PARAMETERS</span></span>

### <span data-ttu-id="3d476-132">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="3d476-132">-AadAudienceId</span></span>
<span data-ttu-id="3d476-133">P2S AAD: AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="3d476-133">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="3d476-134">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="3d476-134">-AadIssuerUri</span></span>
<span data-ttu-id="3d476-135">P2S AAD: AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="3d476-135">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="3d476-136">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="3d476-136">-AadTenantUri</span></span>
<span data-ttu-id="3d476-137">P2S AAD: AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="3d476-137">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="3d476-138">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d476-138">-AsJob</span></span>
<span data-ttu-id="3d476-139">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="3d476-139">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3d476-140">-ASN</span><span class="sxs-lookup"><span data-stu-id="3d476-140">-Asn</span></span>
<span data-ttu-id="3d476-141">ASN för den virtuella Nätverksgatewayen används för att konfigurera BGP-sessioner i IPsec-tunnlar</span><span class="sxs-lookup"><span data-stu-id="3d476-141">The virtual network gateway's ASN, used to set up BGP sessions inside IPsec tunnels</span></span>

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

### <span data-ttu-id="3d476-142">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="3d476-142">-CustomRoute</span></span>
<span data-ttu-id="3d476-143">Anpassade flöden AddressPool anges av kund</span><span class="sxs-lookup"><span data-stu-id="3d476-143">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="3d476-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d476-144">-DefaultProfile</span></span>
<span data-ttu-id="3d476-145">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3d476-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d476-146">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="3d476-146">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="3d476-147">Flagga för att inaktivera aktiv aktive rad funktion i virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="3d476-147">Flag to disable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="3d476-148">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="3d476-148">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="3d476-149">Flagga för att aktivera aktiv aktive rad funktion i virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="3d476-149">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="3d476-150">-EnablePrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="3d476-150">-EnablePrivateIpAddress</span></span>
<span data-ttu-id="3d476-151">Flagga för att aktivera aktiv aktive rad funktion i virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="3d476-151">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="3d476-152">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="3d476-152">-GatewayDefaultSite</span></span>
<span data-ttu-id="3d476-153">Standard webbplatsen som ska användas för Tvingad tunnel trafik.</span><span class="sxs-lookup"><span data-stu-id="3d476-153">The default site to use for force tunneling.</span></span>
<span data-ttu-id="3d476-154">Om en standard webbplats anges routas all Internet trafik från gatewayens VNet till den platsen.</span><span class="sxs-lookup"><span data-stu-id="3d476-154">If a default site is specified, all internet traffic from the gateway's vnet is routed to that site.</span></span>

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

### <span data-ttu-id="3d476-155">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="3d476-155">-GatewaySku</span></span>
<span data-ttu-id="3d476-156">SKU för virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="3d476-156">The virtual network gateway's SKU</span></span>

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

### <span data-ttu-id="3d476-157">-IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="3d476-157">-IpConfigurationBgpPeeringAddresses</span></span>
<span data-ttu-id="3d476-158">BgpPeeringAddresses för virtuell nätverksgateway-bgpsettings.</span><span class="sxs-lookup"><span data-stu-id="3d476-158">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d476-159">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="3d476-159">-PeerWeight</span></span>
<span data-ttu-id="3d476-160">Vikten som läggs till i vägar som upptäckts via BGP från denna virtuella nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="3d476-160">The weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="3d476-161">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="3d476-161">-RadiusServerAddress</span></span>
<span data-ttu-id="3d476-162">P2S externa RADIUS-serveradress.</span><span class="sxs-lookup"><span data-stu-id="3d476-162">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="3d476-163">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="3d476-163">-RadiusServerList</span></span>
<span data-ttu-id="3d476-164">P2S flera externa RADIUS-servrar.</span><span class="sxs-lookup"><span data-stu-id="3d476-164">P2S multiple external Radius servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRadiusServer[]
Parameter Sets: MultipleRadiusServersConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d476-165">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="3d476-165">-RadiusServerSecret</span></span>
<span data-ttu-id="3d476-166">P2S externa RADIUS-server hemlighet.</span><span class="sxs-lookup"><span data-stu-id="3d476-166">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="3d476-167">-RemoveAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="3d476-167">-RemoveAadAuthentication</span></span>
<span data-ttu-id="3d476-168">Flagga för att ta bort AAD-inloggningsautentisering för P2S-klient från virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="3d476-168">Flag to remove AAD authentication for P2S client from virtual network gateway.</span></span>

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

### <span data-ttu-id="3d476-169">-Tagg</span><span class="sxs-lookup"><span data-stu-id="3d476-169">-Tag</span></span>
<span data-ttu-id="3d476-170">P2S externa RADIUS-serveradress.</span><span class="sxs-lookup"><span data-stu-id="3d476-170">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="3d476-171">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3d476-171">-VirtualNetworkGateway</span></span>
<span data-ttu-id="3d476-172">Det virtuella nätverkets gateway-objekt för att basera ändringar från av.</span><span class="sxs-lookup"><span data-stu-id="3d476-172">The virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="3d476-173">Det här kan hämtas med Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3d476-173">This can be retrieved using Get-AzVirtualNetworkGateway</span></span>

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

### <span data-ttu-id="3d476-174">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="3d476-174">-VpnClientAddressPool</span></span>
<span data-ttu-id="3d476-175">Adress utrymmet för tilldelning av IP-adresser för VPN-klienter.</span><span class="sxs-lookup"><span data-stu-id="3d476-175">The address space to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="3d476-176">Detta ska inte överlappa virtuella nätverks-eller lokala områden.</span><span class="sxs-lookup"><span data-stu-id="3d476-176">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="3d476-177">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="3d476-177">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="3d476-178">En lista över IPSec-principer för tunnel protokoll för P2S VPN-klienter.</span><span class="sxs-lookup"><span data-stu-id="3d476-178">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="3d476-179">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="3d476-179">-VpnClientProtocol</span></span>
<span data-ttu-id="3d476-180">En lista över protokoll för P2S VPN-klienter</span><span class="sxs-lookup"><span data-stu-id="3d476-180">A list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="3d476-181">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="3d476-181">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="3d476-182">En lista över återkallade VPN-klientcertifikat.</span><span class="sxs-lookup"><span data-stu-id="3d476-182">A list of revoked VPN client certificates.</span></span>
<span data-ttu-id="3d476-183">En VPN-klient som presenterar ett certifikat som matchar en av dessa kommer att få ett meddelande att bli borta.</span><span class="sxs-lookup"><span data-stu-id="3d476-183">A VPN client presenting a certificate that matches one of these will be told to go away.</span></span>

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

### <span data-ttu-id="3d476-184">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="3d476-184">-VpnClientRootCertificates</span></span>
<span data-ttu-id="3d476-185">En lista över VPN-klientens rot certifikat som används för VPN-klientautentisering.</span><span class="sxs-lookup"><span data-stu-id="3d476-185">A list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="3d476-186">Anslutning av VPN-klienter måste presentera certifikat som genererats från ett av dessa rot certifikat.</span><span class="sxs-lookup"><span data-stu-id="3d476-186">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="3d476-187">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3d476-187">-Confirm</span></span>
<span data-ttu-id="3d476-188">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3d476-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d476-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d476-189">-WhatIf</span></span>
<span data-ttu-id="3d476-190">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3d476-190">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d476-191">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3d476-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d476-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d476-192">CommonParameters</span></span>
<span data-ttu-id="3d476-193">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d476-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d476-194">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d476-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d476-195">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3d476-195">INPUTS</span></span>

### <span data-ttu-id="3d476-196">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3d476-196">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="3d476-197">System. String</span><span class="sxs-lookup"><span data-stu-id="3d476-197">System.String</span></span>

### <span data-ttu-id="3d476-198">Microsoft. Azure. commands. Networks. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3d476-198">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="3d476-199">System. string []</span><span class="sxs-lookup"><span data-stu-id="3d476-199">System.String[]</span></span>

### <span data-ttu-id="3d476-200">Microsoft. Azure. commands. Network. Models. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="3d476-200">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="3d476-201">Microsoft. Azure. commands. Network. Models. PSVpnClientRevokedCertificate []</span><span class="sxs-lookup"><span data-stu-id="3d476-201">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="3d476-202">Microsoft. Azure. commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="3d476-202">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="3d476-203">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="3d476-203">System.UInt32</span></span>

### <span data-ttu-id="3d476-204">System. Int32</span><span class="sxs-lookup"><span data-stu-id="3d476-204">System.Int32</span></span>

### <span data-ttu-id="3d476-205">Microsoft. Azure. commands. Network. Models. PSIpConfigurationBgpPeeringAddress []</span><span class="sxs-lookup"><span data-stu-id="3d476-205">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span></span>

### <span data-ttu-id="3d476-206">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="3d476-206">System.Security.SecureString</span></span>

## <span data-ttu-id="3d476-207">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3d476-207">OUTPUTS</span></span>

### <span data-ttu-id="3d476-208">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3d476-208">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="3d476-209">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3d476-209">NOTES</span></span>

## <span data-ttu-id="3d476-210">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3d476-210">RELATED LINKS</span></span>
