---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 5648bb1cb7497517afb5ff461674294e426c0131
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753975"
---
# <span data-ttu-id="c7d44-101">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c7d44-101">Add-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="c7d44-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c7d44-102">SYNOPSIS</span></span>
<span data-ttu-id="c7d44-103">Lägger till en HTTP-lyssnare till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="c7d44-103">Adds an HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="c7d44-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c7d44-104">SYNTAX</span></span>

### <span data-ttu-id="c7d44-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c7d44-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c7d44-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c7d44-106">SetByResource</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c7d44-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c7d44-107">DESCRIPTION</span></span>
<span data-ttu-id="c7d44-108">Cmdleten **Add-AzApplicationGatewayHttpListener** lägger till en http-lyssnare till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="c7d44-108">The **Add-AzApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="c7d44-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c7d44-109">EXAMPLES</span></span>

### <span data-ttu-id="c7d44-110">Exempel 1: lägga till en HTTP-lyssnare</span><span class="sxs-lookup"><span data-stu-id="c7d44-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="c7d44-111">Med det första kommandot hämtas programgatewayen och lagras i $AppGw variabeln. Med det andra kommandot läggs HTTP-lyssnaren till i programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="c7d44-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="c7d44-112">Exempel 2: lägga till en HTTPS-lyssnare med SSL</span><span class="sxs-lookup"><span data-stu-id="c7d44-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="c7d44-113">Med det första kommandot hämtas programgatewayen och lagras i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="c7d44-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c7d44-114">Det andra kommandot lägger till lyssnaren som använder HTTPS-protokollet för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="c7d44-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

## <span data-ttu-id="c7d44-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c7d44-115">PARAMETERS</span></span>

### <span data-ttu-id="c7d44-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c7d44-116">-ApplicationGateway</span></span>
<span data-ttu-id="c7d44-117">Anger den Programgateway som denna cmdlet lägger till en HTTP-lyssnare i.</span><span class="sxs-lookup"><span data-stu-id="c7d44-117">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="c7d44-118">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7d44-118">-CustomErrorConfiguration</span></span>
<span data-ttu-id="c7d44-119">Kund fel för en Programgateway</span><span class="sxs-lookup"><span data-stu-id="c7d44-119">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="c7d44-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7d44-120">-DefaultProfile</span></span>
<span data-ttu-id="c7d44-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c7d44-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7d44-122">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7d44-122">-FrontendIPConfiguration</span></span>
<span data-ttu-id="c7d44-123">Anger front-IP-startobjektet för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="c7d44-123">Specifies the application gateway front-end IP resource object.</span></span>

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

### <span data-ttu-id="c7d44-124">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c7d44-124">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="c7d44-125">Anger start-ID för front-Gateway.</span><span class="sxs-lookup"><span data-stu-id="c7d44-125">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="c7d44-126">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="c7d44-126">-FrontendPort</span></span>
<span data-ttu-id="c7d44-127">Anger front-end port-objekt för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="c7d44-127">Specifies the application gateway front-end port object.</span></span>

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

### <span data-ttu-id="c7d44-128">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="c7d44-128">-FrontendPortId</span></span>
<span data-ttu-id="c7d44-129">Anger front Port-ID för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="c7d44-129">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="c7d44-130">-HostName</span><span class="sxs-lookup"><span data-stu-id="c7d44-130">-HostName</span></span>
<span data-ttu-id="c7d44-131">Anger värd namnet som denna cmdlet lägger till en HTTP-lyssnare på.</span><span class="sxs-lookup"><span data-stu-id="c7d44-131">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

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

### <span data-ttu-id="c7d44-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="c7d44-132">-Name</span></span>
<span data-ttu-id="c7d44-133">Anger namnet på den frontend-port som kommandot lägger till.</span><span class="sxs-lookup"><span data-stu-id="c7d44-133">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="c7d44-134">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="c7d44-134">-Protocol</span></span>
<span data-ttu-id="c7d44-135">Anger protokollet för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="c7d44-135">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="c7d44-136">Både HTTP och HTTPS stöds.</span><span class="sxs-lookup"><span data-stu-id="c7d44-136">Both HTTP and HTTPS are supported.</span></span>

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

### <span data-ttu-id="c7d44-137">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="c7d44-137">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="c7d44-138">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="c7d44-138">-SslCertificate</span></span>
<span data-ttu-id="c7d44-139">Anger SSL-certifikatet för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="c7d44-139">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="c7d44-140">Måste anges om HTTPS har valts som lyssnings protokoll.</span><span class="sxs-lookup"><span data-stu-id="c7d44-140">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="c7d44-141">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="c7d44-141">-SslCertificateId</span></span>
<span data-ttu-id="c7d44-142">Anger SSL-certifikat-ID för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="c7d44-142">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="c7d44-143">Måste anges om HTTPS har valts som lyssnings protokoll.</span><span class="sxs-lookup"><span data-stu-id="c7d44-143">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="c7d44-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7d44-144">CommonParameters</span></span>
<span data-ttu-id="c7d44-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7d44-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7d44-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7d44-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7d44-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c7d44-147">INPUTS</span></span>

### <span data-ttu-id="c7d44-148">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c7d44-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c7d44-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c7d44-149">OUTPUTS</span></span>

### <span data-ttu-id="c7d44-150">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c7d44-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c7d44-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c7d44-151">NOTES</span></span>

## <span data-ttu-id="c7d44-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c7d44-152">RELATED LINKS</span></span>

[<span data-ttu-id="c7d44-153">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c7d44-153">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="c7d44-154">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c7d44-154">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="c7d44-155">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c7d44-155">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="c7d44-156">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c7d44-156">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


