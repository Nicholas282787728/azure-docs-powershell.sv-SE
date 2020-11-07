---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://go.microsoft.com/fwlink/?LinkId=690296
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultKey.md
ms.openlocfilehash: f6d6b362a93897dc854170b8cbbbfd228b305abc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758401"
---
# Backup-AzureKeyVaultKey

## Sammanfattning
Säkerhetskopierar en nycklar i ett nyckelord.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### ByKeyName (standard)
```
Backup-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByKey
```
Backup-AzureKeyVaultKey [-Key] <KeyBundle> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
**Säkerhets kopiering-AzureKeyVaultKey** cmdlet återställer en specifik server i ett nyckelord genom att ladda ned den och lagra den i en fil.
Om det finns flera versioner av nycklarna är alla versioner inkluderade i säkerhets kopian.
Eftersom det hämtade innehållet är krypterat kan det inte användas utanför Azure Key Vault.
Du kan återställa en säkerhets kopie rad server till ett huvud valv i det abonnemang som den säkerhetskopierades från.

Vanliga skäl till att använda denna cmdlet är: 

- Du vill Escrow en kopia av dina nycklar så att du har en offlinekopia ifall du oavsiktligt tar bort din-post i ditt nyckeltal.
 
- Du har skapat en sessionsnyckel med hjälp av viktiga valv och vill klona tangenten till ett annat Azure-område, så att du kan använda den från alla instanser av det distribuerade programmet.
Använd **säkerhets kopierings-AzureKeyVaultKey** cmdlet för att hämta nycklar i krypterat format och använd sedan Restore-AzureKeyVaultKey cmdlet och ange ett huvud valv i den andra regionen.

## BESKRIVS

### Exempel 1: säkerhetskopiera en nycklar med ett automatiskt genererat fil namn
```
PS C:\>Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
```

Det här kommandot hämtar den nycklar som heter MyKey från nyckelordet MyKeyVault och sparar en säkerhets kopia av den till en fil som automatiskt namnges för dig och visar fil namnet.

### Exempel 2: säkerhetskopiera en nycklar till ett angivet fil namn
```
PS C:\>Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'
```

Det här kommandot hämtar den nycklar som heter MyKey från vaultnamed MyKeyVault och sparar en säkerhets kopia av den i en fil med namnet Backup. blob.

### Exempel 3: säkerhetskopiera en tidigare Hämtad nycklar till ett angivet fil namn och skriv över målfilen utan att fråga.
```
PS C:\>$key = Get-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\>Backup-AzureKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force
```

Det här kommandot skapar en säkerhets kopia av den nycklar som heter $key. Namn i valvet med namnet $key. VaultName till en fil med namnet Backup. blob, och överskriv sedan filen utan att skriva över den.

## MALLPARAMETRAR

### -Force
Skriv över den angivna filen om den finns

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Viktiga
Anger en tidigare Hämtad server som ska säkerhets kopie ras.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.KeyBundle
Parameter Sets: ByKey
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namn
Anger namnet på den som ska säkerhets kopie ras.

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases: KeyName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Utdatafil
Anger den utdatafil där reserv-BLOB lagras.
Om du inte anger den här parametern skapar den här cmdleten ett fil namn.
Om du anger namnet på en befintlig utdatafil slutförs inte åtgärden och returnerar ett fel meddelande om att säkerhets kopian redan finns.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
Anger namnet på det huvud valv som innehåller den säkerhets kopia du vill säkerhetskopiera.

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### Strängvärdet
Cmdleten returnerar sökvägen till utdatafilen med säkerhets kopian av nyckel.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzureKeyVaultKey](./Add-AzureKeyVaultKey.md)

[Get-AzureKeyVaultKey](./Get-AzureKeyVaultKey.md)

[Remove-AzureKeyVaultKey](./Remove-AzureKeyVaultKey.md)

[Återställ-AzureKeyVaultKey](./Restore-AzureKeyVaultKey.md)

