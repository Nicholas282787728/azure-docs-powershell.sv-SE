---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7F07494-FBCA-4A77-92BF-E0A2D7ACCD21
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc350cdf117ebbf72b023f64895f4c563e73566b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099075"
---
# Start-AzureSqlDatabaseCopy

## Sammanfattning
Startar en kopiering av en Azure SQL-databas.

## FRÅGESYNTAXEN

### ByInputObject
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByInputObjectContinuous
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDatabaseName
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDatabaseNameContinuous
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Start-AzureSqlDatabaseCopy** startar en kopiering en gång eller en kontinuerlig kopiering av en specifik Azure SQL-databas.
Denna cmdlet är inte transaktionell.

Den ursprungliga databasen är käll databasen.
Kopian är den sekundära eller mål databasen.
För en kontinuerlig kopiering kan käll-och mål databaserna inte finnas på samma server och servrar som är värdar för käll-och mål databaserna måste ingå i samma prenumeration.

Om du inte anger parametern *ContinuousCopy* skapar denna cmdlet en en kopia av käll databasen.
När svaret tas emot kan operationen fortfarande fortsätta.
Du kan övervaka åtgärden med hjälp av Get-AzureSqlDatabaseCopy eller Get-AzureSqlDatabaseOperation cmdlet.

Om du anger *ContinuousCopy* skapar denna cmdlet en kontinuerlig kopia av käll databasen.
När svaret tas emot behandlas åtgärden.
Du kan övervaka åtgärden genom att använda **Get-AzureSqlDatabaseCopy** eller **Get-AzureSqlDatabaseOperation**.

Du kan skapa en kontinuerlig kopia som en online-eller frånkopplad databas.
Den kontinuerliga kopian online används för att konfigurera Active Geo-Replication för Azure SQL Database https://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/ .
Den kontinuerliga kopian offline används för att konfigurera standard Geo-Replication för Azure SQL Database https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/ .

## BESKRIVS

### Exempel 1: tidsplanera en kontinuerlig kopia av en databas
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy
```

Det här kommandot schemalägger en kontinuerlig kopia av databasen order på den server som heter lpqd0zbr8y.
Kommandot skapar en mål databas på den server som heter bk0b8kf658.

### Exempel 2: skapa en enstaka kopia på samma server
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerDatabase "OrdersCopy"
```

Det här kommandot skapar en enstaka kopia av databasen order på den server som heter lpqd0zbr8y.
Kommandot skapar en kopia med namnet OrdersCopy på samma server.

### Exempel 3: schemalägga en kontinuerlig kopia av en offlinedatabas
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy -OfflineSecondary
```

Det här kommandot schemalägger en kontinuerlig kopia av databasen order på den server som heter lpqd0zbr8y.
Det här kommandot skapar en offlinedatabas för mål på servern med namnet bk0b8kf658.

## MALLPARAMETRAR

### -ContinuousCopy
Visar att databas kopian kommer att vara en kopia (en replik databas).
Kontinuerlig kopiering stöds inte på samma server.
Om den här parametern inte anges utförs en kopiering i taget.
För en enstaka kopia måste käll-och partner databaserna finnas på samma server.

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Databas
Anger ett objekt som representerar käll-Azure SQL-databasen.
Den här parametern accepterar pipeline-inmatning.

```yaml
Type: Database
Parameter Sets: ByInputObject, ByInputObjectContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
Anger namnet på käll databasen.

```yaml
Type: String
Parameter Sets: ByDatabaseName, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Tvingar kommandot att köras utan att fråga efter bekräftelse.

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

### -OfflineSecondary
Anger att en kontinuerlig kopia är en passiv kopia i stället för en aktiv kopia.
Om käll databasen är en vanlig versions databas är den här parametern obligatorisk.
Om du anger den här parametern måste du också ange *ContinuousCopy* .

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerDatabase
Anger namnet på mål databasen.
Om du anger parametern *ContinuousCopy* måste värdet för *PartnerDatabase* matcha namnet på käll databasen.
Om du inte anger *ContinuousCopy* måste du ange ett namn för mål databasen, som kan skilja sig från käll databasens namn.

```yaml
Type: String
Parameter Sets: ByInputObject, ByDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerServer
Anger namnet på den server som är värd för mål databasen.
Den här servern måste finnas i samma Azure-abonnemang som käll databas servern.

```yaml
Type: String
Parameter Sets: ByInputObject, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: True
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

### -ServerName
Anger namnet på den server där käll databasen finns.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Microsoft. WindowsAzure. kommandon. SqlDatabase. Services. Server. Database

## VÄRDEN

### Microsoft. WindowsAzure. kommandon. SqlDatabase. Model. DatabaseCopy

## ANMÄRKNINGAR
* Verifiera: den här cmdleten kräver certifikatbaserad identifiering. Ett exempel på hur certifikatbaserad identifiering används för att ange aktuell prenumeration finns i New-AzureSqlDatabaseServerContext cmdlet.
* Övervakning: Använd cmdleten **Get-AzureSqlDatabaseCopy** för att kontrol lera status för en eller flera kontinuerliga kopior som är aktiva på servern. Använd cmdleten **Get-AzureSqlDatabaseOperation** för att kontrol lera status för åtgärderna på både källa och mål för den kontinuerliga kopierings relationen.

## RELATERADE LÄNKAR

[Azure SQL-databas](https://azure.microsoft.com/en-us/services/sql-database/)

[Åtgärder för Azure SQL-databaser](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Starta databas kopiering](https://msdn.microsoft.com/en-us/library/azure/dn509576.aspx)

[Azure SQL-databas-cmdletar](./Azure.SQLDatabase.md)

[Get-AzureSqlDatabaseCopy](./Get-AzureSqlDatabaseCopy.md)

[Stopp-AzureSqlDatabaseCopy](./Stop-AzureSqlDatabaseCopy.md)


