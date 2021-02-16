---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5AEF7D44-624D-4794-86FF-156E6729BB56
online version: ''
schema: 2.0.0
ms.openlocfilehash: 95e276bf6af11698a4b3b82077175ec2ede2d7dc
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402430"
---
# Get-AzureSqlDatabaseCopy

## SYNOPSIS
Kontrollerar status för kopieringsrelationer.

## SYNTAX

### ByServerNameOnly (standard)
```
Get-AzureSqlDatabaseCopy -ServerName <String> [-DatabaseName <String>] [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByInputObject
```
Get-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ByDatabase
```
Get-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Get-AzureSqlDatabaseCopy** kontrollerar status för en eller flera aktiva kopieringsrelationer.
Kör den här cmdleten när du har kört cmdleten Start-AzureSqlDatabaseCopy eller Stop-AzureSqlDatabaseCopy cmdleten.
Du kan kontrollera en specifik kopieringsrelation, alla kopieringsrelationer eller en filtrerad lista med kopieringsrelationer, till exempel alla kopior på en specifik målserver.
Du kan köra den här cmdleten på servern som är värd för käll- eller måldatabasen.

Den här cmdleten är synkroniserad.
Cmdleten blockerar Azure PowerShell-konsolen tills den returnerar ett statusobjekt.

Parametrarna *PartnerServer* och *PartnerDatabase* är valfria.
Om du inte anger någon av parametrarna returnerar den här cmdleten en resultattabell.
Om du bara vill visa status för en viss databas anger du båda parametrarna.

## EXEMPEL

### Exempel 1: Hämta kopieringsstatus för en databas
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

Det här kommandot får statusen för databasen med namnet Orders på servern lpqd0zgav8y.
*PartnerServer-parametern* begränsar det här kommandot till bk0b8kf658-servern.

### Exempel 2: Hämta statusen för alla kopior på en serverGet the status of all copies on a server
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y"
```

Det här kommandot hämtar statusen för alla aktiva kopior på servern med namnet lpqd0zzen8y.

## PARAMETERS

### -Database
Anger ett objekt som representerar källan Azure SQL Database.
Den här cmdleten får kopieringsstatus för databasen som den här parametern anger.

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
Den här cmdleten får kopieringsstatus för databasen som den här parametern anger.
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
Anger namnet på källdatabasen.
Den här cmdleten får kopieringsstatusen för databasen som den här parametern anger.

```yaml
Type: String
Parameter Sets: ByServerNameOnly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerDatabase
Anger namnet på den sekundära databasen.
Om den här databasen inte finns i sys.dm_database_copies dynamisk hanteringsvy returnerar denna cmdlet ett tomt statusobjekt.

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerServer
Anger namnet på den server som är värd för måldatabasen.
Om den här servern inte sys.dm_database_copies dynamisk hanteringsvy returnerar denna cmdlet ett tomt statusobjekt.

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
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
Anger namnet på den server där databaskopian finns.

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

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### Microsoft.WindowsAzure.Commands.sqlDatabase.Model.DatabaseCopy

### Microsoft.WindowsAzure.Commands.sqlDatabase.Services.Server.Database

## UTDATA

### Microsoft.WindowsAzure.Commands.sqlDatabase.Model.DatabaseCopy

## ANTECKNINGAR
* Autentisering: Den här cmdleten kräver certifikatbaserad autentisering. Ett exempel på hur du använder certifikatbaserad autentisering för att ange aktuell prenumeration finns i New-AzureSqlDatabaseServerContext-cmdleten.

## RELATERADE LÄNKAR

[Azure SQL Database](https://azure.microsoft.com/en-us/services/sql-database/)

[Åtgärder för Azure SQL-databaser](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)



[Start-AzureSqlDatabaseCopy](./Start-AzureSqlDatabaseCopy.md)

[Stop-AzureSqlDatabaseCopy](./Stop-AzureSqlDatabaseCopy.md)


