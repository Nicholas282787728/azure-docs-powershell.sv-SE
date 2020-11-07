---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificatepolicy
schema: 2.0.0
ms.openlocfilehash: b10dd0e034db53af35c930ce1c4588dee2576c75
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929426"
---
# <span data-ttu-id="fd196-101">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="fd196-101">New-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="fd196-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fd196-102">SYNOPSIS</span></span>
<span data-ttu-id="fd196-103">Skapar ett certifikat policy objekt för minnet.</span><span class="sxs-lookup"><span data-stu-id="fd196-103">Creates an in-memory certificate policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd196-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fd196-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificatePolicy [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-SubjectName <String>] [-DnsNames <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] -IssuerName <String>
 [-CertificateType <String>] [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>]
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd196-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fd196-105">DESCRIPTION</span></span>
<span data-ttu-id="fd196-106">Cmdleten **New-AzureKeyVaultCertificatePolicy** skapar ett certifikats princip objekt i minnet för Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="fd196-106">The **New-AzureKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="fd196-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fd196-107">EXAMPLES</span></span>

### <span data-ttu-id="fd196-108">Exempel 1: skapa en certifikat princip</span><span class="sxs-lookup"><span data-stu-id="fd196-108">Example 1: Create a certificate policy</span></span>
```
PS C:\>New-AzureKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
```

<span data-ttu-id="fd196-109">Det här kommandot skapar en certifikat princip som är giltig i sex månader och återanvänder den för att förnya certifikatet.</span><span class="sxs-lookup"><span data-stu-id="fd196-109">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="fd196-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fd196-110">PARAMETERS</span></span>

### <span data-ttu-id="fd196-111">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="fd196-111">-CertificateType</span></span>
<span data-ttu-id="fd196-112">Anger typen av certifikat för utgivaren.</span><span class="sxs-lookup"><span data-stu-id="fd196-112">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd196-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd196-113">-DefaultProfile</span></span>
<span data-ttu-id="fd196-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="fd196-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd196-115">-Inaktive rad</span><span class="sxs-lookup"><span data-stu-id="fd196-115">-Disabled</span></span>
<span data-ttu-id="fd196-116">Anger att certifikat principen är inaktive rad.</span><span class="sxs-lookup"><span data-stu-id="fd196-116">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd196-117">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="fd196-117">-DnsNames</span></span>
<span data-ttu-id="fd196-118">Anger DNS-namnen i certifikatet.</span><span class="sxs-lookup"><span data-stu-id="fd196-118">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="fd196-119">-EKU</span><span class="sxs-lookup"><span data-stu-id="fd196-119">-Ekus</span></span>
<span data-ttu-id="fd196-120">Anger EKU (Enhanced Key Usage) i certifikatet.</span><span class="sxs-lookup"><span data-stu-id="fd196-120">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="fd196-121">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="fd196-121">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="fd196-122">Anger hur många dagar som ska gå innan den automatiska aviseringen startar.</span><span class="sxs-lookup"><span data-stu-id="fd196-122">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="fd196-123">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="fd196-123">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="fd196-124">Anger den procent andel av livs längden som den automatiska processen för aviseringen startar.</span><span class="sxs-lookup"><span data-stu-id="fd196-124">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="fd196-125">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="fd196-125">-IssuerName</span></span>
<span data-ttu-id="fd196-126">Anger namnet på utgivaren av certifikatet.</span><span class="sxs-lookup"><span data-stu-id="fd196-126">Specifies the name of the issuer for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd196-127">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="fd196-127">-KeyNotExportable</span></span>
<span data-ttu-id="fd196-128">Visar att det inte går att exportera den.</span><span class="sxs-lookup"><span data-stu-id="fd196-128">Indicates that the key is not exportable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd196-129">-Värdetyp</span><span class="sxs-lookup"><span data-stu-id="fd196-129">-KeyType</span></span>
<span data-ttu-id="fd196-130">Anger huvud typen för den knapp som återställer certifikatet.</span><span class="sxs-lookup"><span data-stu-id="fd196-130">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="fd196-131">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="fd196-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fd196-132">RSA</span><span class="sxs-lookup"><span data-stu-id="fd196-132">RSA</span></span>
- <span data-ttu-id="fd196-133">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="fd196-133">RSA-HSM</span></span>

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

### <span data-ttu-id="fd196-134">-Använd ande av</span><span class="sxs-lookup"><span data-stu-id="fd196-134">-KeyUsage</span></span>
<span data-ttu-id="fd196-135">Anger de viktigaste användningarna i certifikatet.</span><span class="sxs-lookup"><span data-stu-id="fd196-135">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="fd196-136">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="fd196-136">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="fd196-137">Anger antalet dagar före utgångs datum efter vilket automatisk process för certifikat förnyelse påbörjas.</span><span class="sxs-lookup"><span data-stu-id="fd196-137">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="fd196-138">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="fd196-138">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="fd196-139">Anger den procent andel av livs längden som den automatiska processen för certifikat förnyelse startas.</span><span class="sxs-lookup"><span data-stu-id="fd196-139">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="fd196-140">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="fd196-140">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="fd196-141">Visar att certifikatet återanvändar den under förnyelse.</span><span class="sxs-lookup"><span data-stu-id="fd196-141">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd196-142">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="fd196-142">-SecretContentType</span></span>
<span data-ttu-id="fd196-143">Anger innehålls typen för den nya nyckel valv hemligheten.</span><span class="sxs-lookup"><span data-stu-id="fd196-143">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="fd196-144">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="fd196-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fd196-145">Application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="fd196-145">application/x-pkcs12</span></span>
- <span data-ttu-id="fd196-146">Application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="fd196-146">application/x-pem-file</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd196-147">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="fd196-147">-SubjectName</span></span>
<span data-ttu-id="fd196-148">Anger ämnets namn för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="fd196-148">Specifies the subject name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd196-149">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="fd196-149">-ValidityInMonths</span></span>
<span data-ttu-id="fd196-150">Anger antalet månader som certifikatet är giltigt.</span><span class="sxs-lookup"><span data-stu-id="fd196-150">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="fd196-151">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fd196-151">-Confirm</span></span>
<span data-ttu-id="fd196-152">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fd196-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd196-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd196-153">-WhatIf</span></span>
<span data-ttu-id="fd196-154">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fd196-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd196-155">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fd196-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd196-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd196-156">CommonParameters</span></span>
<span data-ttu-id="fd196-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd196-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd196-158">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd196-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd196-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fd196-159">INPUTS</span></span>

## <span data-ttu-id="fd196-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fd196-160">OUTPUTS</span></span>

### <span data-ttu-id="fd196-161">Microsoft. Azure. commands. valv. Models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="fd196-161">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="fd196-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fd196-162">NOTES</span></span>

## <span data-ttu-id="fd196-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fd196-163">RELATED LINKS</span></span>

[<span data-ttu-id="fd196-164">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="fd196-164">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="fd196-165">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="fd196-165">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

