---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 7427A101-9439-45B9-B72E-F8C2DA85E412
online version: ''
schema: 2.0.0
ms.openlocfilehash: c10ae808d105079b9739516bf9eaf316241b1b11
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099528"
---
# Get-AzureSqlDatabase

## Sammanfattning
Hämtar en eller flera databaser.

## FRÅGESYNTAXEN

### ByConnectionContext (standard)
```
Get-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> [-Database <Database>]
 [-DatabaseName <String>] [-RestorableDropped] [-RestorableDroppedDatabase <RestorableDroppedDatabase>]
 [-DatabaseDeletionDate <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByServerName
```
Get-AzureSqlDatabase -ServerName <String> [-Database <Database>] [-DatabaseName <String>] [-RestorableDropped]
 [-RestorableDroppedDatabase <RestorableDroppedDatabase>] [-DatabaseDeletionDate <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureSqlDatabase** returnerar en eller flera instanser av en Azure SQL-databas från en Azure SQL Database-Server.
Du kan ange den server som du vill använda för att skapa en Azure SQL Database Server-kontext som du skapar via cmdlet **New-AzureSqlDatabaseServerContext** .
Om du anger namnet på en Azure SQL-databas server används den aktuella Azure-prenumerations informationen för att autentisera begäran om att få åtkomst till servern.

Om du inte anger en databas returnerar cmdleten **Get-AzureSqlDatabase** alla databaser från den angivna servern.

Hämtar restorable tappade databaser:

Hämta restorable tappade databaser genom att använda parametern *RestorableDropped* .
Om du vill returnera alla restorable tappade databaser använder du parametern *RestorableDropped* utan *databasename* och *DatabaseDeletionDate*.
Om du vill returnera en viss restorable tappad databas använder du parametern *RestorableDropped* med parametrarna *databasename* och *DatabaseDeletionDate* .
När du hämtar en specifik restorable-avbruten databas med parametern *databasename* måste du också inkludera parametern *DatabaseDeletionDate* och det angivna *DatabaseDeletionDate* -värdet måste innehålla millisekunder för att matcha den önskade databasen.

Cmdleten **Get-AzureSqlDatabase** returnerar antingen alla restorable-förlorade databaser på en server eller en specifik databas som matchar både *databasename* och *DatabaseDeletionDate*.
Om du vill returnera restorable tappade databaser som uppfyller olika villkor, till exempel alla restorable-förlorade databaser med ett visst namn, måste du returnera alla restorable-förlorade databaser och sedan filtrera resultaten på klienten.

## BESKRIVS

### Exempel 1: Hämta alla databaser på en server
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y"
```

Det här kommandot hämtar alla databaser på servern som heter lpqd0zbr8y.

### Exempel 2: Hämta alla restorable tappade databaser på en server
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -RestorableDropped
```

Det här kommandot hämtar alla restorable tappade databaser på servern med namnet lpqd0zbr8y.

### Exempel 3: Hämta en databas från en server som anges av en anslutnings kontext
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
```

Det här kommandot hämtar databasen som heter Database01 från den server som anges av kontexten för anslutning $Context.

### Exempel 4: lagra ett databas objekt i en variabel
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
```

Det här kommandot hämtar databasen med namnet Database01 från servern med namnet lpqd0zbr8y.
Kommandot lagrar databasobjektet i variabeln $Database 01.

### Exempel 5: Hämta en restorable tappad databas
```
PS C:\> $DroppedDB = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01" -DatabaseDeletionDate "2012-11-09T22:59:43.000Z" -RestorableDropped
```

Det här kommandot hämtar den restorable tappade databasen med namnet Database01 som togs bort på 11/9/2012 från servern med namnet lpqd0zbr8y.
Det här kommandot lagrar resultatet i variabeln $DroppedDB.

### Exempel 6: Hämta alla restorable tappade databaser på en server och filtrera resultaten
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -RestorableDropped | Where-Object {$_.Name -eq "ContactDB"}
```

Det här kommandot hämtar alla restorable tappade databaser på servern med namnet lpqd0zbr8y och filtrerar sedan resultatet till de databaser som heter ContactDB.

## MALLPARAMETRAR

### -ConnectionContext
Anger den anslutnings kontext för en server som en databas ska hämtas från.

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Databas
Anger ett objekt som representerar databasen som hämtas av denna cmdlet.

```yaml
Type: Database
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseDeletionDate
Anger datum och tid för en borttagning.
Om du anger parametern *RestorableDropped* anger du den här parametern för att hämta en restorable-frånkopplad databas utifrån borttagnings datum och-tid.

Parametern *DatabaseDeletionDate* måste innehålla millisekunder för att matcha tiden för den önskade databasen.
Om du anger ett värde utan millisekunder hittas inte databasen.

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

### -DatabaseName
Anger namnet på den databas som cmdleten returnerar.

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
Anger att denna cmdlet returnerar *RestorableDroppedDatabase* -objekt i stället för *databas* objekt.
Du kan använda parametern *DatabaseDeletionDate* för att välja en specifik restorable-förlorad databas.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestorableDroppedDatabase
Anger ett objekt som representerar den restorable-släppta databasen som hämtas av denna cmdlet.

```yaml
Type: RestorableDroppedDatabase
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ServerName
Anger namnet på den server som innehåller databasen som hämtas av denna cmdlet.
Cmdleten använder det aktuella Azure-abonnemanget för att komma åt servern.

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Microsoft. WindowsAzure. kommandon. SqlDatabase. Services. Server. Database

### Microsoft. WindowsAzure. kommandon. SqlDatabase. Services. Server. RestorableDroppedDatabase

## VÄRDEN

### IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database\>
Denna cmdlet returnerar ett *databas* objekt om du inte anger parametern *RestorableDropped* .

### IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase\>
Denna cmdlet returnerar ett *RestorableDroppedDatabase* -objekt om du anger parametern *RestorableDropped* .

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Azure SQL-databas](https://azure.microsoft.com/en-us/services/sql-database/)

[Åtgärder för Azure SQL-databaser](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[New-AzureSqlDatabase](./New-AzureSqlDatabase.md)

[New-AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)

[Remove-AzureSqlDatabase](./Remove-AzureSqlDatabase.md)

[Set-AzureSqlDatabase](./Set-AzureSqlDatabase.md)


