---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://go.microsoft.com/fwlink/?LinkId=690296
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultSecret.md
ms.openlocfilehash: c53006a4f059fe1f243d9e0bf7a4c701a4c417a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758399"
---
# <span data-ttu-id="07916-101">Backup-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="07916-101">Backup-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="07916-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="07916-102">SYNOPSIS</span></span>
<span data-ttu-id="07916-103">Säkerhetskopierar en hemlighet i ett nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="07916-103">Backs up a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07916-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="07916-104">SYNTAX</span></span>

### <span data-ttu-id="07916-105">BySecretName (standard)</span><span class="sxs-lookup"><span data-stu-id="07916-105">BySecretName (Default)</span></span>
```
Backup-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07916-106">BySecret</span><span class="sxs-lookup"><span data-stu-id="07916-106">BySecret</span></span>
```
Backup-AzureKeyVaultSecret [-Secret] <Secret> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07916-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="07916-107">DESCRIPTION</span></span>
<span data-ttu-id="07916-108">**Säkerhets kopiering-AzureKeyVaultSecret** cmdlet säkerhetskopierar en angiven hemlighet i ett nyckel valv genom att ladda ned den och lagra den i en fil.</span><span class="sxs-lookup"><span data-stu-id="07916-108">The **Backup-AzureKeyVaultSecret** cmdlet backs up a specified secret in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="07916-109">Om det finns flera versioner av hemligheten ingår alla versioner i säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="07916-109">If there are multiple versions of the secret, all versions are included in the backup.</span></span>
<span data-ttu-id="07916-110">Eftersom det hämtade innehållet är krypterat kan det inte användas utanför Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="07916-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="07916-111">Du kan återställa en säkerhetskopierad hemlighet till ett nyckel valv i det abonnemang som den säkerhetskopierades från.</span><span class="sxs-lookup"><span data-stu-id="07916-111">You can restore a backed-up secret to any key vault in the subscription that it was backed up from.</span></span>

<span data-ttu-id="07916-112">Vanliga skäl till att använda denna cmdlet är:</span><span class="sxs-lookup"><span data-stu-id="07916-112">Typical reasons to use this cmdlet are:</span></span>

- <span data-ttu-id="07916-113">Du vill Escrow en kopia av din hemliga text så att du har en offlinekopia ifall du oavsiktligt tar bort din hemlighet i ditt nyckel valv.</span><span class="sxs-lookup"><span data-stu-id="07916-113">You want to escrow a copy of your secret, so that you have an offline copy in case you accidentally delete your secret in your key vault.</span></span>
- <span data-ttu-id="07916-114">Du har lagt till en hemlighet till ett nyckel valv och vill nu klona hemligheten till ett annat Azure-område, så att du kan använda den från alla instanser av det distribuerade programmet.</span><span class="sxs-lookup"><span data-stu-id="07916-114">You added a secret to a key vault and now want to clone the secret into a different Azure region, so that you can use it from all instances of your distributed application.</span></span> <span data-ttu-id="07916-115">Använd Backup-AzureKeyVaultSecret cmdlet för att hämta hemligheten i krypterat format och Använd sedan Restore-AzureKeyVaultSecret cmdlet och ange ett nyckel valv i den andra regionen.</span><span class="sxs-lookup"><span data-stu-id="07916-115">Use the Backup-AzureKeyVaultSecret cmdlet to retrieve the secret in encrypted format and then use the Restore-AzureKeyVaultSecret cmdlet and specify a key vault in the second region.</span></span> <span data-ttu-id="07916-116">(Observera att regionerna måste tillhöra samma geografi.)</span><span class="sxs-lookup"><span data-stu-id="07916-116">(Note that the regions must belong to the same geography.)</span></span>

## <span data-ttu-id="07916-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="07916-117">EXAMPLES</span></span>

### <span data-ttu-id="07916-118">Exempel 1: säkerhetskopiera en hemlighet med ett automatiskt genererat fil namn</span><span class="sxs-lookup"><span data-stu-id="07916-118">Example 1: Back up a secret with an automatically generated file name</span></span>
```
PS C:\>Backup-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="07916-119">Det här kommandot hämtar hemligheten med namnet hemlig från nyckel valvet som heter MyKeyVault och sparar en säkerhets kopia av den hemligheten i en fil som automatiskt namnges för dig och visar fil namnet.</span><span class="sxs-lookup"><span data-stu-id="07916-119">This command retrieves the secret named MySecret from the key vault named MyKeyVault and saves a backup of that secret to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="07916-120">Exempel 2: säkerhetskopiera en hemlighet till ett angivet fil namn och skriv över den befintliga filen utan att fråga</span><span class="sxs-lookup"><span data-stu-id="07916-120">Example 2: Back up a secret to a specified file name, overwriting the existing file without prompting</span></span>
```
PS C:\>Backup-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force
```

<span data-ttu-id="07916-121">Det här kommandot hämtar hemligheten hemligt från vaultnamed MyKeyVault och sparar en säkerhets kopia av den hemligheten i en fil med namnet Backup. blob.</span><span class="sxs-lookup"><span data-stu-id="07916-121">This command retrieves the secret named MySecret from the key vaultnamed MyKeyVault and saves a backup of that secret to a file named Backup.blob.</span></span>

### <span data-ttu-id="07916-122">Exempel 3: säkerhetskopiera en hemlighet som tidigare hämtats till ett angivet fil namn</span><span class="sxs-lookup"><span data-stu-id="07916-122">Example 3: Back up a secret previously retrieved to a specified file name</span></span>
```
PS C:\>$secret = Get-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\>Backup-AzureKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'
```

<span data-ttu-id="07916-123">Det här kommandot använder $secret objektets valv namn och namn för att hämta hemligheten och spara säkerhets kopian i en fil med namnet Backup. blob.</span><span class="sxs-lookup"><span data-stu-id="07916-123">This command uses the $secret object's vault name and name to retrieves the secret and saves its backup to a file named Backup.blob.</span></span>

## <span data-ttu-id="07916-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="07916-124">PARAMETERS</span></span>

### <span data-ttu-id="07916-125">-Force</span><span class="sxs-lookup"><span data-stu-id="07916-125">-Force</span></span>
<span data-ttu-id="07916-126">Du uppmanas att bekräfta innan utdatafilen skrivs över om den finns.</span><span class="sxs-lookup"><span data-stu-id="07916-126">Prompts you for confirmation before overwriting the output file, if that exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07916-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="07916-127">-Name</span></span>
<span data-ttu-id="07916-128">Anger namnet på den hemlighet som ska säkerhets kopie ras.</span><span class="sxs-lookup"><span data-stu-id="07916-128">Specifies the name of the secret to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07916-129">-Utdatafil</span><span class="sxs-lookup"><span data-stu-id="07916-129">-OutputFile</span></span>
<span data-ttu-id="07916-130">Anger den utdatafil där reserv-BLOB lagras.</span><span class="sxs-lookup"><span data-stu-id="07916-130">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="07916-131">Om du inte anger den här parametern skapar den här cmdleten ett fil namn.</span><span class="sxs-lookup"><span data-stu-id="07916-131">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="07916-132">Om du anger namnet på en befintlig utdatafil slutförs inte åtgärden och returnerar ett fel meddelande om att säkerhets kopian redan finns.</span><span class="sxs-lookup"><span data-stu-id="07916-132">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07916-133">-Secret</span><span class="sxs-lookup"><span data-stu-id="07916-133">-Secret</span></span>
<span data-ttu-id="07916-134">Anger det objekt vars namn och valv ska användas för säkerhets kopieringen.</span><span class="sxs-lookup"><span data-stu-id="07916-134">Specifies the object whose name and vault should be used for the backup operation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.Secret
Parameter Sets: BySecret
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07916-135">-VaultName</span><span class="sxs-lookup"><span data-stu-id="07916-135">-VaultName</span></span>
<span data-ttu-id="07916-136">Anger namnet på det nyckel valv som innehåller hemligheten som ska säkerhets kopie ras.</span><span class="sxs-lookup"><span data-stu-id="07916-136">Specifies the name of the key vault that contains the secret to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07916-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="07916-137">-Confirm</span></span>
<span data-ttu-id="07916-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="07916-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07916-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07916-139">-WhatIf</span></span>
<span data-ttu-id="07916-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="07916-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07916-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="07916-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07916-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07916-142">-DefaultProfile</span></span>
<span data-ttu-id="07916-143">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="07916-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07916-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07916-144">CommonParameters</span></span>
<span data-ttu-id="07916-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07916-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07916-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07916-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07916-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="07916-147">INPUTS</span></span>

## <span data-ttu-id="07916-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="07916-148">OUTPUTS</span></span>

### <span data-ttu-id="07916-149">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="07916-149">String</span></span>
<span data-ttu-id="07916-150">Cmdleten returnerar sökvägen till utdatafilen med säkerhets kopian av nyckel.</span><span class="sxs-lookup"><span data-stu-id="07916-150">The cmdlet returns the path of the output file containing the backup of the key.</span></span>

## <span data-ttu-id="07916-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="07916-151">NOTES</span></span>

## <span data-ttu-id="07916-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="07916-152">RELATED LINKS</span></span>

[<span data-ttu-id="07916-153">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="07916-153">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="07916-154">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="07916-154">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="07916-155">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="07916-155">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="07916-156">Återställ-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="07916-156">Restore-AzureKeyVaultSecret</span></span>](./Restore-AzureKeyVaultSecret.md)

