---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
ms.openlocfilehash: 88decaffa736f015b8e65aa1217eab4899b07c7c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214518"
---
# Backup-AzKeyVaultKey

## SYNOPSIS
Backar upp en nyckel i ett nyckelvalv.

## SYNTAX

### ByKeyName (standard)
```
Backup-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmByKeyName
```
Backup-AzKeyVaultKey -HsmName <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByKey
```
Backup-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Backup-AzKeyVaultKey** säkerhetskopierar en viss nyckel i ett nyckelvalv genom att hämta den och lagra den i en fil.
Om det finns flera versioner av nyckeln ingår alla versioner i säkerhetskopian.
Eftersom det hämtade innehållet krypteras kan det inte användas utanför Azure-nyckelvalvet.
Du kan återställa en säkerhetskopierad nyckel till ett nyckelvalv i prenumerationen som den säkerhetskopierades från.
Vanliga anledningar till att använda den här cmdleten är: 
- Du vill escrow en kopia av nyckeln, så att du har en offlinekopia om du skulle råka ta bort nyckeln i nyckelvalvet.
 
- Du har skapat en nyckel med hjälp av nyckelvalv och vill nu klona nyckeln till en annan Azure-region, så att du kan använda den från alla förekomster av ditt distribuerade program.
Använd cmdleten **Backup-AzKeyVaultKey** för att hämta nyckeln i krypterat format och använd sedan cmdleten Restore-AzKeyVaultKey och ange ett nyckelvalv i den andra regionen.

## EXEMPEL

### Exempel 1: Backa upp en nyckel med ett automatiskt genererat filnamn
```powershell
PS C:\Users\username\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'

C:\Users\username\mykeyvault-mykey-1527029447.01191
```

Det här kommandot hämtar nyckeln MyKey från nyckelvalvet MyKeyVault och sparar en säkerhetskopia av nyckeln i en fil som automatiskt namnges åt dig och visar filnamnet.

### Exempel 2: Backa upp en nyckel till ett angivet filnamn
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

Det här kommandot hämtar nyckeln med namnet MyKey från nyckelvalvnamnet MyKeyVault och sparar en säkerhetskopia av nyckeln till en fil som heter Backup.blob.

### Exempel 3: Back up a previously retrieved key to a specified file name, overwriting the destination file without prompting.
```powershell
PS C:\> $key = Get-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\> Backup-AzKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

Med det här kommandot skapas en säkerhetskopia av nyckeln $key. Namn i valvet med namnet $key. VaultName till en fil med namnet Backup.blob, som tyst skriver över filen om den redan finns.

## PARAMETERS

### -DefaultProfile
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure

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
Skriva över den givna filen om den finns

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

### -HsmName
HSM-namn. Cmdlet skapar FQDN för en hanterad HSM baserat på namnet och den valda miljön.

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

### -InputObject
Nyckelpaket för att backa upp, uppringda från utdata från ett hämtningssamtal.

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

### -Name
Anger namnet på nyckeln som ska backa upp.

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

### -OutputFile
Anger den utdatafil där blob för säkerhetskopian lagras.
Om du inte anger den här parametern genererar cmdleten ett filnamn åt dig.
Om du anger namnet på en befintlig utdatafil slutförs inte åtgärden och ett felmeddelande om att säkerhetskopian redan finns returneras.

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
Anger namnet på nyckelvalvet som innehåller nyckeln som ska backas upp.

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

### -Bekräfta
Frågar dig om bekräftelse innan du kör cmdleten.

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
Visar vad som skulle hända om cmdleten körs.
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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem

## UTDATA

### System.String

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Add-AzKeyVaultKey](./Add-AzKeyVaultKey.md)

[Get-AzKeyVaultKey](./Get-AzKeyVaultKey.md)

[Remove-AzKeyVaultKey](./Remove-AzKeyVaultKey.md)

[Restore-AzKeyVaultKey](./Restore-AzKeyVaultKey.md)

