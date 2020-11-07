---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: 271da96d18628c899b10ac17185fd4c3a921d8a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574837"
---
# <span data-ttu-id="b37d4-101">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="b37d4-101">Set-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="b37d4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b37d4-102">SYNOPSIS</span></span>
<span data-ttu-id="b37d4-103">Skapar eller uppdaterar principen för ett certifikat i ett Key-valv.</span><span class="sxs-lookup"><span data-stu-id="b37d4-103">Creates or updates the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b37d4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b37d4-104">SYNTAX</span></span>

### <span data-ttu-id="b37d4-105">ExpandedRenewPercentage (standard)</span><span class="sxs-lookup"><span data-stu-id="b37d4-105">ExpandedRenewPercentage (Default)</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-RenewAtPercentageLifetime <Int32>]
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b37d4-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="b37d4-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b37d4-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="b37d4-107">ExpandedRenewNumber</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 -RenewAtNumberOfDaysBeforeExpiry <Int32> [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>]
 [-Disabled] [-SubjectName <String>] [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b37d4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b37d4-108">DESCRIPTION</span></span>
<span data-ttu-id="b37d4-109">Cmdleten **set-AzureKeyVaultCertificatePolicy** skapar eller uppdaterar principen för ett certifikat i ett Key-valv.</span><span class="sxs-lookup"><span data-stu-id="b37d4-109">The **Set-AzureKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="b37d4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b37d4-110">EXAMPLES</span></span>

### <span data-ttu-id="b37d4-111">Exempel 1: Ange en certifikat princip</span><span class="sxs-lookup"><span data-stu-id="b37d4-111">Example 1: Set a certificate policy</span></span>
```powershell
PS C:\> Set-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True -PassThru

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

<span data-ttu-id="b37d4-112">Det här kommandot ställer in policyn för TestCert01-certifikatet i ContosoKV01-nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="b37d4-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="b37d4-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b37d4-113">PARAMETERS</span></span>

### <span data-ttu-id="b37d4-114">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="b37d4-114">-CertificateTransparency</span></span>
<span data-ttu-id="b37d4-115">Anger om certifikat transparens är aktiverat för det här certifikatet/utgivaren. Om inget anges är standardvärdet "true"</span><span class="sxs-lookup"><span data-stu-id="b37d4-115">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

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

### <span data-ttu-id="b37d4-116">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="b37d4-116">-CertificateType</span></span>
<span data-ttu-id="b37d4-117">Anger typen av certifikat för utgivaren.</span><span class="sxs-lookup"><span data-stu-id="b37d4-117">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="b37d4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b37d4-118">-DefaultProfile</span></span>
<span data-ttu-id="b37d4-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b37d4-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b37d4-120">-Inaktive rad</span><span class="sxs-lookup"><span data-stu-id="b37d4-120">-Disabled</span></span>
<span data-ttu-id="b37d4-121">Anger att certifikat principen är inaktive rad.</span><span class="sxs-lookup"><span data-stu-id="b37d4-121">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="b37d4-122">-DnsName</span><span class="sxs-lookup"><span data-stu-id="b37d4-122">-DnsName</span></span>
<span data-ttu-id="b37d4-123">Anger ämnets namn för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="b37d4-123">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="b37d4-124">-EKU</span><span class="sxs-lookup"><span data-stu-id="b37d4-124">-Ekus</span></span>
<span data-ttu-id="b37d4-125">Anger EKU (Enhanced Key Usage) i certifikatet.</span><span class="sxs-lookup"><span data-stu-id="b37d4-125">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="b37d4-126">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="b37d4-126">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="b37d4-127">Anger antalet dagar före utgångs datum för automatisk förnyelse.</span><span class="sxs-lookup"><span data-stu-id="b37d4-127">Specifies the number of days before expiration when automatic renewal should start.</span></span>

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

### <span data-ttu-id="b37d4-128">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="b37d4-128">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="b37d4-129">Anger den procent andel av livs längden som den automatiska processen för aviseringen startar.</span><span class="sxs-lookup"><span data-stu-id="b37d4-129">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="b37d4-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b37d4-130">-InputObject</span></span>
<span data-ttu-id="b37d4-131">Anger certifikat policyn.</span><span class="sxs-lookup"><span data-stu-id="b37d4-131">Specifies the certificate policy.</span></span>

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

### <span data-ttu-id="b37d4-132">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="b37d4-132">-IssuerName</span></span>
<span data-ttu-id="b37d4-133">Anger namnet på utgivaren för detta certifikat.</span><span class="sxs-lookup"><span data-stu-id="b37d4-133">Specifies the name of the issuer for this certificate.</span></span>

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

### <span data-ttu-id="b37d4-134">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="b37d4-134">-KeyNotExportable</span></span>
<span data-ttu-id="b37d4-135">Visar att det inte går att exportera den.</span><span class="sxs-lookup"><span data-stu-id="b37d4-135">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="b37d4-136">-Värdetyp</span><span class="sxs-lookup"><span data-stu-id="b37d4-136">-KeyType</span></span>
<span data-ttu-id="b37d4-137">Anger huvud typen för den knapp som återställer certifikatet.</span><span class="sxs-lookup"><span data-stu-id="b37d4-137">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="b37d4-138">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="b37d4-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b37d4-139">RSA</span><span class="sxs-lookup"><span data-stu-id="b37d4-139">RSA</span></span>
- <span data-ttu-id="b37d4-140">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="b37d4-140">RSA-HSM</span></span>

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

### <span data-ttu-id="b37d4-141">-Använd ande av</span><span class="sxs-lookup"><span data-stu-id="b37d4-141">-KeyUsage</span></span>
<span data-ttu-id="b37d4-142">Anger de viktigaste användningarna i certifikatet.</span><span class="sxs-lookup"><span data-stu-id="b37d4-142">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="b37d4-143">-Namn</span><span class="sxs-lookup"><span data-stu-id="b37d4-143">-Name</span></span>
<span data-ttu-id="b37d4-144">Anger namnet på certifikatet.</span><span class="sxs-lookup"><span data-stu-id="b37d4-144">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="b37d4-145">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b37d4-145">-PassThru</span></span>
<span data-ttu-id="b37d4-146">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="b37d4-146">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b37d4-147">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="b37d4-147">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b37d4-148">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="b37d4-148">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="b37d4-149">Anger antalet dagar före utgångs datum efter vilket automatisk process för certifikat förnyelse påbörjas.</span><span class="sxs-lookup"><span data-stu-id="b37d4-149">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="b37d4-150">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="b37d4-150">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="b37d4-151">Anger den procent andel av livs längden som den automatiska processen för certifikat förnyelse startas.</span><span class="sxs-lookup"><span data-stu-id="b37d4-151">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="b37d4-152">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="b37d4-152">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="b37d4-153">Visar att certifikatet återanvändar den under förnyelse.</span><span class="sxs-lookup"><span data-stu-id="b37d4-153">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="b37d4-154">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="b37d4-154">-SecretContentType</span></span>
<span data-ttu-id="b37d4-155">Anger innehålls typen för den nya nyckel valv hemligheten.</span><span class="sxs-lookup"><span data-stu-id="b37d4-155">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="b37d4-156">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="b37d4-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b37d4-157">Application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="b37d4-157">application/x-pkcs12</span></span>
- <span data-ttu-id="b37d4-158">Application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="b37d4-158">application/x-pem-file</span></span>

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

### <span data-ttu-id="b37d4-159">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="b37d4-159">-SubjectName</span></span>
<span data-ttu-id="b37d4-160">Anger ämnets namn för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="b37d4-160">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="b37d4-161">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="b37d4-161">-ValidityInMonths</span></span>
<span data-ttu-id="b37d4-162">Anger antalet månader som certifikatet är giltigt.</span><span class="sxs-lookup"><span data-stu-id="b37d4-162">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="b37d4-163">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b37d4-163">-VaultName</span></span>
<span data-ttu-id="b37d4-164">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="b37d4-164">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="b37d4-165">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b37d4-165">-Confirm</span></span>
<span data-ttu-id="b37d4-166">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b37d4-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b37d4-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b37d4-167">-WhatIf</span></span>
<span data-ttu-id="b37d4-168">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b37d4-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b37d4-169">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b37d4-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b37d4-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b37d4-170">CommonParameters</span></span>
<span data-ttu-id="b37d4-171">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b37d4-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b37d4-172">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b37d4-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b37d4-173">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b37d4-173">INPUTS</span></span>

### <span data-ttu-id="b37d4-174">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="b37d4-174">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="b37d4-175">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b37d4-175">OUTPUTS</span></span>

### <span data-ttu-id="b37d4-176">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="b37d4-176">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="b37d4-177">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b37d4-177">NOTES</span></span>

## <span data-ttu-id="b37d4-178">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b37d4-178">RELATED LINKS</span></span>

[<span data-ttu-id="b37d4-179">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="b37d4-179">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="b37d4-180">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="b37d4-180">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)
