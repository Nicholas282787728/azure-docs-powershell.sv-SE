---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 370662b1d24f9b5b71653506be7a3add5a3801f8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98425843"
---
# <span data-ttu-id="1b502-101">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="1b502-101">New-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="1b502-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1b502-102">SYNOPSIS</span></span>
<span data-ttu-id="1b502-103">Skapar ett certifikat policy objekt för minnet.</span><span class="sxs-lookup"><span data-stu-id="1b502-103">Creates an in-memory certificate policy object.</span></span>

## <span data-ttu-id="1b502-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1b502-104">SYNTAX</span></span>

### <span data-ttu-id="1b502-105">SubjectName (standard)</span><span class="sxs-lookup"><span data-stu-id="1b502-105">SubjectName (Default)</span></span>
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

### <span data-ttu-id="1b502-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="1b502-106">DNSNames</span></span>
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

## <span data-ttu-id="1b502-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1b502-107">DESCRIPTION</span></span>
<span data-ttu-id="1b502-108">Cmdleten **New-AzKeyVaultCertificatePolicy** skapar ett certifikats princip objekt i minnet för Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="1b502-108">The **New-AzKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="1b502-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1b502-109">EXAMPLES</span></span>

### <span data-ttu-id="1b502-110">Exempel 1: skapa en certifikat princip</span><span class="sxs-lookup"><span data-stu-id="1b502-110">Example 1: Create a certificate policy</span></span>
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

<span data-ttu-id="1b502-111">Det här kommandot skapar en certifikat princip som är giltig i sex månader och återanvänder den för att förnya certifikatet.</span><span class="sxs-lookup"><span data-stu-id="1b502-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

### <span data-ttu-id="1b502-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="1b502-112">Example 2</span></span>

<span data-ttu-id="1b502-113">Skapar ett certifikat policy objekt för minnet.</span><span class="sxs-lookup"><span data-stu-id="1b502-113">Creates an in-memory certificate policy object.</span></span> <span data-ttu-id="1b502-114">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="1b502-114">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzKeyVaultCertificatePolicy -IssuerName 'Self' -KeyType RSA -RenewAtNumberOfDaysBeforeExpiry <Int32> -SecretContentType application/x-pkcs12 -SubjectName 'CN=contoso.com' -ValidityInMonths 6
```

### <span data-ttu-id="1b502-115">Exempel 3: skapa ett certifikat för ett alternativt subjekt namn (eller ett SAN)</span><span class="sxs-lookup"><span data-stu-id="1b502-115">Example 3: Create a Subject Alternate Name (or SAN) certificate</span></span>

```powershell
PS C:\> New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -DnsName "contoso.com","support.contoso.com","docs.contoso.com" -IssuerName "Self"

SecretContentType               : application/x-pkcs12
Kty                             : RSA
KeySize                         : 2048
Curve                           :
Exportable                      :
ReuseKeyOnRenewal               : False
SubjectName                     : CN=contoso.com
DnsNames                        : {contoso.com, support.contoso.com, docs.contoso.com}
KeyUsage                        :
Ekus                            :
ValidityInMonths                :
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

<span data-ttu-id="1b502-116">I det här exemplet skapas ett SAN-certifikat med 3 DNS-namn.</span><span class="sxs-lookup"><span data-stu-id="1b502-116">This example creates a SAN certificate with 3 DNS names.</span></span>

## <span data-ttu-id="1b502-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1b502-117">PARAMETERS</span></span>

### <span data-ttu-id="1b502-118">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="1b502-118">-CertificateTransparency</span></span>
<span data-ttu-id="1b502-119">Anger om certifikat transparens är aktiverat för det här certifikatet/utgivaren. Om inget anges är standardvärdet "true"</span><span class="sxs-lookup"><span data-stu-id="1b502-119">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

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

### <span data-ttu-id="1b502-120">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="1b502-120">-CertificateType</span></span>
<span data-ttu-id="1b502-121">Anger typen av certifikat för utgivaren.</span><span class="sxs-lookup"><span data-stu-id="1b502-121">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="1b502-122">-Kurva</span><span class="sxs-lookup"><span data-stu-id="1b502-122">-Curve</span></span>
<span data-ttu-id="1b502-123">Anger Elliptic-kurv namnet på certifikatet.</span><span class="sxs-lookup"><span data-stu-id="1b502-123">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="1b502-124">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="1b502-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1b502-125">P-256</span><span class="sxs-lookup"><span data-stu-id="1b502-125">P-256</span></span>
- <span data-ttu-id="1b502-126">P-384</span><span class="sxs-lookup"><span data-stu-id="1b502-126">P-384</span></span>
- <span data-ttu-id="1b502-127">P-521</span><span class="sxs-lookup"><span data-stu-id="1b502-127">P-521</span></span>
- <span data-ttu-id="1b502-128">P – 256 K</span><span class="sxs-lookup"><span data-stu-id="1b502-128">P-256K</span></span>
- <span data-ttu-id="1b502-129">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="1b502-129">SECP256K1</span></span>

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

### <span data-ttu-id="1b502-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b502-130">-DefaultProfile</span></span>
<span data-ttu-id="1b502-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1b502-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1b502-132">-Inaktive rad</span><span class="sxs-lookup"><span data-stu-id="1b502-132">-Disabled</span></span>
<span data-ttu-id="1b502-133">Anger att certifikat principen är inaktive rad.</span><span class="sxs-lookup"><span data-stu-id="1b502-133">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="1b502-134">-DnsName</span><span class="sxs-lookup"><span data-stu-id="1b502-134">-DnsName</span></span>
<span data-ttu-id="1b502-135">Anger DNS-namnen i certifikatet.</span><span class="sxs-lookup"><span data-stu-id="1b502-135">Specifies the DNS names in the certificate.</span></span> <span data-ttu-id="1b502-136">Alternativa namn för subjekt (San) kan anges som DNS-namn.</span><span class="sxs-lookup"><span data-stu-id="1b502-136">Subject Alternative Names (SANs) can be specified as DNS names.</span></span>

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

### <span data-ttu-id="1b502-137">-EKU</span><span class="sxs-lookup"><span data-stu-id="1b502-137">-Ekus</span></span>
<span data-ttu-id="1b502-138">Anger EKU (Enhanced Key Usage) i certifikatet.</span><span class="sxs-lookup"><span data-stu-id="1b502-138">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="1b502-139">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="1b502-139">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="1b502-140">Anger hur många dagar som ska gå innan den automatiska aviseringen startar.</span><span class="sxs-lookup"><span data-stu-id="1b502-140">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="1b502-141">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="1b502-141">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="1b502-142">Anger den procent andel av livs längden som den automatiska processen för aviseringen startar.</span><span class="sxs-lookup"><span data-stu-id="1b502-142">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="1b502-143">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="1b502-143">-IssuerName</span></span>
<span data-ttu-id="1b502-144">Anger namnet på utgivaren av certifikatet.</span><span class="sxs-lookup"><span data-stu-id="1b502-144">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="1b502-145">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="1b502-145">-KeyNotExportable</span></span>
<span data-ttu-id="1b502-146">Visar att det inte går att exportera den.</span><span class="sxs-lookup"><span data-stu-id="1b502-146">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="1b502-147">-Dubbel storlek</span><span class="sxs-lookup"><span data-stu-id="1b502-147">-KeySize</span></span>
<span data-ttu-id="1b502-148">Anger certifikatets viktigaste storlek.</span><span class="sxs-lookup"><span data-stu-id="1b502-148">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="1b502-149">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="1b502-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1b502-150">2048</span><span class="sxs-lookup"><span data-stu-id="1b502-150">2048</span></span>
- <span data-ttu-id="1b502-151">3072</span><span class="sxs-lookup"><span data-stu-id="1b502-151">3072</span></span>
- <span data-ttu-id="1b502-152">4096</span><span class="sxs-lookup"><span data-stu-id="1b502-152">4096</span></span>
- <span data-ttu-id="1b502-153">256</span><span class="sxs-lookup"><span data-stu-id="1b502-153">256</span></span>
- <span data-ttu-id="1b502-154">384</span><span class="sxs-lookup"><span data-stu-id="1b502-154">384</span></span>
- <span data-ttu-id="1b502-155">521</span><span class="sxs-lookup"><span data-stu-id="1b502-155">521</span></span>

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

### <span data-ttu-id="1b502-156">-Värdetyp</span><span class="sxs-lookup"><span data-stu-id="1b502-156">-KeyType</span></span>
<span data-ttu-id="1b502-157">Anger huvud typen för den knapp som återställer certifikatet.</span><span class="sxs-lookup"><span data-stu-id="1b502-157">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="1b502-158">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="1b502-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1b502-159">RSA</span><span class="sxs-lookup"><span data-stu-id="1b502-159">RSA</span></span>
- <span data-ttu-id="1b502-160">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="1b502-160">RSA-HSM</span></span>
- <span data-ttu-id="1b502-161">EC</span><span class="sxs-lookup"><span data-stu-id="1b502-161">EC</span></span>
- <span data-ttu-id="1b502-162">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="1b502-162">EC-HSM</span></span>

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

### <span data-ttu-id="1b502-163">-Använd ande av</span><span class="sxs-lookup"><span data-stu-id="1b502-163">-KeyUsage</span></span>
<span data-ttu-id="1b502-164">Anger de viktigaste användningarna i certifikatet.</span><span class="sxs-lookup"><span data-stu-id="1b502-164">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="1b502-165">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="1b502-165">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="1b502-166">Anger antalet dagar före utgångs datum efter vilket automatisk process för certifikat förnyelse påbörjas.</span><span class="sxs-lookup"><span data-stu-id="1b502-166">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="1b502-167">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="1b502-167">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="1b502-168">Anger den procent andel av livs längden som den automatiska processen för certifikat förnyelse startas.</span><span class="sxs-lookup"><span data-stu-id="1b502-168">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="1b502-169">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="1b502-169">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="1b502-170">Visar att certifikatet återanvändar den under förnyelse.</span><span class="sxs-lookup"><span data-stu-id="1b502-170">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="1b502-171">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="1b502-171">-SecretContentType</span></span>
<span data-ttu-id="1b502-172">Anger innehålls typen för den nya nyckel valv hemligheten.</span><span class="sxs-lookup"><span data-stu-id="1b502-172">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="1b502-173">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="1b502-173">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1b502-174">Application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="1b502-174">application/x-pkcs12</span></span>
- <span data-ttu-id="1b502-175">Application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="1b502-175">application/x-pem-file</span></span>

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

### <span data-ttu-id="1b502-176">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="1b502-176">-SubjectName</span></span>
<span data-ttu-id="1b502-177">Anger ämnets namn för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="1b502-177">Specifies the subject name of the certificate.</span></span> 

> [!NOTE]
> <span data-ttu-id="1b502-178">Om du måste använda ett kommatecken (,) eller en punkt (.) i en egenskap i `SubjectName` parametern måste du omge egenskaps fältet med citat tecken.</span><span class="sxs-lookup"><span data-stu-id="1b502-178">If you must use a comma (,) or a period (.) within a property in the `SubjectName` parameter, you must enclose the property field in quotation marks.</span></span> <span data-ttu-id="1b502-179">Du kan till exempel använda O = "contoso, Ltd."</span><span class="sxs-lookup"><span data-stu-id="1b502-179">For example, you may use O="Contoso, Ltd."</span></span> <span data-ttu-id="1b502-180">i fältet organisations namn.</span><span class="sxs-lookup"><span data-stu-id="1b502-180">in the Organization Name field.</span></span>

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

### <span data-ttu-id="1b502-181">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="1b502-181">-ValidityInMonths</span></span>
<span data-ttu-id="1b502-182">Anger antalet månader som certifikatet är giltigt.</span><span class="sxs-lookup"><span data-stu-id="1b502-182">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="1b502-183">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1b502-183">-Confirm</span></span>
<span data-ttu-id="1b502-184">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1b502-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b502-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b502-185">-WhatIf</span></span>
<span data-ttu-id="1b502-186">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1b502-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b502-187">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1b502-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b502-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b502-188">CommonParameters</span></span>
<span data-ttu-id="1b502-189">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b502-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b502-190">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1b502-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b502-191">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1b502-191">INPUTS</span></span>

### <span data-ttu-id="1b502-192">System. String</span><span class="sxs-lookup"><span data-stu-id="1b502-192">System.String</span></span>

### <span data-ttu-id="1b502-193">System. Collections. Generic. list ' 1 [[system. String, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1b502-193">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1b502-194">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1b502-194">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1b502-195">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1b502-195">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="1b502-196">System. Collections. Generic. list ' 1 [[system. Security. Cryptography. X509Certificates. X509KeyUsageFlags, system. Security. Cryptography. X509Certificates, version = 4.2.1.0, Culture = neutralt, PublicKeyToken = b03f5f7f11d50a3a]]</span><span class="sxs-lookup"><span data-stu-id="1b502-196">System.Collections.Generic.List\`1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System.Security.Cryptography.X509Certificates, Version=4.2.1.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a]]</span></span>

## <span data-ttu-id="1b502-197">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1b502-197">OUTPUTS</span></span>

### <span data-ttu-id="1b502-198">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="1b502-198">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="1b502-199">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1b502-199">NOTES</span></span>

## <span data-ttu-id="1b502-200">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1b502-200">RELATED LINKS</span></span>

[<span data-ttu-id="1b502-201">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="1b502-201">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="1b502-202">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="1b502-202">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

