---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F63769D6-9A31-4A67-972A-1E0428853C86
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88f61718e363a630b70519590025a6da80364aeb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093149"
---
# Start-AzureSqlDatabaseRecovery

## Sammanfattning
Initierar en återställnings förfrågan för en databas.

## FRÅGESYNTAXEN

### BySourceDatabaseName
```
Start-AzureSqlDatabaseRecovery -SourceServerName <String> -SourceDatabaseName <String>
 [-TargetServerName <String>] [-TargetDatabaseName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BySourceDatabaseObject
```
Start-AzureSqlDatabaseRecovery -SourceDatabase <RecoverableDatabase> [-TargetServerName <String>]
 [-TargetDatabaseName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Start-AzureSqlDatabaseRecovery** initierar en återställnings förfrågan för en Live eller avbruten databas.
Denna cmdlet stöder grundläggande återställning med den senaste tillgängliga säkerhets kopian av databasen.
Återställnings åtgärden skapar en ny databas.
Om du återställer en Live-databas på samma server måste du ange ett annat namn för den nya databasen.

Om du vill göra en tidpunkt för återställning av en databas kan du använda cmdleten **Start-AzureSqlDatabaseRestore** istället.

## BESKRIVS

### Exempel 1: Återställ en databas som har angetts som ett objekt
```
PS C:\> $Database = Get-AzureSqlRecoverableDatabase -ServerName "Server01" -DatabaseName "Database17" 
PS C:\> $Operation = Start-AzureSqlDatabaseRecovery -SourceDatabase $Database -TargetDatabaseName "DatabaseRestored"
```

Det första kommandot får ett databas objekt med cmdleten **Get-AzureSqlRecoverableDatabase** .
Kommandot lagrar objektet i $Database variabel.

Det andra kommandot återställer databasen som är lagrad i $Database.

### Exempel 2: Återställ en databas som anges efter namn
```
PS C:\> $Operation = Start-AzureSqlDatabaseRecovery -SourceServerName "Server01" -SourceDatabaseName "Database17" -TargetDatabaseName "DatabaseRestored"
```

Det här kommandot återställer en databas med hjälp av databas namnet.

## MALLPARAMETRAR

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

### -SourceDatabase
Anger det databas objekt som representerar databasen som denna cmdlet återställer.

```yaml
Type: RecoverableDatabase
Parameter Sets: BySourceDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SourceDatabaseName
Anger namnet på den databas som denna cmdlet återställer.

```yaml
Type: String
Parameter Sets: BySourceDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceServerName
Anger namnet på den server där käll databasen körs, eller som käll databasen kördes innan den togs bort.

```yaml
Type: String
Parameter Sets: BySourceDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetDatabaseName
Anger namnet på den återställda databasen.
Om käll databasen fortfarande är aktiv, för att återställa den till samma server, måste du ange ett namn som skiljer sig från käll databasens namn.

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

### -TargetServerName
Anger namnet på den server som du vill återställa en databas till.
Du kan återställa en databas till samma server eller till en annan server.

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

### Microsoft. WindowsAzure. Management. SQL. Models. RecoverableDatabase

## VÄRDEN

### Microsoft. WindowsAzure. Management. SQL. Models. RecoverDatabaseOperation

## ANMÄRKNINGAR
* Du måste använda certifikatbaserad inloggningsautentisering för att köra denna cmdlet. Kör följande kommandon på den dator där du kör denna cmdlet: 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## RELATERADE LÄNKAR

[Azure SQL-databas](https://azure.microsoft.com/en-us/services/sql-database/)

[Skapa begäran om databas återställning](https://msdn.microsoft.com/en-us/library/dn800986.aspx)

[Geo-replikering i Azure SQL Database](https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/)

[Åtgärder för Azure SQL-databaser](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlRecoverableDatabase](./Get-AzureSqlRecoverableDatabase.md)

[Start-AzureSqlDatabaseRestore](./Start-AzureSqlDatabaseRestore.md)


