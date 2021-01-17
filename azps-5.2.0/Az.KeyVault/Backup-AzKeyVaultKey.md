---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
ms.openlocfilehash: 88decaffa736f015b8e65aa1217eab4899b07c7c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405744"
---
# <span data-ttu-id="1a0b8-101">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1a0b8-101">Backup-AzKeyVaultKey</span></span>

## <span data-ttu-id="1a0b8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1a0b8-102">SYNOPSIS</span></span>
<span data-ttu-id="1a0b8-103">Säkerhetskopierar en nycklar i ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="1a0b8-103">Backs up a key in a key vault.</span></span>

## <span data-ttu-id="1a0b8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1a0b8-104">SYNTAX</span></span>

### <span data-ttu-id="1a0b8-105">ByKeyName (standard)</span><span class="sxs-lookup"><span data-stu-id="1a0b8-105">ByKeyName (Default)</span></span>
```
Backup-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a0b8-106">HsmByKeyName</span><span class="sxs-lookup"><span data-stu-id="1a0b8-106">HsmByKeyName</span></span>
```
Backup-AzKeyVaultKey -HsmName <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a0b8-107">ByKey</span><span class="sxs-lookup"><span data-stu-id="1a0b8-107">ByKey</span></span>
```
Backup-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a0b8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1a0b8-108">DESCRIPTION</span></span>
<span data-ttu-id="1a0b8-109">**Säkerhets kopiering-AzKeyVaultKey** cmdlet återställer en specifik server i ett nyckelord genom att ladda ned den och lagra den i en fil.</span><span class="sxs-lookup"><span data-stu-id="1a0b8-109">The **Backup-AzKeyVaultKey** cmdlet backs up a specified key in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="1a0b8-110">Om det finns flera versioner av nycklarna är alla versioner inkluderade i säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="1a0b8-110">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="1a0b8-111">Eftersom det hämtade innehållet är krypterat kan det inte användas utanför Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="1a0b8-111">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="1a0b8-112">Du kan återställa en säkerhets kopie rad server till ett huvud valv i det abonnemang som den säkerhetskopierades från.</span><span class="sxs-lookup"><span data-stu-id="1a0b8-112">You can restore a backed-up key to any key vault in the subscription that it was backed up from.</span></span>
<span data-ttu-id="1a0b8-113">Vanliga skäl till att använda denna cmdlet är:</span><span class="sxs-lookup"><span data-stu-id="1a0b8-113">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="1a0b8-114">Du vill Escrow en kopia av dina nycklar så att du har en offlinekopia ifall du oavsiktligt tar bort din-post i ditt nyckeltal.</span><span class="sxs-lookup"><span data-stu-id="1a0b8-114">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your key vault.</span></span>
 
- <span data-ttu-id="1a0b8-115">Du har skapat en sessionsnyckel med hjälp av viktiga valv och vill klona tangenten till ett annat Azure-område, så att du kan använda den från alla instanser av det distribuerade programmet.</span><span class="sxs-lookup"><span data-stu-id="1a0b8-115">You created a key using Key Vault and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="1a0b8-116">Använd **säkerhets kopierings-AzKeyVaultKey** cmdlet för att hämta nycklar i krypterat format och använd sedan Restore-AzKeyVaultKey cmdlet och ange ett huvud valv i den andra regionen.</span><span class="sxs-lookup"><span data-stu-id="1a0b8-116">Use the **Backup-AzKeyVaultKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzKeyVaultKey cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="1a0b8-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1a0b8-117">EXAMPLES</span></span>

### <span data-ttu-id="1a0b8-118">Exempel 1: säkerhetskopiera en nycklar med ett automatiskt genererat fil namn</span><span class="sxs-lookup"><span data-stu-id="1a0b8-118">Example 1: Back up a key with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'

C:\Users\username\mykeyvault-mykey-1527029447.01191
```

<span data-ttu-id="1a0b8-119">Det här kommandot hämtar den nycklar som heter MyKey från nyckelordet MyKeyVault och sparar en säkerhets kopia av den till en fil som automatiskt namnges för dig och visar fil namnet.</span><span class="sxs-lookup"><span data-stu-id="1a0b8-119">This command retrieves the key named MyKey from the key vault named MyKeyVault and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="1a0b8-120">Exempel 2: säkerhetskopiera en nycklar till ett angivet fil namn</span><span class="sxs-lookup"><span data-stu-id="1a0b8-120">Example 2: Back up a key to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="1a0b8-121">Det här kommandot hämtar den nycklar som heter MyKey från vaultnamed MyKeyVault och sparar en säkerhets kopia av den i en fil med namnet Backup. blob.</span><span class="sxs-lookup"><span data-stu-id="1a0b8-121">This command retrieves the key named MyKey from the key vaultnamed MyKeyVault and saves a backup of that key to a file named Backup.blob.</span></span>

### <span data-ttu-id="1a0b8-122">Exempel 3: säkerhetskopiera en tidigare Hämtad nycklar till ett angivet fil namn och skriv över målfilen utan att fråga.</span><span class="sxs-lookup"><span data-stu-id="1a0b8-122">Example 3: Back up a previously retrieved key to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $key = Get-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\> Backup-AzKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="1a0b8-123">Det här kommandot skapar en säkerhets kopia av den nycklar som heter $key. Namn i valvet med namnet $key. VaultName till en fil med namnet Backup. blob, och överskriv sedan filen utan att skriva över den.</span><span class="sxs-lookup"><span data-stu-id="1a0b8-123">This command creates a backup of the key named $key.Name in the vault named $key.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="1a0b8-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1a0b8-124">PARAMETERS</span></span>

### <span data-ttu-id="1a0b8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a0b8-125">-DefaultProfile</span></span>
<span data-ttu-id="1a0b8-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1a0b8-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1a0b8-127">-Force</span><span class="sxs-lookup"><span data-stu-id="1a0b8-127">-Force</span></span>
<span data-ttu-id="1a0b8-128">Skriv över den angivna filen om den finns</span><span class="sxs-lookup"><span data-stu-id="1a0b8-128">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="1a0b8-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="1a0b8-129">-HsmName</span></span>
<span data-ttu-id="1a0b8-130">HSM-namn.</span><span class="sxs-lookup"><span data-stu-id="1a0b8-130">HSM name.</span></span> <span data-ttu-id="1a0b8-131">Cmdlet konstruerar FQDN för en hanterad HSM baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="1a0b8-131">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByKeyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a0b8-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a0b8-132">-InputObject</span></span>
<span data-ttu-id="1a0b8-133">Huvud paket att säkerhetskopiera från utdata från ett samtal.</span><span class="sxs-lookup"><span data-stu-id="1a0b8-133">Key bundle to back up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByKey
Aliases: Key

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a0b8-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="1a0b8-134">-Name</span></span>
<span data-ttu-id="1a0b8-135">Anger namnet på den som ska säkerhets kopie ras.</span><span class="sxs-lookup"><span data-stu-id="1a0b8-135">Specifies the name of the key to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName, HsmByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a0b8-136">-Utdatafil</span><span class="sxs-lookup"><span data-stu-id="1a0b8-136">-OutputFile</span></span>
<span data-ttu-id="1a0b8-137">Anger den utdatafil där reserv-BLOB lagras.</span><span class="sxs-lookup"><span data-stu-id="1a0b8-137">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="1a0b8-138">Om du inte anger den här parametern skapar den här cmdleten ett fil namn.</span><span class="sxs-lookup"><span data-stu-id="1a0b8-138">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="1a0b8-139">Om du anger namnet på en befintlig utdatafil slutförs inte åtgärden och returnerar ett fel meddelande om att säkerhets kopian redan finns.</span><span class="sxs-lookup"><span data-stu-id="1a0b8-139">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

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

### <span data-ttu-id="1a0b8-140">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1a0b8-140">-VaultName</span></span>
<span data-ttu-id="1a0b8-141">Anger namnet på det huvud valv som innehåller den säkerhets kopia du vill säkerhetskopiera.</span><span class="sxs-lookup"><span data-stu-id="1a0b8-141">Specifies the name of the key vault that contains the key to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a0b8-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1a0b8-142">-Confirm</span></span>
<span data-ttu-id="1a0b8-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1a0b8-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a0b8-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a0b8-144">-WhatIf</span></span>
<span data-ttu-id="1a0b8-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1a0b8-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a0b8-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1a0b8-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a0b8-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a0b8-147">CommonParameters</span></span>
<span data-ttu-id="1a0b8-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a0b8-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a0b8-149">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1a0b8-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a0b8-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1a0b8-150">INPUTS</span></span>

### <span data-ttu-id="1a0b8-151">Microsoft. Azure. commands. valv. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="1a0b8-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="1a0b8-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1a0b8-152">OUTPUTS</span></span>

### <span data-ttu-id="1a0b8-153">System. String</span><span class="sxs-lookup"><span data-stu-id="1a0b8-153">System.String</span></span>

## <span data-ttu-id="1a0b8-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1a0b8-154">NOTES</span></span>

## <span data-ttu-id="1a0b8-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1a0b8-155">RELATED LINKS</span></span>

[<span data-ttu-id="1a0b8-156">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1a0b8-156">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="1a0b8-157">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1a0b8-157">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="1a0b8-158">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1a0b8-158">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="1a0b8-159">Återställ-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1a0b8-159">Restore-AzKeyVaultKey</span></span>](./Restore-AzKeyVaultKey.md)

