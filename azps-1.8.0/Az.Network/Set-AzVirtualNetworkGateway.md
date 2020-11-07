---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
ms.openlocfilehash: 6576cedfa49d2ba2215d72b7f31ea85288f5cbda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747688"
---
# <span data-ttu-id="fb451-101">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fb451-101">Set-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="fb451-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fb451-102">SYNOPSIS</span></span>
<span data-ttu-id="fb451-103">Uppdaterar en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="fb451-103">Updates a virtual network gateway.</span></span>

## <span data-ttu-id="fb451-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fb451-104">SYNTAX</span></span>

### <span data-ttu-id="fb451-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="fb451-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb451-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="fb451-106">RadiusServerConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb451-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fb451-107">DESCRIPTION</span></span>
<span data-ttu-id="fb451-108">Cmdleten **set-AzVirtualNetworkGateway** uppdaterar en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="fb451-108">The **Set-AzVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="fb451-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fb451-109">EXAMPLES</span></span>

### <span data-ttu-id="fb451-110">Exempel 1: uppdatera ASN för en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="fb451-110">Example 1: Update a virtual network gateway's ASN</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="fb451-111">Det första kommandot får en virtuell nätverksgateway som heter Gateway01 som tillhör resurs gruppens ResourceGroup001 och lagrar den till variabeln $Gateway det andra kommandot uppdaterar den virtuella nätverksgateway som lagras i variabeln $Gateway.</span><span class="sxs-lookup"><span data-stu-id="fb451-111">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="fb451-112">Kommandot anger också ASN till 1337.</span><span class="sxs-lookup"><span data-stu-id="fb451-112">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="fb451-113">Exempel 2: lägga till IPsec-princip till en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="fb451-113">Example 2: Add IPsec policy to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="fb451-114">Det första kommandot får en virtuell nätverksgateway som heter Gateway01 som tillhör resurs gruppens ResourceGroup001 och lagrar det i variabeln $Gateway det andra kommandot skapar IPsec-principobjektet som enligt angivna IPsec-parametrar.</span><span class="sxs-lookup"><span data-stu-id="fb451-114">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="fb451-115">Det tredje kommandot uppdaterar den virtuella Nätverksgatewayen som lagras i variabeln $Gateway.</span><span class="sxs-lookup"><span data-stu-id="fb451-115">The third command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="fb451-116">Kommandot anger även den anpassade IPSec-principen för VPN som anges i $vpnclientipsecpolicy-objekt på virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="fb451-116">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

## <span data-ttu-id="fb451-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fb451-117">PARAMETERS</span></span>

### <span data-ttu-id="fb451-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb451-118">-AsJob</span></span>
<span data-ttu-id="fb451-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="fb451-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb451-120">-ASN</span><span class="sxs-lookup"><span data-stu-id="fb451-120">-Asn</span></span>
<span data-ttu-id="fb451-121">Anger det autonoma system numret för virtuell nätverksgateway (ASN) som används för att konfigurera BGP-sessioner (Border Gateway Protocol) i IPsec-tunnlar.</span><span class="sxs-lookup"><span data-stu-id="fb451-121">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

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

### <span data-ttu-id="fb451-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb451-122">-DefaultProfile</span></span>
<span data-ttu-id="fb451-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fb451-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb451-124">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="fb451-124">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="fb451-125">Inaktiverar den aktiva aktiva funktionen.</span><span class="sxs-lookup"><span data-stu-id="fb451-125">Disables the active-active feature.</span></span>

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

### <span data-ttu-id="fb451-126">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="fb451-126">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="fb451-127">Aktiverar den aktiva aktiva funktionen.</span><span class="sxs-lookup"><span data-stu-id="fb451-127">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="fb451-128">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="fb451-128">-GatewayDefaultSite</span></span>
<span data-ttu-id="fb451-129">Anger standard webbplatsen som ska användas för Tvingad tunnel trafik.</span><span class="sxs-lookup"><span data-stu-id="fb451-129">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="fb451-130">Om en standard webbplats anges routas all Internet trafik från gatewayens virtuella privata nätverk (VPN) till den webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="fb451-130">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

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

### <span data-ttu-id="fb451-131">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="fb451-131">-GatewaySku</span></span>
<span data-ttu-id="fb451-132">Anger lagerhållnings enhet (SKU) för den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="fb451-132">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="fb451-133">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="fb451-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fb451-134">Basisk</span><span class="sxs-lookup"><span data-stu-id="fb451-134">Basic</span></span>
- <span data-ttu-id="fb451-135">Standar</span><span class="sxs-lookup"><span data-stu-id="fb451-135">Standard</span></span>
- <span data-ttu-id="fb451-136">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="fb451-136">HighPerformance</span></span>
- <span data-ttu-id="fb451-137">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="fb451-137">VpnGw1</span></span>
- <span data-ttu-id="fb451-138">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="fb451-138">VpnGw2</span></span>
- <span data-ttu-id="fb451-139">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="fb451-139">VpnGw3</span></span>
- <span data-ttu-id="fb451-140">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="fb451-140">VpnGw1AZ</span></span>
- <span data-ttu-id="fb451-141">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="fb451-141">VpnGw2AZ</span></span>
- <span data-ttu-id="fb451-142">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="fb451-142">VpnGw3AZ</span></span>
- <span data-ttu-id="fb451-143">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="fb451-143">ErGw1AZ</span></span>
- <span data-ttu-id="fb451-144">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="fb451-144">ErGw2AZ</span></span>
- <span data-ttu-id="fb451-145">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="fb451-145">ErGw3AZ</span></span>

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

### <span data-ttu-id="fb451-146">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="fb451-146">-PeerWeight</span></span>
<span data-ttu-id="fb451-147">Anger vikten som har lagts till för vägar som upptäckts via BGP från denna virtuella nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="fb451-147">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="fb451-148">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="fb451-148">-RadiusServerAddress</span></span>
<span data-ttu-id="fb451-149">P2S externa RADIUS-serveradress.</span><span class="sxs-lookup"><span data-stu-id="fb451-149">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="fb451-150">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="fb451-150">-RadiusServerSecret</span></span>
<span data-ttu-id="fb451-151">P2S externa RADIUS-server hemlighet.</span><span class="sxs-lookup"><span data-stu-id="fb451-151">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="fb451-152">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fb451-152">-VirtualNetworkGateway</span></span>
<span data-ttu-id="fb451-153">Anger det virtuella nätverkets gateway-objekt som ska ändras från av.</span><span class="sxs-lookup"><span data-stu-id="fb451-153">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="fb451-154">Du kan använda Get-AzVirtualNetworkGateway cmdlet för att hämta det virtuella nätverkets gateway-objekt.</span><span class="sxs-lookup"><span data-stu-id="fb451-154">You can use the Get-AzVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

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

### <span data-ttu-id="fb451-155">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="fb451-155">-VpnClientAddressPool</span></span>
<span data-ttu-id="fb451-156">Anger det adress utrymme som denna cmdlet använder för att tilldela IP-adresser för VPN-klienter från.</span><span class="sxs-lookup"><span data-stu-id="fb451-156">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="fb451-157">Detta ska inte överlappa virtuella nätverks-eller lokala områden.</span><span class="sxs-lookup"><span data-stu-id="fb451-157">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="fb451-158">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="fb451-158">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="fb451-159">En lista över IPSec-principer för tunnel protokoll för P2S VPN-klienter.</span><span class="sxs-lookup"><span data-stu-id="fb451-159">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="fb451-160">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="fb451-160">-VpnClientProtocol</span></span>
<span data-ttu-id="fb451-161">En lista över protokoll för P2S VPN-klienter</span><span class="sxs-lookup"><span data-stu-id="fb451-161">A list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="fb451-162">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="fb451-162">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="fb451-163">Anger en lista över återkallade VPN-klient certifikat.</span><span class="sxs-lookup"><span data-stu-id="fb451-163">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="fb451-164">En VPN-klient som visar ett certifikat som matchar något av dessa tas bort.</span><span class="sxs-lookup"><span data-stu-id="fb451-164">A VPN client presenting a certificate that matches one of these is removed.</span></span>

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

### <span data-ttu-id="fb451-165">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="fb451-165">-VpnClientRootCertificates</span></span>
<span data-ttu-id="fb451-166">Anger en lista över de VPN-klient rot certifikat som ska användas för VPN-klientautentisering.</span><span class="sxs-lookup"><span data-stu-id="fb451-166">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="fb451-167">Anslutning av VPN-klienter måste presentera certifikat som genererats från ett av dessa rot certifikat.</span><span class="sxs-lookup"><span data-stu-id="fb451-167">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="fb451-168">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fb451-168">-Confirm</span></span>
<span data-ttu-id="fb451-169">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fb451-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb451-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb451-170">-WhatIf</span></span>
<span data-ttu-id="fb451-171">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fb451-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fb451-172">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fb451-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb451-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb451-173">CommonParameters</span></span>
<span data-ttu-id="fb451-174">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb451-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb451-175">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb451-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb451-176">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fb451-176">INPUTS</span></span>

### <span data-ttu-id="fb451-177">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fb451-177">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="fb451-178">System. String</span><span class="sxs-lookup"><span data-stu-id="fb451-178">System.String</span></span>

### <span data-ttu-id="fb451-179">Microsoft. Azure. commands. Networks. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fb451-179">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="fb451-180">System. string []</span><span class="sxs-lookup"><span data-stu-id="fb451-180">System.String[]</span></span>

### <span data-ttu-id="fb451-181">Microsoft. Azure. commands. Network. Models. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="fb451-181">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="fb451-182">Microsoft. Azure. commands. Network. Models. PSVpnClientRevokedCertificate []</span><span class="sxs-lookup"><span data-stu-id="fb451-182">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="fb451-183">Microsoft. Azure. commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="fb451-183">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="fb451-184">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="fb451-184">System.UInt32</span></span>

### <span data-ttu-id="fb451-185">System. Int32</span><span class="sxs-lookup"><span data-stu-id="fb451-185">System.Int32</span></span>

### <span data-ttu-id="fb451-186">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="fb451-186">System.Security.SecureString</span></span>

## <span data-ttu-id="fb451-187">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fb451-187">OUTPUTS</span></span>

### <span data-ttu-id="fb451-188">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fb451-188">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="fb451-189">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fb451-189">NOTES</span></span>
* <span data-ttu-id="fb451-190">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="fb451-190">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="fb451-191">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fb451-191">RELATED LINKS</span></span>

[<span data-ttu-id="fb451-192">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fb451-192">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="fb451-193">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fb451-193">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="fb451-194">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fb451-194">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="fb451-195">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fb451-195">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="fb451-196">Ändra storlek – AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fb451-196">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)
