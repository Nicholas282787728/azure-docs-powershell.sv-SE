---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: c01d07f9408804b229921394c24e444b2a4deb8b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525977"
---
# <span data-ttu-id="30021-101">Backup-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30021-101">Backup-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="30021-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="30021-102">SYNOPSIS</span></span>
<span data-ttu-id="30021-103">Säkerhetskopierar ett valv-hanterat lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="30021-103">Backs up a KeyVault-managed storage account.</span></span>

## <span data-ttu-id="30021-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="30021-104">SYNTAX</span></span>

### <span data-ttu-id="30021-105">ByStorageAccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="30021-105">ByStorageAccountName (Default)</span></span>
```
Backup-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30021-106">ByStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30021-106">ByStorageAccount</span></span>
```
Backup-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-OutputFile] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="30021-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="30021-107">DESCRIPTION</span></span>
<span data-ttu-id="30021-108">**Säkerhets kopiering-AzKeyVaultManagedStorageAccount** cmdlet säkerhetskopierar ett angivet hanterat lagrings konto i ett nyckelord genom att ladda ner det och lagra det i en fil.</span><span class="sxs-lookup"><span data-stu-id="30021-108">The **Backup-AzKeyVaultManagedStorageAccount** cmdlet backs up a specified managed storage account in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="30021-109">Eftersom det hämtade innehållet är krypterat kan det inte användas utanför Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="30021-109">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="30021-110">Du kan återställa ett säkerhets kopie rad lagrings konto till alla viktiga valv i prenumerationen som det säkerhetskopierades från, så länge valvet finns i samma Azure geography.</span><span class="sxs-lookup"><span data-stu-id="30021-110">You can restore a backed-up storage account to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="30021-111">Vanliga skäl till att använda denna cmdlet är:</span><span class="sxs-lookup"><span data-stu-id="30021-111">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="30021-112">Du vill behålla en offlinekopia av lagrings kontot ifall du oavsiktligt tar bort originalet från valvet.</span><span class="sxs-lookup"><span data-stu-id="30021-112">You want to retain an offline copy of the storage account in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="30021-113">Du har skapat ett hanterat lagrings konto med hjälp av viktiga valv och vill klona objektet till ett annat Azure-område, så att du kan använda det från alla instanser av det distribuerade programmet.</span><span class="sxs-lookup"><span data-stu-id="30021-113">You created a managed storage account using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="30021-114">Använd **säkerhets kopierings-AzKeyVaultManagedStorageAccount** cmdlet för att hämta hanterat lagrings konto i krypterat format och sedan använda cmdleten **restore-AzKeyVaultManagedStorageAccount** och ange ett huvud valv i den andra regionen.</span><span class="sxs-lookup"><span data-stu-id="30021-114">Use the **Backup-AzKeyVaultManagedStorageAccount** cmdlet to retrieve the managed storage account in encrypted format and then use the **Restore-AzKeyVaultManagedStorageAccount** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="30021-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="30021-115">EXAMPLES</span></span>

### <span data-ttu-id="30021-116">Exempel 1: säkerhetskopiera ett hanterat lagrings konto med ett automatiskt genererat fil namn</span><span class="sxs-lookup"><span data-stu-id="30021-116">Example 1: Back up a managed storage account with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'

C:\Users\username\mykeyvault-mymsak-1527029447.01191
```

<span data-ttu-id="30021-117">Det här kommandot hämtar det hanterade lagrings kontot med namnet MyMSAK från Key-valvet MyKeyVault och sparar en säkerhets kopia av det hanterade lagrings kontot till en fil som automatiskt heter för dig och visar fil namnet.</span><span class="sxs-lookup"><span data-stu-id="30021-117">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="30021-118">Exempel 2: säkerhetskopiera ett hanterat lagrings konto till ett angivet fil namn</span><span class="sxs-lookup"><span data-stu-id="30021-118">Example 2: Back up a managed storage account to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyMSAK' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="30021-119">Det här kommandot hämtar det hanterade lagrings kontot med namnet MyMSAK från Key-valvet MyKeyVault och sparar en säkerhets kopia av det hanterade lagrings kontot till en fil med namnet Backup. blob.</span><span class="sxs-lookup"><span data-stu-id="30021-119">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file named Backup.blob.</span></span>

### <span data-ttu-id="30021-120">Exempel 3: säkerhetskopiera ett tidigare hämtat hanterat lagrings konto till ett angivet fil namn och skriv över målfilen utan att fråga.</span><span class="sxs-lookup"><span data-stu-id="30021-120">Example 3: Back up a previously retrieved managed storage account to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $msak = Get-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'
PS C:\> Backup-AzKeyVaultManagedStorageAccount -StorageAccount $msak -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="30021-121">Det här kommandot skapar en säkerhets kopia av det hanterade lagrings kontot med namnet $msak. Namn i valvet med namnet $msak. VaultName till en fil med namnet Backup. blob, och överskriv sedan filen utan att skriva över den.</span><span class="sxs-lookup"><span data-stu-id="30021-121">This command creates a backup of the managed storage account named $msak.Name in the vault named $msak.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="30021-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="30021-122">PARAMETERS</span></span>

### <span data-ttu-id="30021-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30021-123">-DefaultProfile</span></span>
<span data-ttu-id="30021-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="30021-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30021-125">-Force</span><span class="sxs-lookup"><span data-stu-id="30021-125">-Force</span></span>
<span data-ttu-id="30021-126">Skriv över den angivna filen om den finns</span><span class="sxs-lookup"><span data-stu-id="30021-126">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="30021-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30021-127">-InputObject</span></span>
<span data-ttu-id="30021-128">Lagrings konto paket som ska säkerhets kopie ras, från utdata från ett samtal.</span><span class="sxs-lookup"><span data-stu-id="30021-128">Storage account bundle to be backed up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByStorageAccount
Aliases: StorageAccount

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30021-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="30021-129">-Name</span></span>
<span data-ttu-id="30021-130">Hemligt namn.</span><span class="sxs-lookup"><span data-stu-id="30021-130">Secret name.</span></span>
<span data-ttu-id="30021-131">Cmdlet konstruerar FQDN för en hemlighet från valv namn, för närvarande valt miljö och hemligt namn.</span><span class="sxs-lookup"><span data-stu-id="30021-131">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByStorageAccountName
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30021-132">-Utdatafil</span><span class="sxs-lookup"><span data-stu-id="30021-132">-OutputFile</span></span>
<span data-ttu-id="30021-133">Utdatafil.</span><span class="sxs-lookup"><span data-stu-id="30021-133">Output file.</span></span>
<span data-ttu-id="30021-134">Utdatafil som lagrar säkerhets kopian av lagrings konton.</span><span class="sxs-lookup"><span data-stu-id="30021-134">The output file to store the storage account backup.</span></span>
<span data-ttu-id="30021-135">Om inget anges genereras ett standard fil namn.</span><span class="sxs-lookup"><span data-stu-id="30021-135">If not specified, a default filename will be generated.</span></span>

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

### <span data-ttu-id="30021-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="30021-136">-VaultName</span></span>
<span data-ttu-id="30021-137">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="30021-137">Vault name.</span></span>
<span data-ttu-id="30021-138">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="30021-138">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByStorageAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30021-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="30021-139">-Confirm</span></span>
<span data-ttu-id="30021-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="30021-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30021-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30021-141">-WhatIf</span></span>
<span data-ttu-id="30021-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="30021-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30021-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="30021-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30021-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30021-144">CommonParameters</span></span>
<span data-ttu-id="30021-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30021-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30021-146">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30021-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30021-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="30021-147">INPUTS</span></span>

### <span data-ttu-id="30021-148">Microsoft. Azure. commands. valv. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="30021-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="30021-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="30021-149">OUTPUTS</span></span>

### <span data-ttu-id="30021-150">System. String</span><span class="sxs-lookup"><span data-stu-id="30021-150">System.String</span></span>

## <span data-ttu-id="30021-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="30021-151">NOTES</span></span>

## <span data-ttu-id="30021-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="30021-152">RELATED LINKS</span></span>
