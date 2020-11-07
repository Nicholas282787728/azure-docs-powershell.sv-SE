---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworkgateway
schema: 2.0.0
ms.openlocfilehash: a2aacf68d20e495856ffd6d5e868b82bed8d34ef
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929709"
---
# <span data-ttu-id="7a2a7-101">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7a2a7-101">New-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="7a2a7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7a2a7-102">SYNOPSIS</span></span>
<span data-ttu-id="7a2a7-103">Skapar en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="7a2a7-103">Creates a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a2a7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7a2a7-104">SYNTAX</span></span>

### <span data-ttu-id="7a2a7-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="7a2a7-105">Default (Default)</span></span>
```
New-AzureRmVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]>]
 [-GatewayType <String>] [-VpnType <String>] [-EnableBgp <Boolean>] [-EnableActiveActiveFeature]
 [-GatewaySku <String>] [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a2a7-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="7a2a7-106">RadiusServerConfiguration</span></span>
```
New-AzureRmVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]>]
 [-GatewayType <String>] [-VpnType <String>] [-EnableBgp <Boolean>] [-EnableActiveActiveFeature]
 [-GatewaySku <String>] [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7a2a7-107">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7a2a7-107">SetByResource</span></span>
```
New-AzureRmVirtualNetworkGateway
 [-IpConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]>]
 [-GatewayType <String>] [-VpnType <String>] [-EnableBgp <Boolean>] [-EnableActiveActiveFeature]
 [-GatewaySku <String>] [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a2a7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7a2a7-108">DESCRIPTION</span></span>
<span data-ttu-id="7a2a7-109">Den virtuella Nätverksgatewayen är det objekt som representerar din gateway i Azure.</span><span class="sxs-lookup"><span data-stu-id="7a2a7-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="7a2a7-110">Cmdleten **New-AzureRmVirtualNetworkGateway** skapar ett objekt för din gateway i Azure baserat på namnet, resurs gruppens namn, plats och IP-konfiguration samt Gateway-typen och om VPN, VPN-typen.</span><span class="sxs-lookup"><span data-stu-id="7a2a7-110">The **New-AzureRmVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="7a2a7-111">Du kan också ge Gateway SKU.</span><span class="sxs-lookup"><span data-stu-id="7a2a7-111">You can also name the Gateway SKU.</span></span>

<span data-ttu-id="7a2a7-112">Om den här gatewayen används för punkt-till-plats-anslutningar måste du även ta med den VPN-adresspool som du vill tilldela adresser för att ansluta klienter och det VPN-klient rot certifikat som används för att autentisera VPN-klienter som ansluter till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="7a2a7-112">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>

<span data-ttu-id="7a2a7-113">Du kan också välja att inkludera andra funktioner som BGP och Active-Active.</span><span class="sxs-lookup"><span data-stu-id="7a2a7-113">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="7a2a7-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7a2a7-114">EXAMPLES</span></span>

### <span data-ttu-id="7a2a7-115">1: skapa en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="7a2a7-115">1: Create a Virtual Network Gateway</span></span>
```
New-AzureRmResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzureRMVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzureRMPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzureRmVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzureRMVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzureRmVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic"
```

<span data-ttu-id="7a2a7-116">Ovanstående skapar en resurs grupp, efterfrågar en offentlig IP-adress, skapar ett virtuellt nätverk och undernät och skapar en virtuell nätverksgateway i Azure.</span><span class="sxs-lookup"><span data-stu-id="7a2a7-116">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="7a2a7-117">Gatewayen kallas "myNGW" i resurs gruppen "VNet-Gateway" i platsen "UK West", med tidigare skapade IP-konfigurationer sparade i variabeln "ngwIPConfig", Gateway-typen för "VPN", VPN-typen "RouteBased" och "Basic"-SKU: n.</span><span class="sxs-lookup"><span data-stu-id="7a2a7-117">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="7a2a7-118">2: skapa en virtuell nätverksgateway med extern RADIUS-konfiguration</span><span class="sxs-lookup"><span data-stu-id="7a2a7-118">2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
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

<span data-ttu-id="7a2a7-119">Ovanstående skapar en resurs grupp, efterfrågar en offentlig IP-adress, skapar ett virtuellt nätverk och undernät och skapar en virtuell nätverksgateway i Azure.</span><span class="sxs-lookup"><span data-stu-id="7a2a7-119">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="7a2a7-120">Gatewayen kallas "myNGW" i resurs gruppen "VNet-Gateway" i platsen "UK West", med tidigare skapade IP-konfigurationer sparade i variabeln "ngwIPConfig", Gateway-typen för "VPN", VPN-typen "RouteBased" och "Basic"-SKU: n.</span><span class="sxs-lookup"><span data-stu-id="7a2a7-120">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="7a2a7-121">Dessutom läggs en extern RADIUS-server till med adressen "TestRadiusServer"</span><span class="sxs-lookup"><span data-stu-id="7a2a7-121">It also adds an external radius server with address "TestRadiusServer"</span></span>

## <span data-ttu-id="7a2a7-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7a2a7-122">PARAMETERS</span></span>

### <span data-ttu-id="7a2a7-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a2a7-123">-AsJob</span></span>
<span data-ttu-id="7a2a7-124">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="7a2a7-124">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a2a7-125">-ASN</span><span class="sxs-lookup"><span data-stu-id="7a2a7-125">-Asn</span></span>
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a2a7-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a2a7-126">-DefaultProfile</span></span>
<span data-ttu-id="7a2a7-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7a2a7-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a2a7-128">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="7a2a7-128">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="7a2a7-129">Aktiverar den aktiva aktiva funktionen.</span><span class="sxs-lookup"><span data-stu-id="7a2a7-129">Enables the active-active feature.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a2a7-130">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="7a2a7-130">-EnableBgp</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a2a7-131">-Force</span><span class="sxs-lookup"><span data-stu-id="7a2a7-131">-Force</span></span>
<span data-ttu-id="7a2a7-132">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="7a2a7-132">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a2a7-133">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="7a2a7-133">-GatewayDefaultSite</span></span>
```yaml
Type: PSLocalNetworkGateway
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a2a7-134">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="7a2a7-134">-GatewaySku</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a2a7-135">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="7a2a7-135">-GatewayType</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Vpn, ExpressRoute

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a2a7-136">-IpConfigurations</span><span class="sxs-lookup"><span data-stu-id="7a2a7-136">-IpConfigurations</span></span>
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

### <span data-ttu-id="7a2a7-137">-Plats</span><span class="sxs-lookup"><span data-stu-id="7a2a7-137">-Location</span></span>
```yaml
Type: String
Parameter Sets: Default, RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a2a7-138">-Namn</span><span class="sxs-lookup"><span data-stu-id="7a2a7-138">-Name</span></span>
```yaml
Type: String
Parameter Sets: Default, RadiusServerConfiguration
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a2a7-139">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="7a2a7-139">-PeerWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a2a7-140">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="7a2a7-140">-RadiusServerAddress</span></span>
<span data-ttu-id="7a2a7-141">P2S externa RADIUS-serveradress.</span><span class="sxs-lookup"><span data-stu-id="7a2a7-141">P2S External Radius server address.</span></span>
```yaml
Type: String
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a2a7-142">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="7a2a7-142">-RadiusServerSecret</span></span>
<span data-ttu-id="7a2a7-143">P2S externa RADIUS-server hemlighet.</span><span class="sxs-lookup"><span data-stu-id="7a2a7-143">P2S External Radius server secret.</span></span>
```yaml
Type: SecureString
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a2a7-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a2a7-144">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: Default, RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a2a7-145">-Tagg</span><span class="sxs-lookup"><span data-stu-id="7a2a7-145">-Tag</span></span>
<span data-ttu-id="7a2a7-146">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="7a2a7-146">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7a2a7-147">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="7a2a7-147">For example:</span></span>

<span data-ttu-id="7a2a7-148">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="7a2a7-148">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a2a7-149">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="7a2a7-149">-VpnClientAddressPool</span></span>
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

### <span data-ttu-id="7a2a7-150">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="7a2a7-150">-VpnClientProtocol</span></span>
<span data-ttu-id="7a2a7-151">Listan med tunnel protokoll för P2S VPN-klienter</span><span class="sxs-lookup"><span data-stu-id="7a2a7-151">The list of P2S VPN client tunneling protocols</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 
Accepted values: SSTP, IkeV2

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a2a7-152">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="7a2a7-152">-VpnClientRevokedCertificates</span></span>
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

### <span data-ttu-id="7a2a7-153">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="7a2a7-153">-VpnClientRootCertificates</span></span>
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

### <span data-ttu-id="7a2a7-154">-VpnType</span><span class="sxs-lookup"><span data-stu-id="7a2a7-154">-VpnType</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PolicyBased, RouteBased

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a2a7-155">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7a2a7-155">-Confirm</span></span>
<span data-ttu-id="7a2a7-156">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7a2a7-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a2a7-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a2a7-157">-WhatIf</span></span>
<span data-ttu-id="7a2a7-158">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7a2a7-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a2a7-159">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7a2a7-159">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a2a7-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a2a7-160">CommonParameters</span></span>
<span data-ttu-id="7a2a7-161">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a2a7-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a2a7-162">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a2a7-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a2a7-163">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7a2a7-163">INPUTS</span></span>

## <span data-ttu-id="7a2a7-164">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7a2a7-164">OUTPUTS</span></span>

### <span data-ttu-id="7a2a7-165">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7a2a7-165">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="7a2a7-166">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7a2a7-166">NOTES</span></span>

## <span data-ttu-id="7a2a7-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7a2a7-167">RELATED LINKS</span></span>

[<span data-ttu-id="7a2a7-168">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7a2a7-168">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="7a2a7-169">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7a2a7-169">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="7a2a7-170">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7a2a7-170">Reset-AzureRmVirtualNetworkGateway</span></span>](./Reset-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="7a2a7-171">Ändra storlek – AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7a2a7-171">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="7a2a7-172">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7a2a7-172">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)
