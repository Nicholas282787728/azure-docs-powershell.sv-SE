---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
ms.openlocfilehash: 51d322ea738a56e4b1fa24cccdb7bb59a6cd0d21
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214542"
---
# Backup-AzKeyVaultCertificate

## SYNOPSIS
Backar upp ett certifikat i ett nyckelvalv.

## SYNTAX

### ByCertificateName (Default)
```
Backup-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCertificate
```
Backup-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Backup-AzKeyVaultCertificate** säkerhetskopierar ett angivet certifikat i ett nyckelvalv genom att hämta det och lagra det i en fil.
Om certifikatet har flera versioner inkluderas alla versioner av certifikatet i säkerhetskopian.
Eftersom det hämtade innehållet krypteras kan det inte användas utanför Azure-nyckelvalvet.
Du kan återställa ett säkerhetskopierat certifikat till alla nyckelvalv i prenumerationen som det säkerhetskopierades från, så länge valvet är i samma Azure-geografi.
Vanliga anledningar till att använda den här cmdleten är: 
- Du vill behålla en offlinekopia av certifikatet om du tar bort originalet från valvet av misstag.
 
- Du har skapat ett certifikat med nyckelvalv och vill nu klona objektet till en annan Azure-region, så att du kan använda det från alla förekomster av det distribuerade programmet.
Använd cmdleten **Backup-AzKeyVaultCertificate** till att hämta certifikatet i krypterat format och sedan använda **cmdleten Restore-AzKeyVaultCertificate** och ange ett nyckelvalv i den andra regionen.

## EXEMPEL

### Exempel 1: Back up a certificate with an automatically generated file name
```powershell
PS C:\Users\username\> Backup-AzKeyVaultCertificate -VaultName 'mykeyvault' -Name 'mycert'

C:\Users\username\mykeyvault-mycert-1527029447.01191
```

Det här kommandot hämtar certifikatet med namnet MyCert från nyckelvalvet MyKeyVault och sparar en säkerhetskopia av certifikatet till en fil som namnges automatiskt åt dig och visar filnamnet.

### Exempel 2: Back up a certificate to a specified file name
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyCert' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

Det här kommandot hämtar certifikatet med namnet MyCert från nyckelvalvet MyKeyVault och sparar en säkerhetskopia av certifikatet till en fil som heter Backup.blob.

### Exempel 3: Back up a previously retrieved certificate to a specified file name, overwriting the destination file without prompting.
```powershell
PS C:\> $cert = Get-AzKeyVaultCertificate -VaultName 'MyKeyVault' -Name 'MyCert'
PS C:\> Backup-AzKeyVaultCertificate -Certificate $cert -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

Det här kommandot skapar en säkerhetskopia av certifikatet $cert. Namn i valvet med namnet $cert. VaultName till en fil med namnet Backup.blob, och skriver över filen så att den redan finns.

## PARAMETERS

### -DefaultProfile
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

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

### -InputObject
Hemligt att säkerhetskopieras i, uppringd från utdata från ett hämtningssamtal.

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

### -Name
Hemligt namn.
Cmdlet skapar FQDN för en hemlig från valv-namn, för närvarande vald miljö och hemligt namn.

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

### -OutputFile
Utdatafil.
Utdatafilen för att lagra säkerhetskopian av certifikatet.
Om det inte anges genereras ett standardfilnamn.

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
Valvnamn.
Cmdlet skapar FQDN för ett valv baserat på namnet och den valda miljön.

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

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem

## UTDATA

### System.String

## ANTECKNINGAR

## RELATERADE LÄNKAR
