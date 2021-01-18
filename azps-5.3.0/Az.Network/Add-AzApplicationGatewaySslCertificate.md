---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 6939f26dc06e0aa5ed56d3e905d30960094e8961
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520979"
---
# <span data-ttu-id="8a23a-101">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8a23a-101">Add-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="8a23a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8a23a-102">SYNOPSIS</span></span>
<span data-ttu-id="8a23a-103">Lägger till ett SSL-certifikat i en programport.</span><span class="sxs-lookup"><span data-stu-id="8a23a-103">Adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="8a23a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8a23a-104">SYNTAX</span></span>

```
Add-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a23a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8a23a-105">DESCRIPTION</span></span>
<span data-ttu-id="8a23a-106">Cmdleten **Add-AzApplicationGatewaySslCertificate** lägger till ett SSL-certifikat till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="8a23a-106">The **Add-AzApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="8a23a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8a23a-107">EXAMPLES</span></span>

### <span data-ttu-id="8a23a-108">Exempel 1: lägga till ett SSL-certifikat med PFX på en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="8a23a-108">Example 1: Add an SSL certificate using pfx to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString $passwordPlainString -AsPlainText -Force
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="8a23a-109">Det här kommandot får en Programgateway med namnet ApplicationGateway01 och lägger sedan till ett SSL-certifikat som heter Cert01.</span><span class="sxs-lookup"><span data-stu-id="8a23a-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

### <span data-ttu-id="8a23a-110">Exempel 2: Lägg till ett SSL-certifikat med nyckel valv hemlighet (version-mindre secretId) på en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="8a23a-110">Example 2: Add an SSL certificate using KeyVault Secret (version-less secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultCertificate -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.SecretId.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="8a23a-111">Skaffa hemligheten och referera till den för `Add-AzApplicationGatewaySslCertificate` att lägga till den i Programgatewayen med namn `Cert01` .</span><span class="sxs-lookup"><span data-stu-id="8a23a-111">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="8a23a-112">Obs! as-version-mindre secretId tillhandahålls här, programgatewayen synkroniserar certifikatet med jämna mellanrum med ett valv.</span><span class="sxs-lookup"><span data-stu-id="8a23a-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="8a23a-113">Exempel 3: lägga till ett SSL-certifikat med nyckel valv hemlighet (versions secretId) i en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="8a23a-113">Example 3: Add an SSL certificate using KeyVault Secret (versioned secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultCertificate -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="8a23a-114">Skaffa hemligheten och referera till den för `Add-AzApplicationGatewaySslCertificate` att lägga till den i Programgatewayen med namn `Cert01` .</span><span class="sxs-lookup"><span data-stu-id="8a23a-114">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="8a23a-115">OBS! om det krävs att Application Gateway synkroniserar certifikatet med ett valv kan du ange secretId.</span><span class="sxs-lookup"><span data-stu-id="8a23a-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="8a23a-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8a23a-116">PARAMETERS</span></span>

### <span data-ttu-id="8a23a-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8a23a-117">-ApplicationGateway</span></span>
<span data-ttu-id="8a23a-118">Anger namnet på den Programgateway som denna cmdlet lägger till ett SSL-certifikat för.</span><span class="sxs-lookup"><span data-stu-id="8a23a-118">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="8a23a-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="8a23a-119">-CertificateFile</span></span>
<span data-ttu-id="8a23a-120">Anger. pfx-filen för ett SSL-certifikat som denna cmdlet lägger till.</span><span class="sxs-lookup"><span data-stu-id="8a23a-120">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="8a23a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a23a-121">-DefaultProfile</span></span>
<span data-ttu-id="8a23a-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8a23a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a23a-123">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="8a23a-123">-KeyVaultSecretId</span></span>
<span data-ttu-id="8a23a-124">SecretId (URI) för nyckel valv hemligheten.</span><span class="sxs-lookup"><span data-stu-id="8a23a-124">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="8a23a-125">Använd det här alternativet om en specifik version av hemlighet måste användas.</span><span class="sxs-lookup"><span data-stu-id="8a23a-125">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="8a23a-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="8a23a-126">-Name</span></span>
<span data-ttu-id="8a23a-127">Anger namnet på det SSL-certifikat som denna cmdlet lägger till.</span><span class="sxs-lookup"><span data-stu-id="8a23a-127">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="8a23a-128">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="8a23a-128">-Password</span></span>
<span data-ttu-id="8a23a-129">Anger lösen ordet för det SSL-certifikat som denna cmdlet lägger till.</span><span class="sxs-lookup"><span data-stu-id="8a23a-129">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="8a23a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a23a-130">CommonParameters</span></span>
<span data-ttu-id="8a23a-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a23a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a23a-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a23a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a23a-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8a23a-133">INPUTS</span></span>

### <span data-ttu-id="8a23a-134">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8a23a-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8a23a-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8a23a-135">OUTPUTS</span></span>

### <span data-ttu-id="8a23a-136">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8a23a-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8a23a-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8a23a-137">NOTES</span></span>

## <span data-ttu-id="8a23a-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8a23a-138">RELATED LINKS</span></span>

[<span data-ttu-id="8a23a-139">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8a23a-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="8a23a-140">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8a23a-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="8a23a-141">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8a23a-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="8a23a-142">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8a23a-142">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


