---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 1884dd461c0433c4f6a68bf906f56653ca960e27
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580047"
---
# <span data-ttu-id="dad3a-101">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="dad3a-101">Set-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="dad3a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dad3a-102">SYNOPSIS</span></span>
<span data-ttu-id="dad3a-103">Uppdaterar en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="dad3a-103">Updates a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dad3a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dad3a-104">SYNTAX</span></span>

### <span data-ttu-id="dad3a-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="dad3a-105">Default (Default)</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-VpnClientIpsecPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dad3a-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="dad3a-106">RadiusServerConfiguration</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-VpnClientIpsecPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dad3a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dad3a-107">DESCRIPTION</span></span>
<span data-ttu-id="dad3a-108">Cmdleten **set-AzureRmVirtualNetworkGateway** uppdaterar en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="dad3a-108">The **Set-AzureRmVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="dad3a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dad3a-109">EXAMPLES</span></span>

### <span data-ttu-id="dad3a-110">Exempel 1: Ange mål tillstånd för en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="dad3a-110">Example 1: Set the goal state a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="dad3a-111">Det första kommandot får en virtuell nätverksgateway som heter Gateway01 som tillhör resurs gruppens ResourceGroup001 och lagrar det i variabeln $Gateway det andra kommandot ställer in mål tillståndet för den virtuella Nätverksgatewayen som lagras i variabeln $Gateway.</span><span class="sxs-lookup"><span data-stu-id="dad3a-111">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command sets the goal state for the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="dad3a-112">Kommandot anger också ASN till 1337.</span><span class="sxs-lookup"><span data-stu-id="dad3a-112">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="dad3a-113">Exempel 2: Ange mål tillstånd för en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="dad3a-113">Example 2: Set the goal state a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzureRmVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="dad3a-114">Det första kommandot får en virtuell nätverksgateway som heter Gateway01 som tillhör resurs gruppens ResourceGroup001 och lagrar det i variabeln $Gateway det andra kommandot skapar IPsec-principobjektet som enligt angivna IPsec-parametrar.</span><span class="sxs-lookup"><span data-stu-id="dad3a-114">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="dad3a-115">Det tredje kommandot anger mål tillståndet för den virtuella Nätverksgatewayen som lagras i variabeln $Gateway.</span><span class="sxs-lookup"><span data-stu-id="dad3a-115">The third command sets the goal state for the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="dad3a-116">Kommandot anger även den anpassade IPSec-principen för VPN som anges i $vpnclientipsecpolicy-objekt på virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="dad3a-116">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

## <span data-ttu-id="dad3a-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dad3a-117">PARAMETERS</span></span>

### <span data-ttu-id="dad3a-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dad3a-118">-AsJob</span></span>
<span data-ttu-id="dad3a-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="dad3a-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dad3a-120">-ASN</span><span class="sxs-lookup"><span data-stu-id="dad3a-120">-Asn</span></span>
<span data-ttu-id="dad3a-121">Anger det autonoma system numret för virtuell nätverksgateway (ASN) som används för att konfigurera BGP-sessioner (Border Gateway Protocol) i IPsec-tunnlar.</span><span class="sxs-lookup"><span data-stu-id="dad3a-121">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

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

### <span data-ttu-id="dad3a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dad3a-122">-DefaultProfile</span></span>
<span data-ttu-id="dad3a-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dad3a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dad3a-124">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="dad3a-124">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="dad3a-125">Inaktiverar den aktiva aktiva funktionen.</span><span class="sxs-lookup"><span data-stu-id="dad3a-125">Disables the active-active feature.</span></span>

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

### <span data-ttu-id="dad3a-126">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="dad3a-126">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="dad3a-127">Aktiverar den aktiva aktiva funktionen.</span><span class="sxs-lookup"><span data-stu-id="dad3a-127">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="dad3a-128">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="dad3a-128">-GatewayDefaultSite</span></span>
<span data-ttu-id="dad3a-129">Anger standard webbplatsen som ska användas för Tvingad tunnel trafik.</span><span class="sxs-lookup"><span data-stu-id="dad3a-129">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="dad3a-130">Om en standard webbplats anges routas all Internet trafik från gatewayens virtuella privata nätverk (VPN) till den webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="dad3a-130">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

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

### <span data-ttu-id="dad3a-131">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="dad3a-131">-GatewaySku</span></span>
<span data-ttu-id="dad3a-132">Anger lagerhållnings enhet (SKU) för den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="dad3a-132">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="dad3a-133">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="dad3a-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dad3a-134">Basisk</span><span class="sxs-lookup"><span data-stu-id="dad3a-134">Basic</span></span>
- <span data-ttu-id="dad3a-135">Standar</span><span class="sxs-lookup"><span data-stu-id="dad3a-135">Standard</span></span>
- <span data-ttu-id="dad3a-136">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="dad3a-136">HighPerformance</span></span>
- <span data-ttu-id="dad3a-137">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="dad3a-137">VpnGw1</span></span>
- <span data-ttu-id="dad3a-138">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="dad3a-138">VpnGw2</span></span>
- <span data-ttu-id="dad3a-139">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="dad3a-139">VpnGw3</span></span>
- <span data-ttu-id="dad3a-140">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="dad3a-140">VpnGw1AZ</span></span>
- <span data-ttu-id="dad3a-141">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="dad3a-141">VpnGw2AZ</span></span>
- <span data-ttu-id="dad3a-142">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="dad3a-142">VpnGw3AZ</span></span>
- <span data-ttu-id="dad3a-143">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="dad3a-143">ErGw1AZ</span></span>
- <span data-ttu-id="dad3a-144">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="dad3a-144">ErGw2AZ</span></span>
- <span data-ttu-id="dad3a-145">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="dad3a-145">ErGw3AZ</span></span>

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

### <span data-ttu-id="dad3a-146">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="dad3a-146">-PeerWeight</span></span>
<span data-ttu-id="dad3a-147">Anger vikten som har lagts till för vägar som upptäckts via BGP från denna virtuella nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="dad3a-147">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="dad3a-148">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="dad3a-148">-RadiusServerAddress</span></span>
<span data-ttu-id="dad3a-149">P2S externa RADIUS-serveradress.</span><span class="sxs-lookup"><span data-stu-id="dad3a-149">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="dad3a-150">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="dad3a-150">-RadiusServerSecret</span></span>
<span data-ttu-id="dad3a-151">P2S externa RADIUS-server hemlighet.</span><span class="sxs-lookup"><span data-stu-id="dad3a-151">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="dad3a-152">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="dad3a-152">-VirtualNetworkGateway</span></span>
<span data-ttu-id="dad3a-153">Anger det virtuella nätverkets gateway-objekt som ska ändras från av.</span><span class="sxs-lookup"><span data-stu-id="dad3a-153">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="dad3a-154">Du kan använda Get-AzureRmVirtualNetworkGateway cmdlet för att hämta det virtuella nätverkets gateway-objekt.</span><span class="sxs-lookup"><span data-stu-id="dad3a-154">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

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

### <span data-ttu-id="dad3a-155">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="dad3a-155">-VpnClientAddressPool</span></span>
<span data-ttu-id="dad3a-156">Anger det adress utrymme som denna cmdlet använder för att tilldela IP-adresser för VPN-klienter från.</span><span class="sxs-lookup"><span data-stu-id="dad3a-156">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="dad3a-157">Detta ska inte överlappa virtuella nätverks-eller lokala områden.</span><span class="sxs-lookup"><span data-stu-id="dad3a-157">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="dad3a-158">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="dad3a-158">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="dad3a-159">En lista över IPSec-principer för tunnel protokoll för P2S VPN-klienter.</span><span class="sxs-lookup"><span data-stu-id="dad3a-159">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="dad3a-160">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="dad3a-160">-VpnClientProtocol</span></span>
<span data-ttu-id="dad3a-161">En lista över protokoll för P2S VPN-klienter</span><span class="sxs-lookup"><span data-stu-id="dad3a-161">A list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="dad3a-162">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="dad3a-162">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="dad3a-163">Anger en lista över återkallade VPN-klient certifikat.</span><span class="sxs-lookup"><span data-stu-id="dad3a-163">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="dad3a-164">En VPN-klient som visar ett certifikat som matchar något av dessa tas bort.</span><span class="sxs-lookup"><span data-stu-id="dad3a-164">A VPN client presenting a certificate that matches one of these is removed.</span></span>

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

### <span data-ttu-id="dad3a-165">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="dad3a-165">-VpnClientRootCertificates</span></span>
<span data-ttu-id="dad3a-166">Anger en lista över de VPN-klient rot certifikat som ska användas för VPN-klientautentisering.</span><span class="sxs-lookup"><span data-stu-id="dad3a-166">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="dad3a-167">Anslutning av VPN-klienter måste presentera certifikat som genererats från ett av dessa rot certifikat.</span><span class="sxs-lookup"><span data-stu-id="dad3a-167">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="dad3a-168">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dad3a-168">-Confirm</span></span>
<span data-ttu-id="dad3a-169">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dad3a-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dad3a-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dad3a-170">-WhatIf</span></span>
<span data-ttu-id="dad3a-171">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dad3a-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dad3a-172">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dad3a-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dad3a-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dad3a-173">CommonParameters</span></span>
<span data-ttu-id="dad3a-174">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dad3a-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dad3a-175">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dad3a-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dad3a-176">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dad3a-176">INPUTS</span></span>

### <span data-ttu-id="dad3a-177">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="dad3a-177">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="dad3a-178">Parametrar: VirtualNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="dad3a-178">Parameters: VirtualNetworkGateway (ByValue)</span></span>

### <span data-ttu-id="dad3a-179">System. String</span><span class="sxs-lookup"><span data-stu-id="dad3a-179">System.String</span></span>

### <span data-ttu-id="dad3a-180">Microsoft. Azure. commands. Networks. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="dad3a-180">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="dad3a-181">System. Collections. Generic. list ' 1 [[system. String, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="dad3a-181">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="dad3a-182">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSVpnClientRootCertificate, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="dad3a-182">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="dad3a-183">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSVpnClientRevokedCertificate, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="dad3a-183">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="dad3a-184">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSIpsecPolicy, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="dad3a-184">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="dad3a-185">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="dad3a-185">System.UInt32</span></span>

### <span data-ttu-id="dad3a-186">System. Int32</span><span class="sxs-lookup"><span data-stu-id="dad3a-186">System.Int32</span></span>

### <span data-ttu-id="dad3a-187">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="dad3a-187">System.Security.SecureString</span></span>

## <span data-ttu-id="dad3a-188">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dad3a-188">OUTPUTS</span></span>

### <span data-ttu-id="dad3a-189">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="dad3a-189">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="dad3a-190">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dad3a-190">NOTES</span></span>
* <span data-ttu-id="dad3a-191">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="dad3a-191">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="dad3a-192">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dad3a-192">RELATED LINKS</span></span>

[<span data-ttu-id="dad3a-193">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="dad3a-193">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="dad3a-194">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="dad3a-194">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="dad3a-195">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="dad3a-195">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="dad3a-196">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="dad3a-196">Reset-AzureRmVirtualNetworkGateway</span></span>](./Reset-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="dad3a-197">Ändra storlek – AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="dad3a-197">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)


