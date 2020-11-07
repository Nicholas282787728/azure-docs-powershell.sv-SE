---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: e6ae1be8599869631698ddd886fa09184abfb867
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743874"
---
# <span data-ttu-id="de8e4-101">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="de8e4-101">Set-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="de8e4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="de8e4-102">SYNOPSIS</span></span>
<span data-ttu-id="de8e4-103">Skapar eller uppdaterar principen för ett certifikat i ett Key-valv.</span><span class="sxs-lookup"><span data-stu-id="de8e4-103">Creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="de8e4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="de8e4-104">SYNTAX</span></span>

### <span data-ttu-id="de8e4-105">ExpandedRenewPercentage (standard)</span><span class="sxs-lookup"><span data-stu-id="de8e4-105">ExpandedRenewPercentage (Default)</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-RenewAtPercentageLifetime <Int32>]
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeySize <Int32>] [-KeyType <String>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de8e4-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="de8e4-106">ByValue</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeySize <Int32>] [-KeyType <String>] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de8e4-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="de8e4-107">ExpandedRenewNumber</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> -RenewAtNumberOfDaysBeforeExpiry <Int32>
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeySize <Int32>] [-KeyType <String>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de8e4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="de8e4-108">DESCRIPTION</span></span>
<span data-ttu-id="de8e4-109">Cmdleten **set-AzKeyVaultCertificatePolicy** skapar eller uppdaterar principen för ett certifikat i ett Key-valv.</span><span class="sxs-lookup"><span data-stu-id="de8e4-109">The **Set-AzKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="de8e4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="de8e4-110">EXAMPLES</span></span>

### <span data-ttu-id="de8e4-111">Exempel 1: Ange en certifikat princip</span><span class="sxs-lookup"><span data-stu-id="de8e4-111">Example 1: Set a certificate policy</span></span>
```powershell
PS C:\> Set-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True -PassThru

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

<span data-ttu-id="de8e4-112">Det här kommandot ställer in policyn för TestCert01-certifikatet i ContosoKV01-nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="de8e4-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="de8e4-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="de8e4-113">PARAMETERS</span></span>

### <span data-ttu-id="de8e4-114">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="de8e4-114">-CertificateTransparency</span></span>
<span data-ttu-id="de8e4-115">Anger om certifikat transparens är aktiverat för det här certifikatet/utgivaren. Om inget anges är standardvärdet "true"</span><span class="sxs-lookup"><span data-stu-id="de8e4-115">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

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

### <span data-ttu-id="de8e4-116">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="de8e4-116">-CertificateType</span></span>
<span data-ttu-id="de8e4-117">Anger typen av certifikat för utgivaren.</span><span class="sxs-lookup"><span data-stu-id="de8e4-117">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="de8e4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de8e4-118">-DefaultProfile</span></span>
<span data-ttu-id="de8e4-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="de8e4-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="de8e4-120">-Inaktive rad</span><span class="sxs-lookup"><span data-stu-id="de8e4-120">-Disabled</span></span>
<span data-ttu-id="de8e4-121">Anger att certifikat principen är inaktive rad.</span><span class="sxs-lookup"><span data-stu-id="de8e4-121">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="de8e4-122">-DnsName</span><span class="sxs-lookup"><span data-stu-id="de8e4-122">-DnsName</span></span>
<span data-ttu-id="de8e4-123">Anger ämnets namn för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="de8e4-123">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="de8e4-124">-EKU</span><span class="sxs-lookup"><span data-stu-id="de8e4-124">-Ekus</span></span>
<span data-ttu-id="de8e4-125">Anger EKU (Enhanced Key Usage) i certifikatet.</span><span class="sxs-lookup"><span data-stu-id="de8e4-125">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="de8e4-126">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="de8e4-126">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="de8e4-127">Anger antalet dagar före utgångs datum för automatisk förnyelse.</span><span class="sxs-lookup"><span data-stu-id="de8e4-127">Specifies the number of days before expiration when automatic renewal should start.</span></span>

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

### <span data-ttu-id="de8e4-128">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="de8e4-128">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="de8e4-129">Anger den procent andel av livs längden som den automatiska processen för aviseringen startar.</span><span class="sxs-lookup"><span data-stu-id="de8e4-129">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="de8e4-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de8e4-130">-InputObject</span></span>
<span data-ttu-id="de8e4-131">Anger certifikat policyn.</span><span class="sxs-lookup"><span data-stu-id="de8e4-131">Specifies the certificate policy.</span></span>

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

### <span data-ttu-id="de8e4-132">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="de8e4-132">-IssuerName</span></span>
<span data-ttu-id="de8e4-133">Anger namnet på utgivaren för detta certifikat.</span><span class="sxs-lookup"><span data-stu-id="de8e4-133">Specifies the name of the issuer for this certificate.</span></span>

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

### <span data-ttu-id="de8e4-134">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="de8e4-134">-KeyNotExportable</span></span>
<span data-ttu-id="de8e4-135">Visar att det inte går att exportera den.</span><span class="sxs-lookup"><span data-stu-id="de8e4-135">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="de8e4-136">-Dubbel storlek</span><span class="sxs-lookup"><span data-stu-id="de8e4-136">-KeySize</span></span>
<span data-ttu-id="de8e4-137">Anger certifikatets viktigaste storlek.</span><span class="sxs-lookup"><span data-stu-id="de8e4-137">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="de8e4-138">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="de8e4-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="de8e4-139">2048</span><span class="sxs-lookup"><span data-stu-id="de8e4-139">2048</span></span>
- <span data-ttu-id="de8e4-140">3072</span><span class="sxs-lookup"><span data-stu-id="de8e4-140">3072</span></span>
- <span data-ttu-id="de8e4-141">4096</span><span class="sxs-lookup"><span data-stu-id="de8e4-141">4096</span></span>

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

### <span data-ttu-id="de8e4-142">-Värdetyp</span><span class="sxs-lookup"><span data-stu-id="de8e4-142">-KeyType</span></span>
<span data-ttu-id="de8e4-143">Anger huvud typen för den knapp som återställer certifikatet.</span><span class="sxs-lookup"><span data-stu-id="de8e4-143">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="de8e4-144">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="de8e4-144">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="de8e4-145">RSA</span><span class="sxs-lookup"><span data-stu-id="de8e4-145">RSA</span></span>
- <span data-ttu-id="de8e4-146">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="de8e4-146">RSA-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de8e4-147">-Använd ande av</span><span class="sxs-lookup"><span data-stu-id="de8e4-147">-KeyUsage</span></span>
<span data-ttu-id="de8e4-148">Anger de viktigaste användningarna i certifikatet.</span><span class="sxs-lookup"><span data-stu-id="de8e4-148">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="de8e4-149">-Namn</span><span class="sxs-lookup"><span data-stu-id="de8e4-149">-Name</span></span>
<span data-ttu-id="de8e4-150">Anger namnet på certifikatet.</span><span class="sxs-lookup"><span data-stu-id="de8e4-150">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="de8e4-151">-PassThru</span><span class="sxs-lookup"><span data-stu-id="de8e4-151">-PassThru</span></span>
<span data-ttu-id="de8e4-152">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="de8e4-152">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="de8e4-153">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="de8e4-153">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="de8e4-154">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="de8e4-154">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="de8e4-155">Anger antalet dagar före utgångs datum efter vilket automatisk process för certifikat förnyelse påbörjas.</span><span class="sxs-lookup"><span data-stu-id="de8e4-155">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="de8e4-156">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="de8e4-156">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="de8e4-157">Anger den procent andel av livs längden som den automatiska processen för certifikat förnyelse startas.</span><span class="sxs-lookup"><span data-stu-id="de8e4-157">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="de8e4-158">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="de8e4-158">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="de8e4-159">Visar att certifikatet återanvändar den under förnyelse.</span><span class="sxs-lookup"><span data-stu-id="de8e4-159">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="de8e4-160">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="de8e4-160">-SecretContentType</span></span>
<span data-ttu-id="de8e4-161">Anger innehålls typen för den nya nyckel valv hemligheten.</span><span class="sxs-lookup"><span data-stu-id="de8e4-161">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="de8e4-162">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="de8e4-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="de8e4-163">Application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="de8e4-163">application/x-pkcs12</span></span>
- <span data-ttu-id="de8e4-164">Application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="de8e4-164">application/x-pem-file</span></span>

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

### <span data-ttu-id="de8e4-165">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="de8e4-165">-SubjectName</span></span>
<span data-ttu-id="de8e4-166">Anger ämnets namn för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="de8e4-166">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="de8e4-167">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="de8e4-167">-ValidityInMonths</span></span>
<span data-ttu-id="de8e4-168">Anger antalet månader som certifikatet är giltigt.</span><span class="sxs-lookup"><span data-stu-id="de8e4-168">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="de8e4-169">-VaultName</span><span class="sxs-lookup"><span data-stu-id="de8e4-169">-VaultName</span></span>
<span data-ttu-id="de8e4-170">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="de8e4-170">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="de8e4-171">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="de8e4-171">-Confirm</span></span>
<span data-ttu-id="de8e4-172">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="de8e4-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de8e4-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de8e4-173">-WhatIf</span></span>
<span data-ttu-id="de8e4-174">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="de8e4-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de8e4-175">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="de8e4-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de8e4-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de8e4-176">CommonParameters</span></span>
<span data-ttu-id="de8e4-177">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de8e4-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de8e4-178">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de8e4-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de8e4-179">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="de8e4-179">INPUTS</span></span>

### <span data-ttu-id="de8e4-180">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="de8e4-180">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="de8e4-181">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="de8e4-181">OUTPUTS</span></span>

### <span data-ttu-id="de8e4-182">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="de8e4-182">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="de8e4-183">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="de8e4-183">NOTES</span></span>

## <span data-ttu-id="de8e4-184">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="de8e4-184">RELATED LINKS</span></span>

[<span data-ttu-id="de8e4-185">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="de8e4-185">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="de8e4-186">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="de8e4-186">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

