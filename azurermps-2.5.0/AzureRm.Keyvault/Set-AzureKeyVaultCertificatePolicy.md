---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificatepolicy
schema: 2.0.0
ms.openlocfilehash: 7a9356952f2ea8b4113f5df0fe364e9647e2c733
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930229"
---
# <span data-ttu-id="3b8a6-101">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="3b8a6-101">Set-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="3b8a6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3b8a6-102">SYNOPSIS</span></span>
<span data-ttu-id="3b8a6-103">Skapar eller uppdaterar principen för ett certifikat i ett Key-valv.</span><span class="sxs-lookup"><span data-stu-id="3b8a6-103">Creates or updates the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b8a6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3b8a6-104">SYNTAX</span></span>

### <span data-ttu-id="3b8a6-105">Expanderat (standard)</span><span class="sxs-lookup"><span data-stu-id="3b8a6-105">Expanded (Default)</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-SecretContentType <String>]
 [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsNames <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>]
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [-KeyNotExportable] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b8a6-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="3b8a6-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [[-CertificatePolicy] <KeyVaultCertificatePolicy>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b8a6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3b8a6-107">DESCRIPTION</span></span>
<span data-ttu-id="3b8a6-108">Cmdleten **set-AzureKeyVaultCertificatePolicy** skapar eller uppdaterar principen för ett certifikat i ett Key-valv.</span><span class="sxs-lookup"><span data-stu-id="3b8a6-108">The **Set-AzureKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="3b8a6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3b8a6-109">EXAMPLES</span></span>

### <span data-ttu-id="3b8a6-110">Exempel 1: Ange en certifikat princip</span><span class="sxs-lookup"><span data-stu-id="3b8a6-110">Example 1: Set a certificate policy</span></span>
```
PS C:\>Set-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True
```

<span data-ttu-id="3b8a6-111">Det här kommandot ställer in policyn för TestCert01-certifikatet i ContosoKV01-nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="3b8a6-111">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="3b8a6-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3b8a6-112">PARAMETERS</span></span>

### <span data-ttu-id="3b8a6-113">-CertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="3b8a6-113">-CertificatePolicy</span></span>
<span data-ttu-id="3b8a6-114">Anger certifikat policyn.</span><span class="sxs-lookup"><span data-stu-id="3b8a6-114">Specifies the certificate policy.</span></span>

```yaml
Type: KeyVaultCertificatePolicy
Parameter Sets: ByValue
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b8a6-115">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="3b8a6-115">-CertificateType</span></span>
<span data-ttu-id="3b8a6-116">Anger typen av certifikat för utgivaren.</span><span class="sxs-lookup"><span data-stu-id="3b8a6-116">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b8a6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b8a6-117">-DefaultProfile</span></span>
<span data-ttu-id="3b8a6-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3b8a6-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3b8a6-119">-Inaktive rad</span><span class="sxs-lookup"><span data-stu-id="3b8a6-119">-Disabled</span></span>
<span data-ttu-id="3b8a6-120">Anger att certifikat principen är inaktive rad.</span><span class="sxs-lookup"><span data-stu-id="3b8a6-120">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b8a6-121">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="3b8a6-121">-DnsNames</span></span>
<span data-ttu-id="3b8a6-122">Anger DNS-namnen i certifikatet.</span><span class="sxs-lookup"><span data-stu-id="3b8a6-122">Specifies the DNS names in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b8a6-123">-EKU</span><span class="sxs-lookup"><span data-stu-id="3b8a6-123">-Ekus</span></span>
<span data-ttu-id="3b8a6-124">Anger EKU (Enhanced Key Usage) i certifikatet.</span><span class="sxs-lookup"><span data-stu-id="3b8a6-124">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b8a6-125">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="3b8a6-125">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="3b8a6-126">Anger hur många dagar som ska gå innan den automatiska aviseringen startar.</span><span class="sxs-lookup"><span data-stu-id="3b8a6-126">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="3b8a6-127">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="3b8a6-127">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="3b8a6-128">Anger den procent andel av livs längden som den automatiska processen för aviseringen startar.</span><span class="sxs-lookup"><span data-stu-id="3b8a6-128">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="3b8a6-129">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="3b8a6-129">-IssuerName</span></span>
<span data-ttu-id="3b8a6-130">Anger namnet på utgivaren för detta certifikat.</span><span class="sxs-lookup"><span data-stu-id="3b8a6-130">Specifies the name of the issuer for this certificate.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b8a6-131">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="3b8a6-131">-KeyNotExportable</span></span>
<span data-ttu-id="3b8a6-132">Visar att det inte går att exportera den.</span><span class="sxs-lookup"><span data-stu-id="3b8a6-132">Indicates that the key is not exportable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b8a6-133">-Värdetyp</span><span class="sxs-lookup"><span data-stu-id="3b8a6-133">-KeyType</span></span>
<span data-ttu-id="3b8a6-134">Anger huvud typen för den knapp som återställer certifikatet.</span><span class="sxs-lookup"><span data-stu-id="3b8a6-134">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="3b8a6-135">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3b8a6-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3b8a6-136">RSA</span><span class="sxs-lookup"><span data-stu-id="3b8a6-136">RSA</span></span>
- <span data-ttu-id="3b8a6-137">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="3b8a6-137">RSA-HSM</span></span>

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

### <span data-ttu-id="3b8a6-138">-Använd ande av</span><span class="sxs-lookup"><span data-stu-id="3b8a6-138">-KeyUsage</span></span>
<span data-ttu-id="3b8a6-139">Anger de viktigaste användningarna i certifikatet.</span><span class="sxs-lookup"><span data-stu-id="3b8a6-139">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b8a6-140">-Namn</span><span class="sxs-lookup"><span data-stu-id="3b8a6-140">-Name</span></span>
<span data-ttu-id="3b8a6-141">Anger namnet på certifikatet.</span><span class="sxs-lookup"><span data-stu-id="3b8a6-141">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="3b8a6-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3b8a6-142">-PassThru</span></span>
<span data-ttu-id="3b8a6-143">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="3b8a6-143">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3b8a6-144">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="3b8a6-144">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b8a6-145">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="3b8a6-145">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="3b8a6-146">Anger antalet dagar före utgångs datum efter vilket automatisk process för certifikat förnyelse påbörjas.</span><span class="sxs-lookup"><span data-stu-id="3b8a6-146">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b8a6-147">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="3b8a6-147">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="3b8a6-148">Anger den procent andel av livs längden som den automatiska processen för certifikat förnyelse startas.</span><span class="sxs-lookup"><span data-stu-id="3b8a6-148">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b8a6-149">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="3b8a6-149">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="3b8a6-150">Visar att certifikatet återanvändar den under förnyelse.</span><span class="sxs-lookup"><span data-stu-id="3b8a6-150">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: Boolean
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b8a6-151">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="3b8a6-151">-SecretContentType</span></span>
<span data-ttu-id="3b8a6-152">Anger innehålls typen för den nya nyckel valv hemligheten.</span><span class="sxs-lookup"><span data-stu-id="3b8a6-152">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="3b8a6-153">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3b8a6-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3b8a6-154">Application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="3b8a6-154">application/x-pkcs12</span></span>
- <span data-ttu-id="3b8a6-155">Application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="3b8a6-155">application/x-pem-file</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b8a6-156">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="3b8a6-156">-SubjectName</span></span>
<span data-ttu-id="3b8a6-157">Anger ämnets namn för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="3b8a6-157">Specifies the subject name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b8a6-158">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="3b8a6-158">-ValidityInMonths</span></span>
<span data-ttu-id="3b8a6-159">Anger antalet månader som certifikatet är giltigt.</span><span class="sxs-lookup"><span data-stu-id="3b8a6-159">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: Int32
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b8a6-160">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3b8a6-160">-VaultName</span></span>
<span data-ttu-id="3b8a6-161">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="3b8a6-161">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="3b8a6-162">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3b8a6-162">-Confirm</span></span>
<span data-ttu-id="3b8a6-163">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3b8a6-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b8a6-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b8a6-164">-WhatIf</span></span>
<span data-ttu-id="3b8a6-165">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3b8a6-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b8a6-166">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3b8a6-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b8a6-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b8a6-167">CommonParameters</span></span>
<span data-ttu-id="3b8a6-168">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b8a6-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b8a6-169">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b8a6-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b8a6-170">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3b8a6-170">INPUTS</span></span>

## <span data-ttu-id="3b8a6-171">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3b8a6-171">OUTPUTS</span></span>

### <span data-ttu-id="3b8a6-172">Microsoft. Azure. commands. valv. Models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="3b8a6-172">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="3b8a6-173">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3b8a6-173">NOTES</span></span>

## <span data-ttu-id="3b8a6-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3b8a6-174">RELATED LINKS</span></span>

[<span data-ttu-id="3b8a6-175">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="3b8a6-175">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="3b8a6-176">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="3b8a6-176">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

