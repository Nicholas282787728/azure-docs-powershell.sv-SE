---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 3cc9af0865ca47099f5617cc1e94f3232ed9bdb7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089076"
---
# <span data-ttu-id="14238-101">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="14238-101">Set-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="14238-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="14238-102">SYNOPSIS</span></span>
<span data-ttu-id="14238-103">Ändrar en HTTP-lyssnare för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="14238-103">Modifies an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="14238-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="14238-104">SYNTAX</span></span>

### <span data-ttu-id="14238-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="14238-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-FirewallPolicyId <String>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="14238-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="14238-106">SetByResource</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="14238-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="14238-107">DESCRIPTION</span></span>
<span data-ttu-id="14238-108">Cmdleten **set-AzApplicationGatewayHttpListener** ändrar en http-lyssnare för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="14238-108">The **Set-AzApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="14238-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="14238-109">EXAMPLES</span></span>

### <span data-ttu-id="14238-110">Exempel 1: Ställ in en HTTP-lyssnare</span><span class="sxs-lookup"><span data-stu-id="14238-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="14238-111">Det första kommandot hämtar den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen med namnet ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="14238-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="14238-112">Det andra kommandot ställer in HTTP-lyssnaren för gatewayen för att använda front konfigurationen som lagras i $FIP 01 med HTTP-protokollet på port 80.</span><span class="sxs-lookup"><span data-stu-id="14238-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

### <span data-ttu-id="14238-113">Exempel 2: lägga till en HTTPS-lyssnare med SSL och värdnamn</span><span class="sxs-lookup"><span data-stu-id="14238-113">Example 2: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="14238-114">Med det första kommandot hämtas programgatewayen och lagras i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="14238-114">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="14238-115">Det andra kommandot lägger till lyssnaren, som använder HTTPS-protokollet, med SSL-certifikat och-värdnamn, i programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="14238-115">The second command adds the listener, which uses the HTTPS protocol, with SSL Certificates and HostNames, to the application gateway.</span></span>

## <span data-ttu-id="14238-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="14238-116">PARAMETERS</span></span>

### <span data-ttu-id="14238-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14238-117">-ApplicationGateway</span></span>
<span data-ttu-id="14238-118">Anger den Programgateway som denna cmdlet associerar HTTP-lyssnaren med.</span><span class="sxs-lookup"><span data-stu-id="14238-118">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14238-119">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="14238-119">-CustomErrorConfiguration</span></span>
<span data-ttu-id="14238-120">Kund fel för en Programgateway</span><span class="sxs-lookup"><span data-stu-id="14238-120">Customer error of an application gateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14238-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14238-121">-DefaultProfile</span></span>
<span data-ttu-id="14238-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="14238-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14238-123">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="14238-123">-FirewallPolicy</span></span>
<span data-ttu-id="14238-124">FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="14238-124">FirewallPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14238-125">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="14238-125">-FirewallPolicyId</span></span>
<span data-ttu-id="14238-126">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="14238-126">FirewallPolicyId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14238-127">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="14238-127">-FrontendIPConfiguration</span></span>
<span data-ttu-id="14238-128">Anger front-IP-adressen för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="14238-128">Specifies the front-end IP address of the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14238-129">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="14238-129">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="14238-130">Anger ID för front-IP-adressen för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="14238-130">Specifies the ID of the front-end IP address of the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14238-131">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="14238-131">-FrontendPort</span></span>
<span data-ttu-id="14238-132">Anger front port för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="14238-132">Specifies the application gateway front-end port.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14238-133">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="14238-133">-FrontendPortId</span></span>
<span data-ttu-id="14238-134">Anger front Port-ID för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="14238-134">Specifies the application gateway front-end port ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14238-135">-HostName</span><span class="sxs-lookup"><span data-stu-id="14238-135">-HostName</span></span>
<span data-ttu-id="14238-136">Anger värd namnet som den här cmdleten skickar HTTP-lyssnaren till.</span><span class="sxs-lookup"><span data-stu-id="14238-136">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="14238-137">-Värdnamn</span><span class="sxs-lookup"><span data-stu-id="14238-137">-HostNames</span></span>
<span data-ttu-id="14238-138">Värdnamn</span><span class="sxs-lookup"><span data-stu-id="14238-138">Host names</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14238-139">-Namn</span><span class="sxs-lookup"><span data-stu-id="14238-139">-Name</span></span>
<span data-ttu-id="14238-140">Anger namnet på HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="14238-140">Specifies the name of the HTTP listener.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14238-141">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="14238-141">-Protocol</span></span>
<span data-ttu-id="14238-142">Anger protokollet som HTTP-lyssnaren använder.</span><span class="sxs-lookup"><span data-stu-id="14238-142">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="14238-143">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="14238-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="14238-144">Inkommande</span><span class="sxs-lookup"><span data-stu-id="14238-144">Http</span></span>
- <span data-ttu-id="14238-145">Https</span><span class="sxs-lookup"><span data-stu-id="14238-145">Https</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14238-146">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="14238-146">-RequireServerNameIndication</span></span>
<span data-ttu-id="14238-147">Anger om cmdleten kräver en server namns indikering.</span><span class="sxs-lookup"><span data-stu-id="14238-147">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="14238-148">De acceptabla värdena för den här parametern är: true eller false.</span><span class="sxs-lookup"><span data-stu-id="14238-148">The acceptable values for this parameter are: true or false.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: true, false

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14238-149">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="14238-149">-SslCertificate</span></span>
<span data-ttu-id="14238-150">Anger SSL-certifikatet för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="14238-150">Specifies the SSL certificate of the HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14238-151">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="14238-151">-SslCertificateId</span></span>
<span data-ttu-id="14238-152">Anger SSL-certifikat-ID för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="14238-152">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14238-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14238-153">CommonParameters</span></span>
<span data-ttu-id="14238-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14238-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14238-155">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14238-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14238-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="14238-156">INPUTS</span></span>

### <span data-ttu-id="14238-157">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14238-157">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="14238-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="14238-158">OUTPUTS</span></span>

### <span data-ttu-id="14238-159">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14238-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="14238-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="14238-160">NOTES</span></span>

## <span data-ttu-id="14238-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="14238-161">RELATED LINKS</span></span>

[<span data-ttu-id="14238-162">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="14238-162">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="14238-163">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="14238-163">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="14238-164">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="14238-164">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="14238-165">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="14238-165">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)


