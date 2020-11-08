---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: d3434a650eb09391aa7505f288667aa130401e26
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100953"
---
# <span data-ttu-id="3de0f-101">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3de0f-101">Add-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="3de0f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3de0f-102">SYNOPSIS</span></span>
<span data-ttu-id="3de0f-103">Lägger till en HTTP-lyssnare till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="3de0f-103">Adds an HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="3de0f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3de0f-104">SYNTAX</span></span>

### <span data-ttu-id="3de0f-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3de0f-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-FirewallPolicyId <String>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3de0f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3de0f-106">SetByResource</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3de0f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3de0f-107">DESCRIPTION</span></span>
<span data-ttu-id="3de0f-108">Cmdleten **Add-AzApplicationGatewayHttpListener** lägger till en http-lyssnare till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="3de0f-108">The **Add-AzApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="3de0f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3de0f-109">EXAMPLES</span></span>

### <span data-ttu-id="3de0f-110">Exempel 1: lägga till en HTTP-lyssnare</span><span class="sxs-lookup"><span data-stu-id="3de0f-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="3de0f-111">Med det första kommandot hämtas programgatewayen och lagras i $AppGw variabeln. Med det andra kommandot läggs HTTP-lyssnaren till i programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="3de0f-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="3de0f-112">Exempel 2: lägga till en HTTPS-lyssnare med SSL</span><span class="sxs-lookup"><span data-stu-id="3de0f-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="3de0f-113">Med det första kommandot hämtas programgatewayen och lagras i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="3de0f-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="3de0f-114">Det andra kommandot lägger till lyssnaren som använder HTTPS-protokollet för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="3de0f-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

### <span data-ttu-id="3de0f-115">Exempel 3: lägga till en HTTPS-lyssnare med SSL och värdnamn</span><span class="sxs-lookup"><span data-stu-id="3de0f-115">Example 3: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="3de0f-116">Med det första kommandot hämtas programgatewayen och lagras i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="3de0f-116">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="3de0f-117">Det andra kommandot lägger till lyssnaren, som använder HTTPS-protokollet, med SSL-certifikat och-värdnamn, i programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="3de0f-117">The second command adds the listener, which uses the HTTPS protocol, with SSL Certificates and HostNames, to the application gateway.</span></span>

## <span data-ttu-id="3de0f-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3de0f-118">PARAMETERS</span></span>

### <span data-ttu-id="3de0f-119">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3de0f-119">-ApplicationGateway</span></span>
<span data-ttu-id="3de0f-120">Anger den Programgateway som denna cmdlet lägger till en HTTP-lyssnare i.</span><span class="sxs-lookup"><span data-stu-id="3de0f-120">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="3de0f-121">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="3de0f-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="3de0f-122">Kund fel för en Programgateway</span><span class="sxs-lookup"><span data-stu-id="3de0f-122">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="3de0f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3de0f-123">-DefaultProfile</span></span>
<span data-ttu-id="3de0f-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3de0f-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3de0f-125">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="3de0f-125">-FirewallPolicy</span></span>
<span data-ttu-id="3de0f-126">FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="3de0f-126">FirewallPolicy</span></span>

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

### <span data-ttu-id="3de0f-127">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="3de0f-127">-FirewallPolicyId</span></span>
<span data-ttu-id="3de0f-128">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="3de0f-128">FirewallPolicyId</span></span>

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

### <span data-ttu-id="3de0f-129">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="3de0f-129">-FrontendIPConfiguration</span></span>
<span data-ttu-id="3de0f-130">Anger front-IP-startobjektet för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="3de0f-130">Specifies the application gateway front-end IP resource object.</span></span>

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

### <span data-ttu-id="3de0f-131">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="3de0f-131">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="3de0f-132">Anger start-ID för front-Gateway.</span><span class="sxs-lookup"><span data-stu-id="3de0f-132">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="3de0f-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="3de0f-133">-FrontendPort</span></span>
<span data-ttu-id="3de0f-134">Anger front-end port-objekt för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="3de0f-134">Specifies the application gateway front-end port object.</span></span>

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

### <span data-ttu-id="3de0f-135">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="3de0f-135">-FrontendPortId</span></span>
<span data-ttu-id="3de0f-136">Anger front Port-ID för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="3de0f-136">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="3de0f-137">-HostName</span><span class="sxs-lookup"><span data-stu-id="3de0f-137">-HostName</span></span>
<span data-ttu-id="3de0f-138">Anger värd namnet som denna cmdlet lägger till en HTTP-lyssnare på.</span><span class="sxs-lookup"><span data-stu-id="3de0f-138">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

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

### <span data-ttu-id="3de0f-139">-Värdnamn</span><span class="sxs-lookup"><span data-stu-id="3de0f-139">-HostNames</span></span>
<span data-ttu-id="3de0f-140">Värdnamn</span><span class="sxs-lookup"><span data-stu-id="3de0f-140">Host names</span></span>

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

### <span data-ttu-id="3de0f-141">-Namn</span><span class="sxs-lookup"><span data-stu-id="3de0f-141">-Name</span></span>
<span data-ttu-id="3de0f-142">Anger namnet på den frontend-port som kommandot lägger till.</span><span class="sxs-lookup"><span data-stu-id="3de0f-142">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="3de0f-143">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="3de0f-143">-Protocol</span></span>
<span data-ttu-id="3de0f-144">Anger protokollet för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="3de0f-144">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="3de0f-145">Både HTTP och HTTPS stöds.</span><span class="sxs-lookup"><span data-stu-id="3de0f-145">Both HTTP and HTTPS are supported.</span></span>

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

### <span data-ttu-id="3de0f-146">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="3de0f-146">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="3de0f-147">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="3de0f-147">-SslCertificate</span></span>
<span data-ttu-id="3de0f-148">Anger SSL-certifikatet för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="3de0f-148">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="3de0f-149">Måste anges om HTTPS har valts som lyssnings protokoll.</span><span class="sxs-lookup"><span data-stu-id="3de0f-149">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="3de0f-150">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="3de0f-150">-SslCertificateId</span></span>
<span data-ttu-id="3de0f-151">Anger SSL-certifikat-ID för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="3de0f-151">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="3de0f-152">Måste anges om HTTPS har valts som lyssnings protokoll.</span><span class="sxs-lookup"><span data-stu-id="3de0f-152">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="3de0f-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3de0f-153">CommonParameters</span></span>
<span data-ttu-id="3de0f-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3de0f-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3de0f-155">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3de0f-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3de0f-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3de0f-156">INPUTS</span></span>

### <span data-ttu-id="3de0f-157">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3de0f-157">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3de0f-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3de0f-158">OUTPUTS</span></span>

### <span data-ttu-id="3de0f-159">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3de0f-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3de0f-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3de0f-160">NOTES</span></span>

## <span data-ttu-id="3de0f-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3de0f-161">RELATED LINKS</span></span>

[<span data-ttu-id="3de0f-162">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3de0f-162">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="3de0f-163">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3de0f-163">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="3de0f-164">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3de0f-164">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="3de0f-165">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3de0f-165">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


