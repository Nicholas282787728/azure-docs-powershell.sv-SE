---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 262c539d9ff97983494de0951c9a5d47510b0d28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743911"
---
# <span data-ttu-id="84ba6-101">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="84ba6-101">New-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="84ba6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="84ba6-102">SYNOPSIS</span></span>
<span data-ttu-id="84ba6-103">Skapar ett certifikat policy objekt för minnet.</span><span class="sxs-lookup"><span data-stu-id="84ba6-103">Creates an in-memory certificate policy object.</span></span>

## <span data-ttu-id="84ba6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="84ba6-104">SYNTAX</span></span>

### <span data-ttu-id="84ba6-105">SubjectName (standard)</span><span class="sxs-lookup"><span data-stu-id="84ba6-105">SubjectName (Default)</span></span>
```
New-AzKeyVaultCertificatePolicy [-IssuerName] <String> [-SubjectName] <String>
 [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>]
 [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeySize <Int32>] [-KeyType <String>] [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="84ba6-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="84ba6-106">DNSNames</span></span>
```
New-AzKeyVaultCertificatePolicy [-IssuerName] <String> [[-SubjectName] <String>]
 [-DnsName] <System.Collections.Generic.List`1[System.String]> [-RenewAtNumberOfDaysBeforeExpiry <Int32>]
 [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeySize <Int32>] [-KeyType <String>] [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="84ba6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="84ba6-107">DESCRIPTION</span></span>
<span data-ttu-id="84ba6-108">Cmdleten **New-AzKeyVaultCertificatePolicy** skapar ett certifikats princip objekt i minnet för Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="84ba6-108">The **New-AzKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="84ba6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="84ba6-109">EXAMPLES</span></span>

### <span data-ttu-id="84ba6-110">Exempel 1: skapa en certifikat princip</span><span class="sxs-lookup"><span data-stu-id="84ba6-110">Example 1: Create a certificate policy</span></span>
```powershell
PS C:\> New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal

SecretContentType               : application/x-pkcs12
Kty                             :
KeySize                         : 2048
Exportable                      :
ReuseKeyOnRenewal               : True
SubjectName                     : CN=contoso.com
DnsNames                        :
KeyUsage                        :
Ekus                            :
ValidityInMonths                : 6
IssuerName                      : Self
CertificateType                 :
RenewAtNumberOfDaysBeforeExpiry :
RenewAtPercentageLifetime       :
EmailAtNumberOfDaysBeforeExpiry :
EmailAtPercentageLifetime       :
CertificateTransparency         :
Enabled                         : True
Created                         :
Updated                         :
```

<span data-ttu-id="84ba6-111">Det här kommandot skapar en certifikat princip som är giltig i sex månader och återanvänder den för att förnya certifikatet.</span><span class="sxs-lookup"><span data-stu-id="84ba6-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="84ba6-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="84ba6-112">PARAMETERS</span></span>

### <span data-ttu-id="84ba6-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="84ba6-113">-CertificateType</span></span>
<span data-ttu-id="84ba6-114">Anger typen av certifikat för utgivaren.</span><span class="sxs-lookup"><span data-stu-id="84ba6-114">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84ba6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84ba6-115">-DefaultProfile</span></span>
<span data-ttu-id="84ba6-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="84ba6-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="84ba6-117">-Inaktive rad</span><span class="sxs-lookup"><span data-stu-id="84ba6-117">-Disabled</span></span>
<span data-ttu-id="84ba6-118">Anger att certifikat principen är inaktive rad.</span><span class="sxs-lookup"><span data-stu-id="84ba6-118">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84ba6-119">-DnsName</span><span class="sxs-lookup"><span data-stu-id="84ba6-119">-DnsName</span></span>
<span data-ttu-id="84ba6-120">Anger DNS-namnen i certifikatet.</span><span class="sxs-lookup"><span data-stu-id="84ba6-120">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="84ba6-121">-EKU</span><span class="sxs-lookup"><span data-stu-id="84ba6-121">-Ekus</span></span>
<span data-ttu-id="84ba6-122">Anger EKU (Enhanced Key Usage) i certifikatet.</span><span class="sxs-lookup"><span data-stu-id="84ba6-122">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="84ba6-123">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="84ba6-123">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="84ba6-124">Anger hur många dagar som ska gå innan den automatiska aviseringen startar.</span><span class="sxs-lookup"><span data-stu-id="84ba6-124">Specifies how many days before expiry the automatic notification process begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84ba6-125">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="84ba6-125">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="84ba6-126">Anger den procent andel av livs längden som den automatiska processen för aviseringen startar.</span><span class="sxs-lookup"><span data-stu-id="84ba6-126">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84ba6-127">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="84ba6-127">-IssuerName</span></span>
<span data-ttu-id="84ba6-128">Anger namnet på utgivaren av certifikatet.</span><span class="sxs-lookup"><span data-stu-id="84ba6-128">Specifies the name of the issuer for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84ba6-129">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="84ba6-129">-KeyNotExportable</span></span>
<span data-ttu-id="84ba6-130">Visar att det inte går att exportera den.</span><span class="sxs-lookup"><span data-stu-id="84ba6-130">Indicates that the key is not exportable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84ba6-131">-Dubbel storlek</span><span class="sxs-lookup"><span data-stu-id="84ba6-131">-KeySize</span></span>
<span data-ttu-id="84ba6-132">Anger certifikatets viktigaste storlek.</span><span class="sxs-lookup"><span data-stu-id="84ba6-132">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="84ba6-133">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="84ba6-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="84ba6-134">2048</span><span class="sxs-lookup"><span data-stu-id="84ba6-134">2048</span></span>
- <span data-ttu-id="84ba6-135">3072</span><span class="sxs-lookup"><span data-stu-id="84ba6-135">3072</span></span>
- <span data-ttu-id="84ba6-136">4096</span><span class="sxs-lookup"><span data-stu-id="84ba6-136">4096</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:
Accepted values: 2048, 3072, 4096

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84ba6-137">-Värdetyp</span><span class="sxs-lookup"><span data-stu-id="84ba6-137">-KeyType</span></span>
<span data-ttu-id="84ba6-138">Anger huvud typen för den knapp som återställer certifikatet.</span><span class="sxs-lookup"><span data-stu-id="84ba6-138">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="84ba6-139">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="84ba6-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="84ba6-140">RSA</span><span class="sxs-lookup"><span data-stu-id="84ba6-140">RSA</span></span>
- <span data-ttu-id="84ba6-141">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="84ba6-141">RSA-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84ba6-142">-Använd ande av</span><span class="sxs-lookup"><span data-stu-id="84ba6-142">-KeyUsage</span></span>
<span data-ttu-id="84ba6-143">Anger de viktigaste användningarna i certifikatet.</span><span class="sxs-lookup"><span data-stu-id="84ba6-143">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]
Parameter Sets: (All)
Aliases:
Accepted values: None, EncipherOnly, CrlSign, KeyCertSign, KeyAgreement, DataEncipherment, KeyEncipherment, NonRepudiation, DigitalSignature, DecipherOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84ba6-144">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="84ba6-144">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="84ba6-145">Anger antalet dagar före utgångs datum efter vilket automatisk process för certifikat förnyelse påbörjas.</span><span class="sxs-lookup"><span data-stu-id="84ba6-145">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84ba6-146">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="84ba6-146">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="84ba6-147">Anger den procent andel av livs längden som den automatiska processen för certifikat förnyelse startas.</span><span class="sxs-lookup"><span data-stu-id="84ba6-147">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84ba6-148">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="84ba6-148">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="84ba6-149">Visar att certifikatet återanvändar den under förnyelse.</span><span class="sxs-lookup"><span data-stu-id="84ba6-149">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84ba6-150">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="84ba6-150">-SecretContentType</span></span>
<span data-ttu-id="84ba6-151">Anger innehålls typen för den nya nyckel valv hemligheten.</span><span class="sxs-lookup"><span data-stu-id="84ba6-151">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="84ba6-152">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="84ba6-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="84ba6-153">Application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="84ba6-153">application/x-pkcs12</span></span>
- <span data-ttu-id="84ba6-154">Application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="84ba6-154">application/x-pem-file</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84ba6-155">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="84ba6-155">-SubjectName</span></span>
<span data-ttu-id="84ba6-156">Anger ämnets namn för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="84ba6-156">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SubjectName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DNSNames
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84ba6-157">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="84ba6-157">-ValidityInMonths</span></span>
<span data-ttu-id="84ba6-158">Anger antalet månader som certifikatet är giltigt.</span><span class="sxs-lookup"><span data-stu-id="84ba6-158">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84ba6-159">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="84ba6-159">-Confirm</span></span>
<span data-ttu-id="84ba6-160">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="84ba6-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84ba6-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84ba6-161">-WhatIf</span></span>
<span data-ttu-id="84ba6-162">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="84ba6-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84ba6-163">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="84ba6-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84ba6-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84ba6-164">CommonParameters</span></span>
<span data-ttu-id="84ba6-165">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84ba6-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84ba6-166">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84ba6-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84ba6-167">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="84ba6-167">INPUTS</span></span>

### <span data-ttu-id="84ba6-168">System. String</span><span class="sxs-lookup"><span data-stu-id="84ba6-168">System.String</span></span>

### <span data-ttu-id="84ba6-169">System. Collections. Generic. list ' 1 [[system. String, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="84ba6-169">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="84ba6-170">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="84ba6-170">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="84ba6-171">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="84ba6-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="84ba6-172">System. Collections. Generic. list ' 1 [[system. Security. Cryptography. X509Certificates. X509KeyUsageFlags, system. Security. Cryptography. X509Certificates, version = 4.2.1.0, Culture = neutralt, PublicKeyToken = b03f5f7f11d50a3a]]</span><span class="sxs-lookup"><span data-stu-id="84ba6-172">System.Collections.Generic.List\`1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System.Security.Cryptography.X509Certificates, Version=4.2.1.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a]]</span></span>

## <span data-ttu-id="84ba6-173">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="84ba6-173">OUTPUTS</span></span>

### <span data-ttu-id="84ba6-174">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="84ba6-174">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="84ba6-175">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="84ba6-175">NOTES</span></span>

## <span data-ttu-id="84ba6-176">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="84ba6-176">RELATED LINKS</span></span>

[<span data-ttu-id="84ba6-177">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="84ba6-177">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="84ba6-178">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="84ba6-178">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

