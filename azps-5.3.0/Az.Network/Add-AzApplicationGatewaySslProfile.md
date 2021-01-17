---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 8930041959712b7533651262a39409e884ffb177
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422344"
---
# <span data-ttu-id="a499d-101">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="a499d-101">Add-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="a499d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a499d-102">SYNOPSIS</span></span>
<span data-ttu-id="a499d-103">Lägger till SSL-profil till en programport.</span><span class="sxs-lookup"><span data-stu-id="a499d-103">Adds SSL profile to an application gateway.</span></span>

## <span data-ttu-id="a499d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a499d-104">SYNTAX</span></span>

```
Add-AzApplicationGatewaySslProfile -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SslPolicy <PSApplicationGatewaySslPolicy>]
 [-ClientAuthConfiguration <PSApplicationGatewayClientAuthConfiguration>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a499d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a499d-105">DESCRIPTION</span></span>
<span data-ttu-id="a499d-106">Cmdleten **Add-AzApplicationGatewaySslProfile** lägger till en SSL-profil till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="a499d-106">The **Add-AzApplicationGatewaySslProfile** cmdlet adds a SSL profile to an application gateway.</span></span> <span data-ttu-id="a499d-107">SSL-profilen används för HTTPS-lyssnare.</span><span class="sxs-lookup"><span data-stu-id="a499d-107">The SSL profile is applied to HTTPS Listeners.</span></span>

## <span data-ttu-id="a499d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a499d-108">EXAMPLES</span></span>

### <span data-ttu-id="a499d-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a499d-109">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
PS C:\> $trustedClient01 = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert01" -CertificateFile "C:\clientCAChain1.cer"
PS C:\> $trustedClient02 = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert02" -CertificateFile "C:\clientCAChain2.cer"
PS C:\> $AppGw = Add-AzApplicationGatewaySslProfile -Name $sslProfile01Name -ApplicationGateway $AppGw -SslPolicy $sslPolicy -TrustedClientCertificates $trustedClient01,$trustedClient02
```

<span data-ttu-id="a499d-110">Med det första kommandot hämtas programgatewayen och lagras i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="a499d-110">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a499d-111">Det andra kommandot skapar en ny SSL-princip och lagrar den i $sslPolicy variabel.</span><span class="sxs-lookup"><span data-stu-id="a499d-111">The second command creates a new SSL policy and stores it in the $sslPolicy variable.</span></span>
<span data-ttu-id="a499d-112">Det tredje och fjärde kommandot skapar två nya certifikat UTFÄRDARes certifikat för betrodda klienter och lagrar dem i $ClientCert 01-och $ClientCert 02-variabler.</span><span class="sxs-lookup"><span data-stu-id="a499d-112">The third and fourth command creates two new trusted client CA certificate chains and stores them in the $ClientCert01 and $ClientCert02 variables.</span></span>
<span data-ttu-id="a499d-113">Det femte kommandot lägger till SSL-profilen med SSL-principen och certifikat utfärdarens certifikatutfärdarcertifikat kedjor för $AppGw Gateway.</span><span class="sxs-lookup"><span data-stu-id="a499d-113">The fifth command adds the SSL profile with the the ssl policy and trusted client CA certificate chains to the application gateway $AppGw.</span></span>

## <span data-ttu-id="a499d-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a499d-114">PARAMETERS</span></span>

### <span data-ttu-id="a499d-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a499d-115">-ApplicationGateway</span></span>
<span data-ttu-id="a499d-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a499d-116">The applicationGateway</span></span>

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

### <span data-ttu-id="a499d-117">-ClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="a499d-117">-ClientAuthConfiguration</span></span>
<span data-ttu-id="a499d-118">Konfigurations inställningar för klientautentisering</span><span class="sxs-lookup"><span data-stu-id="a499d-118">Client authentication configuration settings</span></span>

```yaml
Type: PSApplicationGatewayClientAuthConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a499d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a499d-119">-DefaultProfile</span></span>
<span data-ttu-id="a499d-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a499d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a499d-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="a499d-121">-Name</span></span>
<span data-ttu-id="a499d-122">Namnet på SSL-profilen</span><span class="sxs-lookup"><span data-stu-id="a499d-122">The name of the SSL profile</span></span>

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

### <span data-ttu-id="a499d-123">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="a499d-123">-SslPolicy</span></span>
<span data-ttu-id="a499d-124">SSL-princip</span><span class="sxs-lookup"><span data-stu-id="a499d-124">SSL policy</span></span>

```yaml
Type: PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a499d-125">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="a499d-125">-TrustedClientCertificates</span></span>
<span data-ttu-id="a499d-126">Den betrodda klient certifikat utfärdarens certifikat kedjor</span><span class="sxs-lookup"><span data-stu-id="a499d-126">The trusted client CA certificate chains</span></span>

```yaml
Type: PSApplicationGatewayTrustedClientCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a499d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a499d-127">CommonParameters</span></span>
<span data-ttu-id="a499d-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a499d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a499d-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a499d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a499d-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a499d-130">INPUTS</span></span>

### <span data-ttu-id="a499d-131">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a499d-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a499d-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a499d-132">OUTPUTS</span></span>

### <span data-ttu-id="a499d-133">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a499d-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a499d-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a499d-134">NOTES</span></span>

## <span data-ttu-id="a499d-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a499d-135">RELATED LINKS</span></span>

[<span data-ttu-id="a499d-136">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="a499d-136">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="a499d-137">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="a499d-137">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="a499d-138">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="a499d-138">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="a499d-139">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="a499d-139">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)