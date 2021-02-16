---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautobackupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: ecff02643dd6d0e017d56af01792a06dc7b8d998
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398282"
---
# New-AzVMSqlServerAutoBackupConfig

## SYNOPSIS
Skapar ett konfigurationsobjekt för automatisk säkerhetskopiering av SQL Server.

## SYNTAX

### StorageUriSqlServerAutoBackup (standard)
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable]
 [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption] [[-CertificatePassword] <SecureString>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### StorageContextSqlServerAutoBackup
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable]
 [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption] [[-CertificatePassword] <SecureString>]
 [[-StorageContext] <IStorageContext>] [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs]
 [-BackupScheduleType <String>] [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>]
 [-FullBackupWindowInHours <Int32>] [-LogBackupFrequencyInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **New-AzVMSqlServerAutoBackupConfig** skapar ett konfigurationsobjekt för automatisk säkerhetskopiering av SQL Server.

## EXEMPEL

### Exempel 1: Skapa en automatisk säkerhetskopieringskonfiguration med lagrings-URI och kontonyckel
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

Med det här kommandot skapas ett automatiskt konfigurationsobjekt för säkerhetskopiering genom att lagrings-URI och kontonyckel anges.
Automatisk säkerhetskopiering aktiveras och automatisk säkerhetskopiering sparas i 10 dagar.
Kommandot lagrar resultatet i den $AutoBackupConfig variabeln.
Du kan ange det här konfigurationsobjektet för andra cmdlets, till exempel Set-AzVMSqlServerExtension cmdlet.

### Exempel 2: Skapa en automatisk säkerhetskopieringskonfiguration med hjälp av lagringskontext
```
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

Det första kommandot skapar ett lagringskontext och lagrar det sedan i $StorageContext variabeln.
Mer information finns i New-AzureStorageContext.

Det andra kommandot skapar ett automatiskt konfigurationsobjekt för säkerhetskopiering genom att ange lagringskontexten i $StorageContext.
Automatisk säkerhetskopiering aktiveras och automatisk säkerhetskopiering sparas i 10 dagar.

### Exempel 3: Skapa en automatisk säkerhetskopieringskonfiguration med lagringskontext med kryptering och lösenord
```
PS C:\> $StorageContext = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

Med det här kommandot skapas och lagras ett konfigurationsobjekt för automatisk säkerhetskopiering.
Kommandot anger vilken lagringskontext som skapades i ett tidigare exempel.
Kommandot aktiverar kryptering med lösenord.
Lösenordet lagrades tidigare som en säker sträng i den $CertificatePassword variabeln.
Om du vill skapa en säker sträng använder du ConvertTo-SecureString-cmdleten.

## PARAMETERS

### -BackupScheduleType
Schematyp för säkerhetskopiering, manuellt eller automatiskt

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Manual, Automated

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -BackupSystemDbs
Säkerhetskopiera systemdatabaser

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CertificatePassword
Anger ett lösenord för att kryptera certifikatet som används för att utföra krypterade säkerhetskopior i SQL Server.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifterna, kontot, klientorganisationen och prenumerationen som används för kommunikation med Azure.

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

### -Enable
Anger att automatisk säkerhetskopiering av den virtuella SQL Server-datorn är aktiverad.
Om du anger den här parametern skapar automatisk säkerhetskopiering ett säkerhetskopieringsschema för alla aktuella och nya databaser.
Det här uppdaterar inställningarna för hanterad säkerhetskopiering så att schemat följer det här schemat.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnableEncryption
Anger att den här cmdleten aktiverar kryptering.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FullBackupFrequency
Frekvens för fullständig säkerhetskopiering i Sql Server, dagligen eller veckovis

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Daily, Weekly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FullBackupStartHour
Timme på dagen (0–23) då fullständig säkerhetskopiering av Sql Server ska starta

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FullBackupWindowInHours
Fönstret Fullständig säkerhetskopiering i Sql Server på flera timmar

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LogBackupFrequencyInMinutes
Säkerhetskopieringsfrekvens för Sql Server-logg var 1:60:e minut

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på resursgruppen för den virtuella datorn.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RetentionPeriodInDays
Anger antalet dagar som en säkerhetskopia ska sparas.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageContext
Anger vilket lagringskonto som ska användas för att lagra säkerhetskopior.
Om du vill **hämta ett AzureStorageContext-objekt** använder du New-AzureStorageContext-cmdleten.
Standardinställningen är det lagringskonto som är kopplat till den virtuella SQL Server-datorn.

```yaml
Type: IStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageKey
Anger lagringsnyckeln för blob-lagringskontot.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageUri
Anger URI (Uniform Resource Identifier) för blob-lagringskontot.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### Ingen
Den här cmdleten accepterar inte några indata.

## UTDATA

### Microsoft.Azure.Commands.Compute.AutoBackupSettings

## ANTECKNINGAR

## RELATERADE LÄNKAR

[New-AzureVMSqlServerAutoPatchingConfig](./New-AzVMSqlServerAutoPatchingConfig.md)

[Set-AzVMSqlServerExtension](./Set-AzVMSqlServerExtension.md)


