---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: e5593ae97692813cc36f14942edb21768517f317
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918342"
---
# <span data-ttu-id="9e3ea-101">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9e3ea-101">New-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="9e3ea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9e3ea-102">SYNOPSIS</span></span>
<span data-ttu-id="9e3ea-103">Skapar en HTTP-lyssnare för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="9e3ea-103">Creates an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="9e3ea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9e3ea-104">SYNTAX</span></span>

### <span data-ttu-id="9e3ea-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9e3ea-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-HostName <String>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9e3ea-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9e3ea-106">SetByResource</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e3ea-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9e3ea-107">DESCRIPTION</span></span>
<span data-ttu-id="9e3ea-108">Cmdleten **New-AzApplicationGatewayHttpListener** skapar en http-lyssnare för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="9e3ea-108">The **New-AzApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="9e3ea-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9e3ea-109">EXAMPLES</span></span>

### <span data-ttu-id="9e3ea-110">Exempel 1: skapa en HTTP-lyssnare</span><span class="sxs-lookup"><span data-stu-id="9e3ea-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="9e3ea-111">Det här kommandot skapar en HTTP-lyssnare som heter Listener01 och lagrar resultatet i variabeln som heter $Listener.</span><span class="sxs-lookup"><span data-stu-id="9e3ea-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="9e3ea-112">Exempel 2: skapa en HTTP-lyssnare med SSL</span><span class="sxs-lookup"><span data-stu-id="9e3ea-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="9e3ea-113">Det här kommandot skapar en HTTP-lyssnare som använder SSL Offload och tillhandahåller SSL-certifikatet i variabeln $SSLCert 01.</span><span class="sxs-lookup"><span data-stu-id="9e3ea-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="9e3ea-114">Kommandot lagrar resultatet i variabeln som heter $Listener.</span><span class="sxs-lookup"><span data-stu-id="9e3ea-114">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="9e3ea-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9e3ea-115">PARAMETERS</span></span>

### <span data-ttu-id="9e3ea-116">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e3ea-116">-CustomErrorConfiguration</span></span>
<span data-ttu-id="9e3ea-117">Kund fel för en Programgateway</span><span class="sxs-lookup"><span data-stu-id="9e3ea-117">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="9e3ea-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e3ea-118">-DefaultProfile</span></span>
<span data-ttu-id="9e3ea-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9e3ea-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e3ea-120">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e3ea-120">-FrontendIPConfiguration</span></span>
<span data-ttu-id="9e3ea-121">Anger front-IP-konfigurationsobjekt för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="9e3ea-121">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="9e3ea-122">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="9e3ea-122">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="9e3ea-123">Anger ID för front-IP-konfigurationen för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="9e3ea-123">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="9e3ea-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="9e3ea-124">-FrontendPort</span></span>
<span data-ttu-id="9e3ea-125">Anger front porten för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="9e3ea-125">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="9e3ea-126">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="9e3ea-126">-FrontendPortId</span></span>
<span data-ttu-id="9e3ea-127">Anger ID för front porten för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="9e3ea-127">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="9e3ea-128">-HostName</span><span class="sxs-lookup"><span data-stu-id="9e3ea-128">-HostName</span></span>
<span data-ttu-id="9e3ea-129">Anger värd namnet för Programgateway HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="9e3ea-129">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="9e3ea-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="9e3ea-130">-Name</span></span>
<span data-ttu-id="9e3ea-131">Anger namnet på den HTTP-lyssnare som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="9e3ea-131">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="9e3ea-132">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="9e3ea-132">-Protocol</span></span>
<span data-ttu-id="9e3ea-133">Anger protokollet som HTTP-lyssnaren använder.</span><span class="sxs-lookup"><span data-stu-id="9e3ea-133">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="9e3ea-134">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="9e3ea-134">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="9e3ea-135">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="9e3ea-135">-SslCertificate</span></span>
<span data-ttu-id="9e3ea-136">Anger SSL-certifikatet för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="9e3ea-136">Specifies the SSL certificate object for the HTTP listener.</span></span>

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

### <span data-ttu-id="9e3ea-137">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="9e3ea-137">-SslCertificateId</span></span>
<span data-ttu-id="9e3ea-138">Anger ID för SSL-certifikatet för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="9e3ea-138">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="9e3ea-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e3ea-139">CommonParameters</span></span>
<span data-ttu-id="9e3ea-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e3ea-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e3ea-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e3ea-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e3ea-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9e3ea-142">INPUTS</span></span>

### <span data-ttu-id="9e3ea-143">Ingen</span><span class="sxs-lookup"><span data-stu-id="9e3ea-143">None</span></span>

## <span data-ttu-id="9e3ea-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9e3ea-144">OUTPUTS</span></span>

### <span data-ttu-id="9e3ea-145">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9e3ea-145">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="9e3ea-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9e3ea-146">NOTES</span></span>

## <span data-ttu-id="9e3ea-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9e3ea-147">RELATED LINKS</span></span>

[<span data-ttu-id="9e3ea-148">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9e3ea-148">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="9e3ea-149">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9e3ea-149">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="9e3ea-150">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9e3ea-150">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="9e3ea-151">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9e3ea-151">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


