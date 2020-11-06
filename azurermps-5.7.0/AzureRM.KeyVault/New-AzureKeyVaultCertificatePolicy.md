---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: caa0961c1b7aebd5fd2f9883831d733a0fa69f1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583148"
---
# <span data-ttu-id="f8ea6-101">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f8ea6-101">New-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="f8ea6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f8ea6-102">SYNOPSIS</span></span>
<span data-ttu-id="f8ea6-103">Skapar ett certifikat policy objekt för minnet.</span><span class="sxs-lookup"><span data-stu-id="f8ea6-103">Creates an in-memory certificate policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8ea6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f8ea6-104">SYNTAX</span></span>

### <span data-ttu-id="f8ea6-105">SubjectName (standard)</span><span class="sxs-lookup"><span data-stu-id="f8ea6-105">SubjectName (Default)</span></span>
```
New-AzureKeyVaultCertificatePolicy [-IssuerName] <String> [-SubjectName] <String>
 [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>]
 [-ReuseKeyOnRenewal] [-Disabled] [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f8ea6-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="f8ea6-106">DNSNames</span></span>
```
New-AzureKeyVaultCertificatePolicy [-IssuerName] <String> [[-SubjectName] <String>]
 [-DnsName] <System.Collections.Generic.List`1[System.String]> [-RenewAtNumberOfDaysBeforeExpiry <Int32>]
 [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f8ea6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f8ea6-107">DESCRIPTION</span></span>
<span data-ttu-id="f8ea6-108">Cmdleten **New-AzureKeyVaultCertificatePolicy** skapar ett certifikats princip objekt i minnet för Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="f8ea6-108">The **New-AzureKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="f8ea6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f8ea6-109">EXAMPLES</span></span>

### <span data-ttu-id="f8ea6-110">Exempel 1: skapa en certifikat princip</span><span class="sxs-lookup"><span data-stu-id="f8ea6-110">Example 1: Create a certificate policy</span></span>
```
PS C:\>New-AzureKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
```

<span data-ttu-id="f8ea6-111">Det här kommandot skapar en certifikat princip som är giltig i sex månader och återanvänder den för att förnya certifikatet.</span><span class="sxs-lookup"><span data-stu-id="f8ea6-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="f8ea6-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f8ea6-112">PARAMETERS</span></span>

### <span data-ttu-id="f8ea6-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="f8ea6-113">-CertificateType</span></span>
<span data-ttu-id="f8ea6-114">Anger typen av certifikat för utgivaren.</span><span class="sxs-lookup"><span data-stu-id="f8ea6-114">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8ea6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8ea6-115">-DefaultProfile</span></span>
<span data-ttu-id="f8ea6-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f8ea6-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8ea6-117">-Inaktive rad</span><span class="sxs-lookup"><span data-stu-id="f8ea6-117">-Disabled</span></span>
<span data-ttu-id="f8ea6-118">Anger att certifikat principen är inaktive rad.</span><span class="sxs-lookup"><span data-stu-id="f8ea6-118">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8ea6-119">-DnsName</span><span class="sxs-lookup"><span data-stu-id="f8ea6-119">-DnsName</span></span>
<span data-ttu-id="f8ea6-120">Anger DNS-namnen i certifikatet.</span><span class="sxs-lookup"><span data-stu-id="f8ea6-120">Specifies the DNS names in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: DNSNames
Aliases: DnsNames

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8ea6-121">-EKU</span><span class="sxs-lookup"><span data-stu-id="f8ea6-121">-Ekus</span></span>
<span data-ttu-id="f8ea6-122">Anger EKU (Enhanced Key Usage) i certifikatet.</span><span class="sxs-lookup"><span data-stu-id="f8ea6-122">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8ea6-123">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="f8ea6-123">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="f8ea6-124">Anger hur många dagar som ska gå innan den automatiska aviseringen startar.</span><span class="sxs-lookup"><span data-stu-id="f8ea6-124">Specifies how many days before expiry the automatic notification process begins.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8ea6-125">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="f8ea6-125">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="f8ea6-126">Anger den procent andel av livs längden som den automatiska processen för aviseringen startar.</span><span class="sxs-lookup"><span data-stu-id="f8ea6-126">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8ea6-127">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="f8ea6-127">-IssuerName</span></span>
<span data-ttu-id="f8ea6-128">Anger namnet på utgivaren av certifikatet.</span><span class="sxs-lookup"><span data-stu-id="f8ea6-128">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="f8ea6-129">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="f8ea6-129">-KeyNotExportable</span></span>
<span data-ttu-id="f8ea6-130">Visar att det inte går att exportera den.</span><span class="sxs-lookup"><span data-stu-id="f8ea6-130">Indicates that the key is not exportable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8ea6-131">-Värdetyp</span><span class="sxs-lookup"><span data-stu-id="f8ea6-131">-KeyType</span></span>
<span data-ttu-id="f8ea6-132">Anger huvud typen för den knapp som återställer certifikatet.</span><span class="sxs-lookup"><span data-stu-id="f8ea6-132">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="f8ea6-133">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="f8ea6-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f8ea6-134">RSA</span><span class="sxs-lookup"><span data-stu-id="f8ea6-134">RSA</span></span>
- <span data-ttu-id="f8ea6-135">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="f8ea6-135">RSA-HSM</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8ea6-136">-Använd ande av</span><span class="sxs-lookup"><span data-stu-id="f8ea6-136">-KeyUsage</span></span>
<span data-ttu-id="f8ea6-137">Anger de viktigaste användningarna i certifikatet.</span><span class="sxs-lookup"><span data-stu-id="f8ea6-137">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8ea6-138">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="f8ea6-138">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="f8ea6-139">Anger antalet dagar före utgångs datum efter vilket automatisk process för certifikat förnyelse påbörjas.</span><span class="sxs-lookup"><span data-stu-id="f8ea6-139">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8ea6-140">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="f8ea6-140">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="f8ea6-141">Anger den procent andel av livs längden som den automatiska processen för certifikat förnyelse startas.</span><span class="sxs-lookup"><span data-stu-id="f8ea6-141">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8ea6-142">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="f8ea6-142">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="f8ea6-143">Visar att certifikatet återanvändar den under förnyelse.</span><span class="sxs-lookup"><span data-stu-id="f8ea6-143">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8ea6-144">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="f8ea6-144">-SecretContentType</span></span>
<span data-ttu-id="f8ea6-145">Anger innehålls typen för den nya nyckel valv hemligheten.</span><span class="sxs-lookup"><span data-stu-id="f8ea6-145">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="f8ea6-146">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="f8ea6-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f8ea6-147">Application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="f8ea6-147">application/x-pkcs12</span></span>
- <span data-ttu-id="f8ea6-148">Application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="f8ea6-148">application/x-pem-file</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8ea6-149">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="f8ea6-149">-SubjectName</span></span>
<span data-ttu-id="f8ea6-150">Anger ämnets namn för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="f8ea6-150">Specifies the subject name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: SubjectName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: DNSNames
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8ea6-151">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="f8ea6-151">-ValidityInMonths</span></span>
<span data-ttu-id="f8ea6-152">Anger antalet månader som certifikatet är giltigt.</span><span class="sxs-lookup"><span data-stu-id="f8ea6-152">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8ea6-153">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f8ea6-153">-Confirm</span></span>
<span data-ttu-id="f8ea6-154">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f8ea6-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8ea6-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8ea6-155">-WhatIf</span></span>
<span data-ttu-id="f8ea6-156">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f8ea6-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8ea6-157">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f8ea6-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8ea6-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8ea6-158">CommonParameters</span></span>
<span data-ttu-id="f8ea6-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8ea6-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8ea6-160">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8ea6-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8ea6-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f8ea6-161">INPUTS</span></span>

### <span data-ttu-id="f8ea6-162">Ingen</span><span class="sxs-lookup"><span data-stu-id="f8ea6-162">None</span></span>
<span data-ttu-id="f8ea6-163">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="f8ea6-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f8ea6-164">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f8ea6-164">OUTPUTS</span></span>

### <span data-ttu-id="f8ea6-165">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f8ea6-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="f8ea6-166">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f8ea6-166">NOTES</span></span>

## <span data-ttu-id="f8ea6-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f8ea6-167">RELATED LINKS</span></span>

[<span data-ttu-id="f8ea6-168">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f8ea6-168">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="f8ea6-169">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f8ea6-169">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

