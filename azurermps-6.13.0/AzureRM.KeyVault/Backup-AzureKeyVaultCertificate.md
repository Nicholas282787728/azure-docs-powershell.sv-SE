---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultCertificate.md
ms.openlocfilehash: 7f75f07ee8f53a57cdb2e359fb4addb51b1d7f76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574846"
---
# <span data-ttu-id="8cccc-101">Backup-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="8cccc-101">Backup-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="8cccc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8cccc-102">SYNOPSIS</span></span>
<span data-ttu-id="8cccc-103">Säkerhetskopierar ett certifikat i ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="8cccc-103">Backs up a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cccc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8cccc-104">SYNTAX</span></span>

### <span data-ttu-id="8cccc-105">ByCertificateName (standard)</span><span class="sxs-lookup"><span data-stu-id="8cccc-105">ByCertificateName (Default)</span></span>
```
Backup-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cccc-106">ByCertificate</span><span class="sxs-lookup"><span data-stu-id="8cccc-106">ByCertificate</span></span>
```
Backup-AzureKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cccc-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8cccc-107">DESCRIPTION</span></span>
<span data-ttu-id="8cccc-108">Genom **säkerhets kopiering-AzureKeyVaultCertificate** cmdlet säkerhets kopie ras ett angivet certifikat i ett nyckeltal genom att det laddas ned och lagras i en fil.</span><span class="sxs-lookup"><span data-stu-id="8cccc-108">The **Backup-AzureKeyVaultCertificate** cmdlet backs up a specified certificate in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="8cccc-109">Om certifikatet har flera versioner kommer alla dess versioner att ingå i säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="8cccc-109">If the certificate has multiple versions, all its versions will be included in the backup.</span></span>
<span data-ttu-id="8cccc-110">Eftersom det hämtade innehållet är krypterat kan det inte användas utanför Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="8cccc-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="8cccc-111">Du kan återställa ett säkerhetskopierat certifikat till ett huvud valv i det abonnemang som det säkerhetskopierades från, så länge valvet finns i samma Azure geography.</span><span class="sxs-lookup"><span data-stu-id="8cccc-111">You can restore a backed-up certificate to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="8cccc-112">Vanliga skäl till att använda denna cmdlet är:</span><span class="sxs-lookup"><span data-stu-id="8cccc-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="8cccc-113">Om du vill behålla en offlinekopia av certifikatet ifall du råkar ta bort originalet från valvet.</span><span class="sxs-lookup"><span data-stu-id="8cccc-113">You want to retain an offline copy of the certificate in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="8cccc-114">Du har skapat ett certifikat med hjälp av viktiga valv och vill nu klona objektet till ett annat Azure-område, så att du kan använda det från alla instanser av det distribuerade programmet.</span><span class="sxs-lookup"><span data-stu-id="8cccc-114">You created a certificate using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="8cccc-115">Använd **säkerhets kopierings-AzureKeyVaultCertificate** cmdlet för att hämta certifikatet i krypterat format och sedan använda cmdleten **restore-AzureKeyVaultCertificate** och ange ett nyckeltal i den andra regionen.</span><span class="sxs-lookup"><span data-stu-id="8cccc-115">Use the **Backup-AzureKeyVaultCertificate** cmdlet to retrieve the certificate in encrypted format and then use the **Restore-AzureKeyVaultCertificate** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="8cccc-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8cccc-116">EXAMPLES</span></span>

### <span data-ttu-id="8cccc-117">Exempel 1: säkerhetskopiera ett certifikat med ett automatiskt genererat fil namn</span><span class="sxs-lookup"><span data-stu-id="8cccc-117">Example 1: Back up a certificate with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzureKeyVaultCertificate -VaultName 'mykeyvault' -Name 'mycert'

C:\Users\username\mykeyvault-mycert-1527029447.01191
```

<span data-ttu-id="8cccc-118">Det här kommandot hämtar certifikatet med namnet mina cert från det viktiga valvet som heter MyKeyVault och sparar en säkerhets kopia av certifikatet i en fil som automatiskt namnges för dig och visar fil namnet.</span><span class="sxs-lookup"><span data-stu-id="8cccc-118">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="8cccc-119">Exempel 2: säkerhetskopiera ett certifikat till ett angivet fil namn</span><span class="sxs-lookup"><span data-stu-id="8cccc-119">Example 2: Back up a certificate to a specified file name</span></span>
```powershell
PS C:\> Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyCert' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="8cccc-120">Det här kommandot hämtar certifikatet med namnet mina cert från det nyckelord som heter MyKeyVault och sparar en säkerhets kopia av certifikatet i en fil med namnet Backup. blob.</span><span class="sxs-lookup"><span data-stu-id="8cccc-120">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file named Backup.blob.</span></span>

### <span data-ttu-id="8cccc-121">Exempel 3: säkerhetskopiera ett tidigare hämtat certifikat till ett angivet fil namn och skriv över målfilen utan att fråga.</span><span class="sxs-lookup"><span data-stu-id="8cccc-121">Example 3: Back up a previously retrieved certificate to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $cert = Get-AzureKeyVaultCertificate -VaultName 'MyKeyVault' -Name 'MyCert'
PS C:\> Backup-AzureKeyVaultCertificate -Certificate $cert -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="8cccc-122">Det här kommandot skapar en säkerhets kopia av certifikatet med namnet $cert. Namn i valvet med namnet $cert. VaultName till en fil med namnet Backup. blob, och överskriv sedan filen utan att skriva över den.</span><span class="sxs-lookup"><span data-stu-id="8cccc-122">This command creates a backup of the certificate named $cert.Name in the vault named $cert.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="8cccc-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8cccc-123">PARAMETERS</span></span>

### <span data-ttu-id="8cccc-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cccc-124">-DefaultProfile</span></span>
<span data-ttu-id="8cccc-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8cccc-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cccc-126">-Force</span><span class="sxs-lookup"><span data-stu-id="8cccc-126">-Force</span></span>
<span data-ttu-id="8cccc-127">Skriv över den angivna filen om den finns</span><span class="sxs-lookup"><span data-stu-id="8cccc-127">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="8cccc-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8cccc-128">-InputObject</span></span>
<span data-ttu-id="8cccc-129">Hemlighet som ska säkerhets kopie ras, från utdata från ett samtal.</span><span class="sxs-lookup"><span data-stu-id="8cccc-129">Secret to be backed up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByCertificate
Aliases: Certificate

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8cccc-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="8cccc-130">-Name</span></span>
<span data-ttu-id="8cccc-131">Hemligt namn.</span><span class="sxs-lookup"><span data-stu-id="8cccc-131">Secret name.</span></span>
<span data-ttu-id="8cccc-132">Cmdlet konstruerar FQDN för en hemlighet från valv namn, för närvarande valt miljö och hemligt namn.</span><span class="sxs-lookup"><span data-stu-id="8cccc-132">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cccc-133">-Utdatafil</span><span class="sxs-lookup"><span data-stu-id="8cccc-133">-OutputFile</span></span>
<span data-ttu-id="8cccc-134">Utdatafil.</span><span class="sxs-lookup"><span data-stu-id="8cccc-134">Output file.</span></span>
<span data-ttu-id="8cccc-135">Utdatafil som säkerhetskopierar certifikatet.</span><span class="sxs-lookup"><span data-stu-id="8cccc-135">The output file to store the backup of the certificate.</span></span>
<span data-ttu-id="8cccc-136">Om inget anges genereras ett standard fil namn.</span><span class="sxs-lookup"><span data-stu-id="8cccc-136">If not specified, a default filename will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cccc-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8cccc-137">-VaultName</span></span>
<span data-ttu-id="8cccc-138">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="8cccc-138">Vault name.</span></span>
<span data-ttu-id="8cccc-139">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="8cccc-139">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cccc-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8cccc-140">-Confirm</span></span>
<span data-ttu-id="8cccc-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8cccc-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cccc-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cccc-142">-WhatIf</span></span>
<span data-ttu-id="8cccc-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8cccc-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cccc-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8cccc-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cccc-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cccc-145">CommonParameters</span></span>
<span data-ttu-id="8cccc-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cccc-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cccc-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cccc-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cccc-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8cccc-148">INPUTS</span></span>

### <span data-ttu-id="8cccc-149">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="8cccc-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>
<span data-ttu-id="8cccc-150">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8cccc-150">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="8cccc-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8cccc-151">OUTPUTS</span></span>

### <span data-ttu-id="8cccc-152">System. String</span><span class="sxs-lookup"><span data-stu-id="8cccc-152">System.String</span></span>

## <span data-ttu-id="8cccc-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8cccc-153">NOTES</span></span>

## <span data-ttu-id="8cccc-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8cccc-154">RELATED LINKS</span></span>
