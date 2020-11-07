---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgateway
schema: 2.0.0
ms.openlocfilehash: 622fb5278f7e0a78fb6163954829b1a2aaa6bba7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928662"
---
# <span data-ttu-id="96c24-101">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="96c24-101">Set-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="96c24-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="96c24-102">SYNOPSIS</span></span>
<span data-ttu-id="96c24-103">Uppdaterar en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="96c24-103">Updates a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96c24-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="96c24-104">SYNTAX</span></span>

### <span data-ttu-id="96c24-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="96c24-105">Default (Default)</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96c24-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="96c24-106">RadiusServerConfiguration</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96c24-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="96c24-107">DESCRIPTION</span></span>
<span data-ttu-id="96c24-108">Cmdleten **set-AzureRmVirtualNetworkGateway** uppdaterar en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="96c24-108">The **Set-AzureRmVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="96c24-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="96c24-109">EXAMPLES</span></span>

### <span data-ttu-id="96c24-110">Exempel 1: Ange mål tillstånd för en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="96c24-110">Example 1: Set the goal state a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="96c24-111">Det första kommandot får en virtuell nätverksgateway som heter Gateway01 som tillhör resurs gruppen ResourceGroup001 och lagrar den på variabeln som heter $Gateway</span><span class="sxs-lookup"><span data-stu-id="96c24-111">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway</span></span>

<span data-ttu-id="96c24-112">Det andra kommandot ställer in mål tillståndet för den virtuella Nätverksgatewayen som lagras i variabeln $Gateway.</span><span class="sxs-lookup"><span data-stu-id="96c24-112">The second command sets the goal state for the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="96c24-113">Kommandot anger också ASN till 1337.</span><span class="sxs-lookup"><span data-stu-id="96c24-113">The command also sets the ASN to 1337.</span></span>

## <span data-ttu-id="96c24-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="96c24-114">PARAMETERS</span></span>

### <span data-ttu-id="96c24-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="96c24-115">-AsJob</span></span>
<span data-ttu-id="96c24-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="96c24-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="96c24-117">-ASN</span><span class="sxs-lookup"><span data-stu-id="96c24-117">-Asn</span></span>
<span data-ttu-id="96c24-118">Anger det autonoma system numret för virtuell nätverksgateway (ASN) som används för att konfigurera BGP-sessioner (Border Gateway Protocol) i IPsec-tunnlar.</span><span class="sxs-lookup"><span data-stu-id="96c24-118">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

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

### <span data-ttu-id="96c24-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96c24-119">-DefaultProfile</span></span>
<span data-ttu-id="96c24-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="96c24-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="96c24-121">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="96c24-121">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="96c24-122">Inaktiverar den aktiva aktiva funktionen.</span><span class="sxs-lookup"><span data-stu-id="96c24-122">Disables the active-active feature.</span></span>

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

### <span data-ttu-id="96c24-123">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="96c24-123">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="96c24-124">Aktiverar den aktiva aktiva funktionen.</span><span class="sxs-lookup"><span data-stu-id="96c24-124">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="96c24-125">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="96c24-125">-GatewayDefaultSite</span></span>
<span data-ttu-id="96c24-126">Anger standard webbplatsen som ska användas för Tvingad tunnel trafik.</span><span class="sxs-lookup"><span data-stu-id="96c24-126">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="96c24-127">Om en standard webbplats anges routas all Internet trafik från gatewayens virtuella privata nätverk (VPN) till den webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="96c24-127">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

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

### <span data-ttu-id="96c24-128">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="96c24-128">-GatewaySku</span></span>
<span data-ttu-id="96c24-129">Anger lagerhållnings enhet (SKU) för den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="96c24-129">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="96c24-130">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="96c24-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="96c24-131">Basisk</span><span class="sxs-lookup"><span data-stu-id="96c24-131">Basic</span></span>
- <span data-ttu-id="96c24-132">Standar</span><span class="sxs-lookup"><span data-stu-id="96c24-132">Standard</span></span>
- <span data-ttu-id="96c24-133">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="96c24-133">HighPerformance</span></span>
- <span data-ttu-id="96c24-134">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="96c24-134">VpnGw1</span></span>
- <span data-ttu-id="96c24-135">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="96c24-135">VpnGw2</span></span>
- <span data-ttu-id="96c24-136">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="96c24-136">VpnGw3</span></span>

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

### <span data-ttu-id="96c24-137">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="96c24-137">-PeerWeight</span></span>
<span data-ttu-id="96c24-138">Anger vikten som har lagts till för vägar som upptäckts via BGP från denna virtuella nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="96c24-138">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="96c24-139">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="96c24-139">-RadiusServerAddress</span></span>
<span data-ttu-id="96c24-140">P2S externa RADIUS-serveradress.</span><span class="sxs-lookup"><span data-stu-id="96c24-140">P2S External Radius server address.</span></span>
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

### <span data-ttu-id="96c24-141">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="96c24-141">-RadiusServerSecret</span></span>
<span data-ttu-id="96c24-142">P2S externa RADIUS-server hemlighet.</span><span class="sxs-lookup"><span data-stu-id="96c24-142">P2S External Radius server secret.</span></span>
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

### <span data-ttu-id="96c24-143">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="96c24-143">-VirtualNetworkGateway</span></span>
<span data-ttu-id="96c24-144">Anger det virtuella nätverkets gateway-objekt som ska ändras från av.</span><span class="sxs-lookup"><span data-stu-id="96c24-144">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="96c24-145">Du kan använda Get-AzureRmVirtualNetworkGateway cmdlet för att hämta det virtuella nätverkets gateway-objekt.</span><span class="sxs-lookup"><span data-stu-id="96c24-145">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

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

### <span data-ttu-id="96c24-146">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="96c24-146">-VpnClientAddressPool</span></span>
<span data-ttu-id="96c24-147">Anger det adress utrymme som denna cmdlet använder för att tilldela IP-adresser för VPN-klienter från.</span><span class="sxs-lookup"><span data-stu-id="96c24-147">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="96c24-148">Detta ska inte överlappa virtuella nätverks-eller lokala områden.</span><span class="sxs-lookup"><span data-stu-id="96c24-148">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="96c24-149">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="96c24-149">-VpnClientProtocol</span></span>
<span data-ttu-id="96c24-150">En lista över protokoll för P2S VPN-klienter</span><span class="sxs-lookup"><span data-stu-id="96c24-150">A list of P2S VPN client tunneling protocols</span></span>
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

### <span data-ttu-id="96c24-151">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="96c24-151">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="96c24-152">Anger en lista över återkallade VPN-klient certifikat.</span><span class="sxs-lookup"><span data-stu-id="96c24-152">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="96c24-153">En VPN-klient som visar ett certifikat som matchar något av dessa tas bort.</span><span class="sxs-lookup"><span data-stu-id="96c24-153">A VPN client presenting a certificate that matches one of these is removed.</span></span>

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

### <span data-ttu-id="96c24-154">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="96c24-154">-VpnClientRootCertificates</span></span>
<span data-ttu-id="96c24-155">Anger en lista över de VPN-klient rot certifikat som ska användas för VPN-klientautentisering.</span><span class="sxs-lookup"><span data-stu-id="96c24-155">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="96c24-156">Anslutning av VPN-klienter måste presentera certifikat som genererats från ett av dessa rot certifikat.</span><span class="sxs-lookup"><span data-stu-id="96c24-156">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="96c24-157">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="96c24-157">-Confirm</span></span>
<span data-ttu-id="96c24-158">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="96c24-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96c24-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96c24-159">-WhatIf</span></span>
<span data-ttu-id="96c24-160">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="96c24-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96c24-161">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="96c24-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96c24-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96c24-162">CommonParameters</span></span>
<span data-ttu-id="96c24-163">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96c24-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96c24-164">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96c24-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96c24-165">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="96c24-165">INPUTS</span></span>

### <span data-ttu-id="96c24-166">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="96c24-166">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="96c24-167">Parametern ' VirtualNetworkGateway ' godkänner värdet av typen ' PSVirtualNetworkGateway ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="96c24-167">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="96c24-168">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="96c24-168">OUTPUTS</span></span>

### <span data-ttu-id="96c24-169">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="96c24-169">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="96c24-170">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="96c24-170">NOTES</span></span>
* <span data-ttu-id="96c24-171">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="96c24-171">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="96c24-172">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="96c24-172">RELATED LINKS</span></span>

[<span data-ttu-id="96c24-173">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="96c24-173">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="96c24-174">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="96c24-174">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="96c24-175">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="96c24-175">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="96c24-176">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="96c24-176">Reset-AzureRmVirtualNetworkGateway</span></span>](./Reset-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="96c24-177">Ändra storlek – AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="96c24-177">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)


