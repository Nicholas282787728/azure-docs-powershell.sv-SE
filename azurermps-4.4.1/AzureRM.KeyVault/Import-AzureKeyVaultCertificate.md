---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: D4188DC6-A8AB-4B45-9781-94B74C338C63
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Import-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Import-AzureKeyVaultCertificate.md
ms.openlocfilehash: b97dc509ad6508c2cbec79d6ba1db27508f94c34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574650"
---
# <span data-ttu-id="25092-101">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="25092-101">Import-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="25092-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="25092-102">SYNOPSIS</span></span>
<span data-ttu-id="25092-103">Importerar ett certifikat till ett huvud valv.</span><span class="sxs-lookup"><span data-stu-id="25092-103">Imports a certificate to a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25092-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="25092-104">SYNTAX</span></span>

### <span data-ttu-id="25092-105">ImportCertificateFromFile (standard)</span><span class="sxs-lookup"><span data-stu-id="25092-105">ImportCertificateFromFile (Default)</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25092-106">ImportWithPrivateKeyFromFile</span><span class="sxs-lookup"><span data-stu-id="25092-106">ImportWithPrivateKeyFromFile</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25092-107">ImportWithPrivateKeyFromString</span><span class="sxs-lookup"><span data-stu-id="25092-107">ImportWithPrivateKeyFromString</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -CertificateString <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25092-108">ImportWithPrivateKeyFromCollection</span><span class="sxs-lookup"><span data-stu-id="25092-108">ImportWithPrivateKeyFromCollection</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 -CertificateCollection <X509Certificate2Collection> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25092-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="25092-109">DESCRIPTION</span></span>
<span data-ttu-id="25092-110">Cmdleten **import-AzureKeyVaultCertificate** importerar ett certifikat till ett Key-valv.</span><span class="sxs-lookup"><span data-stu-id="25092-110">The **Import-AzureKeyVaultCertificate** cmdlet imports a certificate into a key vault.</span></span>

<span data-ttu-id="25092-111">Du kan skapa ett certifikat genom att använda någon av följande metoder:</span><span class="sxs-lookup"><span data-stu-id="25092-111">You can create the certificate to import by using one of the following methods:</span></span>

- <span data-ttu-id="25092-112">Använd New-AzureKeyVaultCertificateSigningRequest cmdlet för att skapa en begäran om certifikat signering och skicka den till en certifikat utfärdare.</span><span class="sxs-lookup"><span data-stu-id="25092-112">Use the New-AzureKeyVaultCertificateSigningRequest cmdlet to create a certificate signing request and submit it to a certificate authority.</span></span>
- <span data-ttu-id="25092-113">Använd en befintlig certifikat fil, till exempel en. pfx-eller. P12-fil, som innehåller både certifikatet och den privata knappen.</span><span class="sxs-lookup"><span data-stu-id="25092-113">Use an existing certificate package file, such as a .pfx or .p12 file, which contains both the certificate and private key.</span></span>

## <span data-ttu-id="25092-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="25092-114">EXAMPLES</span></span>

### <span data-ttu-id="25092-115">Exempel 1: importera ett valv certifikat</span><span class="sxs-lookup"><span data-stu-id="25092-115">Example 1: Import a key vault certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS C:\> Import-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "ImportCert01" -FilePath "C:\Users\contosoUser\Desktop\import.pfx" -Password $Password
Name        : importCert01
Certificate : [Subject]
                CN=contoso.com

              [Issuer]
                CN=contoso.com

              [Serial Number]
                05979C5A2F0741D5A3B6F97673E8A118

              [Not Before]
                2/8/2016 3:11:45 PM

              [Not After]
                8/8/2016 4:21:45 PM

              [Thumbprint]
                3E9B6848AD1834284157D68B060F748037F663C8

Thumbprint  : 3E9B6848AD1834284157D68B060F748037F663C8
Tags        :
Enabled     : True
Created     : 2/8/2016 11:50:43 PM
Updated     : 2/8/2016 11:50:43 PM
```

<span data-ttu-id="25092-116">Det första kommandot använder cmdleten ConvertTo-SecureString för att skapa ett säkert lösen ord och lagrar det sedan i $Password-variabeln.</span><span class="sxs-lookup"><span data-stu-id="25092-116">The first command uses the ConvertTo-SecureString cmdlet to create a secure password, and then stores it in the $Password variable.</span></span>

<span data-ttu-id="25092-117">Det andra kommandot importerar certifikatet som heter ImportCert01 till CosotosoKV01-nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="25092-117">The second command imports the certificate named ImportCert01 into the CosotosoKV01 key vault.</span></span>

## <span data-ttu-id="25092-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="25092-118">PARAMETERS</span></span>

### <span data-ttu-id="25092-119">-CertificateCollection</span><span class="sxs-lookup"><span data-stu-id="25092-119">-CertificateCollection</span></span>
<span data-ttu-id="25092-120">Anger den certifikat samling som ska läggas till i ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="25092-120">Specifies the certificate collection to add to a key vault.</span></span>

```yaml
Type: System.Security.Cryptography.X509Certificates.X509Certificate2Collection
Parameter Sets: ImportWithPrivateKeyFromCollection
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25092-121">-CertificateString</span><span class="sxs-lookup"><span data-stu-id="25092-121">-CertificateString</span></span>
<span data-ttu-id="25092-122">Anger en certifikat sträng.</span><span class="sxs-lookup"><span data-stu-id="25092-122">Specifies a certificate string.</span></span>

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

### <span data-ttu-id="25092-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="25092-123">-Confirm</span></span>
<span data-ttu-id="25092-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="25092-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25092-125">-Sökväg</span><span class="sxs-lookup"><span data-stu-id="25092-125">-FilePath</span></span>
<span data-ttu-id="25092-126">Anger sökvägen till den certifikat fil som ska importeras.</span><span class="sxs-lookup"><span data-stu-id="25092-126">Specifies the path of the certificate file that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportCertificateFromFile, ImportWithPrivateKeyFromFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25092-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="25092-127">-Name</span></span>
<span data-ttu-id="25092-128">Anger certifikatets namn.</span><span class="sxs-lookup"><span data-stu-id="25092-128">Specifies the certificate name.</span></span> <span data-ttu-id="25092-129">Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) för ett certifikat från Key valv-namn, markerad miljö och certifikat namn.</span><span class="sxs-lookup"><span data-stu-id="25092-129">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate from key vault name, currently selected environment, and certificate name.</span></span>

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

### <span data-ttu-id="25092-130">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="25092-130">-Password</span></span>
<span data-ttu-id="25092-131">Anger lösen ordet för en certifikat fil.</span><span class="sxs-lookup"><span data-stu-id="25092-131">Specifies the password for a certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ImportWithPrivateKeyFromFile, ImportWithPrivateKeyFromString
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25092-132">-Tagg</span><span class="sxs-lookup"><span data-stu-id="25092-132">-Tag</span></span>
<span data-ttu-id="25092-133">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="25092-133">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="25092-134">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="25092-134">For example:</span></span>

<span data-ttu-id="25092-135">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="25092-135">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="25092-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="25092-136">-VaultName</span></span>
<span data-ttu-id="25092-137">Anger namnet på den Key valv dit denna cmdlet importerar certifikat.</span><span class="sxs-lookup"><span data-stu-id="25092-137">Specifies the key vault name into which this cmdlet imports certificates.</span></span>
<span data-ttu-id="25092-138">Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) för ett Key valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="25092-138">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="25092-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25092-139">-WhatIf</span></span>
<span data-ttu-id="25092-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="25092-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25092-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="25092-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25092-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25092-142">-DefaultProfile</span></span>
<span data-ttu-id="25092-143">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="25092-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25092-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25092-144">CommonParameters</span></span>
<span data-ttu-id="25092-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25092-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25092-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25092-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25092-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="25092-147">INPUTS</span></span>

## <span data-ttu-id="25092-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="25092-148">OUTPUTS</span></span>

### <span data-ttu-id="25092-149">Microsoft. Azure. commands. valv. Models. CertificateBundle</span><span class="sxs-lookup"><span data-stu-id="25092-149">Microsoft.Azure.Commands.KeyVault.Models.CertificateBundle</span></span>

## <span data-ttu-id="25092-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="25092-150">NOTES</span></span>

## <span data-ttu-id="25092-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="25092-151">RELATED LINKS</span></span>

[<span data-ttu-id="25092-152">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="25092-152">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)
