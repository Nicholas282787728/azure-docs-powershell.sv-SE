---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 89299823-3382-402D-9458-519466748051
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificate.md
ms.openlocfilehash: 97b6e34029b4eaac7d2157c2cf224398e8b253f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584708"
---
# <span data-ttu-id="e927e-101">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e927e-101">Add-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="e927e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e927e-102">SYNOPSIS</span></span>
<span data-ttu-id="e927e-103">Lägger till ett certifikat i ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="e927e-103">Adds a certificate to a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e927e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e927e-104">SYNTAX</span></span>

```
Add-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [[-CertificatePolicy] <KeyVaultCertificatePolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e927e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e927e-105">DESCRIPTION</span></span>
<span data-ttu-id="e927e-106">Cmdleten **Add-AzureKeyVaultCertificate** startar processen för registrering av ett certifikat i ett nyckeltal i Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="e927e-106">The **Add-AzureKeyVaultCertificate** cmdlet starts the process of enrolling for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="e927e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e927e-107">EXAMPLES</span></span>

### <span data-ttu-id="e927e-108">Exempel 1: lägga till ett certifikat</span><span class="sxs-lookup"><span data-stu-id="e927e-108">Example 1: Add a certificate</span></span>
```
PS C:\>$Policy = New-AzureKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
PS C:\> Add-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01" -CertificatePolicy $Policy

Status                    : inProgress
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
ErrorCode                 :
ErrorMessage              : PS C:\>Get-AzureKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01"
Status                    : completed
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
ErrorCode                 :
ErrorMessage              : PS C:\>Get-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : testCert01
Certificate : [Subject]
                CN=contoso.com

              [Issuer]
                CN=contoso.com

              [Serial Number]
                05979C5A2F0741D5A3B6F97673E8A118

              [Not Before]
                2/8/2016 3:11:45 PM

              [Not After]
                8/8/2016 4:21:45 PM

              [Thumbprint]
                3E9B6848AD1834284157D68B060F748037F663C8

Thumbprint  : 3E9B6848AD1834284157D68B060F748037F663C8
Tags        :
Enabled     : True
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

<span data-ttu-id="e927e-109">Det första kommandot använder cmdleten New-AzureKeyVaultCertificatePolicy för att skapa en certifikat princip och lagrar den sedan i $Policy variabel.</span><span class="sxs-lookup"><span data-stu-id="e927e-109">The first command uses the New-AzureKeyVaultCertificatePolicy cmdlet to create a certificate policy, and then stores it in the $Policy variable.</span></span>

<span data-ttu-id="e927e-110">Det andra kommandot använder **Add-AzureKeyVaultCertificate** för att starta processen för att skapa ett certifikat.</span><span class="sxs-lookup"><span data-stu-id="e927e-110">The second command uses **Add-AzureKeyVaultCertificate** to start the process to create a certificate.</span></span>

<span data-ttu-id="e927e-111">I det tredje kommandot används cmdleten Get-AzureKeyVaultCertificateOperation för att undersöka om den är slutförd.</span><span class="sxs-lookup"><span data-stu-id="e927e-111">The third command uses the Get-AzureKeyVaultCertificateOperation cmdlet to poll the operation to verify that it's complete.</span></span>

<span data-ttu-id="e927e-112">Det sista kommandot använder cmdleten Get-AzureKeyVaultCertificate för att hämta certifikatet.</span><span class="sxs-lookup"><span data-stu-id="e927e-112">The final command uses the Get-AzureKeyVaultCertificate cmdlet to get the certificate.</span></span>

## <span data-ttu-id="e927e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e927e-113">PARAMETERS</span></span>

### <span data-ttu-id="e927e-114">-CertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="e927e-114">-CertificatePolicy</span></span>
<span data-ttu-id="e927e-115">Anger ett **KeyVaultCertificatePolicy** -objekt.</span><span class="sxs-lookup"><span data-stu-id="e927e-115">Specifies a **KeyVaultCertificatePolicy** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e927e-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="e927e-116">-Name</span></span>
<span data-ttu-id="e927e-117">Anger namnet på det certifikat som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="e927e-117">Specifies the name of the certificate to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e927e-118">-Tagg</span><span class="sxs-lookup"><span data-stu-id="e927e-118">-Tag</span></span>
<span data-ttu-id="e927e-119">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="e927e-119">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e927e-120">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="e927e-120">For example:</span></span>

<span data-ttu-id="e927e-121">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="e927e-121">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e927e-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e927e-122">-VaultName</span></span>
<span data-ttu-id="e927e-123">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="e927e-123">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e927e-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e927e-124">-Confirm</span></span>
<span data-ttu-id="e927e-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e927e-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e927e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e927e-126">-WhatIf</span></span>
<span data-ttu-id="e927e-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e927e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e927e-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e927e-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e927e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e927e-129">-DefaultProfile</span></span>
<span data-ttu-id="e927e-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e927e-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e927e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e927e-131">CommonParameters</span></span>
<span data-ttu-id="e927e-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e927e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e927e-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e927e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e927e-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e927e-134">INPUTS</span></span>

## <span data-ttu-id="e927e-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e927e-135">OUTPUTS</span></span>

### <span data-ttu-id="e927e-136">Microsoft. Azure. commands. valv. Models. KeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="e927e-136">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="e927e-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e927e-137">NOTES</span></span>

## <span data-ttu-id="e927e-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e927e-138">RELATED LINKS</span></span>

[<span data-ttu-id="e927e-139">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e927e-139">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)

[<span data-ttu-id="e927e-140">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e927e-140">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="e927e-141">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e927e-141">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)
