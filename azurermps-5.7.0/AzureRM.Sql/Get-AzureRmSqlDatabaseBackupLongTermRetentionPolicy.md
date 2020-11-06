---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 0f43956dfa29dac2d7c6ca1869716400b8adad35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581952"
---
# Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy

## Sammanfattning
Hämtar en bevarande princip för en tids krävande databas.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-Current] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** hämtar den långsiktiga bevarande principen för databasen.
Principen är en Azure Backup-resurs som används för att definiera säkerhets kopierings lagrings princip.

## BESKRIVS

### Exempel 1: hämta den senaste versionen av princip för bevarande
```powershell
PS C:\> Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -Current


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P2W
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

Med det här kommandot får du den senaste versionen av bevarande principen för lång sikt för database01

### Exempel 2: hämta den bakåtkompatibla versionen av principen för långsiktigt bevarande
```powershell
PS C:\> Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        :
MonthlyRetention                       :
YearlyRetention                        :
WeekOfYear                             :
State                                  : Enabled
RecoveryServicesBackupPolicyResourceId : /subscriptions/4f2b42fc-4fc3-fd41-8ab8-5a382d8b30df/resourceGroups/resourcegroup01/providers/MicrosoftRecoveryServices/vaults/vault01/backupPolicies/policy01
Location                               : Southeast Asia
```

Med det här kommandot får du den bakåtkompatibla versionen av den långsiktiga princip inställningen för database01

## MALLPARAMETRAR

### -Aktuell
Om det inte anges returnerar kommandot den bakåtkompatibla princip informationen för behållnings perioden.
Annars returnerar kommandot den aktuella versionen av en bevarande princip för längre tid.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseName
Namnet på den Azure SQL-databas du vill använda.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

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

### -ResourceGroupName
Namnet på resurs gruppen.

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

### -ServerName
Namnet på den Azure SQL Server-databas som databasen finns i.

```yaml
Type: String
Parameter Sets: (All)
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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.
Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen
Denna cmdlet accepterar inte indata.

## VÄRDEN

### Microsoft. Azure. commands. SQL. backup. Model. AzureSqlDatabaseBackupLongTermRetentionPolicyModel

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmSqlDatabaseLongTermRetentionBackup](./Get-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[Remove-AzureRmSqlDatabaseLongTermRetentionBackup](./Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy](./Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[Dokumentation för SQL-databaser](https://docs.microsoft.com/azure/sql-database/)
