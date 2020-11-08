---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 11a416e237ff4a12dc3aafbd161e1ae77faab732
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918964"
---
# <span data-ttu-id="882b3-101">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="882b3-101">Set-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="882b3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="882b3-102">SYNOPSIS</span></span>
<span data-ttu-id="882b3-103">Ändrar en HTTP-lyssnare för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="882b3-103">Modifies an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="882b3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="882b3-104">SYNTAX</span></span>

### <span data-ttu-id="882b3-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="882b3-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="882b3-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="882b3-106">SetByResource</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="882b3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="882b3-107">DESCRIPTION</span></span>
<span data-ttu-id="882b3-108">Cmdleten **set-AzApplicationGatewayHttpListener** ändrar en http-lyssnare för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="882b3-108">The **Set-AzApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="882b3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="882b3-109">EXAMPLES</span></span>

### <span data-ttu-id="882b3-110">Exempel 1: Ställ in en HTTP-lyssnare</span><span class="sxs-lookup"><span data-stu-id="882b3-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="882b3-111">Det första kommandot hämtar den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen med namnet ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="882b3-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="882b3-112">Det andra kommandot ställer in HTTP-lyssnaren för gatewayen för att använda front konfigurationen som lagras i $FIP 01 med HTTP-protokollet på port 80.</span><span class="sxs-lookup"><span data-stu-id="882b3-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

## <span data-ttu-id="882b3-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="882b3-113">PARAMETERS</span></span>

### <span data-ttu-id="882b3-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="882b3-114">-ApplicationGateway</span></span>
<span data-ttu-id="882b3-115">Anger den Programgateway som denna cmdlet associerar HTTP-lyssnaren med.</span><span class="sxs-lookup"><span data-stu-id="882b3-115">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="882b3-116">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="882b3-116">-CustomErrorConfiguration</span></span>
<span data-ttu-id="882b3-117">Kund fel för en Programgateway</span><span class="sxs-lookup"><span data-stu-id="882b3-117">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="882b3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="882b3-118">-DefaultProfile</span></span>
<span data-ttu-id="882b3-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="882b3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="882b3-120">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="882b3-120">-FrontendIPConfiguration</span></span>
<span data-ttu-id="882b3-121">Anger front-IP-adressen för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="882b3-121">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="882b3-122">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="882b3-122">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="882b3-123">Anger ID för front-IP-adressen för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="882b3-123">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="882b3-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="882b3-124">-FrontendPort</span></span>
<span data-ttu-id="882b3-125">Anger front port för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="882b3-125">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="882b3-126">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="882b3-126">-FrontendPortId</span></span>
<span data-ttu-id="882b3-127">Anger front Port-ID för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="882b3-127">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="882b3-128">-HostName</span><span class="sxs-lookup"><span data-stu-id="882b3-128">-HostName</span></span>
<span data-ttu-id="882b3-129">Anger värd namnet som den här cmdleten skickar HTTP-lyssnaren till.</span><span class="sxs-lookup"><span data-stu-id="882b3-129">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="882b3-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="882b3-130">-Name</span></span>
<span data-ttu-id="882b3-131">Anger namnet på HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="882b3-131">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="882b3-132">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="882b3-132">-Protocol</span></span>
<span data-ttu-id="882b3-133">Anger protokollet som HTTP-lyssnaren använder.</span><span class="sxs-lookup"><span data-stu-id="882b3-133">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="882b3-134">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="882b3-134">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="882b3-135">Inkommande</span><span class="sxs-lookup"><span data-stu-id="882b3-135">Http</span></span>
- <span data-ttu-id="882b3-136">Https</span><span class="sxs-lookup"><span data-stu-id="882b3-136">Https</span></span>

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

### <span data-ttu-id="882b3-137">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="882b3-137">-RequireServerNameIndication</span></span>
<span data-ttu-id="882b3-138">Anger om cmdleten kräver en server namns indikering.</span><span class="sxs-lookup"><span data-stu-id="882b3-138">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="882b3-139">De acceptabla värdena för den här parametern är: true eller false.</span><span class="sxs-lookup"><span data-stu-id="882b3-139">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="882b3-140">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="882b3-140">-SslCertificate</span></span>
<span data-ttu-id="882b3-141">Anger SSL-certifikatet för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="882b3-141">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="882b3-142">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="882b3-142">-SslCertificateId</span></span>
<span data-ttu-id="882b3-143">Anger SSL-certifikat-ID för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="882b3-143">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="882b3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="882b3-144">CommonParameters</span></span>
<span data-ttu-id="882b3-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="882b3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="882b3-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="882b3-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="882b3-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="882b3-147">INPUTS</span></span>

### <span data-ttu-id="882b3-148">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="882b3-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="882b3-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="882b3-149">OUTPUTS</span></span>

### <span data-ttu-id="882b3-150">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="882b3-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="882b3-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="882b3-151">NOTES</span></span>

## <span data-ttu-id="882b3-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="882b3-152">RELATED LINKS</span></span>

[<span data-ttu-id="882b3-153">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="882b3-153">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="882b3-154">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="882b3-154">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="882b3-155">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="882b3-155">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="882b3-156">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="882b3-156">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

