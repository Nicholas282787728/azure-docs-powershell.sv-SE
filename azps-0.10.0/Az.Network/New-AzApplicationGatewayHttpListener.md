---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 104a5e022d89421ac960d699c7391db660c0dd6b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922164"
---
# <span data-ttu-id="3ff57-101">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3ff57-101">New-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="3ff57-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3ff57-102">SYNOPSIS</span></span>
<span data-ttu-id="3ff57-103">Skapar en HTTP-lyssnare för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="3ff57-103">Creates an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="3ff57-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3ff57-104">SYNTAX</span></span>

### <span data-ttu-id="3ff57-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3ff57-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-HostName <String>]
 [-RequireServerNameIndication <String>] -Protocol <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3ff57-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3ff57-106">SetByResource</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ff57-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3ff57-107">DESCRIPTION</span></span>
<span data-ttu-id="3ff57-108">Cmdleten **New-AzApplicationGatewayHttpListener** skapar en http-lyssnare för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="3ff57-108">The **New-AzApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="3ff57-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3ff57-109">EXAMPLES</span></span>

### <span data-ttu-id="3ff57-110">Exempel 1: skapa en HTTP-lyssnare</span><span class="sxs-lookup"><span data-stu-id="3ff57-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="3ff57-111">Det här kommandot skapar en HTTP-lyssnare som heter Listener01 och lagrar resultatet i variabeln som heter $Listener.</span><span class="sxs-lookup"><span data-stu-id="3ff57-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="3ff57-112">Exempel 2: skapa en HTTP-lyssnare med SSL</span><span class="sxs-lookup"><span data-stu-id="3ff57-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="3ff57-113">Det här kommandot skapar en HTTP-lyssnare som använder SSL Offload och tillhandahåller SSL-certifikatet i variabeln $SSLCert 01.</span><span class="sxs-lookup"><span data-stu-id="3ff57-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="3ff57-114">Kommandot lagrar resultatet i variabeln som heter $Listener.</span><span class="sxs-lookup"><span data-stu-id="3ff57-114">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="3ff57-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3ff57-115">PARAMETERS</span></span>

### <span data-ttu-id="3ff57-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ff57-116">-DefaultProfile</span></span>
<span data-ttu-id="3ff57-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3ff57-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ff57-118">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ff57-118">-FrontendIPConfiguration</span></span>
<span data-ttu-id="3ff57-119">Anger front-IP-konfigurationsobjekt för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="3ff57-119">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="3ff57-120">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="3ff57-120">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="3ff57-121">Anger ID för front-IP-konfigurationen för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="3ff57-121">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="3ff57-122">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="3ff57-122">-FrontendPort</span></span>
<span data-ttu-id="3ff57-123">Anger front porten för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="3ff57-123">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="3ff57-124">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="3ff57-124">-FrontendPortId</span></span>
<span data-ttu-id="3ff57-125">Anger ID för front porten för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="3ff57-125">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="3ff57-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="3ff57-126">-HostName</span></span>
<span data-ttu-id="3ff57-127">Anger värd namnet för Programgateway HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="3ff57-127">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="3ff57-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="3ff57-128">-Name</span></span>
<span data-ttu-id="3ff57-129">Anger namnet på den HTTP-lyssnare som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="3ff57-129">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="3ff57-130">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="3ff57-130">-Protocol</span></span>
<span data-ttu-id="3ff57-131">Anger protokollet som HTTP-lyssnaren använder.</span><span class="sxs-lookup"><span data-stu-id="3ff57-131">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="3ff57-132">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="3ff57-132">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="3ff57-133">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="3ff57-133">-SslCertificate</span></span>
<span data-ttu-id="3ff57-134">Anger SSL-certifikatet för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="3ff57-134">Specifies the SSL certificate object for  the HTTP listener.</span></span>

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

### <span data-ttu-id="3ff57-135">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="3ff57-135">-SslCertificateId</span></span>
<span data-ttu-id="3ff57-136">Anger ID för SSL-certifikatet för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="3ff57-136">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="3ff57-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ff57-137">CommonParameters</span></span>
<span data-ttu-id="3ff57-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ff57-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ff57-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ff57-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ff57-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3ff57-140">INPUTS</span></span>

### <span data-ttu-id="3ff57-141">System. String</span><span class="sxs-lookup"><span data-stu-id="3ff57-141">System.String</span></span>

## <span data-ttu-id="3ff57-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3ff57-142">OUTPUTS</span></span>

### <span data-ttu-id="3ff57-143">Microsoft. Azure. commands. Networks. Models. PSHttpListener</span><span class="sxs-lookup"><span data-stu-id="3ff57-143">Microsoft.Azure.Commands.Network.Models.PSHttpListener</span></span>

## <span data-ttu-id="3ff57-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3ff57-144">NOTES</span></span>

## <span data-ttu-id="3ff57-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3ff57-145">RELATED LINKS</span></span>

[<span data-ttu-id="3ff57-146">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3ff57-146">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="3ff57-147">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3ff57-147">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="3ff57-148">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3ff57-148">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="3ff57-149">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3ff57-149">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


