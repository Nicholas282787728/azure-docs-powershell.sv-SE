---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: d3434a650eb09391aa7505f288667aa130401e26
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94262989"
---
# <span data-ttu-id="d1ec2-101">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d1ec2-101">Add-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="d1ec2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d1ec2-102">SYNOPSIS</span></span>
<span data-ttu-id="d1ec2-103">Lägger till en HTTP-lyssnare till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-103">Adds an HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="d1ec2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d1ec2-104">SYNTAX</span></span>

### <span data-ttu-id="d1ec2-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d1ec2-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-FirewallPolicyId <String>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d1ec2-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d1ec2-106">SetByResource</span></span>
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

## <span data-ttu-id="d1ec2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d1ec2-107">DESCRIPTION</span></span>
<span data-ttu-id="d1ec2-108">Cmdleten **Add-AzApplicationGatewayHttpListener** lägger till en http-lyssnare till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-108">The **Add-AzApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="d1ec2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d1ec2-109">EXAMPLES</span></span>

### <span data-ttu-id="d1ec2-110">Exempel 1: lägga till en HTTP-lyssnare</span><span class="sxs-lookup"><span data-stu-id="d1ec2-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="d1ec2-111">Med det första kommandot hämtas programgatewayen och lagras i $AppGw variabeln. Med det andra kommandot läggs HTTP-lyssnaren till i programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="d1ec2-112">Exempel 2: lägga till en HTTPS-lyssnare med SSL</span><span class="sxs-lookup"><span data-stu-id="d1ec2-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="d1ec2-113">Med det första kommandot hämtas programgatewayen och lagras i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d1ec2-114">Det andra kommandot lägger till lyssnaren som använder HTTPS-protokollet för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

### <span data-ttu-id="d1ec2-115">Exempel 3: lägga till en HTTPS-lyssnare med SSL och värdnamn</span><span class="sxs-lookup"><span data-stu-id="d1ec2-115">Example 3: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="d1ec2-116">Med det första kommandot hämtas programgatewayen och lagras i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-116">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d1ec2-117">Det andra kommandot lägger till lyssnaren, som använder HTTPS-protokollet, med SSL-certifikat och-värdnamn, i programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-117">The second command adds the listener, which uses the HTTPS protocol, with SSL Certificates and HostNames, to the application gateway.</span></span>

## <span data-ttu-id="d1ec2-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d1ec2-118">PARAMETERS</span></span>

### <span data-ttu-id="d1ec2-119">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d1ec2-119">-ApplicationGateway</span></span>
<span data-ttu-id="d1ec2-120">Anger den Programgateway som denna cmdlet lägger till en HTTP-lyssnare i.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-120">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="d1ec2-121">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="d1ec2-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="d1ec2-122">Kund fel för en Programgateway</span><span class="sxs-lookup"><span data-stu-id="d1ec2-122">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="d1ec2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1ec2-123">-DefaultProfile</span></span>
<span data-ttu-id="d1ec2-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1ec2-125">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="d1ec2-125">-FirewallPolicy</span></span>
<span data-ttu-id="d1ec2-126">FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="d1ec2-126">FirewallPolicy</span></span>

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

### <span data-ttu-id="d1ec2-127">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="d1ec2-127">-FirewallPolicyId</span></span>
<span data-ttu-id="d1ec2-128">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="d1ec2-128">FirewallPolicyId</span></span>

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

### <span data-ttu-id="d1ec2-129">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d1ec2-129">-FrontendIPConfiguration</span></span>
<span data-ttu-id="d1ec2-130">Anger front-IP-startobjektet för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-130">Specifies the application gateway front-end IP resource object.</span></span>

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

### <span data-ttu-id="d1ec2-131">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d1ec2-131">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="d1ec2-132">Anger start-ID för front-Gateway.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-132">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="d1ec2-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="d1ec2-133">-FrontendPort</span></span>
<span data-ttu-id="d1ec2-134">Anger front-end port-objekt för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-134">Specifies the application gateway front-end port object.</span></span>

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

### <span data-ttu-id="d1ec2-135">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="d1ec2-135">-FrontendPortId</span></span>
<span data-ttu-id="d1ec2-136">Anger front Port-ID för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-136">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="d1ec2-137">-HostName</span><span class="sxs-lookup"><span data-stu-id="d1ec2-137">-HostName</span></span>
<span data-ttu-id="d1ec2-138">Anger värd namnet som denna cmdlet lägger till en HTTP-lyssnare på.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-138">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

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

### <span data-ttu-id="d1ec2-139">-Värdnamn</span><span class="sxs-lookup"><span data-stu-id="d1ec2-139">-HostNames</span></span>
<span data-ttu-id="d1ec2-140">Värdnamn</span><span class="sxs-lookup"><span data-stu-id="d1ec2-140">Host names</span></span>

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

### <span data-ttu-id="d1ec2-141">-Namn</span><span class="sxs-lookup"><span data-stu-id="d1ec2-141">-Name</span></span>
<span data-ttu-id="d1ec2-142">Anger namnet på den frontend-port som kommandot lägger till.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-142">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="d1ec2-143">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="d1ec2-143">-Protocol</span></span>
<span data-ttu-id="d1ec2-144">Anger protokollet för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-144">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="d1ec2-145">Både HTTP och HTTPS stöds.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-145">Both HTTP and HTTPS are supported.</span></span>

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

### <span data-ttu-id="d1ec2-146">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="d1ec2-146">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="d1ec2-147">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="d1ec2-147">-SslCertificate</span></span>
<span data-ttu-id="d1ec2-148">Anger SSL-certifikatet för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-148">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="d1ec2-149">Måste anges om HTTPS har valts som lyssnings protokoll.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-149">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="d1ec2-150">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="d1ec2-150">-SslCertificateId</span></span>
<span data-ttu-id="d1ec2-151">Anger SSL-certifikat-ID för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-151">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="d1ec2-152">Måste anges om HTTPS har valts som lyssnings protokoll.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-152">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="d1ec2-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1ec2-153">CommonParameters</span></span>
<span data-ttu-id="d1ec2-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1ec2-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1ec2-155">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1ec2-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1ec2-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d1ec2-156">INPUTS</span></span>

### <span data-ttu-id="d1ec2-157">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d1ec2-157">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d1ec2-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d1ec2-158">OUTPUTS</span></span>

### <span data-ttu-id="d1ec2-159">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d1ec2-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d1ec2-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d1ec2-160">NOTES</span></span>

## <span data-ttu-id="d1ec2-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d1ec2-161">RELATED LINKS</span></span>

[<span data-ttu-id="d1ec2-162">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d1ec2-162">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="d1ec2-163">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d1ec2-163">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="d1ec2-164">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d1ec2-164">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="d1ec2-165">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d1ec2-165">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


