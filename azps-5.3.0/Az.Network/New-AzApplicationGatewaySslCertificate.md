---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 31d9c5d5c627f4d3451c47584b09760655e77342
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421808"
---
# <span data-ttu-id="b2717-101">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b2717-101">New-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="b2717-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b2717-102">SYNOPSIS</span></span>
<span data-ttu-id="b2717-103">Skapar ett SSL-certifikat för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="b2717-103">Creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="b2717-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b2717-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslCertificate -Name <String> [-CertificateFile <String>] [-Password <SecureString>]
 [-KeyVaultSecretId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2717-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b2717-105">DESCRIPTION</span></span>
<span data-ttu-id="b2717-106">Cmdleten **New-AzApplicationGatewaySslCertificate** skapar ett SSL-certifikat för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="b2717-106">The **New-AzApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="b2717-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b2717-107">EXAMPLES</span></span>

### <span data-ttu-id="b2717-108">Exempel 1: skapa ett SSL-certifikat för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="b2717-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString $passwordPlainString -AsPlainText -Force
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="b2717-109">Det här kommandot skapar ett SSL-certifikat med namnet Cert01 för standard program-gateway och lagrar resultatet i variabeln som heter $Cert.</span><span class="sxs-lookup"><span data-stu-id="b2717-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

### <span data-ttu-id="b2717-110">Exempel 2: skapa ett SSL-certifikat med hjälp av nyckel valv hemlighet (version-mindre secretId) och lägga till i en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="b2717-110">Example 2: Create an SSL certificate using KeyVault Secret (version-less secretId) and add to an application gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="b2717-111">Få hemligheten och skapa ett SSL-certifikat med `New-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="b2717-111">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="b2717-112">Obs! as-version-mindre secretId tillhandahålls här, programgatewayen synkroniserar certifikatet med jämna mellanrum med ett valv.</span><span class="sxs-lookup"><span data-stu-id="b2717-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="b2717-113">Exempel 3: skapa ett SSL-certifikat med hjälp av nyckel valv hemlighet och Lägg till det i en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="b2717-113">Example 3: Create an SSL certificate using KeyVault Secret and add to an Application Gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="b2717-114">Få hemligheten och skapa ett SSL-certifikat med `New-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="b2717-114">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="b2717-115">OBS! om det krävs att Application Gateway synkroniserar certifikatet med ett valv kan du ange secretId.</span><span class="sxs-lookup"><span data-stu-id="b2717-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="b2717-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b2717-116">PARAMETERS</span></span>

### <span data-ttu-id="b2717-117">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="b2717-117">-CertificateFile</span></span>
<span data-ttu-id="b2717-118">Anger sökvägen till. pfx-filen för SSL-certifikatet som den här cmdleten skapar.</span><span class="sxs-lookup"><span data-stu-id="b2717-118">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="b2717-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2717-119">-DefaultProfile</span></span>
<span data-ttu-id="b2717-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b2717-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2717-121">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="b2717-121">-KeyVaultSecretId</span></span>
<span data-ttu-id="b2717-122">SecretId (URI) för nyckel valv hemligheten.</span><span class="sxs-lookup"><span data-stu-id="b2717-122">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="b2717-123">Använd det här alternativet om en specifik version av hemlighet måste användas.</span><span class="sxs-lookup"><span data-stu-id="b2717-123">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="b2717-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="b2717-124">-Name</span></span>
<span data-ttu-id="b2717-125">Anger namnet på det SSL-certifikat som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="b2717-125">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="b2717-126">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="b2717-126">-Password</span></span>
<span data-ttu-id="b2717-127">Anger lösen ordet för SSL som skapas av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2717-127">Specifies the password of the SSL that this cmdlet creates.</span></span>

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

### <span data-ttu-id="b2717-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2717-128">CommonParameters</span></span>
<span data-ttu-id="b2717-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2717-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2717-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2717-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2717-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b2717-131">INPUTS</span></span>

### <span data-ttu-id="b2717-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="b2717-132">None</span></span>

## <span data-ttu-id="b2717-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b2717-133">OUTPUTS</span></span>

### <span data-ttu-id="b2717-134">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b2717-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="b2717-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b2717-135">NOTES</span></span>

## <span data-ttu-id="b2717-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b2717-136">RELATED LINKS</span></span>

[<span data-ttu-id="b2717-137">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b2717-137">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b2717-138">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b2717-138">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b2717-139">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b2717-139">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b2717-140">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b2717-140">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


