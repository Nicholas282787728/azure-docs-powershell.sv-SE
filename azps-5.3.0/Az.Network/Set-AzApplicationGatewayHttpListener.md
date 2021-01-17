---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 8ce5d01d78b8b434e062b0f33ee41a4cbbce20ed
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421467"
---
# <span data-ttu-id="dd2b8-101">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="dd2b8-101">Set-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="dd2b8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dd2b8-102">SYNOPSIS</span></span>
<span data-ttu-id="dd2b8-103">Ändrar en HTTP-lyssnare för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="dd2b8-103">Modifies an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="dd2b8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dd2b8-104">SYNTAX</span></span>

### <span data-ttu-id="dd2b8-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="dd2b8-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-FirewallPolicyId <String>] [-SslProfileId <String>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dd2b8-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="dd2b8-106">SetByResource</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-SslProfile <PSApplicationGatewaySslProfile>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dd2b8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dd2b8-107">DESCRIPTION</span></span>
<span data-ttu-id="dd2b8-108">Cmdleten **set-AzApplicationGatewayHttpListener** ändrar en http-lyssnare för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="dd2b8-108">The **Set-AzApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="dd2b8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dd2b8-109">EXAMPLES</span></span>

### <span data-ttu-id="dd2b8-110">Exempel 1: Ställ in en HTTP-lyssnare</span><span class="sxs-lookup"><span data-stu-id="dd2b8-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="dd2b8-111">Det första kommandot hämtar den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen med namnet ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="dd2b8-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="dd2b8-112">Det andra kommandot ställer in HTTP-lyssnaren för gatewayen för att använda front konfigurationen som lagras i $FIP 01 med HTTP-protokollet på port 80.</span><span class="sxs-lookup"><span data-stu-id="dd2b8-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

### <span data-ttu-id="dd2b8-113">Exempel 2: lägga till en HTTPS-lyssnare med SSL och värdnamn</span><span class="sxs-lookup"><span data-stu-id="dd2b8-113">Example 2: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="dd2b8-114">Med det första kommandot hämtas programgatewayen och lagras i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="dd2b8-114">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="dd2b8-115">Det andra kommandot lägger till lyssnaren, som använder HTTPS-protokollet, med SSL-certifikat och-värdnamn, i programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="dd2b8-115">The second command adds the listener, which uses the HTTPS protocol, with SSL Certificates and HostNames, to the application gateway.</span></span>

## <span data-ttu-id="dd2b8-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dd2b8-116">PARAMETERS</span></span>

### <span data-ttu-id="dd2b8-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dd2b8-117">-ApplicationGateway</span></span>
<span data-ttu-id="dd2b8-118">Anger den Programgateway som denna cmdlet associerar HTTP-lyssnaren med.</span><span class="sxs-lookup"><span data-stu-id="dd2b8-118">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="dd2b8-119">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="dd2b8-119">-CustomErrorConfiguration</span></span>
<span data-ttu-id="dd2b8-120">Kund fel för en Programgateway</span><span class="sxs-lookup"><span data-stu-id="dd2b8-120">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="dd2b8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd2b8-121">-DefaultProfile</span></span>
<span data-ttu-id="dd2b8-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dd2b8-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd2b8-123">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="dd2b8-123">-FirewallPolicy</span></span>
<span data-ttu-id="dd2b8-124">FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="dd2b8-124">FirewallPolicy</span></span>

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

### <span data-ttu-id="dd2b8-125">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="dd2b8-125">-FirewallPolicyId</span></span>
<span data-ttu-id="dd2b8-126">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="dd2b8-126">FirewallPolicyId</span></span>

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

### <span data-ttu-id="dd2b8-127">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="dd2b8-127">-FrontendIPConfiguration</span></span>
<span data-ttu-id="dd2b8-128">Anger front-IP-adressen för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="dd2b8-128">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="dd2b8-129">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="dd2b8-129">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="dd2b8-130">Anger ID för front-IP-adressen för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="dd2b8-130">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="dd2b8-131">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="dd2b8-131">-FrontendPort</span></span>
<span data-ttu-id="dd2b8-132">Anger front port för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="dd2b8-132">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="dd2b8-133">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="dd2b8-133">-FrontendPortId</span></span>
<span data-ttu-id="dd2b8-134">Anger front Port-ID för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="dd2b8-134">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="dd2b8-135">-HostName</span><span class="sxs-lookup"><span data-stu-id="dd2b8-135">-HostName</span></span>
<span data-ttu-id="dd2b8-136">Anger värd namnet som den här cmdleten skickar HTTP-lyssnaren till.</span><span class="sxs-lookup"><span data-stu-id="dd2b8-136">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="dd2b8-137">-Värdnamn</span><span class="sxs-lookup"><span data-stu-id="dd2b8-137">-HostNames</span></span>
<span data-ttu-id="dd2b8-138">Värdnamn</span><span class="sxs-lookup"><span data-stu-id="dd2b8-138">Host names</span></span>

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

### <span data-ttu-id="dd2b8-139">-Namn</span><span class="sxs-lookup"><span data-stu-id="dd2b8-139">-Name</span></span>
<span data-ttu-id="dd2b8-140">Anger namnet på HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="dd2b8-140">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="dd2b8-141">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="dd2b8-141">-Protocol</span></span>
<span data-ttu-id="dd2b8-142">Anger protokollet som HTTP-lyssnaren använder.</span><span class="sxs-lookup"><span data-stu-id="dd2b8-142">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="dd2b8-143">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="dd2b8-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dd2b8-144">Inkommande</span><span class="sxs-lookup"><span data-stu-id="dd2b8-144">Http</span></span>
- <span data-ttu-id="dd2b8-145">Https</span><span class="sxs-lookup"><span data-stu-id="dd2b8-145">Https</span></span>

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

### <span data-ttu-id="dd2b8-146">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="dd2b8-146">-RequireServerNameIndication</span></span>
<span data-ttu-id="dd2b8-147">Anger om cmdleten kräver en server namns indikering.</span><span class="sxs-lookup"><span data-stu-id="dd2b8-147">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="dd2b8-148">De acceptabla värdena för den här parametern är: true eller false.</span><span class="sxs-lookup"><span data-stu-id="dd2b8-148">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="dd2b8-149">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="dd2b8-149">-SslCertificate</span></span>
<span data-ttu-id="dd2b8-150">Anger SSL-certifikatet för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="dd2b8-150">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="dd2b8-151">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="dd2b8-151">-SslCertificateId</span></span>
<span data-ttu-id="dd2b8-152">Anger SSL-certifikat-ID för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="dd2b8-152">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="dd2b8-153">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="dd2b8-153">-SslProfile</span></span>
<span data-ttu-id="dd2b8-154">SslProfile</span><span class="sxs-lookup"><span data-stu-id="dd2b8-154">SslProfile</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd2b8-155">-SslProfileId</span><span class="sxs-lookup"><span data-stu-id="dd2b8-155">-SslProfileId</span></span>
<span data-ttu-id="dd2b8-156">SslProfileId</span><span class="sxs-lookup"><span data-stu-id="dd2b8-156">SslProfileId</span></span>

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

### <span data-ttu-id="dd2b8-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd2b8-157">CommonParameters</span></span>
<span data-ttu-id="dd2b8-158">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd2b8-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd2b8-159">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd2b8-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd2b8-160">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dd2b8-160">INPUTS</span></span>

### <span data-ttu-id="dd2b8-161">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dd2b8-161">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dd2b8-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dd2b8-162">OUTPUTS</span></span>

### <span data-ttu-id="dd2b8-163">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dd2b8-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dd2b8-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dd2b8-164">NOTES</span></span>

## <span data-ttu-id="dd2b8-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dd2b8-165">RELATED LINKS</span></span>

[<span data-ttu-id="dd2b8-166">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="dd2b8-166">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="dd2b8-167">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="dd2b8-167">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="dd2b8-168">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="dd2b8-168">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="dd2b8-169">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="dd2b8-169">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)


