---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 36f45cc5c49cbdf3183f34068fd5b87000c1ede5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747760"
---
# <span data-ttu-id="a069e-101">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a069e-101">Set-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="a069e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a069e-102">SYNOPSIS</span></span>
<span data-ttu-id="a069e-103">Uppdaterar ett SSL-certifikat för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="a069e-103">Updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="a069e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a069e-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a069e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a069e-105">DESCRIPTION</span></span>
<span data-ttu-id="a069e-106">Cmdleten **set-AzApplicationGatewaySslCertificate** uppdaterar ett SSL-certifikat för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="a069e-106">The **Set-AzApplicationGatewaySslCertificate** cmdlet updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="a069e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a069e-107">EXAMPLES</span></span>

### <span data-ttu-id="a069e-108">Exempel 1: uppdatera ett befintligt SSL-certifikat på Application Gateway</span><span class="sxs-lookup"><span data-stu-id="a069e-108">Example 1: Update an existing SSL certificate on Application Gateway</span></span>
```
PS C:\> $appGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="a069e-109">Uppdatera ett befintligt SSL-certifikat för den Programgateway som heter ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="a069e-109">Update an existing SSL certificate for the application gateway named ApplicationGateway01.</span></span>

### <span data-ttu-id="a069e-110">Exempel 2: uppdatera ett befintligt SSL-certifikat med nyckel valv hemlighet (version-mindre secretId) på Application Gateway</span><span class="sxs-lookup"><span data-stu-id="a069e-110">Example 2: Update an existing SSL certificate using KeyVault Secret (version-less secretId) on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="a069e-111">Få hemligheten och uppdatera ett befintligt SSL-certifikat med `Set-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="a069e-111">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>

### <span data-ttu-id="a069e-112">Exempel 3: uppdatera ett befintligt SSL-certifikat med nyckel valv hemlighet på Application Gateway</span><span class="sxs-lookup"><span data-stu-id="a069e-112">Example 3: Update an existing SSL certificate using KeyVault Secret on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="a069e-113">Få hemligheten och uppdatera ett befintligt SSL-certifikat med `Set-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="a069e-113">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="a069e-114">OBS! om det krävs att Application Gateway synkroniserar certifikatet med ett valv kan du ange secretId.</span><span class="sxs-lookup"><span data-stu-id="a069e-114">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="a069e-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a069e-115">PARAMETERS</span></span>

### <span data-ttu-id="a069e-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a069e-116">-ApplicationGateway</span></span>
<span data-ttu-id="a069e-117">Anger den Programgateway som certifikatet för SSL (Secure Socket Layer) är associerat med.</span><span class="sxs-lookup"><span data-stu-id="a069e-117">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

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

### <span data-ttu-id="a069e-118">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="a069e-118">-CertificateFile</span></span>
<span data-ttu-id="a069e-119">Anger sökvägen till SSL-certifikatet.</span><span class="sxs-lookup"><span data-stu-id="a069e-119">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="a069e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a069e-120">-DefaultProfile</span></span>
<span data-ttu-id="a069e-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a069e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a069e-122">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="a069e-122">-KeyVaultSecretId</span></span>
<span data-ttu-id="a069e-123">SecretId (URI) för nyckel valv hemligheten.</span><span class="sxs-lookup"><span data-stu-id="a069e-123">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="a069e-124">Använd det här alternativet om en specifik version av hemlighet måste användas.</span><span class="sxs-lookup"><span data-stu-id="a069e-124">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="a069e-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="a069e-125">-Name</span></span>
<span data-ttu-id="a069e-126">Anger namnet på SSL-certifikatet.</span><span class="sxs-lookup"><span data-stu-id="a069e-126">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="a069e-127">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="a069e-127">-Password</span></span>
<span data-ttu-id="a069e-128">Anger lösen ordet för SSL-certifikatet.</span><span class="sxs-lookup"><span data-stu-id="a069e-128">Specifies the password of the SSL certificate.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a069e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a069e-129">CommonParameters</span></span>
<span data-ttu-id="a069e-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a069e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a069e-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a069e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a069e-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a069e-132">INPUTS</span></span>

### <span data-ttu-id="a069e-133">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a069e-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a069e-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a069e-134">OUTPUTS</span></span>

### <span data-ttu-id="a069e-135">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a069e-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a069e-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a069e-136">NOTES</span></span>

## <span data-ttu-id="a069e-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a069e-137">RELATED LINKS</span></span>

[<span data-ttu-id="a069e-138">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a069e-138">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="a069e-139">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a069e-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="a069e-140">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a069e-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="a069e-141">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a069e-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

