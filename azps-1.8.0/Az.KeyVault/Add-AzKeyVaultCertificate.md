---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 89299823-3382-402D-9458-519466748051
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificate.md
ms.openlocfilehash: 79f8516bbcd33c17e708af1625062e08fb21ebb7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916393"
---
# <span data-ttu-id="a550a-101">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a550a-101">Add-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="a550a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a550a-102">SYNOPSIS</span></span>
<span data-ttu-id="a550a-103">Lägger till ett certifikat i ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="a550a-103">Adds a certificate to a key vault.</span></span>

## <span data-ttu-id="a550a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a550a-104">SYNTAX</span></span>

```
Add-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [-CertificatePolicy] <PSKeyVaultCertificatePolicy> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a550a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a550a-105">DESCRIPTION</span></span>
<span data-ttu-id="a550a-106">Cmdleten **Add-AzKeyVaultCertificate** startar processen för registrering av ett certifikat i ett nyckeltal i Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="a550a-106">The **Add-AzKeyVaultCertificate** cmdlet starts the process of enrolling for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="a550a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a550a-107">EXAMPLES</span></span>

### <span data-ttu-id="a550a-108">Exempel 1: lägga till ett certifikat</span><span class="sxs-lookup"><span data-stu-id="a550a-108">Example 1: Add a certificate</span></span>
```powershell
PS C:\> $Policy = New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
PS C:\> Add-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01" -CertificatePolicy $Policy

Status                    : inProgress
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
ErrorCode                 :
ErrorMessage              : 

PS C:\> Get-AzKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01"
Status                    : completed
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
ErrorCode                 :
ErrorMessage              : 

PS C:\> Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"

Name        : testCert01
Certificate : [Subject]
                CN=contoso.com

              [Issuer]
                CN=contoso.com

              [Serial Number]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

              [Not Before]
                2/8/2016 3:11:45 PM

              [Not After]
                8/8/2016 4:21:45 PM

              [Thumbprint]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        :
Enabled     : True
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

<span data-ttu-id="a550a-109">Det första kommandot använder cmdleten New-AzKeyVaultCertificatePolicy för att skapa en certifikat princip och lagrar den sedan i $Policy variabel.</span><span class="sxs-lookup"><span data-stu-id="a550a-109">The first command uses the New-AzKeyVaultCertificatePolicy cmdlet to create a certificate policy, and then stores it in the $Policy variable.</span></span>
<span data-ttu-id="a550a-110">Det andra kommandot använder **Add-AzKeyVaultCertificate** för att starta processen för att skapa ett certifikat.</span><span class="sxs-lookup"><span data-stu-id="a550a-110">The second command uses **Add-AzKeyVaultCertificate** to start the process to create a certificate.</span></span>
<span data-ttu-id="a550a-111">I det tredje kommandot används cmdleten Get-AzKeyVaultCertificateOperation för att undersöka om den är slutförd.</span><span class="sxs-lookup"><span data-stu-id="a550a-111">The third command uses the Get-AzKeyVaultCertificateOperation cmdlet to poll the operation to verify that it's complete.</span></span>
<span data-ttu-id="a550a-112">Det sista kommandot använder cmdleten Get-AzKeyVaultCertificate för att hämta certifikatet.</span><span class="sxs-lookup"><span data-stu-id="a550a-112">The final command uses the Get-AzKeyVaultCertificate cmdlet to get the certificate.</span></span>

## <span data-ttu-id="a550a-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a550a-113">PARAMETERS</span></span>

### <span data-ttu-id="a550a-114">-CertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="a550a-114">-CertificatePolicy</span></span>
<span data-ttu-id="a550a-115">Anger ett **KeyVaultCertificatePolicy** -objekt.</span><span class="sxs-lookup"><span data-stu-id="a550a-115">Specifies a **KeyVaultCertificatePolicy** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a550a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a550a-116">-DefaultProfile</span></span>
<span data-ttu-id="a550a-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a550a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a550a-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="a550a-118">-Name</span></span>
<span data-ttu-id="a550a-119">Anger namnet på det certifikat som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="a550a-119">Specifies the name of the certificate to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a550a-120">-Tagg</span><span class="sxs-lookup"><span data-stu-id="a550a-120">-Tag</span></span>
<span data-ttu-id="a550a-121">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="a550a-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a550a-122">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="a550a-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a550a-123">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a550a-123">-VaultName</span></span>
<span data-ttu-id="a550a-124">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="a550a-124">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a550a-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a550a-125">-Confirm</span></span>
<span data-ttu-id="a550a-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a550a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a550a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a550a-127">-WhatIf</span></span>
<span data-ttu-id="a550a-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a550a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a550a-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a550a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a550a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a550a-130">CommonParameters</span></span>
<span data-ttu-id="a550a-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a550a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a550a-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a550a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a550a-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a550a-133">INPUTS</span></span>

### <span data-ttu-id="a550a-134">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="a550a-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="a550a-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a550a-135">OUTPUTS</span></span>

### <span data-ttu-id="a550a-136">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="a550a-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="a550a-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a550a-137">NOTES</span></span>

## <span data-ttu-id="a550a-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a550a-138">RELATED LINKS</span></span>

[<span data-ttu-id="a550a-139">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a550a-139">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)

[<span data-ttu-id="a550a-140">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a550a-140">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="a550a-141">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a550a-141">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)
