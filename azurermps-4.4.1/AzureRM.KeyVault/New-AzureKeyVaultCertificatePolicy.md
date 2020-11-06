---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: 381ce302a8404c0bb643db0fc82e392fe53d956a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574642"
---
# <span data-ttu-id="9b274-101">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="9b274-101">New-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="9b274-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9b274-102">SYNOPSIS</span></span>
<span data-ttu-id="9b274-103">Skapar ett certifikat policy objekt för minnet.</span><span class="sxs-lookup"><span data-stu-id="9b274-103">Creates an in-memory certificate policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b274-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9b274-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificatePolicy [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-SubjectName <String>] [-DnsNames <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] -IssuerName <String>
 [-CertificateType <String>] [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>]
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b274-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9b274-105">DESCRIPTION</span></span>
<span data-ttu-id="9b274-106">Cmdleten **New-AzureKeyVaultCertificatePolicy** skapar ett certifikats princip objekt i minnet för Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="9b274-106">The **New-AzureKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="9b274-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9b274-107">EXAMPLES</span></span>

### <span data-ttu-id="9b274-108">Exempel 1: skapa en certifikat princip</span><span class="sxs-lookup"><span data-stu-id="9b274-108">Example 1: Create a certificate policy</span></span>
```
PS C:\>New-AzureKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
```

<span data-ttu-id="9b274-109">Det här kommandot skapar en certifikat princip som är giltig i sex månader och återanvänder den för att förnya certifikatet.</span><span class="sxs-lookup"><span data-stu-id="9b274-109">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="9b274-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9b274-110">PARAMETERS</span></span>

### <span data-ttu-id="9b274-111">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="9b274-111">-CertificateType</span></span>
<span data-ttu-id="9b274-112">Anger typen av certifikat för utgivaren.</span><span class="sxs-lookup"><span data-stu-id="9b274-112">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="9b274-113">-Inaktive rad</span><span class="sxs-lookup"><span data-stu-id="9b274-113">-Disabled</span></span>
<span data-ttu-id="9b274-114">Anger att certifikat principen är inaktive rad.</span><span class="sxs-lookup"><span data-stu-id="9b274-114">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="9b274-115">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="9b274-115">-DnsNames</span></span>
<span data-ttu-id="9b274-116">Anger DNS-namnen i certifikatet.</span><span class="sxs-lookup"><span data-stu-id="9b274-116">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="9b274-117">-EKU</span><span class="sxs-lookup"><span data-stu-id="9b274-117">-Ekus</span></span>
<span data-ttu-id="9b274-118">Anger EKU (Enhanced Key Usage) i certifikatet.</span><span class="sxs-lookup"><span data-stu-id="9b274-118">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="9b274-119">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="9b274-119">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="9b274-120">Anger hur många dagar som ska gå innan den automatiska aviseringen startar.</span><span class="sxs-lookup"><span data-stu-id="9b274-120">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="9b274-121">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="9b274-121">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="9b274-122">Anger den procent andel av livs längden som den automatiska processen för aviseringen startar.</span><span class="sxs-lookup"><span data-stu-id="9b274-122">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="9b274-123">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="9b274-123">-IssuerName</span></span>
<span data-ttu-id="9b274-124">Anger namnet på utgivaren av certifikatet.</span><span class="sxs-lookup"><span data-stu-id="9b274-124">Specifies the name of the issuer for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b274-125">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="9b274-125">-KeyNotExportable</span></span>
<span data-ttu-id="9b274-126">Visar att det inte går att exportera den.</span><span class="sxs-lookup"><span data-stu-id="9b274-126">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="9b274-127">-Värdetyp</span><span class="sxs-lookup"><span data-stu-id="9b274-127">-KeyType</span></span>
<span data-ttu-id="9b274-128">Anger huvud typen för den knapp som återställer certifikatet.</span><span class="sxs-lookup"><span data-stu-id="9b274-128">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="9b274-129">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="9b274-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9b274-130">RSA</span><span class="sxs-lookup"><span data-stu-id="9b274-130">RSA</span></span>
- <span data-ttu-id="9b274-131">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="9b274-131">RSA-HSM</span></span>

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

### <span data-ttu-id="9b274-132">-Använd ande av</span><span class="sxs-lookup"><span data-stu-id="9b274-132">-KeyUsage</span></span>
<span data-ttu-id="9b274-133">Anger de viktigaste användningarna i certifikatet.</span><span class="sxs-lookup"><span data-stu-id="9b274-133">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="9b274-134">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="9b274-134">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="9b274-135">Anger antalet dagar före utgångs datum efter vilket automatisk process för certifikat förnyelse påbörjas.</span><span class="sxs-lookup"><span data-stu-id="9b274-135">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="9b274-136">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="9b274-136">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="9b274-137">Anger den procent andel av livs längden som den automatiska processen för certifikat förnyelse startas.</span><span class="sxs-lookup"><span data-stu-id="9b274-137">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="9b274-138">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="9b274-138">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="9b274-139">Visar att certifikatet återanvändar den under förnyelse.</span><span class="sxs-lookup"><span data-stu-id="9b274-139">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="9b274-140">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="9b274-140">-SecretContentType</span></span>
<span data-ttu-id="9b274-141">Anger innehålls typen för den nya nyckel valv hemligheten.</span><span class="sxs-lookup"><span data-stu-id="9b274-141">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="9b274-142">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="9b274-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9b274-143">Application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="9b274-143">application/x-pkcs12</span></span>
- <span data-ttu-id="9b274-144">Application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="9b274-144">application/x-pem-file</span></span>

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

### <span data-ttu-id="9b274-145">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="9b274-145">-SubjectName</span></span>
<span data-ttu-id="9b274-146">Anger ämnets namn för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="9b274-146">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="9b274-147">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="9b274-147">-ValidityInMonths</span></span>
<span data-ttu-id="9b274-148">Anger antalet månader som certifikatet är giltigt.</span><span class="sxs-lookup"><span data-stu-id="9b274-148">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="9b274-149">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9b274-149">-Confirm</span></span>
<span data-ttu-id="9b274-150">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9b274-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b274-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b274-151">-WhatIf</span></span>
<span data-ttu-id="9b274-152">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9b274-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b274-153">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9b274-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b274-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b274-154">-DefaultProfile</span></span>
<span data-ttu-id="9b274-155">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9b274-155">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b274-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b274-156">CommonParameters</span></span>
<span data-ttu-id="9b274-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b274-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b274-158">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b274-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b274-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9b274-159">INPUTS</span></span>

## <span data-ttu-id="9b274-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9b274-160">OUTPUTS</span></span>

### <span data-ttu-id="9b274-161">Microsoft. Azure. commands. valv. Models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="9b274-161">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="9b274-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9b274-162">NOTES</span></span>

## <span data-ttu-id="9b274-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9b274-163">RELATED LINKS</span></span>

[<span data-ttu-id="9b274-164">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="9b274-164">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="9b274-165">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="9b274-165">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

