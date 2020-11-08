---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: b0d690358fb5598b1a88ecb7fe169c8ef3d2718f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092607"
---
# <span data-ttu-id="71070-101">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="71070-101">New-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="71070-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="71070-102">SYNOPSIS</span></span>
<span data-ttu-id="71070-103">Skapar ett certifikat policy objekt för minnet.</span><span class="sxs-lookup"><span data-stu-id="71070-103">Creates an in-memory certificate policy object.</span></span>

## <span data-ttu-id="71070-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="71070-104">SYNTAX</span></span>

### <span data-ttu-id="71070-105">SubjectName (standard)</span><span class="sxs-lookup"><span data-stu-id="71070-105">SubjectName (Default)</span></span>
```
New-AzKeyVaultCertificatePolicy [-IssuerName] <String> [-SubjectName] <String>
 [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>]
 [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71070-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="71070-106">DNSNames</span></span>
```
New-AzKeyVaultCertificatePolicy [-IssuerName] <String> [[-SubjectName] <String>]
 [-DnsName] <System.Collections.Generic.List`1[System.String]> [-RenewAtNumberOfDaysBeforeExpiry <Int32>]
 [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71070-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="71070-107">DESCRIPTION</span></span>
<span data-ttu-id="71070-108">Cmdleten **New-AzKeyVaultCertificatePolicy** skapar ett certifikats princip objekt i minnet för Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="71070-108">The **New-AzKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="71070-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="71070-109">EXAMPLES</span></span>

### <span data-ttu-id="71070-110">Exempel 1: skapa en certifikat princip</span><span class="sxs-lookup"><span data-stu-id="71070-110">Example 1: Create a certificate policy</span></span>
```powershell
PS C:\> New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal

SecretContentType               : application/x-pkcs12
Kty                             :
KeySize                         : 2048
Curve                           :
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

<span data-ttu-id="71070-111">Det här kommandot skapar en certifikat princip som är giltig i sex månader och återanvänder den för att förnya certifikatet.</span><span class="sxs-lookup"><span data-stu-id="71070-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="71070-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="71070-112">PARAMETERS</span></span>

### <span data-ttu-id="71070-113">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="71070-113">-CertificateTransparency</span></span>
<span data-ttu-id="71070-114">Anger om certifikat transparens är aktiverat för det här certifikatet/utgivaren. Om inget anges är standardvärdet "true"</span><span class="sxs-lookup"><span data-stu-id="71070-114">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71070-115">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="71070-115">-CertificateType</span></span>
<span data-ttu-id="71070-116">Anger typen av certifikat för utgivaren.</span><span class="sxs-lookup"><span data-stu-id="71070-116">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="71070-117">-Kurva</span><span class="sxs-lookup"><span data-stu-id="71070-117">-Curve</span></span>
<span data-ttu-id="71070-118">Anger Elliptic-kurv namnet på certifikatet.</span><span class="sxs-lookup"><span data-stu-id="71070-118">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="71070-119">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="71070-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="71070-120">P-256</span><span class="sxs-lookup"><span data-stu-id="71070-120">P-256</span></span>
- <span data-ttu-id="71070-121">P-384</span><span class="sxs-lookup"><span data-stu-id="71070-121">P-384</span></span>
- <span data-ttu-id="71070-122">P-521</span><span class="sxs-lookup"><span data-stu-id="71070-122">P-521</span></span>
- <span data-ttu-id="71070-123">P – 256 K</span><span class="sxs-lookup"><span data-stu-id="71070-123">P-256K</span></span>
- <span data-ttu-id="71070-124">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="71070-124">SECP256K1</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: P-256, P-384, P-521, P-256K, SECP256K1

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71070-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71070-125">-DefaultProfile</span></span>
<span data-ttu-id="71070-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="71070-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71070-127">-Inaktive rad</span><span class="sxs-lookup"><span data-stu-id="71070-127">-Disabled</span></span>
<span data-ttu-id="71070-128">Anger att certifikat principen är inaktive rad.</span><span class="sxs-lookup"><span data-stu-id="71070-128">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="71070-129">-DnsName</span><span class="sxs-lookup"><span data-stu-id="71070-129">-DnsName</span></span>
<span data-ttu-id="71070-130">Anger DNS-namnen i certifikatet.</span><span class="sxs-lookup"><span data-stu-id="71070-130">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="71070-131">-EKU</span><span class="sxs-lookup"><span data-stu-id="71070-131">-Ekus</span></span>
<span data-ttu-id="71070-132">Anger EKU (Enhanced Key Usage) i certifikatet.</span><span class="sxs-lookup"><span data-stu-id="71070-132">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="71070-133">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="71070-133">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="71070-134">Anger hur många dagar som ska gå innan den automatiska aviseringen startar.</span><span class="sxs-lookup"><span data-stu-id="71070-134">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="71070-135">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="71070-135">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="71070-136">Anger den procent andel av livs längden som den automatiska processen för aviseringen startar.</span><span class="sxs-lookup"><span data-stu-id="71070-136">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="71070-137">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="71070-137">-IssuerName</span></span>
<span data-ttu-id="71070-138">Anger namnet på utgivaren av certifikatet.</span><span class="sxs-lookup"><span data-stu-id="71070-138">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="71070-139">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="71070-139">-KeyNotExportable</span></span>
<span data-ttu-id="71070-140">Visar att det inte går att exportera den.</span><span class="sxs-lookup"><span data-stu-id="71070-140">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="71070-141">-Dubbel storlek</span><span class="sxs-lookup"><span data-stu-id="71070-141">-KeySize</span></span>
<span data-ttu-id="71070-142">Anger certifikatets viktigaste storlek.</span><span class="sxs-lookup"><span data-stu-id="71070-142">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="71070-143">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="71070-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="71070-144">2048</span><span class="sxs-lookup"><span data-stu-id="71070-144">2048</span></span>
- <span data-ttu-id="71070-145">3072</span><span class="sxs-lookup"><span data-stu-id="71070-145">3072</span></span>
- <span data-ttu-id="71070-146">4096</span><span class="sxs-lookup"><span data-stu-id="71070-146">4096</span></span>
- <span data-ttu-id="71070-147">256</span><span class="sxs-lookup"><span data-stu-id="71070-147">256</span></span>
- <span data-ttu-id="71070-148">384</span><span class="sxs-lookup"><span data-stu-id="71070-148">384</span></span>
- <span data-ttu-id="71070-149">521</span><span class="sxs-lookup"><span data-stu-id="71070-149">521</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:
Accepted values: 2048, 3072, 4096, 256, 384, 521

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71070-150">-Värdetyp</span><span class="sxs-lookup"><span data-stu-id="71070-150">-KeyType</span></span>
<span data-ttu-id="71070-151">Anger huvud typen för den knapp som återställer certifikatet.</span><span class="sxs-lookup"><span data-stu-id="71070-151">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="71070-152">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="71070-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="71070-153">RSA</span><span class="sxs-lookup"><span data-stu-id="71070-153">RSA</span></span>
- <span data-ttu-id="71070-154">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="71070-154">RSA-HSM</span></span>
- <span data-ttu-id="71070-155">EC</span><span class="sxs-lookup"><span data-stu-id="71070-155">EC</span></span>
- <span data-ttu-id="71070-156">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="71070-156">EC-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM, EC, EC-HSM

Required: False
Position: Named
Default value: RSA
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71070-157">-Använd ande av</span><span class="sxs-lookup"><span data-stu-id="71070-157">-KeyUsage</span></span>
<span data-ttu-id="71070-158">Anger de viktigaste användningarna i certifikatet.</span><span class="sxs-lookup"><span data-stu-id="71070-158">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="71070-159">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="71070-159">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="71070-160">Anger antalet dagar före utgångs datum efter vilket automatisk process för certifikat förnyelse påbörjas.</span><span class="sxs-lookup"><span data-stu-id="71070-160">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="71070-161">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="71070-161">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="71070-162">Anger den procent andel av livs längden som den automatiska processen för certifikat förnyelse startas.</span><span class="sxs-lookup"><span data-stu-id="71070-162">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="71070-163">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="71070-163">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="71070-164">Visar att certifikatet återanvändar den under förnyelse.</span><span class="sxs-lookup"><span data-stu-id="71070-164">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="71070-165">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="71070-165">-SecretContentType</span></span>
<span data-ttu-id="71070-166">Anger innehålls typen för den nya nyckel valv hemligheten.</span><span class="sxs-lookup"><span data-stu-id="71070-166">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="71070-167">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="71070-167">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="71070-168">Application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="71070-168">application/x-pkcs12</span></span>
- <span data-ttu-id="71070-169">Application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="71070-169">application/x-pem-file</span></span>

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

### <span data-ttu-id="71070-170">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="71070-170">-SubjectName</span></span>
<span data-ttu-id="71070-171">Anger ämnets namn för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="71070-171">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="71070-172">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="71070-172">-ValidityInMonths</span></span>
<span data-ttu-id="71070-173">Anger antalet månader som certifikatet är giltigt.</span><span class="sxs-lookup"><span data-stu-id="71070-173">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="71070-174">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="71070-174">-Confirm</span></span>
<span data-ttu-id="71070-175">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="71070-175">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71070-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71070-176">-WhatIf</span></span>
<span data-ttu-id="71070-177">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="71070-177">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71070-178">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="71070-178">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71070-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71070-179">CommonParameters</span></span>
<span data-ttu-id="71070-180">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71070-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71070-181">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71070-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71070-182">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="71070-182">INPUTS</span></span>

### <span data-ttu-id="71070-183">System. String</span><span class="sxs-lookup"><span data-stu-id="71070-183">System.String</span></span>

### <span data-ttu-id="71070-184">System. Collections. Generic. list ' 1 [[system. String, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="71070-184">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="71070-185">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="71070-185">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="71070-186">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="71070-186">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="71070-187">System. Collections. Generic. list ' 1 [[system. Security. Cryptography. X509Certificates. X509KeyUsageFlags, system. Security. Cryptography. X509Certificates, version = 4.2.1.0, Culture = neutralt, PublicKeyToken = b03f5f7f11d50a3a]]</span><span class="sxs-lookup"><span data-stu-id="71070-187">System.Collections.Generic.List\`1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System.Security.Cryptography.X509Certificates, Version=4.2.1.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a]]</span></span>

## <span data-ttu-id="71070-188">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="71070-188">OUTPUTS</span></span>

### <span data-ttu-id="71070-189">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="71070-189">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="71070-190">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="71070-190">NOTES</span></span>

## <span data-ttu-id="71070-191">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="71070-191">RELATED LINKS</span></span>

[<span data-ttu-id="71070-192">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="71070-192">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="71070-193">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="71070-193">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

