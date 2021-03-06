---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/backup-AzKeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
ms.openlocfilehash: b1f26123579589c15ac4eff6b577706270a7e15a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922750"
---
# Backup-AzKeyVaultSecret

## Sammanfattning
Säkerhetskopierar en hemlighet i ett nyckel valv.

## FRÅGESYNTAXEN

### BySecretName (standard)
```
Backup-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### BySecret
```
Backup-AzKeyVaultSecret [-Secret] <Secret> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
**Säkerhets kopiering-AzKeyVaultSecret** cmdlet säkerhetskopierar en angiven hemlighet i ett nyckel valv genom att ladda ned den och lagra den i en fil.
Om det finns flera versioner av hemligheten ingår alla versioner i säkerhets kopian.
Eftersom det hämtade innehållet är krypterat kan det inte användas utanför Azure Key Vault.
Du kan återställa en säkerhetskopierad hemlighet till ett nyckel valv i det abonnemang som den säkerhetskopierades från.

Vanliga skäl till att använda denna cmdlet är:

- Du vill Escrow en kopia av din hemliga text så att du har en offlinekopia ifall du oavsiktligt tar bort din hemlighet i ditt nyckel valv.
- Du har lagt till en hemlighet till ett nyckel valv och vill nu klona hemligheten till ett annat Azure-område, så att du kan använda den från alla instanser av det distribuerade programmet. Använd Backup-AzKeyVaultSecret cmdlet för att hämta hemligheten i krypterat format och Använd sedan Restore-AzKeyVaultSecret cmdlet och ange ett nyckel valv i den andra regionen. (Observera att regionerna måste tillhöra samma geografi.)

## BESKRIVS

### Exempel 1: säkerhetskopiera en hemlighet med ett automatiskt genererat fil namn
```
PS C:\>Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
```

Det här kommandot hämtar hemligheten med namnet hemlig från nyckel valvet som heter MyKeyVault och sparar en säkerhets kopia av den hemligheten i en fil som automatiskt namnges för dig och visar fil namnet.

### Exempel 2: säkerhetskopiera en hemlighet till ett angivet fil namn och skriv över den befintliga filen utan att fråga
```
PS C:\>Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force
```

Det här kommandot hämtar hemligheten hemligt från vaultnamed MyKeyVault och sparar en säkerhets kopia av den hemligheten i en fil med namnet Backup. blob.

### Exempel 3: säkerhetskopiera en hemlighet som tidigare hämtats till ett angivet fil namn
```
PS C:\>$secret = Get-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\>Backup-AzKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'
```

Det här kommandot använder $secret objektets valv namn och namn för att hämta hemligheten och spara säkerhets kopian i en fil med namnet Backup. blob.

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

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

### -Secret
Anger det objekt vars namn och valv ska användas för säkerhets kopieringen.

```yaml
Type: Secret
Parameter Sets: BySecret
Aliases: 

Required: True
Position: 0
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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen
Denna cmdlet accepterar inte indata.

## VÄRDEN

### Strängvärdet
Cmdleten returnerar sökvägen till utdatafilen med säkerhets kopian av nyckel.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Set-AzKeyVaultSecret](./Set-AzKeyVaultSecret.md)

[Get-AzKeyVaultSecret](./Get-AzKeyVaultSecret.md)

[Remove-AzKeyVaultSecret](./Remove-AzKeyVaultSecret.md)

[Återställ-AzKeyVaultSecret](./Restore-AzKeyVaultSecret.md)

