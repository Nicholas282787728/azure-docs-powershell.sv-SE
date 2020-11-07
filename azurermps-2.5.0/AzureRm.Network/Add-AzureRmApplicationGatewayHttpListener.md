---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayhttplistener
schema: 2.0.0
ms.openlocfilehash: bda8ce00d316d57522bb307518c535c591e7b602
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931393"
---
# <span data-ttu-id="ca7d5-101">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ca7d5-101">Add-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="ca7d5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ca7d5-102">SYNOPSIS</span></span>
<span data-ttu-id="ca7d5-103">Lägger till en HTTP-lyssnare till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="ca7d5-103">Adds an HTTP listener to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca7d5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ca7d5-104">SYNTAX</span></span>

### <span data-ttu-id="ca7d5-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ca7d5-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca7d5-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ca7d5-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca7d5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ca7d5-107">DESCRIPTION</span></span>
<span data-ttu-id="ca7d5-108">Cmdleten **Add-AzureRmApplicationGatewayHttpListener** lägger till en http-lyssnare till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="ca7d5-108">The **Add-AzureRmApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="ca7d5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ca7d5-109">EXAMPLES</span></span>

### <span data-ttu-id="ca7d5-110">Exempel 1: lägga till en HTTP-lyssnare</span><span class="sxs-lookup"><span data-stu-id="ca7d5-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="ca7d5-111">Med det första kommandot hämtas programgatewayen och lagras i $AppGw variabeln. Med det andra kommandot läggs HTTP-lyssnaren till i programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="ca7d5-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="ca7d5-112">Exempel 2: lägga till en HTTPS-lyssnare med SSL</span><span class="sxs-lookup"><span data-stu-id="ca7d5-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="ca7d5-113">Med det första kommandot hämtas programgatewayen och lagras i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="ca7d5-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ca7d5-114">Det andra kommandot lägger till lyssnaren som använder HTTPS-protokollet för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="ca7d5-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

## <span data-ttu-id="ca7d5-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ca7d5-115">PARAMETERS</span></span>

### <span data-ttu-id="ca7d5-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ca7d5-116">-ApplicationGateway</span></span>
<span data-ttu-id="ca7d5-117">Anger den Programgateway som denna cmdlet lägger till en HTTP-lyssnare i.</span><span class="sxs-lookup"><span data-stu-id="ca7d5-117">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca7d5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca7d5-118">-DefaultProfile</span></span>
<span data-ttu-id="ca7d5-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ca7d5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca7d5-120">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca7d5-120">-FrontendIPConfiguration</span></span>
<span data-ttu-id="ca7d5-121">Anger front-IP-startobjektet för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="ca7d5-121">Specifies the application gateway front-end IP resource object.</span></span>

```yaml
Type: PSApplicationGatewayFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca7d5-122">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="ca7d5-122">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="ca7d5-123">Anger start-ID för front-Gateway.</span><span class="sxs-lookup"><span data-stu-id="ca7d5-123">Specifies the application gateway front-end IP ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca7d5-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="ca7d5-124">-FrontendPort</span></span>
<span data-ttu-id="ca7d5-125">Anger front-end port-objekt för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="ca7d5-125">Specifies the application gateway front-end port object.</span></span>

```yaml
Type: PSApplicationGatewayFrontendPort
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca7d5-126">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="ca7d5-126">-FrontendPortId</span></span>
<span data-ttu-id="ca7d5-127">Anger front Port-ID för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="ca7d5-127">Specifies the application gateway front-end port ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca7d5-128">-HostName</span><span class="sxs-lookup"><span data-stu-id="ca7d5-128">-HostName</span></span>
<span data-ttu-id="ca7d5-129">Anger värd namnet som denna cmdlet lägger till en HTTP-lyssnare på.</span><span class="sxs-lookup"><span data-stu-id="ca7d5-129">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca7d5-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="ca7d5-130">-Name</span></span>
<span data-ttu-id="ca7d5-131">Anger namnet på den frontend-port som kommandot lägger till.</span><span class="sxs-lookup"><span data-stu-id="ca7d5-131">Specifies the name of the front-end port that this command adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca7d5-132">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="ca7d5-132">-Protocol</span></span>
<span data-ttu-id="ca7d5-133">Anger protokollet för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="ca7d5-133">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="ca7d5-134">Både HTTP och HTTPS stöds.</span><span class="sxs-lookup"><span data-stu-id="ca7d5-134">Both HTTP and HTTPS are supported.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca7d5-135">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="ca7d5-135">-RequireServerNameIndication</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: true, false

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca7d5-136">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="ca7d5-136">-SslCertificate</span></span>
<span data-ttu-id="ca7d5-137">Anger SSL-certifikatet för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="ca7d5-137">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="ca7d5-138">Måste anges om HTTPS har valts som lyssnings protokoll.</span><span class="sxs-lookup"><span data-stu-id="ca7d5-138">Must be specified if HTTPS is chosen as listener protocol.</span></span>

```yaml
Type: PSApplicationGatewaySslCertificate
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca7d5-139">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="ca7d5-139">-SslCertificateId</span></span>
<span data-ttu-id="ca7d5-140">Anger SSL-certifikat-ID för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="ca7d5-140">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="ca7d5-141">Måste anges om HTTPS har valts som lyssnings protokoll.</span><span class="sxs-lookup"><span data-stu-id="ca7d5-141">Must be specified if HTTPS is chosen as listener protocol.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca7d5-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca7d5-142">CommonParameters</span></span>
<span data-ttu-id="ca7d5-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca7d5-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca7d5-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca7d5-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca7d5-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ca7d5-145">INPUTS</span></span>

### <span data-ttu-id="ca7d5-146">System. String</span><span class="sxs-lookup"><span data-stu-id="ca7d5-146">System.String</span></span>

## <span data-ttu-id="ca7d5-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ca7d5-147">OUTPUTS</span></span>

### <span data-ttu-id="ca7d5-148">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ca7d5-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ca7d5-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ca7d5-149">NOTES</span></span>

## <span data-ttu-id="ca7d5-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ca7d5-150">RELATED LINKS</span></span>

[<span data-ttu-id="ca7d5-151">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ca7d5-151">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="ca7d5-152">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ca7d5-152">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="ca7d5-153">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ca7d5-153">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="ca7d5-154">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ca7d5-154">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


