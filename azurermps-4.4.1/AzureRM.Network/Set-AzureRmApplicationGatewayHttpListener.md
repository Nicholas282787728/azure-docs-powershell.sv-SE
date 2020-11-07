---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 6805eaa6f1d710c607a7911b628d3642d48ece29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756327"
---
# <span data-ttu-id="d6691-101">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d6691-101">Set-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="d6691-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d6691-102">SYNOPSIS</span></span>
<span data-ttu-id="d6691-103">Ändrar en HTTP-lyssnare för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="d6691-103">Modifies an HTTP listener for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6691-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d6691-104">SYNTAX</span></span>

### <span data-ttu-id="d6691-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d6691-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6691-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d6691-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6691-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d6691-107">DESCRIPTION</span></span>
<span data-ttu-id="d6691-108">Cmdleten **set-AzureRmApplicationGatewayHttpListener** ändrar en http-lyssnare för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="d6691-108">The **Set-AzureRmApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="d6691-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d6691-109">EXAMPLES</span></span>

### <span data-ttu-id="d6691-110">Exempel 1: Ställ in en HTTP-lyssnare</span><span class="sxs-lookup"><span data-stu-id="d6691-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="d6691-111">Det första kommandot hämtar den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen med namnet ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="d6691-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="d6691-112">Det andra kommandot ställer in HTTP-lyssnaren för gatewayen för att använda front konfigurationen som lagras i $FIP 01 med HTTP-protokollet på port 80.</span><span class="sxs-lookup"><span data-stu-id="d6691-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

## <span data-ttu-id="d6691-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d6691-113">PARAMETERS</span></span>

### <span data-ttu-id="d6691-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d6691-114">-ApplicationGateway</span></span>
<span data-ttu-id="d6691-115">Anger den Programgateway som denna cmdlet associerar HTTP-lyssnaren med.</span><span class="sxs-lookup"><span data-stu-id="d6691-115">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="d6691-116">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6691-116">-FrontendIPConfiguration</span></span>
<span data-ttu-id="d6691-117">Anger front-IP-adressen för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="d6691-117">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="d6691-118">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d6691-118">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="d6691-119">Anger ID för front-IP-adressen för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="d6691-119">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="d6691-120">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="d6691-120">-FrontendPort</span></span>
<span data-ttu-id="d6691-121">Anger front port för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="d6691-121">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="d6691-122">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="d6691-122">-FrontendPortId</span></span>
<span data-ttu-id="d6691-123">Anger front Port-ID för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="d6691-123">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="d6691-124">-HostName</span><span class="sxs-lookup"><span data-stu-id="d6691-124">-HostName</span></span>
<span data-ttu-id="d6691-125">Anger värd namnet som den här cmdleten skickar HTTP-lyssnaren till.</span><span class="sxs-lookup"><span data-stu-id="d6691-125">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="d6691-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="d6691-126">-Name</span></span>
<span data-ttu-id="d6691-127">Anger namnet på HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="d6691-127">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="d6691-128">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="d6691-128">-Protocol</span></span>
<span data-ttu-id="d6691-129">Anger protokollet som HTTP-lyssnaren använder.</span><span class="sxs-lookup"><span data-stu-id="d6691-129">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="d6691-130">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="d6691-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d6691-131">Inkommande</span><span class="sxs-lookup"><span data-stu-id="d6691-131">Http</span></span>
- <span data-ttu-id="d6691-132">Https</span><span class="sxs-lookup"><span data-stu-id="d6691-132">Https</span></span>

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

### <span data-ttu-id="d6691-133">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="d6691-133">-RequireServerNameIndication</span></span>
<span data-ttu-id="d6691-134">Anger om cmdleten kräver en server namns indikering.</span><span class="sxs-lookup"><span data-stu-id="d6691-134">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="d6691-135">De acceptabla värdena för den här parametern är: true eller false.</span><span class="sxs-lookup"><span data-stu-id="d6691-135">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="d6691-136">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="d6691-136">-SslCertificate</span></span>
<span data-ttu-id="d6691-137">Anger SSL-certifikatet för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="d6691-137">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="d6691-138">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="d6691-138">-SslCertificateId</span></span>
<span data-ttu-id="d6691-139">Anger SSL-certifikat-ID för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="d6691-139">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="d6691-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6691-140">-DefaultProfile</span></span>
<span data-ttu-id="d6691-141">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d6691-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6691-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6691-142">CommonParameters</span></span>
<span data-ttu-id="d6691-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6691-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6691-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6691-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6691-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d6691-145">INPUTS</span></span>

### <span data-ttu-id="d6691-146">System. String</span><span class="sxs-lookup"><span data-stu-id="d6691-146">System.String</span></span>

## <span data-ttu-id="d6691-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d6691-147">OUTPUTS</span></span>

### <span data-ttu-id="d6691-148">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d6691-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d6691-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d6691-149">NOTES</span></span>

## <span data-ttu-id="d6691-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d6691-150">RELATED LINKS</span></span>

[<span data-ttu-id="d6691-151">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d6691-151">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="d6691-152">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d6691-152">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="d6691-153">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d6691-153">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="d6691-154">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d6691-154">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)


