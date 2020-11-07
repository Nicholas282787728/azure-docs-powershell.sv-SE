---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: ea07f3b9f2dd1e79f59b3369f3f8d3a8c1434deb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924269"
---
# <span data-ttu-id="f9d5a-101">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f9d5a-101">Set-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="f9d5a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f9d5a-102">SYNOPSIS</span></span>
<span data-ttu-id="f9d5a-103">Ändrar en HTTP-lyssnare för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-103">Modifies an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="f9d5a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f9d5a-104">SYNTAX</span></span>

### <span data-ttu-id="f9d5a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f9d5a-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9d5a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f9d5a-106">SetByResource</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9d5a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f9d5a-107">DESCRIPTION</span></span>
<span data-ttu-id="f9d5a-108">Cmdleten **set-AzApplicationGatewayHttpListener** ändrar en http-lyssnare för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-108">The **Set-AzApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="f9d5a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f9d5a-109">EXAMPLES</span></span>

### <span data-ttu-id="f9d5a-110">Exempel 1: Ställ in en HTTP-lyssnare</span><span class="sxs-lookup"><span data-stu-id="f9d5a-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="f9d5a-111">Det första kommandot hämtar den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen med namnet ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="f9d5a-112">Det andra kommandot ställer in HTTP-lyssnaren för gatewayen för att använda front konfigurationen som lagras i $FIP 01 med HTTP-protokollet på port 80.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

## <span data-ttu-id="f9d5a-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f9d5a-113">PARAMETERS</span></span>

### <span data-ttu-id="f9d5a-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f9d5a-114">-ApplicationGateway</span></span>
<span data-ttu-id="f9d5a-115">Anger den Programgateway som denna cmdlet associerar HTTP-lyssnaren med.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-115">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="f9d5a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9d5a-116">-DefaultProfile</span></span>
<span data-ttu-id="f9d5a-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9d5a-118">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9d5a-118">-FrontendIPConfiguration</span></span>
<span data-ttu-id="f9d5a-119">Anger front-IP-adressen för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-119">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="f9d5a-120">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f9d5a-120">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="f9d5a-121">Anger ID för front-IP-adressen för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-121">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="f9d5a-122">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="f9d5a-122">-FrontendPort</span></span>
<span data-ttu-id="f9d5a-123">Anger front port för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-123">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="f9d5a-124">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="f9d5a-124">-FrontendPortId</span></span>
<span data-ttu-id="f9d5a-125">Anger front Port-ID för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-125">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="f9d5a-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="f9d5a-126">-HostName</span></span>
<span data-ttu-id="f9d5a-127">Anger värd namnet som den här cmdleten skickar HTTP-lyssnaren till.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-127">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="f9d5a-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="f9d5a-128">-Name</span></span>
<span data-ttu-id="f9d5a-129">Anger namnet på HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-129">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="f9d5a-130">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="f9d5a-130">-Protocol</span></span>
<span data-ttu-id="f9d5a-131">Anger protokollet som HTTP-lyssnaren använder.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-131">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="f9d5a-132">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="f9d5a-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f9d5a-133">Inkommande</span><span class="sxs-lookup"><span data-stu-id="f9d5a-133">Http</span></span>
- <span data-ttu-id="f9d5a-134">Https</span><span class="sxs-lookup"><span data-stu-id="f9d5a-134">Https</span></span>

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

### <span data-ttu-id="f9d5a-135">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="f9d5a-135">-RequireServerNameIndication</span></span>
<span data-ttu-id="f9d5a-136">Anger om cmdleten kräver en server namns indikering.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-136">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="f9d5a-137">De acceptabla värdena för den här parametern är: true eller false.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-137">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="f9d5a-138">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="f9d5a-138">-SslCertificate</span></span>
<span data-ttu-id="f9d5a-139">Anger SSL-certifikatet för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-139">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="f9d5a-140">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="f9d5a-140">-SslCertificateId</span></span>
<span data-ttu-id="f9d5a-141">Anger SSL-certifikat-ID för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-141">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="f9d5a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9d5a-142">CommonParameters</span></span>
<span data-ttu-id="f9d5a-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9d5a-144">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9d5a-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9d5a-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f9d5a-145">INPUTS</span></span>

### <span data-ttu-id="f9d5a-146">System. String</span><span class="sxs-lookup"><span data-stu-id="f9d5a-146">System.String</span></span>

## <span data-ttu-id="f9d5a-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f9d5a-147">OUTPUTS</span></span>

### <span data-ttu-id="f9d5a-148">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f9d5a-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f9d5a-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f9d5a-149">NOTES</span></span>

## <span data-ttu-id="f9d5a-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f9d5a-150">RELATED LINKS</span></span>

[<span data-ttu-id="f9d5a-151">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f9d5a-151">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="f9d5a-152">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f9d5a-152">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="f9d5a-153">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f9d5a-153">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="f9d5a-154">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f9d5a-154">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)


