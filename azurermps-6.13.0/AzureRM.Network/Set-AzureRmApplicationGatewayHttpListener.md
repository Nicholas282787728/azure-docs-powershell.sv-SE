---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 231ee3dc8d66d3960f0416cb410b6747b25ae278
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584047"
---
# <span data-ttu-id="745e1-101">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="745e1-101">Set-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="745e1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="745e1-102">SYNOPSIS</span></span>
<span data-ttu-id="745e1-103">Ändrar en HTTP-lyssnare för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="745e1-103">Modifies an HTTP listener for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="745e1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="745e1-104">SYNTAX</span></span>

### <span data-ttu-id="745e1-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="745e1-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="745e1-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="745e1-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="745e1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="745e1-107">DESCRIPTION</span></span>
<span data-ttu-id="745e1-108">Cmdleten **set-AzureRmApplicationGatewayHttpListener** ändrar en http-lyssnare för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="745e1-108">The **Set-AzureRmApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="745e1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="745e1-109">EXAMPLES</span></span>

### <span data-ttu-id="745e1-110">Exempel 1: Ställ in en HTTP-lyssnare</span><span class="sxs-lookup"><span data-stu-id="745e1-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="745e1-111">Det första kommandot hämtar den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen med namnet ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="745e1-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="745e1-112">Det andra kommandot ställer in HTTP-lyssnaren för gatewayen för att använda front konfigurationen som lagras i $FIP 01 med HTTP-protokollet på port 80.</span><span class="sxs-lookup"><span data-stu-id="745e1-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

## <span data-ttu-id="745e1-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="745e1-113">PARAMETERS</span></span>

### <span data-ttu-id="745e1-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="745e1-114">-ApplicationGateway</span></span>
<span data-ttu-id="745e1-115">Anger den Programgateway som denna cmdlet associerar HTTP-lyssnaren med.</span><span class="sxs-lookup"><span data-stu-id="745e1-115">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="745e1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="745e1-116">-DefaultProfile</span></span>
<span data-ttu-id="745e1-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="745e1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="745e1-118">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="745e1-118">-FrontendIPConfiguration</span></span>
<span data-ttu-id="745e1-119">Anger front-IP-adressen för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="745e1-119">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="745e1-120">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="745e1-120">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="745e1-121">Anger ID för front-IP-adressen för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="745e1-121">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="745e1-122">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="745e1-122">-FrontendPort</span></span>
<span data-ttu-id="745e1-123">Anger front port för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="745e1-123">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="745e1-124">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="745e1-124">-FrontendPortId</span></span>
<span data-ttu-id="745e1-125">Anger front Port-ID för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="745e1-125">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="745e1-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="745e1-126">-HostName</span></span>
<span data-ttu-id="745e1-127">Anger värd namnet som den här cmdleten skickar HTTP-lyssnaren till.</span><span class="sxs-lookup"><span data-stu-id="745e1-127">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="745e1-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="745e1-128">-Name</span></span>
<span data-ttu-id="745e1-129">Anger namnet på HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="745e1-129">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="745e1-130">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="745e1-130">-Protocol</span></span>
<span data-ttu-id="745e1-131">Anger protokollet som HTTP-lyssnaren använder.</span><span class="sxs-lookup"><span data-stu-id="745e1-131">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="745e1-132">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="745e1-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="745e1-133">Inkommande</span><span class="sxs-lookup"><span data-stu-id="745e1-133">Http</span></span>
- <span data-ttu-id="745e1-134">Https</span><span class="sxs-lookup"><span data-stu-id="745e1-134">Https</span></span>

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

### <span data-ttu-id="745e1-135">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="745e1-135">-RequireServerNameIndication</span></span>
<span data-ttu-id="745e1-136">Anger om cmdleten kräver en server namns indikering.</span><span class="sxs-lookup"><span data-stu-id="745e1-136">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="745e1-137">De acceptabla värdena för den här parametern är: true eller false.</span><span class="sxs-lookup"><span data-stu-id="745e1-137">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="745e1-138">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="745e1-138">-SslCertificate</span></span>
<span data-ttu-id="745e1-139">Anger SSL-certifikatet för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="745e1-139">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="745e1-140">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="745e1-140">-SslCertificateId</span></span>
<span data-ttu-id="745e1-141">Anger SSL-certifikat-ID för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="745e1-141">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="745e1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="745e1-142">CommonParameters</span></span>
<span data-ttu-id="745e1-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="745e1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="745e1-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="745e1-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="745e1-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="745e1-145">INPUTS</span></span>

### <span data-ttu-id="745e1-146">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="745e1-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="745e1-147">Parametrar: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="745e1-147">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="745e1-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="745e1-148">OUTPUTS</span></span>

### <span data-ttu-id="745e1-149">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="745e1-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="745e1-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="745e1-150">NOTES</span></span>

## <span data-ttu-id="745e1-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="745e1-151">RELATED LINKS</span></span>

[<span data-ttu-id="745e1-152">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="745e1-152">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="745e1-153">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="745e1-153">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="745e1-154">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="745e1-154">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="745e1-155">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="745e1-155">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)


