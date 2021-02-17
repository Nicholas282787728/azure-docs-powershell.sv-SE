---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7F07494-FBCA-4A77-92BF-E0A2D7ACCD21
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35e29655e8447644b6c5449309424595e45ca187
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100413072"
---
# Start-AzureSqlDatabaseCopy

## SYNOPSIS
Startar en kopiering av en Azure SQL-databas.

## SYNTAX

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

## BESKRIVNING
**Start-AzureSqlDatabaseCopy-cmdleten** startar en kopieringsåtgärd på en gång eller en kontinuerlig kopiering av en viss Azure SQL-databas.
Den här cmdleten är inte transaktionsell.

Den ursprungliga databasen är källdatabasen.
Kopian är den sekundära databasen eller måldatabasen.
För en kontinuerlig kopia får käll- och måldatabaserna inte finnas på samma server, och servrarna som är värd för käll- och måldatabaserna måste ingå i samma prenumeration.

Om du inte anger *parametern ContinuousCopy* skapas en kopia av källdatabasen med den här cmdleten.
När svaret tas emot kan åtgärden fortfarande pågår.
Du kan övervaka åtgärden med hjälp av cmdleten Get-AzureSqlDatabaseCopy eller Get-AzureSqlDatabaseOperation.

Om du anger *ContinuousCopy* skapar den här cmdleten en kontinuerlig kopia av källdatabasen.
När svaret tas emot pågår åtgärden.
Du kan övervaka åtgärden med hjälp av **Get-AzureSqlDatabaseCopy** eller **Get-AzureSqlDatabaseOperation.**

Du kan skapa en kontinuerlig kopia som en online- eller offlinedatabas.
Den kontinuerliga onlinekopian används för att konfigurera Active Geo-Replication för Azure SQL https://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/ Database.
Den kontinuerliga offlinekopian används för att konfigurera Geo-Replication för Azure SQL https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/ Database.

## EXEMPEL

### Exempel 1: Schemalägga en kontinuerlig databaskopia
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy
```

Det här kommandot schemalägger en kontinuerlig kopia av databasen med namnet Orders på servern lpqd0zgav8y.
Kommandot skapar en måldatabas på servern med namnet bk0b8kf658.

### Exempel 2: Skapa en enda kopia på samma server
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerDatabase "OrdersCopy"
```

Det här kommandot skapar en kopia på en gång av databasen med namnet Orders på servern lpqd0z inköpsorder8y.
Med kommandot skapas en kopia med namnet OrdersCopy på samma server.

### Exempel 3: Schemalägga en kontinuerlig offlinedatabaskopia
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy -OfflineSecondary
```

Det här kommandot schemalägger en kontinuerlig kopia av databasen med namnet Orders på servern lpqd0zgav8y.
Med det här kommandot skapas en offlinemåldatabas på servern med namnet bk0b8kf658.

## PARAMETERS

### -ContinuousCopy
Anger att databaskopian kommer att vara en kontinuerlig kopia (en kopia av databasen).
Kontinuerlig kopiering stöds inte på samma server.
Om parametern inte anges utförs en kopierad gång.
För en enda kopia måste käll- och partnerdatabaserna finnas på samma server.

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

### -Database
Anger ett objekt som representerar källan Azure SQL Database.
Den här parametern accepterar inmatning från pipeline.

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
Anger namnet på källdatabasen.

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
Tvingar kommandot att köras utan att användaren uppmanas att bekräfta.

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
Om källdatabasen är en standardversionsdatabas krävs den här parametern.
Om du anger den här *parametern måste ContinuousCopy* också anges.

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
Anger namnet på måldatabasen.
Om du anger *parametern ContinuousCopy* måste värdet *för PartnerDatabase* matcha namnet på källdatabasen.
Om du inte anger *ContinuousCopy* måste du ange ett namn för måldatabasen, som kan vara ett annat än källdatabasnamnet.

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
Anger namnet på den server som är värd för måldatabasen.
Servern måste vara i samma Azure-prenumeration som källdatabasservern.

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

### -Profile
Anger den Azure-profil som cmdleten läser upp.
Om du inte anger en profil läser den här cmdleten från den lokala standardprofilen.

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

### -Servernamn
Anger namnet på den server där källdatabasen finns.

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
Frågar dig om bekräftelse innan du kör cmdleten.

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
Visar vad som skulle hända om cmdleten körs.
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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### Microsoft.WindowsAzure.Commands.sqlDatabase.Services.Server.Database

## UTDATA

### Microsoft.WindowsAzure.Commands.sqlDatabase.Model.DatabaseCopy

## ANTECKNINGAR
* Autentisering: Den här cmdleten kräver certifikatbaserad autentisering. Ett exempel på hur du använder certifikatbaserad autentisering för att ange aktuell prenumeration finns i New-AzureSqlDatabaseServerContext cmdlet.
* Övervakning: Om du vill kontrollera status för en eller flera kontinuerliga kopieringsrelationer som är aktiva på servern använder du cmdleten **Get-AzureSqlDatabaseCopy.** Använd cmdleten **Get-AzureSqlDatabaseOperation** för att verifiera status för operationerna i både källan och målet för den kontinuerliga kopieringsrelationen.

## RELATERADE LÄNKAR

[Azure SQL Database](https://azure.microsoft.com/en-us/services/sql-database/)

[Åtgärder för Azure SQL-databaser](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Starta databaskopia](https://msdn.microsoft.com/en-us/library/azure/dn509576.aspx)



[Get-AzureSqlDatabaseCopy](./Get-AzureSqlDatabaseCopy.md)

[Stop-AzureSqlDatabaseCopy](./Stop-AzureSqlDatabaseCopy.md)


