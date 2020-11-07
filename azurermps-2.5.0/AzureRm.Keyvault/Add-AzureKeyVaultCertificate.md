---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 89299823-3382-402D-9458-519466748051
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultcertificate
schema: 2.0.0
ms.openlocfilehash: e94a93be6070a6800ef7528004d8b64ab28fc6fd
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928842"
---
# <span data-ttu-id="b655d-101">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b655d-101">Add-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="b655d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b655d-102">SYNOPSIS</span></span>
<span data-ttu-id="b655d-103">Lägger till ett certifikat i ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="b655d-103">Adds a certificate to a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b655d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b655d-104">SYNTAX</span></span>

```
Add-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [[-CertificatePolicy] <KeyVaultCertificatePolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b655d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b655d-105">DESCRIPTION</span></span>
<span data-ttu-id="b655d-106">Cmdleten **Add-AzureKeyVaultCertificate** startar processen för registrering av ett certifikat i ett nyckeltal i Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="b655d-106">The **Add-AzureKeyVaultCertificate** cmdlet starts the process of enrolling for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="b655d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b655d-107">EXAMPLES</span></span>

### <span data-ttu-id="b655d-108">Exempel 1: lägga till ett certifikat</span><span class="sxs-lookup"><span data-stu-id="b655d-108">Example 1: Add a certificate</span></span>
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

<span data-ttu-id="b655d-109">Det första kommandot använder cmdleten New-AzureKeyVaultCertificatePolicy för att skapa en certifikat princip och lagrar den sedan i $Policy variabel.</span><span class="sxs-lookup"><span data-stu-id="b655d-109">The first command uses the New-AzureKeyVaultCertificatePolicy cmdlet to create a certificate policy, and then stores it in the $Policy variable.</span></span>

<span data-ttu-id="b655d-110">Det andra kommandot använder **Add-AzureKeyVaultCertificate** för att starta processen för att skapa ett certifikat.</span><span class="sxs-lookup"><span data-stu-id="b655d-110">The second command uses **Add-AzureKeyVaultCertificate** to start the process to create a certificate.</span></span>

<span data-ttu-id="b655d-111">I det tredje kommandot används cmdleten Get-AzureKeyVaultCertificateOperation för att undersöka om den är slutförd.</span><span class="sxs-lookup"><span data-stu-id="b655d-111">The third command uses the Get-AzureKeyVaultCertificateOperation cmdlet to poll the operation to verify that it's complete.</span></span>

<span data-ttu-id="b655d-112">Det sista kommandot använder cmdleten Get-AzureKeyVaultCertificate för att hämta certifikatet.</span><span class="sxs-lookup"><span data-stu-id="b655d-112">The final command uses the Get-AzureKeyVaultCertificate cmdlet to get the certificate.</span></span>

## <span data-ttu-id="b655d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b655d-113">PARAMETERS</span></span>

### <span data-ttu-id="b655d-114">-CertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="b655d-114">-CertificatePolicy</span></span>
<span data-ttu-id="b655d-115">Anger ett **KeyVaultCertificatePolicy** -objekt.</span><span class="sxs-lookup"><span data-stu-id="b655d-115">Specifies a **KeyVaultCertificatePolicy** object.</span></span>

```yaml
Type: KeyVaultCertificatePolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b655d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b655d-116">-DefaultProfile</span></span>
<span data-ttu-id="b655d-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b655d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b655d-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="b655d-118">-Name</span></span>
<span data-ttu-id="b655d-119">Anger namnet på det certifikat som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="b655d-119">Specifies the name of the certificate to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b655d-120">-Tagg</span><span class="sxs-lookup"><span data-stu-id="b655d-120">-Tag</span></span>
<span data-ttu-id="b655d-121">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="b655d-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b655d-122">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="b655d-122">For example:</span></span>

<span data-ttu-id="b655d-123">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="b655d-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b655d-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b655d-124">-VaultName</span></span>
<span data-ttu-id="b655d-125">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="b655d-125">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b655d-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b655d-126">-Confirm</span></span>
<span data-ttu-id="b655d-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b655d-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b655d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b655d-128">-WhatIf</span></span>
<span data-ttu-id="b655d-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b655d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b655d-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b655d-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b655d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b655d-131">CommonParameters</span></span>
<span data-ttu-id="b655d-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b655d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b655d-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b655d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b655d-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b655d-134">INPUTS</span></span>

## <span data-ttu-id="b655d-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b655d-135">OUTPUTS</span></span>

### <span data-ttu-id="b655d-136">Microsoft. Azure. commands. valv. Models. KeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="b655d-136">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="b655d-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b655d-137">NOTES</span></span>

## <span data-ttu-id="b655d-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b655d-138">RELATED LINKS</span></span>

[<span data-ttu-id="b655d-139">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b655d-139">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)

[<span data-ttu-id="b655d-140">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b655d-140">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="b655d-141">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b655d-141">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)
