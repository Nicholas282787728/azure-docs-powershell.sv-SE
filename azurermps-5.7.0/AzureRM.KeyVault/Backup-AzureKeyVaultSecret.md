---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultSecret.md
ms.openlocfilehash: 1a2445509aca49c28320ad1fc1685daa0127fa50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575648"
---
# Backup-AzureKeyVaultSecret

## Sammanfattning
Säkerhetskopierar en hemlighet i ett nyckel valv.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### BySecretName (standard)
```
Backup-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### BySecret
```
Backup-AzureKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
**Säkerhets kopiering-AzureKeyVaultSecret** cmdlet säkerhetskopierar en angiven hemlighet i ett nyckel valv genom att ladda ned den och lagra den i en fil.
Om det finns flera versioner av hemligheten ingår alla versioner i säkerhets kopian.
Eftersom det hämtade innehållet är krypterat kan det inte användas utanför Azure Key Vault.
Du kan återställa en säkerhetskopierad hemlighet till ett nyckel valv i det abonnemang som den säkerhetskopierades från.

Vanliga skäl till att använda denna cmdlet är:

- Du vill Escrow en kopia av din hemliga text så att du har en offlinekopia ifall du oavsiktligt tar bort din hemlighet i ditt nyckel valv.
- Du har lagt till en hemlighet till ett nyckel valv och vill nu klona hemligheten till ett annat Azure-område, så att du kan använda den från alla instanser av det distribuerade programmet. Använd Backup-AzureKeyVaultSecret cmdlet för att hämta hemligheten i krypterat format och Använd sedan Restore-AzureKeyVaultSecret cmdlet och ange ett nyckel valv i den andra regionen. (Observera att regionerna måste tillhöra samma geografi.)

## BESKRIVS

### Exempel 1: säkerhetskopiera en hemlighet med ett automatiskt genererat fil namn
```
PS C:\>Backup-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
```

Det här kommandot hämtar hemligheten med namnet hemlig från nyckel valvet som heter MyKeyVault och sparar en säkerhets kopia av den hemligheten i en fil som automatiskt namnges för dig och visar fil namnet.

### Exempel 2: säkerhetskopiera en hemlighet till ett angivet fil namn och skriv över den befintliga filen utan att fråga
```
PS C:\>Backup-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force
```

Det här kommandot hämtar hemligheten hemligt från vaultnamed MyKeyVault och sparar en säkerhets kopia av den hemligheten i en fil med namnet Backup. blob.

### Exempel 3: säkerhetskopiera en hemlighet som tidigare hämtats till ett angivet fil namn
```
PS C:\>$secret = Get-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\>Backup-AzureKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'
```

Det här kommandot använder $secret objektets valv namn och namn för att hämta hemligheten och spara säkerhets kopian i en fil med namnet Backup. blob.

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

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

### -Force
Du uppmanas att bekräfta innan utdatafilen skrivs över om den finns.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InputObject
Hemlighet som ska säkerhets kopie ras, från utdata från ett samtal.

```yaml
Type: PSKeyVaultSecretIdentityItem
Parameter Sets: BySecret
Aliases: Secret

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Namn
Anger namnet på den hemlighet som ska säkerhets kopie ras.

```yaml
Type: String
Parameter Sets: BySecretName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Utdatafil
Anger den utdatafil där reserv-BLOB lagras.
Om du inte anger den här parametern skapar den här cmdleten ett fil namn.
Om du anger namnet på en befintlig utdatafil slutförs inte åtgärden och returnerar ett fel meddelande om att säkerhets kopian redan finns.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
Anger namnet på det nyckel valv som innehåller hemligheten som ska säkerhets kopie ras.

```yaml
Type: String
Parameter Sets: BySecretName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som händer om cmdleten körs.
Cmdleten körs inte.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen
Denna cmdlet accepterar inte indata.

## VÄRDEN

### Strängvärdet
Cmdleten returnerar sökvägen till utdatafilen med säkerhets kopian av nyckel.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Set-AzureKeyVaultSecret](./Set-AzureKeyVaultSecret.md)

[Get-AzureKeyVaultSecret](./Get-AzureKeyVaultSecret.md)

[Remove-AzureKeyVaultSecret](./Remove-AzureKeyVaultSecret.md)

[Återställ-AzureKeyVaultSecret](./Restore-AzureKeyVaultSecret.md)

