---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
ms.openlocfilehash: c6c3e7826b7b9c8aa80e362ad579c1875d53bbce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271547"
---
# <span data-ttu-id="627bb-101">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="627bb-101">New-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="627bb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="627bb-102">SYNOPSIS</span></span>
<span data-ttu-id="627bb-103">Skapar en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="627bb-103">Creates a Virtual Network Gateway</span></span>

## <span data-ttu-id="627bb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="627bb-104">SYNTAX</span></span>

### <span data-ttu-id="627bb-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="627bb-105">Default (Default)</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-EnablePrivateIpAddress] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-Force]
 [-CustomRoute <String[]>] [-VpnGatewayGeneration <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="627bb-106">MultipleRadiusServersConfiguration</span><span class="sxs-lookup"><span data-stu-id="627bb-106">MultipleRadiusServersConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-EnablePrivateIpAddress] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-Force]
 -RadiusServerList <PSRadiusServer[]> [-CustomRoute <String[]>] [-VpnGatewayGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="627bb-107">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="627bb-107">RadiusServerConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-EnablePrivateIpAddress] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-Force]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-CustomRoute <String[]>]
 [-VpnGatewayGeneration <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="627bb-108">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="627bb-108">AadAuthenticationConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-EnablePrivateIpAddress] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-Force]
 -AadTenantUri <String> -AadAudienceId <String> -AadIssuerUri <String> [-CustomRoute <String[]>]
 [-VpnGatewayGeneration <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="627bb-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="627bb-109">DESCRIPTION</span></span>
<span data-ttu-id="627bb-110">Den virtuella Nätverksgatewayen är det objekt som representerar din gateway i Azure.</span><span class="sxs-lookup"><span data-stu-id="627bb-110">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="627bb-111">Cmdleten **New-AzVirtualNetworkGateway** skapar ett objekt för din gateway i Azure baserat på namnet, resurs gruppens namn, plats och IP-konfiguration samt Gateway-typen och om VPN, VPN-typen.</span><span class="sxs-lookup"><span data-stu-id="627bb-111">The **New-AzVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="627bb-112">Du kan också ge Gateway SKU.</span><span class="sxs-lookup"><span data-stu-id="627bb-112">You can also name the Gateway SKU.</span></span>
<span data-ttu-id="627bb-113">Om den här gatewayen används för punkt-till-plats-anslutningar måste du även ta med den VPN-adresspool som du vill tilldela adresser för att ansluta klienter och det VPN-klient rot certifikat som används för att autentisera VPN-klienter som ansluter till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="627bb-113">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>
<span data-ttu-id="627bb-114">Du kan också välja att inkludera andra funktioner som BGP och Active-Active.</span><span class="sxs-lookup"><span data-stu-id="627bb-114">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="627bb-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="627bb-115">EXAMPLES</span></span>

### <span data-ttu-id="627bb-116">Exempel 1: skapa en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="627bb-116">Example 1: Create a Virtual Network Gateway</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="627bb-117">Ovanstående skapar en resurs grupp, efterfrågar en offentlig IP-adress, skapar ett virtuellt nätverk och undernät och skapar en virtuell nätverksgateway i Azure.</span><span class="sxs-lookup"><span data-stu-id="627bb-117">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="627bb-118">Gatewayen kallas "myNGW" i resurs gruppen "VNet-Gateway" i platsen "UK West", med tidigare skapade IP-konfigurationer sparade i variabeln "ngwIPConfig", Gateway-typen för "VPN", VPN-typen "RouteBased" och "Basic"-SKU: n.</span><span class="sxs-lookup"><span data-stu-id="627bb-118">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="627bb-119">Exempel 2: skapa en virtuell nätverksgateway med en extern RADIUS-konfiguration</span><span class="sxs-lookup"><span data-stu-id="627bb-119">Example 2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="627bb-120">Ovanstående skapar en resurs grupp, efterfrågar en offentlig IP-adress, skapar ett virtuellt nätverk och undernät och skapar en virtuell nätverksgateway i Azure.</span><span class="sxs-lookup"><span data-stu-id="627bb-120">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="627bb-121">Gatewayen kallas "myNGW" i resurs gruppen "VNet-Gateway" i platsen "UK West", med tidigare skapade IP-konfigurationer sparade i variabeln "ngwIPConfig", Gateway-typen för "VPN", VPN-typen "RouteBased" och "Basic"-SKU: n.</span><span class="sxs-lookup"><span data-stu-id="627bb-121">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="627bb-122">Dessutom läggs en extern RADIUS-server till med adressen "TestRadiusServer".</span><span class="sxs-lookup"><span data-stu-id="627bb-122">It also adds an external radius server with address "TestRadiusServer".</span></span> <span data-ttu-id="627bb-123">Dessutom anges anpassade vägar som anges av kunder på gatewayen.</span><span class="sxs-lookup"><span data-stu-id="627bb-123">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="627bb-124">Exempel 3: skapa en virtuell nätverksgateway med P2S-inställningar</span><span class="sxs-lookup"><span data-stu-id="627bb-124">Example 3: Create a Virtual Network Gateway with P2S settings</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$rootCert = New-AzVpnClientRootCertificate -Name $clientRootCertName -PublicCertData $samplePublicCertData
$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86471 -SADataSizeKilobytes 429496 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw1" -VpnClientProtocol IkeV2 -VpnClientAddressPool 201.169.0.0/16 -VpnClientRootCertificates $rootCert -VpnClientIpsecPolicy $vpnclientipsecpolicy -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="627bb-125">Ovanstående skapar en resurs grupp, efterfrågar en offentlig IP-adress, skapar ett virtuellt nätverk och undernät och skapar en virtuell nätverksgateway med P2S-inställningar, till exempel VpnProtocol, VpnClientAddressPool, VpnClientRootCertificates, VpnClientIpsecPolicy osv. i Azure.</span><span class="sxs-lookup"><span data-stu-id="627bb-125">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway with P2S settings e.g. VpnProtocol,VpnClientAddressPool,VpnClientRootCertificates,VpnClientIpsecPolicy etc. in Azure.</span></span>
<span data-ttu-id="627bb-126">Gatewayen kallas "myNGW" i resurs gruppen "VNet-Gateway" i platsen "UK West", med tidigare skapade IP-konfigurationer sparade i variabeln "ngwIPConfig", Gateway-typen för "VPN", VPN-typen "RouteBased" och "SKU" VpnGw1 ".</span><span class="sxs-lookup"><span data-stu-id="627bb-126">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "VpnGw1."</span></span> <span data-ttu-id="627bb-127">VPN-inställningar kommer att anges på gateway som VpnProtocol angiven som Ikev2, VpnClientAddressPool som "201.169.0.0/16", VpnClientRootCertificate angett en: clientRootCertName och anpassad IPsec-princip för VPN som överförts i objekt: $vpnclientipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="627bb-127">Vpn settings will be set on Gateway such as VpnProtocol set as Ikev2, VpnClientAddressPool as "201.169.0.0/16", VpnClientRootCertificate set as passed one: clientRootCertName and custom vpn ipsec policy passed in object:$vpnclientipsecpolicy</span></span>  
<span data-ttu-id="627bb-128">Dessutom anges anpassade vägar som anges av kunder på gatewayen.</span><span class="sxs-lookup"><span data-stu-id="627bb-128">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="627bb-129">Exempel 4: skapa en virtuell nätverksgateway med identifiering av AAD-konfiguration för VpnClient av virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="627bb-129">Example 4: Create a Virtual Network Gateway with AAD authentication Configuration for VpnClient of virtual network gateway.</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw1" -VpnClientProtocol OpenVPN   -VpnClientAddressPool 201.169.0.0/16 -AadTenantUri "https://login.microsoftonline.com/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4" -AadIssuerUri "https://sts.windows.net/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4/" -AadAudienceId "a21fce82-76af-45e6-8583-a08cb3b956f9"
```

<span data-ttu-id="627bb-130">Ovanstående skapar en resurs grupp, efterfrågar en offentlig IP-adress, skapar ett virtuellt nätverk och undernät och skapar en virtuell nätverksgateway i Azure.</span><span class="sxs-lookup"><span data-stu-id="627bb-130">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="627bb-131">Gatewayen kallas "myNGW" i resurs gruppen "VNet-Gateway" i platsen "UK West", med tidigare skapade IP-konfigurationer sparade i variabeln "ngwIPConfig", Gateway-typen för "VPN", VPN-typen "RouteBased" och "Basic"-SKU: n.</span><span class="sxs-lookup"><span data-stu-id="627bb-131">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="627bb-132">Den konfigurerar också inloggningsautentisering för AAD: AadTenantUri, AadIssuerUri och AadAudienceId för VpnClient för virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="627bb-132">It also configures AAD authentication configurations: AadTenantUri, AadIssuerUri and AadAudienceId for VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="627bb-133">Exempel 5: skapa en virtuell nätverksgateway med VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="627bb-133">Example 5: Create a Virtual Network Gateway with VpnGatewayGeneration</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw4" -VpnGatewayGeneration "Generation2"
```

<span data-ttu-id="627bb-134">Ovanstående skapar en resurs grupp, efterfrågar en offentlig IP-adress, skapar ett virtuellt nätverk och undernät och skapar en virtuell nätverksgateway i Azure.</span><span class="sxs-lookup"><span data-stu-id="627bb-134">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="627bb-135">Gatewayen kallas "myNGW" i resurs gruppen "VNet-Gateway" på platsen "UK West" med tidigare skapade IP-konfigurationer sparade i variabeln "ngwIPConfig", Gateway-typen för VPN, VPN-typen "RouteBased", SKU "VpnGw4" och VpnGatewayGeneration Generation2 Enabled.</span><span class="sxs-lookup"><span data-stu-id="627bb-135">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

### <span data-ttu-id="627bb-136">Exempel 6: skapa en virtuell nätverksgateway med IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="627bb-136">Example 6: Create a Virtual Network Gateway with IpConfigurationBgpPeeringAddresses</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "resourcegroup1"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "resourcegroup1" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "resourcegroup1" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ipconfig1 -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

$ipconfigurationId1 = ngwipconfig.id
$addresslist1 = @('169.254.21.10')
$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1

New-AzVirtualNetworkGateway -Name gateway1 -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig -IpConfigurationBgpPeeringAddresses $gw1ipconfBgp1 -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw4" -VpnGatewayGeneration "Generation2"
```

<span data-ttu-id="627bb-137">Ovanstående skapar en resurs grupp, efterfrågar en offentlig IP-adress, skapar ett virtuellt nätverk och undernät och skapar en virtuell nätverksgateway i Azure.</span><span class="sxs-lookup"><span data-stu-id="627bb-137">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="627bb-138">ipconfigurationId1 av Gateway ipconfiguration som nyss skapats och lagrats i ngwipconfig.</span><span class="sxs-lookup"><span data-stu-id="627bb-138">ipconfigurationId1 of gateway ipconfiguration just created and stored in ngwipconfig.</span></span>
<span data-ttu-id="627bb-139">Gatewayen kallas "gateway1" i resurs gruppen "resourcegroup1resourcegroup1" i platsen "UK West" med tidigare skapad-adress för IP-konfiguration som sparats i variabeln "gw1ipconfBgp1", Gateway-typen för VPN, VPN-typen "RouteBased", SKU "VpnGw4" och VpnGatewayGeneration Generation2 Enabled.</span><span class="sxs-lookup"><span data-stu-id="627bb-139">The gateway will be called "gateway1" within the resource group "resourcegroup1resourcegroup1" in the location "UK West" with the previously created IP configurations Bgppeering address saved in the variable "gw1ipconfBgp1," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

## <span data-ttu-id="627bb-140">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="627bb-140">PARAMETERS</span></span>

### <span data-ttu-id="627bb-141">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="627bb-141">-AadAudienceId</span></span>
<span data-ttu-id="627bb-142">P2S AAD: AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="627bb-142">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="627bb-143">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="627bb-143">-AadIssuerUri</span></span>
<span data-ttu-id="627bb-144">P2S AAD: AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="627bb-144">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="627bb-145">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="627bb-145">-AadTenantUri</span></span>
<span data-ttu-id="627bb-146">P2S AAD: AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="627bb-146">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="627bb-147">-AsJob</span><span class="sxs-lookup"><span data-stu-id="627bb-147">-AsJob</span></span>
<span data-ttu-id="627bb-148">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="627bb-148">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="627bb-149">-ASN</span><span class="sxs-lookup"><span data-stu-id="627bb-149">-Asn</span></span>
<span data-ttu-id="627bb-150">ASN för BGP over VPN för den virtuella Nätverksgatewayen</span><span class="sxs-lookup"><span data-stu-id="627bb-150">The virtual network gateway's ASN for BGP over VPN</span></span>

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

### <span data-ttu-id="627bb-151">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="627bb-151">-CustomRoute</span></span>
<span data-ttu-id="627bb-152">Anpassade flöden AddressPool anges av kund</span><span class="sxs-lookup"><span data-stu-id="627bb-152">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="627bb-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="627bb-153">-DefaultProfile</span></span>
<span data-ttu-id="627bb-154">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="627bb-154">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="627bb-155">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="627bb-155">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="627bb-156">Flagga för att aktivera aktiv aktive rad funktion i virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="627bb-156">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="627bb-157">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="627bb-157">-EnableBgp</span></span>
<span data-ttu-id="627bb-158">Flaggan EnableBgp</span><span class="sxs-lookup"><span data-stu-id="627bb-158">EnableBgp Flag</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="627bb-159">-EnablePrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="627bb-159">-EnablePrivateIpAddress</span></span>
<span data-ttu-id="627bb-160">Flagga för att aktivera privat IP-adress på virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="627bb-160">Flag to enable private IPAddress on virtual network gateway</span></span>

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

### <span data-ttu-id="627bb-161">-Force</span><span class="sxs-lookup"><span data-stu-id="627bb-161">-Force</span></span>
<span data-ttu-id="627bb-162">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="627bb-162">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="627bb-163">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="627bb-163">-GatewayDefaultSite</span></span>
<span data-ttu-id="627bb-164">GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="627bb-164">GatewayDefaultSite</span></span>

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

### <span data-ttu-id="627bb-165">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="627bb-165">-GatewaySku</span></span>
<span data-ttu-id="627bb-166">Gateway SKU-nivån</span><span class="sxs-lookup"><span data-stu-id="627bb-166">The Gateway Sku Tier</span></span>

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

### <span data-ttu-id="627bb-167">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="627bb-167">-GatewayType</span></span>
<span data-ttu-id="627bb-168">Den här virtuella Nätverksgatewayen: VPN, ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="627bb-168">The type of this virtual network gateway: Vpn, ExpressRoute</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Vpn, ExpressRoute

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="627bb-169">-IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="627bb-169">-IpConfigurationBgpPeeringAddresses</span></span>
<span data-ttu-id="627bb-170">BgpPeeringAddresses för virtuell nätverksgateway-bgpsettings.</span><span class="sxs-lookup"><span data-stu-id="627bb-170">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span></span>

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

### <span data-ttu-id="627bb-171">-IpConfigurations</span><span class="sxs-lookup"><span data-stu-id="627bb-171">-IpConfigurations</span></span>
<span data-ttu-id="627bb-172">IpConfigurations för virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="627bb-172">The IpConfigurations for Virtual network gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="627bb-173">-Plats</span><span class="sxs-lookup"><span data-stu-id="627bb-173">-Location</span></span>
<span data-ttu-id="627bb-174">plats.</span><span class="sxs-lookup"><span data-stu-id="627bb-174">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="627bb-175">-Namn</span><span class="sxs-lookup"><span data-stu-id="627bb-175">-Name</span></span>
<span data-ttu-id="627bb-176">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="627bb-176">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="627bb-177">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="627bb-177">-PeerWeight</span></span>
<span data-ttu-id="627bb-178">Vikten som läggs till i vägar som upptäckts via BGP från denna virtuella nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="627bb-178">The weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="627bb-179">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="627bb-179">-RadiusServerAddress</span></span>
<span data-ttu-id="627bb-180">P2S externa RADIUS-serveradress.</span><span class="sxs-lookup"><span data-stu-id="627bb-180">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="627bb-181">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="627bb-181">-RadiusServerList</span></span>
<span data-ttu-id="627bb-182">P2S flera externa RADIUS-servrar.</span><span class="sxs-lookup"><span data-stu-id="627bb-182">P2S multiple external Radius server servers.</span></span>

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

### <span data-ttu-id="627bb-183">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="627bb-183">-RadiusServerSecret</span></span>
<span data-ttu-id="627bb-184">P2S externa RADIUS-server hemlighet.</span><span class="sxs-lookup"><span data-stu-id="627bb-184">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="627bb-185">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="627bb-185">-ResourceGroupName</span></span>
<span data-ttu-id="627bb-186">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="627bb-186">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="627bb-187">-Tagg</span><span class="sxs-lookup"><span data-stu-id="627bb-187">-Tag</span></span>
<span data-ttu-id="627bb-188">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="627bb-188">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="627bb-189">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="627bb-189">-VpnClientAddressPool</span></span>
<span data-ttu-id="627bb-190">P2S VpnClient AddressPool</span><span class="sxs-lookup"><span data-stu-id="627bb-190">P2S VpnClient AddressPool</span></span>

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

### <span data-ttu-id="627bb-191">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="627bb-191">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="627bb-192">En lista över IPSec-principer för tunnel protokoll för P2S VPN-klienter.</span><span class="sxs-lookup"><span data-stu-id="627bb-192">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="627bb-193">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="627bb-193">-VpnClientProtocol</span></span>
<span data-ttu-id="627bb-194">Listan med tunnel protokoll för P2S VPN-klienter</span><span class="sxs-lookup"><span data-stu-id="627bb-194">The list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="627bb-195">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="627bb-195">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="627bb-196">Listan med VpnClientCertificates som ska återkallas.</span><span class="sxs-lookup"><span data-stu-id="627bb-196">The list of VpnClientCertificates to be revoked.</span></span>

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

### <span data-ttu-id="627bb-197">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="627bb-197">-VpnClientRootCertificates</span></span>
<span data-ttu-id="627bb-198">Listan med VpnClientRootCertificates som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="627bb-198">The list of VpnClientRootCertificates to be added.</span></span>

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

### <span data-ttu-id="627bb-199">-VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="627bb-199">-VpnGatewayGeneration</span></span>
<span data-ttu-id="627bb-200">Genereringen för denna VirtualNetwork VPN gateway.</span><span class="sxs-lookup"><span data-stu-id="627bb-200">The generation for this VirtualNetwork VPN gateway.</span></span>
<span data-ttu-id="627bb-201">Måste vara ingen om GatewayType inte är VPN.</span><span class="sxs-lookup"><span data-stu-id="627bb-201">Must be None if GatewayType is not VPN.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="627bb-202">-VpnType</span><span class="sxs-lookup"><span data-stu-id="627bb-202">-VpnType</span></span>
<span data-ttu-id="627bb-203">Typen för VPN: PolicyBased/RouteBased</span><span class="sxs-lookup"><span data-stu-id="627bb-203">The type of the Vpn:PolicyBased/RouteBased</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PolicyBased, RouteBased

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="627bb-204">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="627bb-204">-Confirm</span></span>
<span data-ttu-id="627bb-205">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="627bb-205">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="627bb-206">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="627bb-206">-WhatIf</span></span>
<span data-ttu-id="627bb-207">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="627bb-207">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="627bb-208">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="627bb-208">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="627bb-209">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="627bb-209">CommonParameters</span></span>
<span data-ttu-id="627bb-210">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="627bb-210">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="627bb-211">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="627bb-211">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="627bb-212">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="627bb-212">INPUTS</span></span>

### <span data-ttu-id="627bb-213">System. String</span><span class="sxs-lookup"><span data-stu-id="627bb-213">System.String</span></span>

### <span data-ttu-id="627bb-214">Microsoft. Azure. commands. Network. Models. PSVirtualNetworkGatewayIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="627bb-214">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span></span>

### <span data-ttu-id="627bb-215">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="627bb-215">System.Boolean</span></span>

### <span data-ttu-id="627bb-216">Microsoft. Azure. commands. Networks. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="627bb-216">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="627bb-217">System. string []</span><span class="sxs-lookup"><span data-stu-id="627bb-217">System.String[]</span></span>

### <span data-ttu-id="627bb-218">Microsoft. Azure. commands. Network. Models. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="627bb-218">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="627bb-219">Microsoft. Azure. commands. Network. Models. PSVpnClientRevokedCertificate []</span><span class="sxs-lookup"><span data-stu-id="627bb-219">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="627bb-220">Microsoft. Azure. commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="627bb-220">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="627bb-221">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="627bb-221">System.UInt32</span></span>

### <span data-ttu-id="627bb-222">System. Int32</span><span class="sxs-lookup"><span data-stu-id="627bb-222">System.Int32</span></span>

### <span data-ttu-id="627bb-223">Microsoft. Azure. commands. Network. Models. PSIpConfigurationBgpPeeringAddress []</span><span class="sxs-lookup"><span data-stu-id="627bb-223">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span></span>

### <span data-ttu-id="627bb-224">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="627bb-224">System.Collections.Hashtable</span></span>

### <span data-ttu-id="627bb-225">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="627bb-225">System.Security.SecureString</span></span>

## <span data-ttu-id="627bb-226">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="627bb-226">OUTPUTS</span></span>

### <span data-ttu-id="627bb-227">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="627bb-227">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="627bb-228">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="627bb-228">NOTES</span></span>

## <span data-ttu-id="627bb-229">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="627bb-229">RELATED LINKS</span></span>