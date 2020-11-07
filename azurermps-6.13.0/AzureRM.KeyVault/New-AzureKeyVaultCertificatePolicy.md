---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: a77cd700064777c769d5499cb099cfa3f9a53ec0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755707"
---
# <span data-ttu-id="bdddc-101">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="bdddc-101">New-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="bdddc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bdddc-102">SYNOPSIS</span></span>
<span data-ttu-id="bdddc-103">Skapar ett certifikat policy objekt för minnet.</span><span class="sxs-lookup"><span data-stu-id="bdddc-103">Creates an in-memory certificate policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bdddc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bdddc-104">SYNTAX</span></span>

### <span data-ttu-id="bdddc-105">SubjectName (standard)</span><span class="sxs-lookup"><span data-stu-id="bdddc-105">SubjectName (Default)</span></span>
```
New-AzureKeyVaultCertificatePolicy [-IssuerName] <String> [-SubjectName] <String>
 [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>]
 [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bdddc-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="bdddc-106">DNSNames</span></span>
```
New-AzureKeyVaultCertificatePolicy [-IssuerName] <String> [[-SubjectName] <String>]
 [-DnsName] <System.Collections.Generic.List`1[System.String]> [-RenewAtNumberOfDaysBeforeExpiry <Int32>]
 [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bdddc-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bdddc-107">DESCRIPTION</span></span>
<span data-ttu-id="bdddc-108">Cmdleten **New-AzureKeyVaultCertificatePolicy** skapar ett certifikats princip objekt i minnet för Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="bdddc-108">The **New-AzureKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="bdddc-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bdddc-109">EXAMPLES</span></span>

### <span data-ttu-id="bdddc-110">Exempel 1: skapa en certifikat princip</span><span class="sxs-lookup"><span data-stu-id="bdddc-110">Example 1: Create a certificate policy</span></span>
```powershell
PS C:\> New-AzureKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal

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

<span data-ttu-id="bdddc-111">Det här kommandot skapar en certifikat princip som är giltig i sex månader och återanvänder den för att förnya certifikatet.</span><span class="sxs-lookup"><span data-stu-id="bdddc-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="bdddc-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bdddc-112">PARAMETERS</span></span>

### <span data-ttu-id="bdddc-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="bdddc-113">-CertificateType</span></span>
<span data-ttu-id="bdddc-114">Anger typen av certifikat för utgivaren.</span><span class="sxs-lookup"><span data-stu-id="bdddc-114">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="bdddc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdddc-115">-DefaultProfile</span></span>
<span data-ttu-id="bdddc-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="bdddc-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bdddc-117">-Inaktive rad</span><span class="sxs-lookup"><span data-stu-id="bdddc-117">-Disabled</span></span>
<span data-ttu-id="bdddc-118">Anger att certifikat principen är inaktive rad.</span><span class="sxs-lookup"><span data-stu-id="bdddc-118">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="bdddc-119">-DnsName</span><span class="sxs-lookup"><span data-stu-id="bdddc-119">-DnsName</span></span>
<span data-ttu-id="bdddc-120">Anger DNS-namnen i certifikatet.</span><span class="sxs-lookup"><span data-stu-id="bdddc-120">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="bdddc-121">-EKU</span><span class="sxs-lookup"><span data-stu-id="bdddc-121">-Ekus</span></span>
<span data-ttu-id="bdddc-122">Anger EKU (Enhanced Key Usage) i certifikatet.</span><span class="sxs-lookup"><span data-stu-id="bdddc-122">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="bdddc-123">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="bdddc-123">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="bdddc-124">Anger hur många dagar som ska gå innan den automatiska aviseringen startar.</span><span class="sxs-lookup"><span data-stu-id="bdddc-124">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="bdddc-125">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="bdddc-125">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="bdddc-126">Anger den procent andel av livs längden som den automatiska processen för aviseringen startar.</span><span class="sxs-lookup"><span data-stu-id="bdddc-126">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="bdddc-127">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="bdddc-127">-IssuerName</span></span>
<span data-ttu-id="bdddc-128">Anger namnet på utgivaren av certifikatet.</span><span class="sxs-lookup"><span data-stu-id="bdddc-128">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="bdddc-129">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="bdddc-129">-KeyNotExportable</span></span>
<span data-ttu-id="bdddc-130">Visar att det inte går att exportera den.</span><span class="sxs-lookup"><span data-stu-id="bdddc-130">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="bdddc-131">-Värdetyp</span><span class="sxs-lookup"><span data-stu-id="bdddc-131">-KeyType</span></span>
<span data-ttu-id="bdddc-132">Anger huvud typen för den knapp som återställer certifikatet.</span><span class="sxs-lookup"><span data-stu-id="bdddc-132">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="bdddc-133">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="bdddc-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bdddc-134">RSA</span><span class="sxs-lookup"><span data-stu-id="bdddc-134">RSA</span></span>
- <span data-ttu-id="bdddc-135">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="bdddc-135">RSA-HSM</span></span>

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

### <span data-ttu-id="bdddc-136">-Använd ande av</span><span class="sxs-lookup"><span data-stu-id="bdddc-136">-KeyUsage</span></span>
<span data-ttu-id="bdddc-137">Anger de viktigaste användningarna i certifikatet.</span><span class="sxs-lookup"><span data-stu-id="bdddc-137">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="bdddc-138">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="bdddc-138">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="bdddc-139">Anger antalet dagar före utgångs datum efter vilket automatisk process för certifikat förnyelse påbörjas.</span><span class="sxs-lookup"><span data-stu-id="bdddc-139">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="bdddc-140">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="bdddc-140">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="bdddc-141">Anger den procent andel av livs längden som den automatiska processen för certifikat förnyelse startas.</span><span class="sxs-lookup"><span data-stu-id="bdddc-141">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="bdddc-142">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="bdddc-142">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="bdddc-143">Visar att certifikatet återanvändar den under förnyelse.</span><span class="sxs-lookup"><span data-stu-id="bdddc-143">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="bdddc-144">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="bdddc-144">-SecretContentType</span></span>
<span data-ttu-id="bdddc-145">Anger innehålls typen för den nya nyckel valv hemligheten.</span><span class="sxs-lookup"><span data-stu-id="bdddc-145">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="bdddc-146">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="bdddc-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bdddc-147">Application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="bdddc-147">application/x-pkcs12</span></span>
- <span data-ttu-id="bdddc-148">Application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="bdddc-148">application/x-pem-file</span></span>

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

### <span data-ttu-id="bdddc-149">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="bdddc-149">-SubjectName</span></span>
<span data-ttu-id="bdddc-150">Anger ämnets namn för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="bdddc-150">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="bdddc-151">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="bdddc-151">-ValidityInMonths</span></span>
<span data-ttu-id="bdddc-152">Anger antalet månader som certifikatet är giltigt.</span><span class="sxs-lookup"><span data-stu-id="bdddc-152">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="bdddc-153">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bdddc-153">-Confirm</span></span>
<span data-ttu-id="bdddc-154">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bdddc-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdddc-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdddc-155">-WhatIf</span></span>
<span data-ttu-id="bdddc-156">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bdddc-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdddc-157">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bdddc-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdddc-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdddc-158">CommonParameters</span></span>
<span data-ttu-id="bdddc-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdddc-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdddc-160">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdddc-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdddc-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bdddc-161">INPUTS</span></span>

### <span data-ttu-id="bdddc-162">System. String</span><span class="sxs-lookup"><span data-stu-id="bdddc-162">System.String</span></span>

### <span data-ttu-id="bdddc-163">System. Collections. Generic. list ' 1 [[system. String, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="bdddc-163">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="bdddc-164">System. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="bdddc-164">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="bdddc-165">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bdddc-165">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="bdddc-166">System. Collections. Generic. list ' 1 [[system. Security. Cryptography. X509Certificates. X509KeyUsageFlags, system, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="bdddc-166">System.Collections.Generic.List\`1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="bdddc-167">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bdddc-167">OUTPUTS</span></span>

### <span data-ttu-id="bdddc-168">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="bdddc-168">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="bdddc-169">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bdddc-169">NOTES</span></span>

## <span data-ttu-id="bdddc-170">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bdddc-170">RELATED LINKS</span></span>

[<span data-ttu-id="bdddc-171">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="bdddc-171">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="bdddc-172">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="bdddc-172">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

