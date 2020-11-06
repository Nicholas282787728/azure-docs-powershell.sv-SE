---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 29df7c4ac7cb941e8826c3e1fb929d92cc626512
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580795"
---
# <span data-ttu-id="e0d4d-101">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="e0d4d-101">New-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="e0d4d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e0d4d-102">SYNOPSIS</span></span>
<span data-ttu-id="e0d4d-103">Skapar en HTTP-lyssnare för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="e0d4d-103">Creates an HTTP listener for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0d4d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e0d4d-104">SYNTAX</span></span>

### <span data-ttu-id="e0d4d-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e0d4d-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-HostName <String>]
 [-RequireServerNameIndication <String>] -Protocol <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e0d4d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e0d4d-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0d4d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e0d4d-107">DESCRIPTION</span></span>
<span data-ttu-id="e0d4d-108">Cmdleten **New-AzureRmApplicationGatewayHttpListener** skapar en http-lyssnare för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="e0d4d-108">The **New-AzureRmApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="e0d4d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e0d4d-109">EXAMPLES</span></span>

### <span data-ttu-id="e0d4d-110">Exempel 1: skapa en HTTP-lyssnare</span><span class="sxs-lookup"><span data-stu-id="e0d4d-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzureRmApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="e0d4d-111">Det här kommandot skapar en HTTP-lyssnare som heter Listener01 och lagrar resultatet i variabeln som heter $Listener.</span><span class="sxs-lookup"><span data-stu-id="e0d4d-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="e0d4d-112">Exempel 2: skapa en HTTP-lyssnare med SSL</span><span class="sxs-lookup"><span data-stu-id="e0d4d-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzureRmApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="e0d4d-113">Det här kommandot skapar en HTTP-lyssnare som använder SSL Offload och tillhandahåller SSL-certifikatet i variabeln $SSLCert 01.</span><span class="sxs-lookup"><span data-stu-id="e0d4d-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="e0d4d-114">Kommandot lagrar resultatet i variabeln som heter $Listener.</span><span class="sxs-lookup"><span data-stu-id="e0d4d-114">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="e0d4d-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e0d4d-115">PARAMETERS</span></span>

### <span data-ttu-id="e0d4d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0d4d-116">-DefaultProfile</span></span>
<span data-ttu-id="e0d4d-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e0d4d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0d4d-118">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e0d4d-118">-FrontendIPConfiguration</span></span>
<span data-ttu-id="e0d4d-119">Anger front-IP-konfigurationsobjekt för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="e0d4d-119">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="e0d4d-120">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e0d4d-120">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="e0d4d-121">Anger ID för front-IP-konfigurationen för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="e0d4d-121">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="e0d4d-122">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="e0d4d-122">-FrontendPort</span></span>
<span data-ttu-id="e0d4d-123">Anger front porten för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="e0d4d-123">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="e0d4d-124">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="e0d4d-124">-FrontendPortId</span></span>
<span data-ttu-id="e0d4d-125">Anger ID för front porten för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="e0d4d-125">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="e0d4d-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="e0d4d-126">-HostName</span></span>
<span data-ttu-id="e0d4d-127">Anger värd namnet för Programgateway HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="e0d4d-127">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="e0d4d-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="e0d4d-128">-Name</span></span>
<span data-ttu-id="e0d4d-129">Anger namnet på den HTTP-lyssnare som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="e0d4d-129">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="e0d4d-130">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="e0d4d-130">-Protocol</span></span>
<span data-ttu-id="e0d4d-131">Anger protokollet som HTTP-lyssnaren använder.</span><span class="sxs-lookup"><span data-stu-id="e0d4d-131">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="e0d4d-132">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="e0d4d-132">-RequireServerNameIndication</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: true, false

Required: False
Position: Named
Default value: true
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0d4d-133">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="e0d4d-133">-SslCertificate</span></span>
<span data-ttu-id="e0d4d-134">Anger SSL-certifikatet för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="e0d4d-134">Specifies the SSL certificate object for  the HTTP listener.</span></span>

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

### <span data-ttu-id="e0d4d-135">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="e0d4d-135">-SslCertificateId</span></span>
<span data-ttu-id="e0d4d-136">Anger ID för SSL-certifikatet för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="e0d4d-136">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="e0d4d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0d4d-137">CommonParameters</span></span>
<span data-ttu-id="e0d4d-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0d4d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0d4d-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0d4d-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0d4d-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e0d4d-140">INPUTS</span></span>

### <span data-ttu-id="e0d4d-141">Ingen</span><span class="sxs-lookup"><span data-stu-id="e0d4d-141">None</span></span>

## <span data-ttu-id="e0d4d-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e0d4d-142">OUTPUTS</span></span>

### <span data-ttu-id="e0d4d-143">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="e0d4d-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="e0d4d-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e0d4d-144">NOTES</span></span>

## <span data-ttu-id="e0d4d-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e0d4d-145">RELATED LINKS</span></span>

[<span data-ttu-id="e0d4d-146">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="e0d4d-146">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="e0d4d-147">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="e0d4d-147">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="e0d4d-148">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="e0d4d-148">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="e0d4d-149">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="e0d4d-149">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


