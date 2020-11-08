---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: CB601E21-424D-4B09-85E5-A4B2A5068267
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b7674cb5b7abc489dc6aa6d3746f499b9686312
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099633"
---
# Stop-AzureSqlDatabaseCopy

## Sammanfattning
Avbryter en kontinuerlig kopierings relation.

## FRÅGESYNTAXEN

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

## PROBLEMBESKRIVNING
Cmdleten **Stop-AzureSqlDatabaseCopy** avbryter en kontinuerlig kopierings relation.
Denna cmdlet stoppar data förflyttningen mellan käll databasen och den sekundära databasen eller måltypen och ändrar sedan den sekundära databasens status till en fristående databas.

Det finns två sätt att avsluta ett fort löp ande kopierings förhållande, uppsägning eller planerad uppsägning med möjlig data förlust.
På den server som är värd för käll databasen kan du köra denna cmdlet i uppsägning eller framtvingat avslutnings läge.
På den server som är värd för den sekundära databasen måste du använda framtvingat avslutnings läge.

En planerad uppsägning väntar tills alla genomförda transaktioner på käll databasen, när du kör cmdleten, har repliker ATS till den sekundära databasen.
Framtvingad uppsägning väntar inte på replikering av utestående transaktioner och kan leda till förlust av data i den sekundära databasen.

När replikeringsstatus är pågående kan endast tvingande uppsägning avsluta en kontinuerlig kopierings relation.
Om replikeringsstatus är avvaktat stöds inte uppsägning som inte framtvingas.

## BESKRIVS

### Exempel 1: avsluta en kontinuerlig kopierings relation
```
PS C:\>Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

Det här kommandot avbryter den kontinuerliga kopierings relationen för databasen order på den server som heter lpqd0zbr8y.
Servern med namnet bk0b8kf658 är värd för den sekundära databasen.

### Exempel 2: tvinga fram en kontinuerlig kopierings relation
```
PS C:\>$DatabaseCopy = Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders"
PS C:\> $DatabaseCopy | Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -ForcedTermination
```

Det första kommandot får databas kopierings relationen för databasen order på den server som heter lpqd0zbr8y.

Det andra kommandot avslutar en kontinuerlig kopierings relation från den server som är värd för den sekundära databasen.

## MALLPARAMETRAR

### -Databas
Anger ett objekt som representerar käll-Azure SQL-databasen.
Denna cmdlet avbryter den kontinuerliga kopierings relationen för databasen som anges av den här parametern.

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
Denna cmdlet avbryter den kontinuerliga kopierings relationen för databasen som anges av den här parametern.
Den här parametern accepterar pipeline-inmatning.

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
Denna cmdlet avbryter den kontinuerliga kopierings relationen för databasen som anges av den här parametern.

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

### -ForcedTermination
Anger att denna cmdlet orsakar tvingande uppsägning av den kontinuerliga kopierings relationen.
Det kan orsaka förlust av data.
Om du vill köra denna cmdlet på en server som är värd för mål databasen måste du ange den här parametern.
Om du vill köra denna cmdlet på en server som är värd för käll databasen, om den sekundära databasen inte är tillgänglig, måste du ange den här parametern.

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
Om du anger ett namn måste det matcha käll databasens namn.

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
Anger namnet på den server som är värd för mål databasen.

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

### Microsoft. WindowsAzure. kommandon. SqlDatabase. Model. DatabaseCopy

### Microsoft. WindowsAzure. kommandon. SqlDatabase. Services. Server. Database

## VÄRDEN

### Ingen

## ANMÄRKNINGAR
* Verifiera: den här cmdleten kräver certifikatbaserad identifiering. Ett exempel på hur certifikatbaserad identifiering används för att ange aktuellt abonnemang finns i cmdleten **New-AzureSqlDatabaseServerContext** .
* Restriktioner: på den server som är värd för den sekundära databasen kan endast tvingande uppsägning användas.
* Konsekvenserna av uppsägningen på den tidigare sekundära databasen: efter uppsägning blir den sekundära databasen en självständig databas. Om dirigering redan har slutförts på den sekundära databasen är den här databasen öppen för fullständig åtkomst efter uppsägning. Om käll databasen är en skrivskyddad databas blir den tidigare sekundära databasen en skrivskyddad databas också.

  Om dirigering pågår avbryts dirigeringen och den tidigare sekundära databasen blir aldrig synlig på den server som är värd för den sekundära databasen.

* Du kan ange skrivskyddad käll databas. Detta garanterar att källan och sekundära databaser synkroniseras efter uppsägning och ser till att inga transaktioner bevaras under uppsägningen. När uppsägningen är klar återställer du källan till Läs-och skriv läge. Du kan också ange den tidigare sekundära databasen till Läs-och skriv läge.
* Övervakning: Använd cmdleten **Get-AzureSqlDatabaseOperation** för att bekräfta statusen för åtgärderna på både källa och mål för den kontinuerliga kopierings relationen.

## RELATERADE LÄNKAR

[Azure SQL-databas](https://azure.microsoft.com/en-us/services/sql-database/)

[Åtgärder för Azure SQL-databaser](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Stoppa databas kopiering](https://msdn.microsoft.com/en-us/library/dn509573.aspx)

[Azure SQL-databas-cmdletar](./Azure.SQLDatabase.md)

[Get-AzureSqlDatabaseCopy](./Get-AzureSqlDatabaseCopy.md)

[Start-AzureSqlDatabaseCopy](./Start-AzureSqlDatabaseCopy.md)


