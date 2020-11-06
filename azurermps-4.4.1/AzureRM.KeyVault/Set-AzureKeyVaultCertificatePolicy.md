---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: 94f8b6e136925956faf4402b583d80f6a675cca3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584687"
---
# <span data-ttu-id="9ffbc-101">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="9ffbc-101">Set-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="9ffbc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9ffbc-102">SYNOPSIS</span></span>
<span data-ttu-id="9ffbc-103">Skapar eller uppdaterar principen för ett certifikat i ett Key-valv.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-103">Creates or updates the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ffbc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9ffbc-104">SYNTAX</span></span>

### <span data-ttu-id="9ffbc-105">Expanderat (standard)</span><span class="sxs-lookup"><span data-stu-id="9ffbc-105">Expanded (Default)</span></span>
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

### <span data-ttu-id="9ffbc-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="9ffbc-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [[-CertificatePolicy] <KeyVaultCertificatePolicy>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ffbc-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9ffbc-107">DESCRIPTION</span></span>
<span data-ttu-id="9ffbc-108">Cmdleten **set-AzureKeyVaultCertificatePolicy** skapar eller uppdaterar principen för ett certifikat i ett Key-valv.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-108">The **Set-AzureKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="9ffbc-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9ffbc-109">EXAMPLES</span></span>

### <span data-ttu-id="9ffbc-110">Exempel 1: Ange en certifikat princip</span><span class="sxs-lookup"><span data-stu-id="9ffbc-110">Example 1: Set a certificate policy</span></span>
```
PS C:\>Set-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True
```

<span data-ttu-id="9ffbc-111">Det här kommandot ställer in policyn för TestCert01-certifikatet i ContosoKV01-nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-111">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="9ffbc-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9ffbc-112">PARAMETERS</span></span>

### <span data-ttu-id="9ffbc-113">-CertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="9ffbc-113">-CertificatePolicy</span></span>
<span data-ttu-id="9ffbc-114">Anger certifikat policyn.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-114">Specifies the certificate policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy
Parameter Sets: ByValue
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ffbc-115">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="9ffbc-115">-CertificateType</span></span>
<span data-ttu-id="9ffbc-116">Anger typen av certifikat för utgivaren.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-116">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ffbc-117">-Inaktive rad</span><span class="sxs-lookup"><span data-stu-id="9ffbc-117">-Disabled</span></span>
<span data-ttu-id="9ffbc-118">Anger att certifikat principen är inaktive rad.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-118">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ffbc-119">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="9ffbc-119">-DnsNames</span></span>
<span data-ttu-id="9ffbc-120">Anger DNS-namnen i certifikatet.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-120">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="9ffbc-121">-EKU</span><span class="sxs-lookup"><span data-stu-id="9ffbc-121">-Ekus</span></span>
<span data-ttu-id="9ffbc-122">Anger EKU (Enhanced Key Usage) i certifikatet.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-122">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="9ffbc-123">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="9ffbc-123">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="9ffbc-124">Anger hur många dagar som ska gå innan den automatiska aviseringen startar.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-124">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="9ffbc-125">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="9ffbc-125">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="9ffbc-126">Anger den procent andel av livs längden som den automatiska processen för aviseringen startar.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-126">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="9ffbc-127">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="9ffbc-127">-IssuerName</span></span>
<span data-ttu-id="9ffbc-128">Anger namnet på utgivaren för detta certifikat.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-128">Specifies the name of the issuer for this certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ffbc-129">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="9ffbc-129">-KeyNotExportable</span></span>
<span data-ttu-id="9ffbc-130">Visar att det inte går att exportera den.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-130">Indicates that the key is not exportable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ffbc-131">-Värdetyp</span><span class="sxs-lookup"><span data-stu-id="9ffbc-131">-KeyType</span></span>
<span data-ttu-id="9ffbc-132">Anger huvud typen för den knapp som återställer certifikatet.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-132">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="9ffbc-133">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="9ffbc-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9ffbc-134">RSA</span><span class="sxs-lookup"><span data-stu-id="9ffbc-134">RSA</span></span>
- <span data-ttu-id="9ffbc-135">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="9ffbc-135">RSA-HSM</span></span>

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

### <span data-ttu-id="9ffbc-136">-Använd ande av</span><span class="sxs-lookup"><span data-stu-id="9ffbc-136">-KeyUsage</span></span>
<span data-ttu-id="9ffbc-137">Anger de viktigaste användningarna i certifikatet.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-137">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="9ffbc-138">-Namn</span><span class="sxs-lookup"><span data-stu-id="9ffbc-138">-Name</span></span>
<span data-ttu-id="9ffbc-139">Anger namnet på certifikatet.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-139">Specifies the name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ffbc-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ffbc-140">-PassThru</span></span>
<span data-ttu-id="9ffbc-141">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-141">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9ffbc-142">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-142">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9ffbc-143">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="9ffbc-143">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="9ffbc-144">Anger antalet dagar före utgångs datum efter vilket automatisk process för certifikat förnyelse påbörjas.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-144">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ffbc-145">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="9ffbc-145">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="9ffbc-146">Anger den procent andel av livs längden som den automatiska processen för certifikat förnyelse startas.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-146">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ffbc-147">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="9ffbc-147">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="9ffbc-148">Visar att certifikatet återanvändar den under förnyelse.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-148">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ffbc-149">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="9ffbc-149">-SecretContentType</span></span>
<span data-ttu-id="9ffbc-150">Anger innehålls typen för den nya nyckel valv hemligheten.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-150">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="9ffbc-151">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="9ffbc-151">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9ffbc-152">Application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="9ffbc-152">application/x-pkcs12</span></span>
- <span data-ttu-id="9ffbc-153">Application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="9ffbc-153">application/x-pem-file</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ffbc-154">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="9ffbc-154">-SubjectName</span></span>
<span data-ttu-id="9ffbc-155">Anger ämnets namn för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-155">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ffbc-156">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="9ffbc-156">-ValidityInMonths</span></span>
<span data-ttu-id="9ffbc-157">Anger antalet månader som certifikatet är giltigt.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-157">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ffbc-158">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9ffbc-158">-VaultName</span></span>
<span data-ttu-id="9ffbc-159">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-159">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ffbc-160">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9ffbc-160">-Confirm</span></span>
<span data-ttu-id="9ffbc-161">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ffbc-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ffbc-162">-WhatIf</span></span>
<span data-ttu-id="9ffbc-163">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ffbc-164">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ffbc-165">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ffbc-165">-DefaultProfile</span></span>
<span data-ttu-id="9ffbc-166">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-166">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ffbc-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ffbc-167">CommonParameters</span></span>
<span data-ttu-id="9ffbc-168">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ffbc-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ffbc-169">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ffbc-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ffbc-170">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9ffbc-170">INPUTS</span></span>

## <span data-ttu-id="9ffbc-171">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9ffbc-171">OUTPUTS</span></span>

### <span data-ttu-id="9ffbc-172">Microsoft. Azure. commands. valv. Models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="9ffbc-172">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="9ffbc-173">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9ffbc-173">NOTES</span></span>

## <span data-ttu-id="9ffbc-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9ffbc-174">RELATED LINKS</span></span>

[<span data-ttu-id="9ffbc-175">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="9ffbc-175">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="9ffbc-176">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="9ffbc-176">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

