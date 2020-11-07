---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 7a818ba86092200c31d9d0a217042e6f6dce4857
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756375"
---
# <span data-ttu-id="b5074-101">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b5074-101">New-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="b5074-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b5074-102">SYNOPSIS</span></span>
<span data-ttu-id="b5074-103">Skapar en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="b5074-103">Creates a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5074-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b5074-104">SYNTAX</span></span>

### <span data-ttu-id="b5074-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="b5074-105">Default (Default)</span></span>
```
New-AzureRmVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]>]
 [-GatewayType <String>] [-VpnType <String>] [-EnableBgp <Boolean>] [-EnableActiveActiveFeature]
 [-GatewaySku <String>] [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-VpnClientIpsecPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5074-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="b5074-106">RadiusServerConfiguration</span></span>
```
New-AzureRmVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]>]
 [-GatewayType <String>] [-VpnType <String>] [-EnableBgp <Boolean>] [-EnableActiveActiveFeature]
 [-GatewaySku <String>] [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-VpnClientIpsecPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b5074-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b5074-107">DESCRIPTION</span></span>
<span data-ttu-id="b5074-108">Den virtuella Nätverksgatewayen är det objekt som representerar din gateway i Azure.</span><span class="sxs-lookup"><span data-stu-id="b5074-108">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="b5074-109">Cmdleten **New-AzureRmVirtualNetworkGateway** skapar ett objekt för din gateway i Azure baserat på namnet, resurs gruppens namn, plats och IP-konfiguration samt Gateway-typen och om VPN, VPN-typen.</span><span class="sxs-lookup"><span data-stu-id="b5074-109">The **New-AzureRmVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="b5074-110">Du kan också ge Gateway SKU.</span><span class="sxs-lookup"><span data-stu-id="b5074-110">You can also name the Gateway SKU.</span></span>
<span data-ttu-id="b5074-111">Om den här gatewayen används för punkt-till-plats-anslutningar måste du även ta med den VPN-adresspool som du vill tilldela adresser för att ansluta klienter och det VPN-klient rot certifikat som används för att autentisera VPN-klienter som ansluter till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="b5074-111">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>
<span data-ttu-id="b5074-112">Du kan också välja att inkludera andra funktioner som BGP och Active-Active.</span><span class="sxs-lookup"><span data-stu-id="b5074-112">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="b5074-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b5074-113">EXAMPLES</span></span>

### <span data-ttu-id="b5074-114">1: skapa en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="b5074-114">1: Create a Virtual Network Gateway</span></span>
```
New-AzureRmResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzureRMVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzureRMPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzureRmVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzureRMVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzureRmVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic"
```

<span data-ttu-id="b5074-115">Ovanstående skapar en resurs grupp, efterfrågar en offentlig IP-adress, skapar ett virtuellt nätverk och undernät och skapar en virtuell nätverksgateway i Azure.</span><span class="sxs-lookup"><span data-stu-id="b5074-115">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="b5074-116">Gatewayen kallas "myNGW" i resurs gruppen "VNet-Gateway" i platsen "UK West", med tidigare skapade IP-konfigurationer sparade i variabeln "ngwIPConfig", Gateway-typen för "VPN", VPN-typen "RouteBased" och "Basic"-SKU: n.</span><span class="sxs-lookup"><span data-stu-id="b5074-116">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="b5074-117">2: skapa en virtuell nätverksgateway med extern RADIUS-konfiguration</span><span class="sxs-lookup"><span data-stu-id="b5074-117">2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
```
New-AzureRmResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzureRMVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzureRMPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzureRmVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzureRMVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzureRmVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd
```

<span data-ttu-id="b5074-118">Ovanstående skapar en resurs grupp, efterfrågar en offentlig IP-adress, skapar ett virtuellt nätverk och undernät och skapar en virtuell nätverksgateway i Azure.</span><span class="sxs-lookup"><span data-stu-id="b5074-118">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="b5074-119">Gatewayen kallas "myNGW" i resurs gruppen "VNet-Gateway" i platsen "UK West", med tidigare skapade IP-konfigurationer sparade i variabeln "ngwIPConfig", Gateway-typen för "VPN", VPN-typen "RouteBased" och "Basic"-SKU: n.</span><span class="sxs-lookup"><span data-stu-id="b5074-119">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="b5074-120">Dessutom läggs en extern RADIUS-server till med adressen "TestRadiusServer"</span><span class="sxs-lookup"><span data-stu-id="b5074-120">It also adds an external radius server with address "TestRadiusServer"</span></span>

### <span data-ttu-id="b5074-121">1: skapa en virtuell nätverksgateway med P2S-inställningar</span><span class="sxs-lookup"><span data-stu-id="b5074-121">1: Create a Virtual Network Gateway with P2S settings</span></span>
```
New-AzureRmResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzureRMVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzureRMPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzureRmVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzureRMVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$rootCert = New-AzureRmVpnClientRootCertificate -Name $clientRootCertName -PublicCertData $samplePublicCertData
$vpnclientipsecpolicy = New-AzureRmVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86471 -SADataSizeKilobytes 429496 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2

New-AzureRmVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw1" -VpnClientProtocol IkeV2 -VpnClientAddressPool 201.169.0.0/16 -VpnClientRootCertificates $rootCert -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="b5074-122">Ovanstående skapar en resurs grupp, efterfrågar en offentlig IP-adress, skapar ett virtuellt nätverk och undernät och skapar en virtuell nätverksgateway med P2S-inställningar, till exempel VpnProtocol, VpnClientAddressPool, VpnClientRootCertificates, VpnClientIpsecPolicy osv. i Azure.</span><span class="sxs-lookup"><span data-stu-id="b5074-122">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway with P2S settings e.g. VpnProtocol,VpnClientAddressPool,VpnClientRootCertificates,VpnClientIpsecPolicy etc. in Azure.</span></span>
<span data-ttu-id="b5074-123">Gatewayen kallas "myNGW" i resurs gruppen "VNet-Gateway" i platsen "UK West", med tidigare skapade IP-konfigurationer sparade i variabeln "ngwIPConfig", Gateway-typen för "VPN", VPN-typen "RouteBased" och "SKU" VpnGw1 ".</span><span class="sxs-lookup"><span data-stu-id="b5074-123">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "VpnGw1."</span></span> <span data-ttu-id="b5074-124">VPN-inställningar kommer att anges på gateway som VpnProtocol angiven som Ikev2, VpnClientAddressPool som "201.169.0.0/16", VpnClientRootCertificate angett en: clientRootCertName och anpassad IPsec-princip för VPN som överförts i objekt: $vpnclientipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="b5074-124">Vpn settings will be set on Gateway such as VpnProtocol set as Ikev2, VpnClientAddressPool as "201.169.0.0/16", VpnClientRootCertificate set as passed one: clientRootCertName and custom vpn ipsec policy passed in object:$vpnclientipsecpolicy</span></span>  

## <span data-ttu-id="b5074-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b5074-125">PARAMETERS</span></span>

### <span data-ttu-id="b5074-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5074-126">-AsJob</span></span>
<span data-ttu-id="b5074-127">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b5074-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b5074-128">-ASN</span><span class="sxs-lookup"><span data-stu-id="b5074-128">-Asn</span></span>

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

### <span data-ttu-id="b5074-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5074-129">-DefaultProfile</span></span>
<span data-ttu-id="b5074-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b5074-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5074-131">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="b5074-131">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="b5074-132">Aktiverar den aktiva aktiva funktionen.</span><span class="sxs-lookup"><span data-stu-id="b5074-132">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="b5074-133">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="b5074-133">-EnableBgp</span></span>

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

### <span data-ttu-id="b5074-134">-Force</span><span class="sxs-lookup"><span data-stu-id="b5074-134">-Force</span></span>
<span data-ttu-id="b5074-135">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="b5074-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b5074-136">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="b5074-136">-GatewayDefaultSite</span></span>

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

### <span data-ttu-id="b5074-137">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="b5074-137">-GatewaySku</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5074-138">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="b5074-138">-GatewayType</span></span>

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

### <span data-ttu-id="b5074-139">-IpConfigurations</span><span class="sxs-lookup"><span data-stu-id="b5074-139">-IpConfigurations</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5074-140">-Plats</span><span class="sxs-lookup"><span data-stu-id="b5074-140">-Location</span></span>

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

### <span data-ttu-id="b5074-141">-Namn</span><span class="sxs-lookup"><span data-stu-id="b5074-141">-Name</span></span>

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

### <span data-ttu-id="b5074-142">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="b5074-142">-PeerWeight</span></span>

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

### <span data-ttu-id="b5074-143">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="b5074-143">-RadiusServerAddress</span></span>
<span data-ttu-id="b5074-144">P2S externa RADIUS-serveradress.</span><span class="sxs-lookup"><span data-stu-id="b5074-144">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="b5074-145">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="b5074-145">-RadiusServerSecret</span></span>
<span data-ttu-id="b5074-146">P2S externa RADIUS-server hemlighet.</span><span class="sxs-lookup"><span data-stu-id="b5074-146">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="b5074-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5074-147">-ResourceGroupName</span></span>

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

### <span data-ttu-id="b5074-148">-Tagg</span><span class="sxs-lookup"><span data-stu-id="b5074-148">-Tag</span></span>
<span data-ttu-id="b5074-149">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="b5074-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b5074-150">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="b5074-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b5074-151">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="b5074-151">-VpnClientAddressPool</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5074-152">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="b5074-152">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="b5074-153">En lista över IPSec-principer för tunnel protokoll för P2S VPN-klienter.</span><span class="sxs-lookup"><span data-stu-id="b5074-153">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5074-154">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="b5074-154">-VpnClientProtocol</span></span>
<span data-ttu-id="b5074-155">Listan med tunnel protokoll för P2S VPN-klienter</span><span class="sxs-lookup"><span data-stu-id="b5074-155">The list of P2S VPN client tunneling protocols</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:
Accepted values: SSTP, IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5074-156">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="b5074-156">-VpnClientRevokedCertificates</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5074-157">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="b5074-157">-VpnClientRootCertificates</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5074-158">-VpnType</span><span class="sxs-lookup"><span data-stu-id="b5074-158">-VpnType</span></span>

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

### <span data-ttu-id="b5074-159">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b5074-159">-Confirm</span></span>
<span data-ttu-id="b5074-160">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b5074-160">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5074-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5074-161">-WhatIf</span></span>
<span data-ttu-id="b5074-162">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b5074-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5074-163">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b5074-163">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5074-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5074-164">CommonParameters</span></span>
<span data-ttu-id="b5074-165">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5074-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5074-166">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5074-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5074-167">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b5074-167">INPUTS</span></span>

### <span data-ttu-id="b5074-168">System. String</span><span class="sxs-lookup"><span data-stu-id="b5074-168">System.String</span></span>

### <span data-ttu-id="b5074-169">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSVirtualNetworkGatewayIpConfiguration, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b5074-169">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="b5074-170">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b5074-170">System.Boolean</span></span>

### <span data-ttu-id="b5074-171">Microsoft. Azure. commands. Networks. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b5074-171">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="b5074-172">System. Collections. Generic. list ' 1 [[system. String, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b5074-172">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="b5074-173">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSVpnClientRootCertificate, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b5074-173">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="b5074-174">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSVpnClientRevokedCertificate, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b5074-174">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="b5074-175">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSIpsecPolicy, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b5074-175">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="b5074-176">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="b5074-176">System.UInt32</span></span>

### <span data-ttu-id="b5074-177">System. Int32</span><span class="sxs-lookup"><span data-stu-id="b5074-177">System.Int32</span></span>

### <span data-ttu-id="b5074-178">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="b5074-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b5074-179">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="b5074-179">System.Security.SecureString</span></span>

## <span data-ttu-id="b5074-180">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b5074-180">OUTPUTS</span></span>

### <span data-ttu-id="b5074-181">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b5074-181">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="b5074-182">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b5074-182">NOTES</span></span>

## <span data-ttu-id="b5074-183">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b5074-183">RELATED LINKS</span></span>

[<span data-ttu-id="b5074-184">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b5074-184">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="b5074-185">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b5074-185">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="b5074-186">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b5074-186">Reset-AzureRmVirtualNetworkGateway</span></span>](./Reset-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="b5074-187">Ändra storlek – AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b5074-187">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="b5074-188">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b5074-188">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)
