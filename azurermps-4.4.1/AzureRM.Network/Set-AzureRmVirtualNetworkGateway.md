---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 41c94d0dd8401399f360af89f1744cc10e900e1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577616"
---
# <span data-ttu-id="bd6c1-101">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bd6c1-101">Set-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="bd6c1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bd6c1-102">SYNOPSIS</span></span>
<span data-ttu-id="bd6c1-103">Uppdaterar en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="bd6c1-103">Updates a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd6c1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bd6c1-104">SYNTAX</span></span>

### <span data-ttu-id="bd6c1-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="bd6c1-105">Default (Default)</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd6c1-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="bd6c1-106">RadiusServerConfiguration</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd6c1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bd6c1-107">DESCRIPTION</span></span>
<span data-ttu-id="bd6c1-108">Cmdleten **set-AzureRmVirtualNetworkGateway** uppdaterar en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="bd6c1-108">The **Set-AzureRmVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="bd6c1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bd6c1-109">EXAMPLES</span></span>

### <span data-ttu-id="bd6c1-110">Exempel 1: Ange mål tillstånd för en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="bd6c1-110">Example 1: Set the goal state a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="bd6c1-111">Det första kommandot får en virtuell nätverksgateway som heter Gateway01 som tillhör resurs gruppen ResourceGroup001 och lagrar den på variabeln som heter $Gateway</span><span class="sxs-lookup"><span data-stu-id="bd6c1-111">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway</span></span>

<span data-ttu-id="bd6c1-112">Det andra kommandot ställer in mål tillståndet för den virtuella Nätverksgatewayen som lagras i variabeln $Gateway.</span><span class="sxs-lookup"><span data-stu-id="bd6c1-112">The second command sets the goal state for the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="bd6c1-113">Kommandot anger också ASN till 1337.</span><span class="sxs-lookup"><span data-stu-id="bd6c1-113">The command also sets the ASN to 1337.</span></span>

## <span data-ttu-id="bd6c1-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bd6c1-114">PARAMETERS</span></span>

### <span data-ttu-id="bd6c1-115">-ASN</span><span class="sxs-lookup"><span data-stu-id="bd6c1-115">-Asn</span></span>
<span data-ttu-id="bd6c1-116">Anger det autonoma system numret för virtuell nätverksgateway (ASN) som används för att konfigurera BGP-sessioner (Border Gateway Protocol) i IPsec-tunnlar.</span><span class="sxs-lookup"><span data-stu-id="bd6c1-116">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

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

### <span data-ttu-id="bd6c1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd6c1-117">-DefaultProfile</span></span>
<span data-ttu-id="bd6c1-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bd6c1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="bd6c1-119">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="bd6c1-119">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="bd6c1-120">Inaktiverar den aktiva aktiva funktionen.</span><span class="sxs-lookup"><span data-stu-id="bd6c1-120">Disables the active-active feature.</span></span>

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

### <span data-ttu-id="bd6c1-121">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="bd6c1-121">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="bd6c1-122">Aktiverar den aktiva aktiva funktionen.</span><span class="sxs-lookup"><span data-stu-id="bd6c1-122">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="bd6c1-123">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="bd6c1-123">-GatewayDefaultSite</span></span>
<span data-ttu-id="bd6c1-124">Anger standard webbplatsen som ska användas för Tvingad tunnel trafik.</span><span class="sxs-lookup"><span data-stu-id="bd6c1-124">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="bd6c1-125">Om en standard webbplats anges routas all Internet trafik från gatewayens virtuella privata nätverk (VPN) till den webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="bd6c1-125">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

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

### <span data-ttu-id="bd6c1-126">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="bd6c1-126">-GatewaySku</span></span>
<span data-ttu-id="bd6c1-127">Anger lagerhållnings enhet (SKU) för den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="bd6c1-127">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="bd6c1-128">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="bd6c1-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bd6c1-129">Basisk</span><span class="sxs-lookup"><span data-stu-id="bd6c1-129">Basic</span></span>
- <span data-ttu-id="bd6c1-130">Standar</span><span class="sxs-lookup"><span data-stu-id="bd6c1-130">Standard</span></span>
- <span data-ttu-id="bd6c1-131">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="bd6c1-131">HighPerformance</span></span>
- <span data-ttu-id="bd6c1-132">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="bd6c1-132">VpnGw1</span></span>
- <span data-ttu-id="bd6c1-133">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="bd6c1-133">VpnGw2</span></span>
- <span data-ttu-id="bd6c1-134">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="bd6c1-134">VpnGw3</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd6c1-135">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="bd6c1-135">-PeerWeight</span></span>
<span data-ttu-id="bd6c1-136">Anger vikten som har lagts till för vägar som upptäckts via BGP från denna virtuella nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="bd6c1-136">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="bd6c1-137">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="bd6c1-137">-RadiusServerAddress</span></span>
<span data-ttu-id="bd6c1-138">P2S externa RADIUS-serveradress.</span><span class="sxs-lookup"><span data-stu-id="bd6c1-138">P2S External Radius server address.</span></span>
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

### <span data-ttu-id="bd6c1-139">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="bd6c1-139">-RadiusServerSecret</span></span>
<span data-ttu-id="bd6c1-140">P2S externa RADIUS-server hemlighet.</span><span class="sxs-lookup"><span data-stu-id="bd6c1-140">P2S External Radius server secret.</span></span>
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

### <span data-ttu-id="bd6c1-141">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bd6c1-141">-VirtualNetworkGateway</span></span>
<span data-ttu-id="bd6c1-142">Anger det virtuella nätverkets gateway-objekt som ska ändras från av.</span><span class="sxs-lookup"><span data-stu-id="bd6c1-142">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="bd6c1-143">Du kan använda Get-AzureRmVirtualNetworkGateway cmdlet för att hämta det virtuella nätverkets gateway-objekt.</span><span class="sxs-lookup"><span data-stu-id="bd6c1-143">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

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

### <span data-ttu-id="bd6c1-144">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="bd6c1-144">-VpnClientAddressPool</span></span>
<span data-ttu-id="bd6c1-145">Anger det adress utrymme som denna cmdlet använder för att tilldela IP-adresser för VPN-klienter från.</span><span class="sxs-lookup"><span data-stu-id="bd6c1-145">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="bd6c1-146">Detta ska inte överlappa virtuella nätverks-eller lokala områden.</span><span class="sxs-lookup"><span data-stu-id="bd6c1-146">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="bd6c1-147">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="bd6c1-147">-VpnClientProtocol</span></span>
<span data-ttu-id="bd6c1-148">En lista över protokoll för P2S VPN-klienter</span><span class="sxs-lookup"><span data-stu-id="bd6c1-148">A list of P2S VPN client tunneling protocols</span></span>
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

### <span data-ttu-id="bd6c1-149">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="bd6c1-149">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="bd6c1-150">Anger en lista över återkallade VPN-klient certifikat.</span><span class="sxs-lookup"><span data-stu-id="bd6c1-150">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="bd6c1-151">En VPN-klient som visar ett certifikat som matchar något av dessa tas bort.</span><span class="sxs-lookup"><span data-stu-id="bd6c1-151">A VPN client presenting a certificate that matches one of these is removed.</span></span>

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

### <span data-ttu-id="bd6c1-152">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="bd6c1-152">-VpnClientRootCertificates</span></span>
<span data-ttu-id="bd6c1-153">Anger en lista över de VPN-klient rot certifikat som ska användas för VPN-klientautentisering.</span><span class="sxs-lookup"><span data-stu-id="bd6c1-153">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="bd6c1-154">Anslutning av VPN-klienter måste presentera certifikat som genererats från ett av dessa rot certifikat.</span><span class="sxs-lookup"><span data-stu-id="bd6c1-154">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="bd6c1-155">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bd6c1-155">-Confirm</span></span>
<span data-ttu-id="bd6c1-156">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bd6c1-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd6c1-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd6c1-157">-WhatIf</span></span>
<span data-ttu-id="bd6c1-158">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bd6c1-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bd6c1-159">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bd6c1-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd6c1-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd6c1-160">CommonParameters</span></span>
<span data-ttu-id="bd6c1-161">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd6c1-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd6c1-162">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd6c1-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd6c1-163">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bd6c1-163">INPUTS</span></span>

### <span data-ttu-id="bd6c1-164">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bd6c1-164">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="bd6c1-165">Parametern ' VirtualNetworkGateway ' godkänner värdet av typen ' PSVirtualNetworkGateway ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="bd6c1-165">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="bd6c1-166">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bd6c1-166">OUTPUTS</span></span>

### <span data-ttu-id="bd6c1-167">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bd6c1-167">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="bd6c1-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bd6c1-168">NOTES</span></span>
* <span data-ttu-id="bd6c1-169">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="bd6c1-169">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="bd6c1-170">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bd6c1-170">RELATED LINKS</span></span>

[<span data-ttu-id="bd6c1-171">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bd6c1-171">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="bd6c1-172">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bd6c1-172">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="bd6c1-173">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bd6c1-173">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="bd6c1-174">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bd6c1-174">Reset-AzureRmVirtualNetworkGateway</span></span>](./Reset-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="bd6c1-175">Ändra storlek – AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bd6c1-175">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)


