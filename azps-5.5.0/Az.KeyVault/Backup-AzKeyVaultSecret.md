---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
ms.openlocfilehash: a171f967a937873b85adcfca732987037e6db0a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226463"
---
# Backup-AzKeyVaultSecret

## SYNOPSIS
Backar upp en hemlig i ett nyckelvalv.

## SYNTAX

### BySecretName (standard)
```
Backup-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### BySecret
```
Backup-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Backup-AzKeyVaultSecret** säkerhetskopierar en viss hemligt i ett nyckelvalv genom att hämta och lagra den i en fil.
Om det finns flera versioner av den hemliga kopian inkluderas alla versioner i säkerhetskopian.
Eftersom det hämtade innehållet krypteras kan det inte användas utanför Azure-nyckelvalvet.
Du kan återställa en säkerhetskopierad hemligt till ett nyckelvalv i prenumerationen som den säkerhetskopierades från.
Vanliga anledningar till att använda den här cmdleten är:
- Du vill trycka på en kopia av hemligheten, så att du har en offlinekopia om du råkar ta bort hemligheten i nyckelvalvet av misstag.
- Du lade till en hemligt till ett nyckelvalv och vill nu klona hemligheten till en annan Azure-region, så att du kan använda den från alla förekomster av ditt distribuerade program. Använd cmdleten Backup-AzKeyVaultSecret för att hämta hemligheten i krypterat format och använd sedan cmdleten Restore-AzKeyVaultSecret och ange ett nyckelvalv i den andra regionen. (Observera att regionerna måste tillhöra samma geografi.)

## EXEMPEL

### Exempel 1: Backa upp en hemlig med ett automatiskt genererat filnamn
```powershell
PS C:\Users\username\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'

C:\Users\username\mykeyvault-mysecret-1527029447.01191
```

Det här kommandot hämtar hemligheten med namnet MySecret från nyckelvalvet MyKeyVault och sparar en säkerhetskopia av hemligheten till en fil som automatiskt namnges åt dig och visar filnamnet.

### Exempel 2: Backa upp en hemlig fil med ett visst filnamn och skriva över den befintliga filen utan att fråga
```powershell
PS C:\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

Det här kommandot hämtar hemligheten med namnet MySecret från nyckeln MyKeyVault och sparar en säkerhetskopia av hemligheten till en fil med namnet Backup.blob.

### Exempel 3: Back up a secret previously retrieved to a specified file name
```powershell
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\> Backup-AzKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

Det här kommandot använder $secret objektets valvnamn och namn för att hämta hemligheten och sparar säkerhetskopian i en fil som heter Backup.blob.

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
Frågar dig om bekräftelse innan du skriver över utdatafilen, om det finns en sådan.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Hemligt att säkerhetskopieras i, uppringd från utdata från ett hämtningssamtal.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: BySecret
Aliases: Secret

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Anger namnet på hemligheten som ska backa upp.

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases: SecretName

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
Anger namnet på nyckelvalvet som innehåller hemligheten som ska valv upp.

```yaml
Type: System.String
Parameter Sets: BySecretName
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem

## UTDATA

### System.String

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Set-AzKeyVaultSecret](./Set-AzKeyVaultSecret.md)

[Get-AzKeyVaultSecret](./Get-AzKeyVaultSecret.md)

[Remove-AzKeyVaultSecret](./Remove-AzKeyVaultSecret.md)

[Restore-AzKeyVaultSecret](./Restore-AzKeyVaultSecret.md)

