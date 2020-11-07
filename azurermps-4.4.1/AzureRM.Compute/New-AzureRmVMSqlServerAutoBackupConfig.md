---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
Module Name: Azure
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: 2617ca54050f6a37fcc5714fe80e2f2d50e33e40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758128"
---
# New-AzureVMSqlServerAutoBackupConfig

## Sammanfattning
Skapar ett konfigurations objekt för automatisk säkerhets kopiering av SQL Server.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### StorageUriSqlServerAutoBackup (standard)
```
New-AzureVMSqlServerAutoBackupConfig [-Enable] [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption]
 [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>]
 [-BackupSystemDbs] [-BackupScheduleType <String>] [-FullBackupFrequency <String>]
 [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>] [-LogBackupFrequencyInMinutes <Int32>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### StorageContextSqlServerAutoBackup
```
New-AzureVMSqlServerAutoBackupConfig [-Enable] [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption]
 [[-CertificatePassword] <SecureString>] [[-StorageContext] <IStorageContext>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureVMSqlServerAutoBackupConfig** skapar ett konfigurations objekt för automatisk säkerhets kopiering av SQL Server.

## BESKRIVS

### Exempel 1: skapa en automatisk säkerhets kopierings konfiguration med lagrings-URI och konto nycklar
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

Det här kommandot skapar ett automatiskt konfigurations objekt för säkerhets kopior genom att ange lagrings-URI och konto nycklar.
Automatisk säkerhets kopiering är aktive rad och automatisk säkerhets kopiering sparas i 10 dagar.
Resultatet sparas i $AutoBackupConfig variabel.
Du kan ange det här konfigurationsobjektet för andra cmdlets, till exempel Set-AzureRmVMSqlServerExtension cmdlet.

### Exempel 2: skapa en automatisk säkerhets kopierings konfiguration med lagrings kontext
```
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

Det första kommandot skapar en lagrings kontext och lagrar den sedan i $StorageContext variabel.
Mer information finns i New-AzureStorageContext.

Det andra kommandot skapar ett automatiskt konfigurations objekt genom att ange lagrings kontexten i $StorageContext.
Automatisk säkerhets kopiering är aktive rad och automatisk säkerhets kopiering sparas i 10 dagar.

### Exempel 3: skapa en automatisk säkerhets kopierings konfiguration med lagrings kontext med kryptering och lösen ord
```
PS C:\> $StorageContext = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

Det här kommandot skapar och lagrar ett automatiskt konfigurations objekt för säkerhets kopiering.
Kommandot anger den lagrings kontext som skapades i ett tidigare exempel.
Kommandot aktiverar kryptering med lösen ord.
Lösen ordet har sparats som en säker sträng i $CertificatePassword variabel.
Om du vill skapa en skyddad sträng använder du ConvertTo-SecureString cmdleten.

## MALLPARAMETRAR

### -Aktivera
Anger att automatisk säkerhets kopiering för den virtuella SQL Server-datorn är aktive rad.
Om du anger den här parametern ställer automatisk säkerhets kopiering ett schema för säkerhets kopiering för alla befintliga och nya databaser.
Då uppdateras de hanterade säkerhets kopierings inställningarna efter detta schema.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RetentionPeriodInDays
Anger antalet dagar som en säkerhets kopia ska behållas.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnableEncryption
Anger att denna cmdlet aktiverar kryptering.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CertificatePassword
Anger ett lösen ord för att kryptera certifikatet som används för att utföra SQL Server-krypterade säkerhets kopieringar.

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageUri
Anger URI (Uniform Resource Identifier) för Blob Storage-kontot.

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageKey
Anger lagrings Key för Blob Storage-kontot.

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profil
Anger den Azure-profil från vilken denna cmdlet läser. Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.

```yaml
Type: Microsoft.WindowsAzure.Commands.Utilities.Common.AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationAction
@ {Text =}

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
@ {Text =}

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageContext
Anger det lagrings konto som ska användas för att lagra säkerhets kopior.
Använd New-AzureStorageContext cmdlet för att få ett **AzureStorageContext** -objekt.
Standardvärdet är det lagrings konto som är kopplat till den virtuella SQL Server-datorn.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -BackupScheduleType
Schema typ för säkerhets kopiering, manuell eller automatisk

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -BackupSystemDbs
Säkerhetskopiera system databaser

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FullBackupFrequency
Frekvens för fullständig säkerhets kopiering av SQL Server, dag eller vecka

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FullBackupStartHour
Timme på dagen (0-23) när fullständig säkerhets kopiering av SQL Server startar

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FullBackupWindowInHours
Fönstret full säkerhets kopiering i timmar i SQL Server

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LogBackupFrequencyInMinutes
Säkerhets kopierings frekvens för SQL Server-loggning, en gång var 1-60 minuter

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzureVMSqlServerAutoPatchingConfig](./New-AzureVMSqlServerAutoPatchingConfig.md)

[Set-AzureRmVMSqlServerExtension](./Set-AzureRMVMSqlServerExtension.md)


