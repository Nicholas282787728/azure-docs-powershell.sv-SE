---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: c01d07f9408804b229921394c24e444b2a4deb8b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237591"
---
# Backup-AzKeyVaultManagedStorageAccount

## SYNOPSIS
Backar upp ett KeyVault-hanterat lagringskonto.

## SYNTAX

### ByStorageAccountName (standard)
```
Backup-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByStorageAccount
```
Backup-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-OutputFile] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Backup-AzKeyVaultManagedStorageAccount** säkerhetskopierar ett visst hanterat lagringskonto i ett nyckelvalv genom att hämta och lagra det i en fil.
Eftersom det hämtade innehållet krypteras kan det inte användas utanför Azure-nyckelvalvet.
Du kan återställa ett säkerhetskopierat lagringskonto till alla viktiga valv i prenumerationen som det säkerhetskopierades från, så länge valvet är i samma Azure-geografi.
Vanliga anledningar till att använda den här cmdleten är: 
- Du vill behålla en offlinekopia av lagringskontot om du råkar ta bort originalet från valvet.
 
- Du har skapat ett hanterat lagringskonto med hjälp av nyckelvalv och vill nu klona objektet till en annan Azure-region, så att du kan använda det från alla förekomster av ditt distribuerade program.
Använd cmdleten **Backup-AzKeyVaultManagedStorageAccount** för att hämta kontot för hanterad lagring i krypterat format och använd sedan cmdleten **Restore-AzKeyVaultManagedStorageAccount** och ange ett nyckelvalv i den andra regionen.

## EXEMPEL

### Exempel 1: Back up a managed storage account with an automatically generated file name
```powershell
PS C:\Users\username\> Backup-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'

C:\Users\username\mykeyvault-mymsak-1527029447.01191
```

Det här kommandot hämtar det hanterade lagringskontot med namnet MyMSAK från nyckelvalvet MyKeyVault och sparar en säkerhetskopia av det hanterade lagringskontot till en fil som namnges automatiskt åt dig och visar filnamnet.

### Exempel 2: Back up a managed storage account to a specified file name
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyMSAK' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

Det här kommandot hämtar det hanterade lagringskontot med namnet MyMSAK från nyckelvalvet MyKeyVault och sparar en säkerhetskopia av det hanterade lagringskontot till en fil med namnet Backup.blob.

### Exempel 3: Back up a previously retrieved managed storage account to a specified file name, overwriting the destination file without prompting.
```powershell
PS C:\> $msak = Get-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'
PS C:\> Backup-AzKeyVaultManagedStorageAccount -StorageAccount $msak -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

Med det här kommandot skapas en säkerhetskopia av det hanterade lagringskontot $msak. Namn i valvet med namnet $msak. VaultName till en fil med namnet Backup.blob, och skriver över filen så att den redan finns.

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
Lagringskontopaket som ska säkerhetskopieras, pipelines in från utdata från ett hämtningssamtal.

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

### -Name
Hemligt namn.
Cmdlet skapar FQDN för en hemlig från valv-namn, för närvarande vald miljö och hemligt namn.

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

### -OutputFile
Utdatafil.
Den utdatafil där du kan spara säkerhetskopian av lagringskontot.
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
Parameter Sets: ByStorageAccountName
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

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem

## UTDATA

### System.String

## ANTECKNINGAR

## RELATERADE LÄNKAR
