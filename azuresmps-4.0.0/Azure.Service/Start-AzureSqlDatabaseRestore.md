---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 383F36F3-3F52-4FC3-99F7-831096E6037D
online version: ''
schema: 2.0.0
ms.openlocfilehash: ff7c7cd50b06a4110b6af12611f3d91eaedfd227
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093152"
---
# Start-AzureSqlDatabaseRestore

## Sammanfattning
Utför en tidpunkt för återställning av en databas.

## FRÅGESYNTAXEN

### BySourceDatabaseObject
```
Start-AzureSqlDatabaseRestore [-SourceServerName <String>] -SourceDatabase <Database>
 [-TargetServerName <String>] -TargetDatabaseName <String> [-PointInTime <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BySourceRestorableDroppedDatabaseObject
```
Start-AzureSqlDatabaseRestore [-SourceServerName <String>]
 -SourceRestorableDroppedDatabase <RestorableDroppedDatabase> [-TargetServerName <String>]
 -TargetDatabaseName <String> [-PointInTime <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BySourceDatabaseName
```
Start-AzureSqlDatabaseRestore -SourceServerName <String> -SourceDatabaseName <String>
 [-TargetServerName <String>] -TargetDatabaseName <String> [-PointInTime <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BySourceRestorableDroppedDatabaseName
```
Start-AzureSqlDatabaseRestore -SourceServerName <String> -SourceDatabaseName <String>
 -SourceDatabaseDeletionDate <DateTime> [-TargetServerName <String>] [-RestorableDropped]
 -TargetDatabaseName <String> [-PointInTime <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Start-AzureSqlDatabaseRestore** utför en tidpunkt för återställning av en bas-, standard-eller Premium-databas.
Azure SQL Database behåller grundläggande säkerhets kopiering av databaser 7 dagar, standard i 14 dagar och Premium för 35 dagar.
Återställnings åtgärden skapar en ny databas.
Om käll databasen inte tas bort måste *SourceDatabaseName* -och *TargetDatabaseName* -parametern ha olika värden.

Azure SQL Database stöder för närvarande inte återställning mellan servrar.
Namnet på käll-och mål servern måste vara samma.

## BESKRIVS

### Exempel 1: återställa en databas som angetts som ett objekt till en tidpunkt
```
PS C:\> $Database = Get-AzureSqlDatabase -ServerName "Server01" -DatabaseName "Database17" 
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceDatabase $Database -TargetDatabaseName "DatabaseRestored" -PointInTime "2013-01-01 06:00:00"
```

Det första kommandot får ett databas objekt för databasen som heter Database17 på servern Server01 och lagrar det sedan i $Database variabel.

Det andra kommandot återställer databasen till en viss tidpunkt.
Kommandot anger namnet på den nya databasen.

### Exempel 2: återställa en databas som anges efter namn till en tidpunkt
```
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceServerName "Server01" -SourceDatabaseName "Database17" -TargetDatabaseName "DatabaseRestored" -PointInTime "2013-01-01 06:00:00"
```

Det här kommandot återställer databasen med namnet Database17 till en viss tidpunkt.
Kommandot anger namnet på den nya databasen.

### Exempel 3: återställa en borttagen databas som angetts som ett objekt till en tidpunkt
```
PS C:\> $Database = Get-AzureSqlDatabase -RestorableDropped -ServerName "Server01" -DatabaseName "Database01" -DatabaseDeletionDate "2012-11-09T22:59:43.000Z" 
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceRestorableDroppedDatabase $Database -TargetDatabaseName "DroppedDatabaseRestored"
```

Det första kommandot får ett databas objekt för databasen som heter Database01 på den server som heter Server01.
Kommandot anger parametern *RestorableDropped* .
Därför får cmdleten restorable tappad databas den angivna återställnings punkten.
Kommandot lagrar databasobjektet i $Database variabel.

Det andra kommandot återställer den avbrutna databasen som anges av $Database.
Kommandot anger namnet på den nya databasen.

## MALLPARAMETRAR

### -PointInTime
Anger återställnings punkten som databasen ska återställas till.
När återställningen är slutförd återställs databasen till den status den hade vid det datum och den tid som den här parametern anger.
För en Live-databas som används som standard till den aktuella tiden och för en borttagen databas använder denna cmdlet den tid då databasen släpptes.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Anger den Azure-profil från vilken denna cmdlet läser.
Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestorableDropped
Anger att den här cmdleten återställer en restorable tappad databas.

```yaml
Type: SwitchParameter
Parameter Sets: BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceDatabase
Anger namnet på den databas som denna cmdlet återställer.

```yaml
Type: Database
Parameter Sets: BySourceDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SourceDatabaseDeletionDate
Anger datum och tid när databasen togs bort.
Du måste inkludera millisekunder om du anger tiden för att matcha den faktiska borttagnings tiden för databasen.

```yaml
Type: DateTime
Parameter Sets: BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceDatabaseName
Anger namnet på den Live-databas som denna cmdlet återställer.

```yaml
Type: String
Parameter Sets: BySourceDatabaseName, BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceRestorableDroppedDatabase
Anger ett objekt som representerar den restorable-släppta databasen som lagras i den här cmdleten.
För att få ett **RestorableDroppedDatabase** -objekt, Använd cmdleten Get-AzureSqlDatabase och ange parametern *RestorableDropped* .

```yaml
Type: RestorableDroppedDatabase
Parameter Sets: BySourceRestorableDroppedDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SourceServerName
Anger namnet på den server där käll databasen körs, eller som käll databasen kördes innan den togs bort.

```yaml
Type: String
Parameter Sets: BySourceDatabaseObject, BySourceRestorableDroppedDatabaseObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: BySourceDatabaseName, BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetDatabaseName
Anger namnet på den nya databasen som återställnings åtgärden skapar.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetServerName
Anger namnet på den server där denna cmdlet återställer databasen.

Azure SQL Database stöder för närvarande inte återställning mellan servrar.
Namnet på käll-och mål servern måste vara samma.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Microsoft. WindowsAzure. kommandon. SqlDatabase. Services. Server. RestorableDroppedDatabase

### Microsoft. WindowsAzure. kommandon. SqlDatabase. Services. Server. Database

## VÄRDEN

### Microsoft. WindowsAzure. kommandon. SqlDatabase. Services. Server. RestoreDatabaseOperation

## ANMÄRKNINGAR
* Du måste använda certifikatbaserad inloggningsautentisering för att köra denna cmdlet. Kör följande kommandon på den dator där kör denna cmdlet: 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## RELATERADE LÄNKAR

[Azure SQL-databas](https://azure.microsoft.com/en-us/services/sql-database/)

[Skapa en begäran om databas återställning](https://msdn.microsoft.com/en-us/library/dn509571.aspx)

[Åtgärder för Azure SQL-databaser](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)


