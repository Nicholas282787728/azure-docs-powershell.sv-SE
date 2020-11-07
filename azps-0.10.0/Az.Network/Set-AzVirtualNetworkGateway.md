---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
ms.openlocfilehash: 87840267cf85997da83af590664c473a61f74033
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924138"
---
# <span data-ttu-id="c2b20-101">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c2b20-101">Set-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="c2b20-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c2b20-102">SYNOPSIS</span></span>
<span data-ttu-id="c2b20-103">Uppdaterar en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="c2b20-103">Updates a virtual network gateway.</span></span>

## <span data-ttu-id="c2b20-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c2b20-104">SYNTAX</span></span>

### <span data-ttu-id="c2b20-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="c2b20-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2b20-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2b20-106">RadiusServerConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2b20-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c2b20-107">DESCRIPTION</span></span>
<span data-ttu-id="c2b20-108">Cmdleten **set-AzVirtualNetworkGateway** uppdaterar en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="c2b20-108">The **Set-AzVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="c2b20-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c2b20-109">EXAMPLES</span></span>

### <span data-ttu-id="c2b20-110">Exempel 1: Ange mål tillstånd för en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="c2b20-110">Example 1: Set the goal state a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="c2b20-111">Det första kommandot får en virtuell nätverksgateway som heter Gateway01 som tillhör resurs gruppen ResourceGroup001 och lagrar den på variabeln som heter $Gateway</span><span class="sxs-lookup"><span data-stu-id="c2b20-111">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway</span></span>

<span data-ttu-id="c2b20-112">Det andra kommandot ställer in mål tillståndet för den virtuella Nätverksgatewayen som lagras i variabeln $Gateway.</span><span class="sxs-lookup"><span data-stu-id="c2b20-112">The second command sets the goal state for the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="c2b20-113">Kommandot anger också ASN till 1337.</span><span class="sxs-lookup"><span data-stu-id="c2b20-113">The command also sets the ASN to 1337.</span></span>

## <span data-ttu-id="c2b20-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c2b20-114">PARAMETERS</span></span>

### <span data-ttu-id="c2b20-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c2b20-115">-AsJob</span></span>
<span data-ttu-id="c2b20-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="c2b20-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c2b20-117">-ASN</span><span class="sxs-lookup"><span data-stu-id="c2b20-117">-Asn</span></span>
<span data-ttu-id="c2b20-118">Anger det autonoma system numret för virtuell nätverksgateway (ASN) som används för att konfigurera BGP-sessioner (Border Gateway Protocol) i IPsec-tunnlar.</span><span class="sxs-lookup"><span data-stu-id="c2b20-118">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

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

### <span data-ttu-id="c2b20-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2b20-119">-DefaultProfile</span></span>
<span data-ttu-id="c2b20-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c2b20-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="c2b20-121">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="c2b20-121">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="c2b20-122">Inaktiverar den aktiva aktiva funktionen.</span><span class="sxs-lookup"><span data-stu-id="c2b20-122">Disables the active-active feature.</span></span>

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

### <span data-ttu-id="c2b20-123">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="c2b20-123">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="c2b20-124">Aktiverar den aktiva aktiva funktionen.</span><span class="sxs-lookup"><span data-stu-id="c2b20-124">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="c2b20-125">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="c2b20-125">-GatewayDefaultSite</span></span>
<span data-ttu-id="c2b20-126">Anger standard webbplatsen som ska användas för Tvingad tunnel trafik.</span><span class="sxs-lookup"><span data-stu-id="c2b20-126">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="c2b20-127">Om en standard webbplats anges routas all Internet trafik från gatewayens virtuella privata nätverk (VPN) till den webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="c2b20-127">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2b20-128">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="c2b20-128">-GatewaySku</span></span>
<span data-ttu-id="c2b20-129">Anger lagerhållnings enhet (SKU) för den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="c2b20-129">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="c2b20-130">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="c2b20-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c2b20-131">Basisk</span><span class="sxs-lookup"><span data-stu-id="c2b20-131">Basic</span></span>
- <span data-ttu-id="c2b20-132">Standar</span><span class="sxs-lookup"><span data-stu-id="c2b20-132">Standard</span></span>
- <span data-ttu-id="c2b20-133">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="c2b20-133">HighPerformance</span></span>
- <span data-ttu-id="c2b20-134">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="c2b20-134">VpnGw1</span></span>
- <span data-ttu-id="c2b20-135">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="c2b20-135">VpnGw2</span></span>
- <span data-ttu-id="c2b20-136">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="c2b20-136">VpnGw3</span></span>

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

### <span data-ttu-id="c2b20-137">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="c2b20-137">-PeerWeight</span></span>
<span data-ttu-id="c2b20-138">Anger vikten som har lagts till för vägar som upptäckts via BGP från denna virtuella nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="c2b20-138">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="c2b20-139">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="c2b20-139">-RadiusServerAddress</span></span>
<span data-ttu-id="c2b20-140">P2S externa RADIUS-serveradress.</span><span class="sxs-lookup"><span data-stu-id="c2b20-140">P2S External Radius server address.</span></span>
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

### <span data-ttu-id="c2b20-141">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="c2b20-141">-RadiusServerSecret</span></span>
<span data-ttu-id="c2b20-142">P2S externa RADIUS-server hemlighet.</span><span class="sxs-lookup"><span data-stu-id="c2b20-142">P2S External Radius server secret.</span></span>
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

### <span data-ttu-id="c2b20-143">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c2b20-143">-VirtualNetworkGateway</span></span>
<span data-ttu-id="c2b20-144">Anger det virtuella nätverkets gateway-objekt som ska ändras från av.</span><span class="sxs-lookup"><span data-stu-id="c2b20-144">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="c2b20-145">Du kan använda Get-AzVirtualNetworkGateway cmdlet för att hämta det virtuella nätverkets gateway-objekt.</span><span class="sxs-lookup"><span data-stu-id="c2b20-145">You can use the Get-AzVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2b20-146">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="c2b20-146">-VpnClientAddressPool</span></span>
<span data-ttu-id="c2b20-147">Anger det adress utrymme som denna cmdlet använder för att tilldela IP-adresser för VPN-klienter från.</span><span class="sxs-lookup"><span data-stu-id="c2b20-147">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="c2b20-148">Detta ska inte överlappa virtuella nätverks-eller lokala områden.</span><span class="sxs-lookup"><span data-stu-id="c2b20-148">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="c2b20-149">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="c2b20-149">-VpnClientProtocol</span></span>
<span data-ttu-id="c2b20-150">En lista över protokoll för P2S VPN-klienter</span><span class="sxs-lookup"><span data-stu-id="c2b20-150">A list of P2S VPN client tunneling protocols</span></span>
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

### <span data-ttu-id="c2b20-151">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="c2b20-151">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="c2b20-152">Anger en lista över återkallade VPN-klient certifikat.</span><span class="sxs-lookup"><span data-stu-id="c2b20-152">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="c2b20-153">En VPN-klient som visar ett certifikat som matchar något av dessa tas bort.</span><span class="sxs-lookup"><span data-stu-id="c2b20-153">A VPN client presenting a certificate that matches one of these is removed.</span></span>

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

### <span data-ttu-id="c2b20-154">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="c2b20-154">-VpnClientRootCertificates</span></span>
<span data-ttu-id="c2b20-155">Anger en lista över de VPN-klient rot certifikat som ska användas för VPN-klientautentisering.</span><span class="sxs-lookup"><span data-stu-id="c2b20-155">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="c2b20-156">Anslutning av VPN-klienter måste presentera certifikat som genererats från ett av dessa rot certifikat.</span><span class="sxs-lookup"><span data-stu-id="c2b20-156">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="c2b20-157">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c2b20-157">-Confirm</span></span>
<span data-ttu-id="c2b20-158">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c2b20-158">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b20-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2b20-159">-WhatIf</span></span>
<span data-ttu-id="c2b20-160">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c2b20-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c2b20-161">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c2b20-161">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b20-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2b20-162">CommonParameters</span></span>
<span data-ttu-id="c2b20-163">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2b20-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2b20-164">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2b20-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2b20-165">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c2b20-165">INPUTS</span></span>

### <span data-ttu-id="c2b20-166">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c2b20-166">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="c2b20-167">Parametern ' VirtualNetworkGateway ' godkänner värdet av typen ' PSVirtualNetworkGateway ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="c2b20-167">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="c2b20-168">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c2b20-168">OUTPUTS</span></span>

### <span data-ttu-id="c2b20-169">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c2b20-169">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="c2b20-170">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c2b20-170">NOTES</span></span>
* <span data-ttu-id="c2b20-171">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="c2b20-171">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="c2b20-172">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c2b20-172">RELATED LINKS</span></span>

[<span data-ttu-id="c2b20-173">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c2b20-173">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="c2b20-174">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c2b20-174">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="c2b20-175">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c2b20-175">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="c2b20-176">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c2b20-176">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="c2b20-177">Ändra storlek – AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c2b20-177">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)


