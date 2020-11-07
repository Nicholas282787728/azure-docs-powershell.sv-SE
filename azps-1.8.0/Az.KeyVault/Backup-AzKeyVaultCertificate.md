---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
ms.openlocfilehash: 0c92dbea0127db82a1b1f4605cd581f31c872a57
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916365"
---
# Backup-AzKeyVaultCertificate

## Sammanfattning
Säkerhetskopierar ett certifikat i ett nyckelord.

## FRÅGESYNTAXEN

### ByCertificateName (standard)
```
Backup-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCertificate
```
Backup-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Genom **säkerhets kopiering-AzKeyVaultCertificate** cmdlet säkerhets kopie ras ett angivet certifikat i ett nyckeltal genom att det laddas ned och lagras i en fil.
Om certifikatet har flera versioner kommer alla dess versioner att ingå i säkerhets kopian.
Eftersom det hämtade innehållet är krypterat kan det inte användas utanför Azure Key Vault.
Du kan återställa ett säkerhetskopierat certifikat till ett huvud valv i det abonnemang som det säkerhetskopierades från, så länge valvet finns i samma Azure geography.
Vanliga skäl till att använda denna cmdlet är: 
- Om du vill behålla en offlinekopia av certifikatet ifall du råkar ta bort originalet från valvet.
 
- Du har skapat ett certifikat med hjälp av viktiga valv och vill nu klona objektet till ett annat Azure-område, så att du kan använda det från alla instanser av det distribuerade programmet.
Använd **säkerhets kopierings-AzKeyVaultCertificate** cmdlet för att hämta certifikatet i krypterat format och sedan använda cmdleten **restore-AzKeyVaultCertificate** och ange ett nyckeltal i den andra regionen.

## BESKRIVS

### Exempel 1: säkerhetskopiera ett certifikat med ett automatiskt genererat fil namn
```powershell
PS C:\Users\username\> Backup-AzKeyVaultCertificate -VaultName 'mykeyvault' -Name 'mycert'

C:\Users\username\mykeyvault-mycert-1527029447.01191
```

Det här kommandot hämtar certifikatet med namnet mina cert från det viktiga valvet som heter MyKeyVault och sparar en säkerhets kopia av certifikatet i en fil som automatiskt namnges för dig och visar fil namnet.

### Exempel 2: säkerhetskopiera ett certifikat till ett angivet fil namn
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyCert' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

Det här kommandot hämtar certifikatet med namnet mina cert från det nyckelord som heter MyKeyVault och sparar en säkerhets kopia av certifikatet i en fil med namnet Backup. blob.

### Exempel 3: säkerhetskopiera ett tidigare hämtat certifikat till ett angivet fil namn och skriv över målfilen utan att fråga.
```powershell
PS C:\> $cert = Get-AzKeyVaultCertificate -VaultName 'MyKeyVault' -Name 'MyCert'
PS C:\> Backup-AzKeyVaultCertificate -Certificate $cert -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

Det här kommandot skapar en säkerhets kopia av certifikatet med namnet $cert. Namn i valvet med namnet $cert. VaultName till en fil med namnet Backup. blob, och överskriv sedan filen utan att skriva över den.

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

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
Hemlighet som ska säkerhets kopie ras, från utdata från ett samtal.

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

### -Namn
Hemligt namn.
Cmdlet konstruerar FQDN för en hemlighet från valv namn, för närvarande valt miljö och hemligt namn.

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

### -Utdatafil
Utdatafil.
Utdatafil som säkerhetskopierar certifikatet.
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
Parameter Sets: ByCertificateName
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

### Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificateIdentityItem

## VÄRDEN

### System. String

## ANMÄRKNINGAR

## RELATERADE LÄNKAR
