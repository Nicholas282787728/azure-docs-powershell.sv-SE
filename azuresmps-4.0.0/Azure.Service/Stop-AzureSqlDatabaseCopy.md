---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: CB601E21-424D-4B09-85E5-A4B2A5068267
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7716587787515221a6e016436a6e3d030c1ab0eb
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405626"
---
# Stop-AzureSqlDatabaseCopy

## SYNOPSIS
Avslutar en kontinuerlig kopieringsrelation.

## SYNTAX

### ByInputObject
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-ForcedTermination] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDatabase
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByDatabaseName
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Stop-AzureSqlDatabaseCopy** avslutar en kontinuerlig kopieringsrelation.
Med den här cmdleten stoppar du dataförflyttningen mellan källdatabasen och den sekundära databasen eller måldatabasen, och ändrar sedan statusen för den sekundära databasen till en fristående onlinedatabas.

Det finns två sätt att avsluta en kontinuerlig kopieringsrelation, uppsägning eller planerad uppsägning och tvingad uppsägning med eventuell dataförlust.
Du kan köra den här cmdleten i läget uppsägning eller tvingad uppsägning på servern som är värd för källdatabasen.
Du måste använda tvingad uppsägningsläge på servern som är värd för den sekundära databasen.

En planerad uppsägning väntar tills alla genomfört transaktioner i källdatabasen, vid tidpunkten då du kör cmdleten, har replikerats till den sekundära databasen.
Tvingad uppsägning väntar inte på replikering av eventuella utestående utestående transaktioner och kan orsaka eventuell dataförlust i den sekundära databasen.

Medan replikeringsstatus är VÄNTANDE kan endast tvingad uppsägning avsluta en kontinuerlig kopieringsrelation.
Om replikeringsstatusen är VÄNTANDE stöds inte uppsägning som inte tvingas.

## EXEMPEL

### Exempel 1: Avsluta en kontinuerlig kopieringsrelation
```
PS C:\>Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

Det här kommandot avslutar den kontinuerliga kopieringsrelationen för databasen med namnet Orders på servern lpqd0zgav8y.
Servern som heter bk0b8kf658 är värd för den sekundära databasen.

### Exempel 2: Avbryt en kontinuerlig kopieringsrelation
```
PS C:\>$DatabaseCopy = Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders"
PS C:\> $DatabaseCopy | Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -ForcedTermination
```

Det första kommandot får databasens databaskopieringsrelation med namnet Orders på servern lpqd0z inköpsorder8y.

Med det andra kommandot avbryts en kontinuerlig kopieringsrelation från servern som är värd för den sekundära databasen.

## PARAMETERS

### -Database
Anger ett objekt som representerar källan Azure SQL Database.
Den här cmdleten avslutar den kontinuerliga kopieringsrelationen för databasen som parametern anger.

```yaml
Type: Database
Parameter Sets: ByDatabase
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseCopy
Anger ett objekt som representerar en databas.
Den här cmdleten avslutar den kontinuerliga kopieringsrelationen för databasen som parametern anger.
Den här parametern accepterar inmatning från pipeline.

```yaml
Type: DatabaseCopy
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
Anger namnet på en databas.
Den här cmdleten avslutar den kontinuerliga kopieringsrelationen för databasen som parametern anger.

```yaml
Type: String
Parameter Sets: ByDatabaseName
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

### -ForcedTermination
Anger att denna cmdlet leder till att den kontinuerliga kopieringsrelationen avslutas.
Tvingad uppsägning kan orsaka dataförlust.
Om du vill köra den här cmdleten på en server som är värd för måldatabasen måste du ange den här parametern.
Om du vill köra den här cmdleten på en server som är värd för källdatabasen måste du ange den här parametern om den sekundära databasen inte är tillgänglig.

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

### -PartnerDatabase
Anger namnet på den sekundära databasen.
Om du anger ett namn måste det matcha namnet på källdatabasen.

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerServer
Anger namnet på den server som är värd för måldatabasen.

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
Aliases: 

Required: False
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

### Microsoft.WindowsAzure.Commands.sqlDatabase.Model.DatabaseCopy

### Microsoft.WindowsAzure.Commands.sqlDatabase.Services.Server.Database

## UTDATA

### Ingen

## ANTECKNINGAR
* Autentisering: Den här cmdleten kräver certifikatbaserad autentisering. Ett exempel på hur du använder certifikatbaserad autentisering för att ange aktuell prenumeration finns i cmdleten **New-AzureSqlDatabaseServerContext.**
* Begränsningar: På servern som är värd för den sekundära databasen stöds endast tvingad uppsägning.
* Påverkan på uppsägning av den tidigare sekundära databasen: När den sekundära databasen avslutas blir den en oberoende databas. Om dirigeringen redan är klar i den sekundära databasen är den här databasen öppen för fullständig åtkomst när databasen avslutas. Om källdatabasen är en skrivskyddsdatabas blir även den tidigare sekundära databasen en skrivskyddsdatabas.

  Om start är under utveckling avbryts startningen och den tidigare sekundära databasen visas aldrig på servern som är värd för den sekundära databasen.

* Källdatabasen kan ställas in i skrivskyddsläge. Detta garanterar att källdatabaser och sekundära databaser synkroniseras efter att de avslutats och att inga transaktioner genomförs vid uppsägning. När avslutningen har avslutats ställer du in källan på läs-och skrivläge igen. Om du vill kan du också ange den tidigare sekundära databasen till läs-och skrivläge.
* Övervakning: Om du vill verifiera status för operationerna i både källan och målet för den kontinuerliga kopieringsrelationen använder du **cmdleten Get-AzureSqlDatabaseOperation.**

## RELATERADE LÄNKAR

[Azure SQL Database](https://azure.microsoft.com/en-us/services/sql-database/)

[Åtgärder för Azure SQL-databaser](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Stoppa databaskopia](https://msdn.microsoft.com/en-us/library/dn509573.aspx)



[Get-AzureSqlDatabaseCopy](./Get-AzureSqlDatabaseCopy.md)

[Start-AzureSqlDatabaseCopy](./Start-AzureSqlDatabaseCopy.md)


