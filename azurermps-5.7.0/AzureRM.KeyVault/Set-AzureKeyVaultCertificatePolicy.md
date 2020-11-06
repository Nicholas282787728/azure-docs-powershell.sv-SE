---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: e960aa211b53c79087e67e2bd86504e597a718d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585127"
---
# <span data-ttu-id="f3b06-101">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f3b06-101">Set-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="f3b06-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f3b06-102">SYNOPSIS</span></span>
<span data-ttu-id="f3b06-103">Skapar eller uppdaterar principen för ett certifikat i ett Key-valv.</span><span class="sxs-lookup"><span data-stu-id="f3b06-103">Creates or updates the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3b06-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f3b06-104">SYNTAX</span></span>

### <span data-ttu-id="f3b06-105">ExpandedRenewPercentage (standard)</span><span class="sxs-lookup"><span data-stu-id="f3b06-105">ExpandedRenewPercentage (Default)</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-RenewAtPercentageLifetime <Int32>]
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3b06-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="f3b06-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3b06-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="f3b06-107">ExpandedRenewNumber</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 -RenewAtNumberOfDaysBeforeExpiry <Int32> [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>]
 [-Disabled] [-SubjectName <String>] [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3b06-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f3b06-108">DESCRIPTION</span></span>
<span data-ttu-id="f3b06-109">Cmdleten **set-AzureKeyVaultCertificatePolicy** skapar eller uppdaterar principen för ett certifikat i ett Key-valv.</span><span class="sxs-lookup"><span data-stu-id="f3b06-109">The **Set-AzureKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="f3b06-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f3b06-110">EXAMPLES</span></span>

### <span data-ttu-id="f3b06-111">Exempel 1: Ange en certifikat princip</span><span class="sxs-lookup"><span data-stu-id="f3b06-111">Example 1: Set a certificate policy</span></span>
```
PS C:\>Set-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True
```

<span data-ttu-id="f3b06-112">Det här kommandot ställer in policyn för TestCert01-certifikatet i ContosoKV01-nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="f3b06-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="f3b06-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f3b06-113">PARAMETERS</span></span>

### <span data-ttu-id="f3b06-114">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="f3b06-114">-CertificateType</span></span>
<span data-ttu-id="f3b06-115">Anger typen av certifikat för utgivaren.</span><span class="sxs-lookup"><span data-stu-id="f3b06-115">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3b06-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3b06-116">-DefaultProfile</span></span>
<span data-ttu-id="f3b06-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f3b06-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3b06-118">-Inaktive rad</span><span class="sxs-lookup"><span data-stu-id="f3b06-118">-Disabled</span></span>
<span data-ttu-id="f3b06-119">Anger att certifikat principen är inaktive rad.</span><span class="sxs-lookup"><span data-stu-id="f3b06-119">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3b06-120">-DnsName</span><span class="sxs-lookup"><span data-stu-id="f3b06-120">-DnsName</span></span>
<span data-ttu-id="f3b06-121">Anger ämnets namn för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="f3b06-121">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases: DnsNames

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3b06-122">-EKU</span><span class="sxs-lookup"><span data-stu-id="f3b06-122">-Ekus</span></span>
<span data-ttu-id="f3b06-123">Anger EKU (Enhanced Key Usage) i certifikatet.</span><span class="sxs-lookup"><span data-stu-id="f3b06-123">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3b06-124">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="f3b06-124">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="f3b06-125">Anger antalet dagar före utgångs datum för automatisk förnyelse.</span><span class="sxs-lookup"><span data-stu-id="f3b06-125">Specifies the number of days before expiration when automatic renewal should start.</span></span>

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

### <span data-ttu-id="f3b06-126">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="f3b06-126">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="f3b06-127">Anger den procent andel av livs längden som den automatiska processen för aviseringen startar.</span><span class="sxs-lookup"><span data-stu-id="f3b06-127">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="f3b06-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3b06-128">-InputObject</span></span>
<span data-ttu-id="f3b06-129">Anger certifikat policyn.</span><span class="sxs-lookup"><span data-stu-id="f3b06-129">Specifies the certificate policy.</span></span>

```yaml
Type: PSKeyVaultCertificatePolicy
Parameter Sets: ByValue
Aliases: CertificatePolicy

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3b06-130">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="f3b06-130">-IssuerName</span></span>
<span data-ttu-id="f3b06-131">Anger namnet på utgivaren för detta certifikat.</span><span class="sxs-lookup"><span data-stu-id="f3b06-131">Specifies the name of the issuer for this certificate.</span></span>

```yaml
Type: String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3b06-132">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="f3b06-132">-KeyNotExportable</span></span>
<span data-ttu-id="f3b06-133">Visar att det inte går att exportera den.</span><span class="sxs-lookup"><span data-stu-id="f3b06-133">Indicates that the key is not exportable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3b06-134">-Värdetyp</span><span class="sxs-lookup"><span data-stu-id="f3b06-134">-KeyType</span></span>
<span data-ttu-id="f3b06-135">Anger huvud typen för den knapp som återställer certifikatet.</span><span class="sxs-lookup"><span data-stu-id="f3b06-135">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="f3b06-136">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="f3b06-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f3b06-137">RSA</span><span class="sxs-lookup"><span data-stu-id="f3b06-137">RSA</span></span>
- <span data-ttu-id="f3b06-138">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="f3b06-138">RSA-HSM</span></span>

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

### <span data-ttu-id="f3b06-139">-Använd ande av</span><span class="sxs-lookup"><span data-stu-id="f3b06-139">-KeyUsage</span></span>
<span data-ttu-id="f3b06-140">Anger de viktigaste användningarna i certifikatet.</span><span class="sxs-lookup"><span data-stu-id="f3b06-140">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3b06-141">-Namn</span><span class="sxs-lookup"><span data-stu-id="f3b06-141">-Name</span></span>
<span data-ttu-id="f3b06-142">Anger namnet på certifikatet.</span><span class="sxs-lookup"><span data-stu-id="f3b06-142">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="f3b06-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3b06-143">-PassThru</span></span>
<span data-ttu-id="f3b06-144">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="f3b06-144">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f3b06-145">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="f3b06-145">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f3b06-146">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="f3b06-146">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="f3b06-147">Anger antalet dagar före utgångs datum efter vilket automatisk process för certifikat förnyelse påbörjas.</span><span class="sxs-lookup"><span data-stu-id="f3b06-147">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: ExpandedRenewNumber
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3b06-148">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="f3b06-148">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="f3b06-149">Anger den procent andel av livs längden som den automatiska processen för certifikat förnyelse startas.</span><span class="sxs-lookup"><span data-stu-id="f3b06-149">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: ExpandedRenewPercentage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3b06-150">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="f3b06-150">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="f3b06-151">Visar att certifikatet återanvändar den under förnyelse.</span><span class="sxs-lookup"><span data-stu-id="f3b06-151">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: Boolean
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3b06-152">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="f3b06-152">-SecretContentType</span></span>
<span data-ttu-id="f3b06-153">Anger innehålls typen för den nya nyckel valv hemligheten.</span><span class="sxs-lookup"><span data-stu-id="f3b06-153">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="f3b06-154">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="f3b06-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f3b06-155">Application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="f3b06-155">application/x-pkcs12</span></span>
- <span data-ttu-id="f3b06-156">Application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="f3b06-156">application/x-pem-file</span></span>

```yaml
Type: String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3b06-157">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="f3b06-157">-SubjectName</span></span>
<span data-ttu-id="f3b06-158">Anger ämnets namn för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="f3b06-158">Specifies the subject name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3b06-159">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="f3b06-159">-ValidityInMonths</span></span>
<span data-ttu-id="f3b06-160">Anger antalet månader som certifikatet är giltigt.</span><span class="sxs-lookup"><span data-stu-id="f3b06-160">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: Int32
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3b06-161">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f3b06-161">-VaultName</span></span>
<span data-ttu-id="f3b06-162">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="f3b06-162">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="f3b06-163">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f3b06-163">-Confirm</span></span>
<span data-ttu-id="f3b06-164">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f3b06-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3b06-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3b06-165">-WhatIf</span></span>
<span data-ttu-id="f3b06-166">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f3b06-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3b06-167">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f3b06-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3b06-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3b06-168">CommonParameters</span></span>
<span data-ttu-id="f3b06-169">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3b06-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3b06-170">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3b06-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3b06-171">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f3b06-171">INPUTS</span></span>

### <span data-ttu-id="f3b06-172">Ingen</span><span class="sxs-lookup"><span data-stu-id="f3b06-172">None</span></span>
<span data-ttu-id="f3b06-173">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="f3b06-173">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f3b06-174">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f3b06-174">OUTPUTS</span></span>

### <span data-ttu-id="f3b06-175">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f3b06-175">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="f3b06-176">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f3b06-176">NOTES</span></span>

## <span data-ttu-id="f3b06-177">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f3b06-177">RELATED LINKS</span></span>

[<span data-ttu-id="f3b06-178">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f3b06-178">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="f3b06-179">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f3b06-179">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

