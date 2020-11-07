---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: D4188DC6-A8AB-4B45-9781-94B74C338C63
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/import-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultCertificate.md
ms.openlocfilehash: 6591b96257a1c94cd2da9d0bc6f2995dc2034a40
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743913"
---
# <span data-ttu-id="7858c-101">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="7858c-101">Import-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="7858c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7858c-102">SYNOPSIS</span></span>
<span data-ttu-id="7858c-103">Importerar ett certifikat till ett huvud valv.</span><span class="sxs-lookup"><span data-stu-id="7858c-103">Imports a certificate to a key vault.</span></span>

## <span data-ttu-id="7858c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7858c-104">SYNTAX</span></span>

### <span data-ttu-id="7858c-105">ImportCertificateFromFile (standard)</span><span class="sxs-lookup"><span data-stu-id="7858c-105">ImportCertificateFromFile (Default)</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7858c-106">ImportWithPrivateKeyFromString</span><span class="sxs-lookup"><span data-stu-id="7858c-106">ImportWithPrivateKeyFromString</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -CertificateString <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7858c-107">ImportWithPrivateKeyFromCollection</span><span class="sxs-lookup"><span data-stu-id="7858c-107">ImportWithPrivateKeyFromCollection</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [-CertificateCollection] <X509Certificate2Collection> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7858c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7858c-108">DESCRIPTION</span></span>
<span data-ttu-id="7858c-109">Cmdleten **import-AzKeyVaultCertificate** importerar ett certifikat till ett Key-valv.</span><span class="sxs-lookup"><span data-stu-id="7858c-109">The **Import-AzKeyVaultCertificate** cmdlet imports a certificate into a key vault.</span></span>
<span data-ttu-id="7858c-110">Du kan skapa ett certifikat genom att använda någon av följande metoder:</span><span class="sxs-lookup"><span data-stu-id="7858c-110">You can create the certificate to import by using one of the following methods:</span></span>
- <span data-ttu-id="7858c-111">Använd New-AzKeyVaultCertificateSigningRequest cmdlet för att skapa en begäran om certifikat signering och skicka den till en certifikat utfärdare.</span><span class="sxs-lookup"><span data-stu-id="7858c-111">Use the New-AzKeyVaultCertificateSigningRequest cmdlet to create a certificate signing request and submit it to a certificate authority.</span></span>
- <span data-ttu-id="7858c-112">Använd en befintlig certifikat fil, till exempel en. pfx-eller. P12-fil, som innehåller både certifikatet och den privata knappen.</span><span class="sxs-lookup"><span data-stu-id="7858c-112">Use an existing certificate package file, such as a .pfx or .p12 file, which contains both the certificate and private key.</span></span>

## <span data-ttu-id="7858c-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7858c-113">EXAMPLES</span></span>

### <span data-ttu-id="7858c-114">Exempel 1: importera ett valv certifikat</span><span class="sxs-lookup"><span data-stu-id="7858c-114">Example 1: Import a key vault certificate</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS C:\> Import-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "ImportCert01" -FilePath "C:\Users\contosoUser\Desktop\import.pfx" -Password $Password

Name        : importCert01
Certificate : [Subject]
                CN=contoso.com

              [Issuer]
                CN=contoso.com

              [Serial Number]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

              [Not Before]
                2/8/2016 3:11:45 PM

              [Not After]
                8/8/2016 4:21:45 PM

              [Thumbprint]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        :
Enabled     : True
Created     : 2/8/2016 11:50:43 PM
Updated     : 2/8/2016 11:50:43 PM
```

<span data-ttu-id="7858c-115">Det första kommandot använder cmdleten ConvertTo-SecureString för att skapa ett säkert lösen ord och lagrar det sedan i $Password-variabeln.</span><span class="sxs-lookup"><span data-stu-id="7858c-115">The first command uses the ConvertTo-SecureString cmdlet to create a secure password, and then stores it in the $Password variable.</span></span>
<span data-ttu-id="7858c-116">Det andra kommandot importerar certifikatet som heter ImportCert01 till CosotosoKV01-nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="7858c-116">The second command imports the certificate named ImportCert01 into the CosotosoKV01 key vault.</span></span>

## <span data-ttu-id="7858c-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7858c-117">PARAMETERS</span></span>

### <span data-ttu-id="7858c-118">-CertificateCollection</span><span class="sxs-lookup"><span data-stu-id="7858c-118">-CertificateCollection</span></span>
<span data-ttu-id="7858c-119">Anger den certifikat samling som ska läggas till i ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="7858c-119">Specifies the certificate collection to add to a key vault.</span></span>

```yaml
Type: System.Security.Cryptography.X509Certificates.X509Certificate2Collection
Parameter Sets: ImportWithPrivateKeyFromCollection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7858c-120">-CertificateString</span><span class="sxs-lookup"><span data-stu-id="7858c-120">-CertificateString</span></span>
<span data-ttu-id="7858c-121">Anger en certifikat sträng.</span><span class="sxs-lookup"><span data-stu-id="7858c-121">Specifies a certificate string.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportWithPrivateKeyFromString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7858c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7858c-122">-DefaultProfile</span></span>
<span data-ttu-id="7858c-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7858c-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7858c-124">-Sökväg</span><span class="sxs-lookup"><span data-stu-id="7858c-124">-FilePath</span></span>
<span data-ttu-id="7858c-125">Anger sökvägen till den certifikat fil som ska importeras.</span><span class="sxs-lookup"><span data-stu-id="7858c-125">Specifies the path of the certificate file that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportCertificateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7858c-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="7858c-126">-Name</span></span>
<span data-ttu-id="7858c-127">Anger certifikatets namn.</span><span class="sxs-lookup"><span data-stu-id="7858c-127">Specifies the certificate name.</span></span> <span data-ttu-id="7858c-128">Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) för ett certifikat från Key valv-namn, markerad miljö och certifikat namn.</span><span class="sxs-lookup"><span data-stu-id="7858c-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate from key vault name, currently selected environment, and certificate name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7858c-129">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="7858c-129">-Password</span></span>
<span data-ttu-id="7858c-130">Anger lösen ordet för en certifikat fil.</span><span class="sxs-lookup"><span data-stu-id="7858c-130">Specifies the password for a certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ImportCertificateFromFile, ImportWithPrivateKeyFromString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7858c-131">-Tagg</span><span class="sxs-lookup"><span data-stu-id="7858c-131">-Tag</span></span>
<span data-ttu-id="7858c-132">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="7858c-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7858c-133">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="7858c-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7858c-134">-VaultName</span><span class="sxs-lookup"><span data-stu-id="7858c-134">-VaultName</span></span>
<span data-ttu-id="7858c-135">Anger namnet på den Key valv dit denna cmdlet importerar certifikat.</span><span class="sxs-lookup"><span data-stu-id="7858c-135">Specifies the key vault name into which this cmdlet imports certificates.</span></span>
<span data-ttu-id="7858c-136">Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) för ett Key valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="7858c-136">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="7858c-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7858c-137">-Confirm</span></span>
<span data-ttu-id="7858c-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7858c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7858c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7858c-139">-WhatIf</span></span>
<span data-ttu-id="7858c-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7858c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7858c-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7858c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7858c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7858c-142">CommonParameters</span></span>
<span data-ttu-id="7858c-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7858c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7858c-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7858c-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7858c-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7858c-145">INPUTS</span></span>

### <span data-ttu-id="7858c-146">System. String</span><span class="sxs-lookup"><span data-stu-id="7858c-146">System.String</span></span>

### <span data-ttu-id="7858c-147">System. Security. Cryptography. X509Certificates. X509Certificate2Collection</span><span class="sxs-lookup"><span data-stu-id="7858c-147">System.Security.Cryptography.X509Certificates.X509Certificate2Collection</span></span>

### <span data-ttu-id="7858c-148">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="7858c-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7858c-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7858c-149">OUTPUTS</span></span>

### <span data-ttu-id="7858c-150">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="7858c-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="7858c-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7858c-151">NOTES</span></span>

## <span data-ttu-id="7858c-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7858c-152">RELATED LINKS</span></span>

[<span data-ttu-id="7858c-153">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="7858c-153">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)
