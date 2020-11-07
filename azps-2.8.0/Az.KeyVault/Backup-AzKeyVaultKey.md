---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
ms.openlocfilehash: cd5e869b1f1d367002b33c5976434f16b22744e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743937"
---
# <span data-ttu-id="75b3f-101">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="75b3f-101">Backup-AzKeyVaultKey</span></span>

## <span data-ttu-id="75b3f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="75b3f-102">SYNOPSIS</span></span>
<span data-ttu-id="75b3f-103">Säkerhetskopierar en nycklar i ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="75b3f-103">Backs up a key in a key vault.</span></span>

## <span data-ttu-id="75b3f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="75b3f-104">SYNTAX</span></span>

### <span data-ttu-id="75b3f-105">ByKeyName (standard)</span><span class="sxs-lookup"><span data-stu-id="75b3f-105">ByKeyName (Default)</span></span>
```
Backup-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75b3f-106">ByKey</span><span class="sxs-lookup"><span data-stu-id="75b3f-106">ByKey</span></span>
```
Backup-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75b3f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="75b3f-107">DESCRIPTION</span></span>
<span data-ttu-id="75b3f-108">**Säkerhets kopiering-AzKeyVaultKey** cmdlet återställer en specifik server i ett nyckelord genom att ladda ned den och lagra den i en fil.</span><span class="sxs-lookup"><span data-stu-id="75b3f-108">The **Backup-AzKeyVaultKey** cmdlet backs up a specified key in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="75b3f-109">Om det finns flera versioner av nycklarna är alla versioner inkluderade i säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="75b3f-109">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="75b3f-110">Eftersom det hämtade innehållet är krypterat kan det inte användas utanför Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="75b3f-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="75b3f-111">Du kan återställa en säkerhets kopie rad server till ett huvud valv i det abonnemang som den säkerhetskopierades från.</span><span class="sxs-lookup"><span data-stu-id="75b3f-111">You can restore a backed-up key to any key vault in the subscription that it was backed up from.</span></span>
<span data-ttu-id="75b3f-112">Vanliga skäl till att använda denna cmdlet är:</span><span class="sxs-lookup"><span data-stu-id="75b3f-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="75b3f-113">Du vill Escrow en kopia av dina nycklar så att du har en offlinekopia ifall du oavsiktligt tar bort din-post i ditt nyckeltal.</span><span class="sxs-lookup"><span data-stu-id="75b3f-113">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your key vault.</span></span>
 
- <span data-ttu-id="75b3f-114">Du har skapat en sessionsnyckel med hjälp av viktiga valv och vill klona tangenten till ett annat Azure-område, så att du kan använda den från alla instanser av det distribuerade programmet.</span><span class="sxs-lookup"><span data-stu-id="75b3f-114">You created a key using Key Vault and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="75b3f-115">Använd **säkerhets kopierings-AzKeyVaultKey** cmdlet för att hämta nycklar i krypterat format och använd sedan Restore-AzKeyVaultKey cmdlet och ange ett huvud valv i den andra regionen.</span><span class="sxs-lookup"><span data-stu-id="75b3f-115">Use the **Backup-AzKeyVaultKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzKeyVaultKey cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="75b3f-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="75b3f-116">EXAMPLES</span></span>

### <span data-ttu-id="75b3f-117">Exempel 1: säkerhetskopiera en nycklar med ett automatiskt genererat fil namn</span><span class="sxs-lookup"><span data-stu-id="75b3f-117">Example 1: Back up a key with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'

C:\Users\username\mykeyvault-mykey-1527029447.01191
```

<span data-ttu-id="75b3f-118">Det här kommandot hämtar den nycklar som heter MyKey från nyckelordet MyKeyVault och sparar en säkerhets kopia av den till en fil som automatiskt namnges för dig och visar fil namnet.</span><span class="sxs-lookup"><span data-stu-id="75b3f-118">This command retrieves the key named MyKey from the key vault named MyKeyVault and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="75b3f-119">Exempel 2: säkerhetskopiera en nycklar till ett angivet fil namn</span><span class="sxs-lookup"><span data-stu-id="75b3f-119">Example 2: Back up a key to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="75b3f-120">Det här kommandot hämtar den nycklar som heter MyKey från vaultnamed MyKeyVault och sparar en säkerhets kopia av den i en fil med namnet Backup. blob.</span><span class="sxs-lookup"><span data-stu-id="75b3f-120">This command retrieves the key named MyKey from the key vaultnamed MyKeyVault and saves a backup of that key to a file named Backup.blob.</span></span>

### <span data-ttu-id="75b3f-121">Exempel 3: säkerhetskopiera en tidigare Hämtad nycklar till ett angivet fil namn och skriv över målfilen utan att fråga.</span><span class="sxs-lookup"><span data-stu-id="75b3f-121">Example 3: Back up a previously retrieved key to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $key = Get-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\> Backup-AzKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="75b3f-122">Det här kommandot skapar en säkerhets kopia av den nycklar som heter $key. Namn i valvet med namnet $key. VaultName till en fil med namnet Backup. blob, och överskriv sedan filen utan att skriva över den.</span><span class="sxs-lookup"><span data-stu-id="75b3f-122">This command creates a backup of the key named $key.Name in the vault named $key.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="75b3f-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="75b3f-123">PARAMETERS</span></span>

### <span data-ttu-id="75b3f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75b3f-124">-DefaultProfile</span></span>
<span data-ttu-id="75b3f-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="75b3f-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75b3f-126">-Force</span><span class="sxs-lookup"><span data-stu-id="75b3f-126">-Force</span></span>
<span data-ttu-id="75b3f-127">Skriv över den angivna filen om den finns</span><span class="sxs-lookup"><span data-stu-id="75b3f-127">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="75b3f-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75b3f-128">-InputObject</span></span>
<span data-ttu-id="75b3f-129">Huvud paket att säkerhetskopiera från utdata från ett samtal.</span><span class="sxs-lookup"><span data-stu-id="75b3f-129">Key bundle to back up, pipelined in from the output of a retrieval call.</span></span>

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

### <span data-ttu-id="75b3f-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="75b3f-130">-Name</span></span>
<span data-ttu-id="75b3f-131">Anger namnet på den som ska säkerhets kopie ras.</span><span class="sxs-lookup"><span data-stu-id="75b3f-131">Specifies the name of the key to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b3f-132">-Utdatafil</span><span class="sxs-lookup"><span data-stu-id="75b3f-132">-OutputFile</span></span>
<span data-ttu-id="75b3f-133">Anger den utdatafil där reserv-BLOB lagras.</span><span class="sxs-lookup"><span data-stu-id="75b3f-133">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="75b3f-134">Om du inte anger den här parametern skapar den här cmdleten ett fil namn.</span><span class="sxs-lookup"><span data-stu-id="75b3f-134">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="75b3f-135">Om du anger namnet på en befintlig utdatafil slutförs inte åtgärden och returnerar ett fel meddelande om att säkerhets kopian redan finns.</span><span class="sxs-lookup"><span data-stu-id="75b3f-135">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

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

### <span data-ttu-id="75b3f-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="75b3f-136">-VaultName</span></span>
<span data-ttu-id="75b3f-137">Anger namnet på det huvud valv som innehåller den säkerhets kopia du vill säkerhetskopiera.</span><span class="sxs-lookup"><span data-stu-id="75b3f-137">Specifies the name of the key vault that contains the key to back up.</span></span>

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

### <span data-ttu-id="75b3f-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="75b3f-138">-Confirm</span></span>
<span data-ttu-id="75b3f-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="75b3f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75b3f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75b3f-140">-WhatIf</span></span>
<span data-ttu-id="75b3f-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="75b3f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75b3f-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="75b3f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75b3f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75b3f-143">CommonParameters</span></span>
<span data-ttu-id="75b3f-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75b3f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75b3f-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75b3f-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75b3f-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="75b3f-146">INPUTS</span></span>

### <span data-ttu-id="75b3f-147">Microsoft. Azure. commands. valv. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="75b3f-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="75b3f-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="75b3f-148">OUTPUTS</span></span>

### <span data-ttu-id="75b3f-149">System. String</span><span class="sxs-lookup"><span data-stu-id="75b3f-149">System.String</span></span>

## <span data-ttu-id="75b3f-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="75b3f-150">NOTES</span></span>

## <span data-ttu-id="75b3f-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="75b3f-151">RELATED LINKS</span></span>

[<span data-ttu-id="75b3f-152">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="75b3f-152">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="75b3f-153">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="75b3f-153">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="75b3f-154">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="75b3f-154">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="75b3f-155">Återställ-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="75b3f-155">Restore-AzKeyVaultKey</span></span>](./Restore-AzKeyVaultKey.md)

