---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 1520acb94ffe587fb96eaa9c2ba565bcf31cc87e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584215"
---
# Backup-AzureKeyVaultManagedStorageAccount

## Sammanfattning
Säkerhetskopierar ett valv-hanterat lagrings konto.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### ByStorageAccountName (standard)
```
Backup-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByStorageAccount
```
Backup-AzureKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-OutputFile] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
**Säkerhets kopiering-AzureKeyVaultManagedStorageAccount** cmdlet säkerhetskopierar ett angivet hanterat lagrings konto i ett nyckelord genom att ladda ner det och lagra det i en fil.
Eftersom det hämtade innehållet är krypterat kan det inte användas utanför Azure Key Vault.
Du kan återställa ett säkerhets kopie rad lagrings konto till alla viktiga valv i prenumerationen som det säkerhetskopierades från, så länge valvet finns i samma Azure geography.
Vanliga skäl till att använda denna cmdlet är: 
- Du vill behålla en offlinekopia av lagrings kontot ifall du oavsiktligt tar bort originalet från valvet.
 
- Du har skapat ett hanterat lagrings konto med hjälp av viktiga valv och vill klona objektet till ett annat Azure-område, så att du kan använda det från alla instanser av det distribuerade programmet.
Använd **säkerhets kopierings-AzureKeyVaultManagedStorageAccount** cmdlet för att hämta hanterat lagrings konto i krypterat format och sedan använda cmdleten **restore-AzureKeyVaultManagedStorageAccount** och ange ett huvud valv i den andra regionen.

## BESKRIVS

### Exempel 1: säkerhetskopiera ett hanterat lagrings konto med ett automatiskt genererat fil namn
```powershell
PS C:\Users\username\> Backup-AzureKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'

C:\Users\username\mykeyvault-mymsak-1527029447.01191
```

Det här kommandot hämtar det hanterade lagrings kontot med namnet MyMSAK från Key-valvet MyKeyVault och sparar en säkerhets kopia av det hanterade lagrings kontot till en fil som automatiskt heter för dig och visar fil namnet.

### Exempel 2: säkerhetskopiera ett hanterat lagrings konto till ett angivet fil namn
```powershell
PS C:\> Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyMSAK' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

Det här kommandot hämtar det hanterade lagrings kontot med namnet MyMSAK från Key-valvet MyKeyVault och sparar en säkerhets kopia av det hanterade lagrings kontot till en fil med namnet Backup. blob.

### Exempel 3: säkerhetskopiera ett tidigare hämtat hanterat lagrings konto till ett angivet fil namn och skriv över målfilen utan att fråga.
```powershell
PS C:\> $msak = Get-AzureKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'
PS C:\> Backup-AzureKeyVaultManagedStorageAccount -StorageAccount $msak -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

Det här kommandot skapar en säkerhets kopia av det hanterade lagrings kontot med namnet $msak. Namn i valvet med namnet $msak. VaultName till en fil med namnet Backup. blob, och överskriv sedan filen utan att skriva över den.

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

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

### -Force
Skriv över den angivna filen om den finns

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

### -InputObject
Lagrings konto paket som ska säkerhets kopie ras, från utdata från ett samtal.

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

### -Namn
Hemligt namn.
Cmdlet konstruerar FQDN för en hemlighet från valv namn, för närvarande valt miljö och hemligt namn.

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

### -Utdatafil
Utdatafil.
Utdatafil som lagrar säkerhets kopian av lagrings konton.
Om inget anges genereras ett standard fil namn.

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

### -VaultName
Valv namn.
Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.

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

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

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

### -WhatIf
Visar vad som händer om cmdleten körs.
Cmdleten körs inte.

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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Microsoft. Azure. commands. valv. Models. PSKeyVaultManagedStorageAccountIdentityItem
Parametrar: InputObject (ByValue)

## VÄRDEN

### System. String

## ANMÄRKNINGAR

## RELATERADE LÄNKAR
