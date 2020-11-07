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
ms.locfileid: "93918851"
---
# <span data-ttu-id="4f752-101">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4f752-101">Add-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="4f752-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4f752-102">SYNOPSIS</span></span>
<span data-ttu-id="4f752-103">Lägger till en HTTP-lyssnare till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="4f752-103">Adds an HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="4f752-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4f752-104">SYNTAX</span></span>

### <span data-ttu-id="4f752-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4f752-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4f752-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4f752-106">SetByResource</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4f752-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4f752-107">DESCRIPTION</span></span>
<span data-ttu-id="4f752-108">Cmdleten **Add-AzApplicationGatewayHttpListener** lägger till en http-lyssnare till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="4f752-108">The **Add-AzApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="4f752-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4f752-109">EXAMPLES</span></span>

### <span data-ttu-id="4f752-110">Exempel 1: lägga till en HTTP-lyssnare</span><span class="sxs-lookup"><span data-stu-id="4f752-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="4f752-111">Med det första kommandot hämtas programgatewayen och lagras i $AppGw variabeln. Med det andra kommandot läggs HTTP-lyssnaren till i programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="4f752-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="4f752-112">Exempel 2: lägga till en HTTPS-lyssnare med SSL</span><span class="sxs-lookup"><span data-stu-id="4f752-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="4f752-113">Med det första kommandot hämtas programgatewayen och lagras i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="4f752-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4f752-114">Det andra kommandot lägger till lyssnaren som använder HTTPS-protokollet för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="4f752-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

## <span data-ttu-id="4f752-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4f752-115">PARAMETERS</span></span>

### <span data-ttu-id="4f752-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4f752-116">-ApplicationGateway</span></span>
<span data-ttu-id="4f752-117">Anger den Programgateway som denna cmdlet lägger till en HTTP-lyssnare i.</span><span class="sxs-lookup"><span data-stu-id="4f752-117">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="4f752-118">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="4f752-118">-CustomErrorConfiguration</span></span>
<span data-ttu-id="4f752-119">Kund fel för en Programgateway</span><span class="sxs-lookup"><span data-stu-id="4f752-119">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="4f752-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f752-120">-DefaultProfile</span></span>
<span data-ttu-id="4f752-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4f752-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f752-122">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4f752-122">-FrontendIPConfiguration</span></span>
<span data-ttu-id="4f752-123">Anger front-IP-startobjektet för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="4f752-123">Specifies the application gateway front-end IP resource object.</span></span>

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

### <span data-ttu-id="4f752-124">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="4f752-124">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="4f752-125">Anger start-ID för front-Gateway.</span><span class="sxs-lookup"><span data-stu-id="4f752-125">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="4f752-126">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="4f752-126">-FrontendPort</span></span>
<span data-ttu-id="4f752-127">Anger front-end port-objekt för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="4f752-127">Specifies the application gateway front-end port object.</span></span>

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

### <span data-ttu-id="4f752-128">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="4f752-128">-FrontendPortId</span></span>
<span data-ttu-id="4f752-129">Anger front Port-ID för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="4f752-129">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="4f752-130">-HostName</span><span class="sxs-lookup"><span data-stu-id="4f752-130">-HostName</span></span>
<span data-ttu-id="4f752-131">Anger värd namnet som denna cmdlet lägger till en HTTP-lyssnare på.</span><span class="sxs-lookup"><span data-stu-id="4f752-131">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

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

### <span data-ttu-id="4f752-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="4f752-132">-Name</span></span>
<span data-ttu-id="4f752-133">Anger namnet på den frontend-port som kommandot lägger till.</span><span class="sxs-lookup"><span data-stu-id="4f752-133">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="4f752-134">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="4f752-134">-Protocol</span></span>
<span data-ttu-id="4f752-135">Anger protokollet för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="4f752-135">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="4f752-136">Både HTTP och HTTPS stöds.</span><span class="sxs-lookup"><span data-stu-id="4f752-136">Both HTTP and HTTPS are supported.</span></span>

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

### <span data-ttu-id="4f752-137">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="4f752-137">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="4f752-138">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="4f752-138">-SslCertificate</span></span>
<span data-ttu-id="4f752-139">Anger SSL-certifikatet för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="4f752-139">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="4f752-140">Måste anges om HTTPS har valts som lyssnings protokoll.</span><span class="sxs-lookup"><span data-stu-id="4f752-140">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="4f752-141">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="4f752-141">-SslCertificateId</span></span>
<span data-ttu-id="4f752-142">Anger SSL-certifikat-ID för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="4f752-142">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="4f752-143">Måste anges om HTTPS har valts som lyssnings protokoll.</span><span class="sxs-lookup"><span data-stu-id="4f752-143">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="4f752-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f752-144">CommonParameters</span></span>
<span data-ttu-id="4f752-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f752-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f752-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f752-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f752-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4f752-147">INPUTS</span></span>

### <span data-ttu-id="4f752-148">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4f752-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4f752-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4f752-149">OUTPUTS</span></span>

### <span data-ttu-id="4f752-150">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4f752-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4f752-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4f752-151">NOTES</span></span>

## <span data-ttu-id="4f752-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4f752-152">RELATED LINKS</span></span>

[<span data-ttu-id="4f752-153">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4f752-153">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="4f752-154">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4f752-154">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="4f752-155">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4f752-155">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="4f752-156">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4f752-156">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


