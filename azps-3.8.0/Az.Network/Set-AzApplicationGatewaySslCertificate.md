---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 0fa72c48693335dd3df6ab3c1cf8040c5343cc84
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090387"
---
# <span data-ttu-id="3e369-101">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3e369-101">Set-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="3e369-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3e369-102">SYNOPSIS</span></span>
<span data-ttu-id="3e369-103">Uppdaterar ett SSL-certifikat för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="3e369-103">Updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="3e369-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3e369-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e369-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3e369-105">DESCRIPTION</span></span>
<span data-ttu-id="3e369-106">Cmdleten **set-AzApplicationGatewaySslCertificate** uppdaterar ett SSL-certifikat för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="3e369-106">The **Set-AzApplicationGatewaySslCertificate** cmdlet updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="3e369-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3e369-107">EXAMPLES</span></span>

### <span data-ttu-id="3e369-108">Exempel 1: uppdatera ett befintligt SSL-certifikat på Application Gateway</span><span class="sxs-lookup"><span data-stu-id="3e369-108">Example 1: Update an existing SSL certificate on Application Gateway</span></span>
```
PS C:\> $appGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="3e369-109">Uppdatera ett befintligt SSL-certifikat för den Programgateway som heter ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="3e369-109">Update an existing SSL certificate for the application gateway named ApplicationGateway01.</span></span>

### <span data-ttu-id="3e369-110">Exempel 2: uppdatera ett befintligt SSL-certifikat med nyckel valv hemlighet (version-mindre secretId) på Application Gateway</span><span class="sxs-lookup"><span data-stu-id="3e369-110">Example 2: Update an existing SSL certificate using KeyVault Secret (version-less secretId) on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="3e369-111">Få hemligheten och uppdatera ett befintligt SSL-certifikat med `Set-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="3e369-111">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>

### <span data-ttu-id="3e369-112">Exempel 3: uppdatera ett befintligt SSL-certifikat med nyckel valv hemlighet på Application Gateway</span><span class="sxs-lookup"><span data-stu-id="3e369-112">Example 3: Update an existing SSL certificate using KeyVault Secret on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="3e369-113">Få hemligheten och uppdatera ett befintligt SSL-certifikat med `Set-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="3e369-113">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="3e369-114">OBS! om det krävs att Application Gateway synkroniserar certifikatet med ett valv kan du ange secretId.</span><span class="sxs-lookup"><span data-stu-id="3e369-114">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="3e369-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3e369-115">PARAMETERS</span></span>

### <span data-ttu-id="3e369-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3e369-116">-ApplicationGateway</span></span>
<span data-ttu-id="3e369-117">Anger den Programgateway som certifikatet för SSL (Secure Socket Layer) är associerat med.</span><span class="sxs-lookup"><span data-stu-id="3e369-117">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

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

### <span data-ttu-id="3e369-118">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="3e369-118">-CertificateFile</span></span>
<span data-ttu-id="3e369-119">Anger sökvägen till SSL-certifikatet.</span><span class="sxs-lookup"><span data-stu-id="3e369-119">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="3e369-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e369-120">-DefaultProfile</span></span>
<span data-ttu-id="3e369-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3e369-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e369-122">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="3e369-122">-KeyVaultSecretId</span></span>
<span data-ttu-id="3e369-123">SecretId (URI) för nyckel valv hemligheten.</span><span class="sxs-lookup"><span data-stu-id="3e369-123">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="3e369-124">Använd det här alternativet om en specifik version av hemlighet måste användas.</span><span class="sxs-lookup"><span data-stu-id="3e369-124">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="3e369-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="3e369-125">-Name</span></span>
<span data-ttu-id="3e369-126">Anger namnet på SSL-certifikatet.</span><span class="sxs-lookup"><span data-stu-id="3e369-126">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="3e369-127">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="3e369-127">-Password</span></span>
<span data-ttu-id="3e369-128">Anger lösen ordet för SSL-certifikatet.</span><span class="sxs-lookup"><span data-stu-id="3e369-128">Specifies the password of the SSL certificate.</span></span>

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

### <span data-ttu-id="3e369-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e369-129">CommonParameters</span></span>
<span data-ttu-id="3e369-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e369-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e369-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e369-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e369-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3e369-132">INPUTS</span></span>

### <span data-ttu-id="3e369-133">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3e369-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3e369-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3e369-134">OUTPUTS</span></span>

### <span data-ttu-id="3e369-135">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3e369-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3e369-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3e369-136">NOTES</span></span>

## <span data-ttu-id="3e369-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3e369-137">RELATED LINKS</span></span>

[<span data-ttu-id="3e369-138">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3e369-138">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="3e369-139">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3e369-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="3e369-140">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3e369-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="3e369-141">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3e369-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)


