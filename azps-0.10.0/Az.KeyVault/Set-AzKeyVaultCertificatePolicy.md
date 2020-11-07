---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 160c98b141dbde36786404b58c694772dc86d323
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924441"
---
# <span data-ttu-id="9eadf-101">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="9eadf-101">Set-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="9eadf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9eadf-102">SYNOPSIS</span></span>
<span data-ttu-id="9eadf-103">Skapar eller uppdaterar principen för ett certifikat i ett Key-valv.</span><span class="sxs-lookup"><span data-stu-id="9eadf-103">Creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="9eadf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9eadf-104">SYNTAX</span></span>

### <span data-ttu-id="9eadf-105">Expanderat (standard)</span><span class="sxs-lookup"><span data-stu-id="9eadf-105">Expanded (Default)</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-SecretContentType <String>]
 [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsNames <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>]
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [-KeyNotExportable] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9eadf-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="9eadf-106">ByValue</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [[-CertificatePolicy] <KeyVaultCertificatePolicy>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9eadf-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9eadf-107">DESCRIPTION</span></span>
<span data-ttu-id="9eadf-108">Cmdleten **set-AzKeyVaultCertificatePolicy** skapar eller uppdaterar principen för ett certifikat i ett Key-valv.</span><span class="sxs-lookup"><span data-stu-id="9eadf-108">The **Set-AzKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="9eadf-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9eadf-109">EXAMPLES</span></span>

### <span data-ttu-id="9eadf-110">Exempel 1: Ange en certifikat princip</span><span class="sxs-lookup"><span data-stu-id="9eadf-110">Example 1: Set a certificate policy</span></span>
```
PS C:\>Set-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True
```

<span data-ttu-id="9eadf-111">Det här kommandot ställer in policyn för TestCert01-certifikatet i ContosoKV01-nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="9eadf-111">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="9eadf-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9eadf-112">PARAMETERS</span></span>

### <span data-ttu-id="9eadf-113">-CertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="9eadf-113">-CertificatePolicy</span></span>
<span data-ttu-id="9eadf-114">Anger certifikat policyn.</span><span class="sxs-lookup"><span data-stu-id="9eadf-114">Specifies the certificate policy.</span></span>

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

### <span data-ttu-id="9eadf-115">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="9eadf-115">-CertificateType</span></span>
<span data-ttu-id="9eadf-116">Anger typen av certifikat för utgivaren.</span><span class="sxs-lookup"><span data-stu-id="9eadf-116">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="9eadf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eadf-117">-DefaultProfile</span></span>
<span data-ttu-id="9eadf-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9eadf-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eadf-119">-Inaktive rad</span><span class="sxs-lookup"><span data-stu-id="9eadf-119">-Disabled</span></span>
<span data-ttu-id="9eadf-120">Anger att certifikat principen är inaktive rad.</span><span class="sxs-lookup"><span data-stu-id="9eadf-120">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="9eadf-121">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="9eadf-121">-DnsNames</span></span>
<span data-ttu-id="9eadf-122">Anger DNS-namnen i certifikatet.</span><span class="sxs-lookup"><span data-stu-id="9eadf-122">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="9eadf-123">-EKU</span><span class="sxs-lookup"><span data-stu-id="9eadf-123">-Ekus</span></span>
<span data-ttu-id="9eadf-124">Anger EKU (Enhanced Key Usage) i certifikatet.</span><span class="sxs-lookup"><span data-stu-id="9eadf-124">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="9eadf-125">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="9eadf-125">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="9eadf-126">Anger hur många dagar som ska gå innan den automatiska aviseringen startar.</span><span class="sxs-lookup"><span data-stu-id="9eadf-126">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="9eadf-127">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="9eadf-127">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="9eadf-128">Anger den procent andel av livs längden som den automatiska processen för aviseringen startar.</span><span class="sxs-lookup"><span data-stu-id="9eadf-128">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="9eadf-129">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="9eadf-129">-IssuerName</span></span>
<span data-ttu-id="9eadf-130">Anger namnet på utgivaren för detta certifikat.</span><span class="sxs-lookup"><span data-stu-id="9eadf-130">Specifies the name of the issuer for this certificate.</span></span>

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

### <span data-ttu-id="9eadf-131">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="9eadf-131">-KeyNotExportable</span></span>
<span data-ttu-id="9eadf-132">Visar att det inte går att exportera den.</span><span class="sxs-lookup"><span data-stu-id="9eadf-132">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="9eadf-133">-Värdetyp</span><span class="sxs-lookup"><span data-stu-id="9eadf-133">-KeyType</span></span>
<span data-ttu-id="9eadf-134">Anger huvud typen för den knapp som återställer certifikatet.</span><span class="sxs-lookup"><span data-stu-id="9eadf-134">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="9eadf-135">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="9eadf-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9eadf-136">RSA</span><span class="sxs-lookup"><span data-stu-id="9eadf-136">RSA</span></span>
- <span data-ttu-id="9eadf-137">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="9eadf-137">RSA-HSM</span></span>

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

### <span data-ttu-id="9eadf-138">-Använd ande av</span><span class="sxs-lookup"><span data-stu-id="9eadf-138">-KeyUsage</span></span>
<span data-ttu-id="9eadf-139">Anger de viktigaste användningarna i certifikatet.</span><span class="sxs-lookup"><span data-stu-id="9eadf-139">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="9eadf-140">-Namn</span><span class="sxs-lookup"><span data-stu-id="9eadf-140">-Name</span></span>
<span data-ttu-id="9eadf-141">Anger namnet på certifikatet.</span><span class="sxs-lookup"><span data-stu-id="9eadf-141">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="9eadf-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9eadf-142">-PassThru</span></span>
<span data-ttu-id="9eadf-143">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="9eadf-143">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9eadf-144">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="9eadf-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9eadf-145">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="9eadf-145">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="9eadf-146">Anger antalet dagar före utgångs datum efter vilket automatisk process för certifikat förnyelse påbörjas.</span><span class="sxs-lookup"><span data-stu-id="9eadf-146">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="9eadf-147">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="9eadf-147">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="9eadf-148">Anger den procent andel av livs längden som den automatiska processen för certifikat förnyelse startas.</span><span class="sxs-lookup"><span data-stu-id="9eadf-148">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="9eadf-149">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="9eadf-149">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="9eadf-150">Visar att certifikatet återanvändar den under förnyelse.</span><span class="sxs-lookup"><span data-stu-id="9eadf-150">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="9eadf-151">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="9eadf-151">-SecretContentType</span></span>
<span data-ttu-id="9eadf-152">Anger innehålls typen för den nya nyckel valv hemligheten.</span><span class="sxs-lookup"><span data-stu-id="9eadf-152">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="9eadf-153">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="9eadf-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9eadf-154">Application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="9eadf-154">application/x-pkcs12</span></span>
- <span data-ttu-id="9eadf-155">Application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="9eadf-155">application/x-pem-file</span></span>

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

### <span data-ttu-id="9eadf-156">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="9eadf-156">-SubjectName</span></span>
<span data-ttu-id="9eadf-157">Anger ämnets namn för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="9eadf-157">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="9eadf-158">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="9eadf-158">-ValidityInMonths</span></span>
<span data-ttu-id="9eadf-159">Anger antalet månader som certifikatet är giltigt.</span><span class="sxs-lookup"><span data-stu-id="9eadf-159">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="9eadf-160">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9eadf-160">-VaultName</span></span>
<span data-ttu-id="9eadf-161">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="9eadf-161">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="9eadf-162">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9eadf-162">-Confirm</span></span>
<span data-ttu-id="9eadf-163">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9eadf-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9eadf-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9eadf-164">-WhatIf</span></span>
<span data-ttu-id="9eadf-165">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9eadf-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9eadf-166">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9eadf-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9eadf-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eadf-167">CommonParameters</span></span>
<span data-ttu-id="9eadf-168">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9eadf-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eadf-169">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9eadf-169">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eadf-170">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9eadf-170">INPUTS</span></span>

### <span data-ttu-id="9eadf-171">Ingen</span><span class="sxs-lookup"><span data-stu-id="9eadf-171">None</span></span>
<span data-ttu-id="9eadf-172">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="9eadf-172">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9eadf-173">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9eadf-173">OUTPUTS</span></span>

### <span data-ttu-id="9eadf-174">Microsoft. Azure. commands. valv. Models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="9eadf-174">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="9eadf-175">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9eadf-175">NOTES</span></span>

## <span data-ttu-id="9eadf-176">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9eadf-176">RELATED LINKS</span></span>

[<span data-ttu-id="9eadf-177">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="9eadf-177">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="9eadf-178">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="9eadf-178">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

