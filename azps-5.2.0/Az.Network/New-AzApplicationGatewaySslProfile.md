---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: a9b0d41ad700d0591e38fa339c38efb85cb00859
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416115"
---
# <span data-ttu-id="43205-101">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="43205-101">New-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="43205-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="43205-102">SYNOPSIS</span></span>
<span data-ttu-id="43205-103">Skapar SSL-profil för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="43205-103">Creates SSL profile for an application gateway.</span></span>

## <span data-ttu-id="43205-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="43205-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslProfile -Name <String> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 [-ClientAuthConfiguration <PSApplicationGatewayClientAuthConfiguration>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43205-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="43205-105">DESCRIPTION</span></span>
<span data-ttu-id="43205-106">Cmdleten **New-AzApplicationGatewaySslProfile** skapar SSL-profil för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="43205-106">The **New-AzApplicationGatewaySslProfile** cmdlet creates SSL profile for an application gateway.</span></span> <span data-ttu-id="43205-107">SSL-profilen är konfigurerad för HTTPS-lyssnarna.</span><span class="sxs-lookup"><span data-stu-id="43205-107">The ssl profile is configured on the HTTPS listeners.</span></span>

## <span data-ttu-id="43205-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="43205-108">EXAMPLES</span></span>

### <span data-ttu-id="43205-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="43205-109">Example 1</span></span>
```powershell
PS C:\> $sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
PS C:\> $trustedClient01 = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert01" -CertificateFile "C:\clientCAChain1.cer"
PS C:\> $profile = New-AzApplicationGatewaySslProfile -Name $sslProfile01Name -SslPolicy $sslPolicy -TrustedClientCertificates $trustedClient01
```
<span data-ttu-id="43205-110">Det första kommandot skapar en ny SSL-princip och lagrar den i $sslPolicy variabel.</span><span class="sxs-lookup"><span data-stu-id="43205-110">The first command creates a new SSL policy and stores it in the $sslPolicy variable.</span></span>
<span data-ttu-id="43205-111">Det andra kommandot skapar ett certifikat för betrodd klient certifikat kedjor och lagrar dem i $ClientCert 01-variabeln.</span><span class="sxs-lookup"><span data-stu-id="43205-111">The second command creates a trusted client CA certificate chains and stores them in the $ClientCert01 variable.</span></span>
<span data-ttu-id="43205-112">Det tredje kommandot skapar en ny SSL-profil med SSL-principen och kedjan med betrodda klient certifikat utfärdare.</span><span class="sxs-lookup"><span data-stu-id="43205-112">The third command create a new SSL profile with the the ssl policy and trusted client CA certificate chain.</span></span>

## <span data-ttu-id="43205-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="43205-113">PARAMETERS</span></span>

### <span data-ttu-id="43205-114">-ClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="43205-114">-ClientAuthConfiguration</span></span>
<span data-ttu-id="43205-115">Konfigurations inställningar för klientautentisering</span><span class="sxs-lookup"><span data-stu-id="43205-115">Client authentication configuration settings</span></span>

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

### <span data-ttu-id="43205-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43205-116">-DefaultProfile</span></span>
<span data-ttu-id="43205-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="43205-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43205-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="43205-118">-Name</span></span>
<span data-ttu-id="43205-119">Namnet på SSL-profilen</span><span class="sxs-lookup"><span data-stu-id="43205-119">The name of the SSL profile</span></span>

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

### <span data-ttu-id="43205-120">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="43205-120">-SslPolicy</span></span>
<span data-ttu-id="43205-121">SSL-princip</span><span class="sxs-lookup"><span data-stu-id="43205-121">SSL policy</span></span>

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

### <span data-ttu-id="43205-122">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="43205-122">-TrustedClientCertificates</span></span>
<span data-ttu-id="43205-123">Den betrodda klient certifikat utfärdarens certifikat kedjor</span><span class="sxs-lookup"><span data-stu-id="43205-123">The trusted client CA certificate chains</span></span>

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

### <span data-ttu-id="43205-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43205-124">CommonParameters</span></span>
<span data-ttu-id="43205-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43205-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43205-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43205-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43205-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="43205-127">INPUTS</span></span>

### <span data-ttu-id="43205-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="43205-128">None</span></span>

## <span data-ttu-id="43205-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="43205-129">OUTPUTS</span></span>

### <span data-ttu-id="43205-130">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="43205-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="43205-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="43205-131">NOTES</span></span>

## <span data-ttu-id="43205-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="43205-132">RELATED LINKS</span></span>

[<span data-ttu-id="43205-133">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="43205-133">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="43205-134">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="43205-134">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="43205-135">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="43205-135">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="43205-136">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="43205-136">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)