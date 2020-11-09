---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 963a7005e95941a644b35a57f80b558f02e2d6a0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319899"
---
# <span data-ttu-id="b74b8-101">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="b74b8-101">Set-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="b74b8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b74b8-102">SYNOPSIS</span></span>
<span data-ttu-id="b74b8-103">Skapar eller uppdaterar principen för ett certifikat i ett Key-valv.</span><span class="sxs-lookup"><span data-stu-id="b74b8-103">Creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="b74b8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b74b8-104">SYNTAX</span></span>

### <span data-ttu-id="b74b8-105">ExpandedRenewPercentage (standard)</span><span class="sxs-lookup"><span data-stu-id="b74b8-105">ExpandedRenewPercentage (Default)</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-RenewAtPercentageLifetime <Int32>]
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b74b8-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="b74b8-106">ByValue</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-KeySize <Int32>]
 [-CertificateTransparency <Boolean>] [-PassThru] [-Curve <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b74b8-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="b74b8-107">ExpandedRenewNumber</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> -RenewAtNumberOfDaysBeforeExpiry <Int32>
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b74b8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b74b8-108">DESCRIPTION</span></span>
<span data-ttu-id="b74b8-109">Cmdleten **set-AzKeyVaultCertificatePolicy** skapar eller uppdaterar principen för ett certifikat i ett Key-valv.</span><span class="sxs-lookup"><span data-stu-id="b74b8-109">The **Set-AzKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="b74b8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b74b8-110">EXAMPLES</span></span>

### <span data-ttu-id="b74b8-111">Exempel 1: Ange en certifikat princip</span><span class="sxs-lookup"><span data-stu-id="b74b8-111">Example 1: Set a certificate policy</span></span>
```powershell
PS C:\> Set-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True -PassThru

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

<span data-ttu-id="b74b8-112">Det här kommandot ställer in policyn för TestCert01-certifikatet i ContosoKV01-nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="b74b8-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="b74b8-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b74b8-113">PARAMETERS</span></span>

### <span data-ttu-id="b74b8-114">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="b74b8-114">-CertificateTransparency</span></span>
<span data-ttu-id="b74b8-115">Anger om certifikat transparens är aktiverat för det här certifikatet/utgivaren. Om inget anges är standardvärdet "true".</span><span class="sxs-lookup"><span data-stu-id="b74b8-115">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'.</span></span>
<span data-ttu-id="b74b8-116">`-IssuerName` måste anges när du ställer in den här egenskapen.</span><span class="sxs-lookup"><span data-stu-id="b74b8-116">`-IssuerName` needs to be specified when setting this property.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b74b8-117">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="b74b8-117">-CertificateType</span></span>
<span data-ttu-id="b74b8-118">Anger typen av certifikat för utgivaren.</span><span class="sxs-lookup"><span data-stu-id="b74b8-118">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b74b8-119">-Kurva</span><span class="sxs-lookup"><span data-stu-id="b74b8-119">-Curve</span></span>
<span data-ttu-id="b74b8-120">Anger Elliptic-kurv namnet på certifikatet.</span><span class="sxs-lookup"><span data-stu-id="b74b8-120">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="b74b8-121">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="b74b8-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b74b8-122">P-256</span><span class="sxs-lookup"><span data-stu-id="b74b8-122">P-256</span></span>
- <span data-ttu-id="b74b8-123">P-384</span><span class="sxs-lookup"><span data-stu-id="b74b8-123">P-384</span></span>
- <span data-ttu-id="b74b8-124">P-521</span><span class="sxs-lookup"><span data-stu-id="b74b8-124">P-521</span></span>
- <span data-ttu-id="b74b8-125">P – 256 K</span><span class="sxs-lookup"><span data-stu-id="b74b8-125">P-256K</span></span>
- <span data-ttu-id="b74b8-126">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="b74b8-126">SECP256K1</span></span>

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

### <span data-ttu-id="b74b8-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b74b8-127">-DefaultProfile</span></span>
<span data-ttu-id="b74b8-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b74b8-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b74b8-129">-Inaktive rad</span><span class="sxs-lookup"><span data-stu-id="b74b8-129">-Disabled</span></span>
<span data-ttu-id="b74b8-130">Anger att certifikat principen är inaktive rad.</span><span class="sxs-lookup"><span data-stu-id="b74b8-130">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b74b8-131">-DnsName</span><span class="sxs-lookup"><span data-stu-id="b74b8-131">-DnsName</span></span>
<span data-ttu-id="b74b8-132">Anger ämnets namn för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="b74b8-132">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases: DnsNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b74b8-133">-EKU</span><span class="sxs-lookup"><span data-stu-id="b74b8-133">-Ekus</span></span>
<span data-ttu-id="b74b8-134">Anger EKU (Enhanced Key Usage) i certifikatet.</span><span class="sxs-lookup"><span data-stu-id="b74b8-134">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b74b8-135">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="b74b8-135">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="b74b8-136">Anger antalet dagar före utgångs datum för automatisk förnyelse.</span><span class="sxs-lookup"><span data-stu-id="b74b8-136">Specifies the number of days before expiration when automatic renewal should start.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b74b8-137">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="b74b8-137">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="b74b8-138">Anger den procent andel av livs längden som den automatiska processen för aviseringen startar.</span><span class="sxs-lookup"><span data-stu-id="b74b8-138">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b74b8-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b74b8-139">-InputObject</span></span>
<span data-ttu-id="b74b8-140">Anger certifikat policyn.</span><span class="sxs-lookup"><span data-stu-id="b74b8-140">Specifies the certificate policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy
Parameter Sets: ByValue
Aliases: CertificatePolicy

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b74b8-141">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="b74b8-141">-IssuerName</span></span>
<span data-ttu-id="b74b8-142">Anger namnet på utgivaren för detta certifikat.</span><span class="sxs-lookup"><span data-stu-id="b74b8-142">Specifies the name of the issuer for this certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b74b8-143">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="b74b8-143">-KeyNotExportable</span></span>
<span data-ttu-id="b74b8-144">Visar att det inte går att exportera den.</span><span class="sxs-lookup"><span data-stu-id="b74b8-144">Indicates that the key is not exportable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b74b8-145">-Dubbel storlek</span><span class="sxs-lookup"><span data-stu-id="b74b8-145">-KeySize</span></span>
<span data-ttu-id="b74b8-146">Anger certifikatets viktigaste storlek.</span><span class="sxs-lookup"><span data-stu-id="b74b8-146">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="b74b8-147">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="b74b8-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b74b8-148">2048</span><span class="sxs-lookup"><span data-stu-id="b74b8-148">2048</span></span>
- <span data-ttu-id="b74b8-149">3072</span><span class="sxs-lookup"><span data-stu-id="b74b8-149">3072</span></span>
- <span data-ttu-id="b74b8-150">4096</span><span class="sxs-lookup"><span data-stu-id="b74b8-150">4096</span></span>
- <span data-ttu-id="b74b8-151">256</span><span class="sxs-lookup"><span data-stu-id="b74b8-151">256</span></span>
- <span data-ttu-id="b74b8-152">384</span><span class="sxs-lookup"><span data-stu-id="b74b8-152">384</span></span>
- <span data-ttu-id="b74b8-153">521</span><span class="sxs-lookup"><span data-stu-id="b74b8-153">521</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:
Accepted values: 2048, 3072, 4096, 256, 384, 521

Required: False
Position: Named
Default value: 2048
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b74b8-154">-Värdetyp</span><span class="sxs-lookup"><span data-stu-id="b74b8-154">-KeyType</span></span>
<span data-ttu-id="b74b8-155">Anger huvud typen för den knapp som återställer certifikatet.</span><span class="sxs-lookup"><span data-stu-id="b74b8-155">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="b74b8-156">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="b74b8-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b74b8-157">RSA</span><span class="sxs-lookup"><span data-stu-id="b74b8-157">RSA</span></span>
- <span data-ttu-id="b74b8-158">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="b74b8-158">RSA-HSM</span></span>
- <span data-ttu-id="b74b8-159">EC</span><span class="sxs-lookup"><span data-stu-id="b74b8-159">EC</span></span>
- <span data-ttu-id="b74b8-160">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="b74b8-160">EC-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM, EC, EC-HSM

Required: False
Position: Named
Default value: RSA
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b74b8-161">-Använd ande av</span><span class="sxs-lookup"><span data-stu-id="b74b8-161">-KeyUsage</span></span>
<span data-ttu-id="b74b8-162">Anger de viktigaste användningarna i certifikatet.</span><span class="sxs-lookup"><span data-stu-id="b74b8-162">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:
Accepted values: None, EncipherOnly, CrlSign, KeyCertSign, KeyAgreement, DataEncipherment, KeyEncipherment, NonRepudiation, DigitalSignature, DecipherOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b74b8-163">-Namn</span><span class="sxs-lookup"><span data-stu-id="b74b8-163">-Name</span></span>
<span data-ttu-id="b74b8-164">Anger namnet på certifikatet.</span><span class="sxs-lookup"><span data-stu-id="b74b8-164">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="b74b8-165">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b74b8-165">-PassThru</span></span>
<span data-ttu-id="b74b8-166">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="b74b8-166">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b74b8-167">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="b74b8-167">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b74b8-168">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="b74b8-168">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="b74b8-169">Anger antalet dagar före utgångs datum efter vilket automatisk process för certifikat förnyelse påbörjas.</span><span class="sxs-lookup"><span data-stu-id="b74b8-169">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ExpandedRenewNumber
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b74b8-170">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="b74b8-170">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="b74b8-171">Anger den procent andel av livs längden som den automatiska processen för certifikat förnyelse startas.</span><span class="sxs-lookup"><span data-stu-id="b74b8-171">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ExpandedRenewPercentage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b74b8-172">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="b74b8-172">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="b74b8-173">Visar att certifikatet återanvändar den under förnyelse.</span><span class="sxs-lookup"><span data-stu-id="b74b8-173">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b74b8-174">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="b74b8-174">-SecretContentType</span></span>
<span data-ttu-id="b74b8-175">Anger innehålls typen för den nya nyckel valv hemligheten.</span><span class="sxs-lookup"><span data-stu-id="b74b8-175">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="b74b8-176">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="b74b8-176">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b74b8-177">Application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="b74b8-177">application/x-pkcs12</span></span>
- <span data-ttu-id="b74b8-178">Application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="b74b8-178">application/x-pem-file</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b74b8-179">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="b74b8-179">-SubjectName</span></span>
<span data-ttu-id="b74b8-180">Anger ämnets namn för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="b74b8-180">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b74b8-181">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="b74b8-181">-ValidityInMonths</span></span>
<span data-ttu-id="b74b8-182">Anger antalet månader som certifikatet är giltigt.</span><span class="sxs-lookup"><span data-stu-id="b74b8-182">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b74b8-183">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b74b8-183">-VaultName</span></span>
<span data-ttu-id="b74b8-184">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="b74b8-184">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="b74b8-185">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b74b8-185">-Confirm</span></span>
<span data-ttu-id="b74b8-186">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b74b8-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b74b8-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b74b8-187">-WhatIf</span></span>
<span data-ttu-id="b74b8-188">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b74b8-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b74b8-189">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b74b8-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b74b8-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b74b8-190">CommonParameters</span></span>
<span data-ttu-id="b74b8-191">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b74b8-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b74b8-192">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b74b8-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b74b8-193">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b74b8-193">INPUTS</span></span>

### <span data-ttu-id="b74b8-194">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="b74b8-194">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="b74b8-195">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b74b8-195">OUTPUTS</span></span>

### <span data-ttu-id="b74b8-196">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="b74b8-196">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="b74b8-197">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b74b8-197">NOTES</span></span>

## <span data-ttu-id="b74b8-198">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b74b8-198">RELATED LINKS</span></span>

[<span data-ttu-id="b74b8-199">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="b74b8-199">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="b74b8-200">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="b74b8-200">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

