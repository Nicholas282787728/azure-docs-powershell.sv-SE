---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5AEF7D44-624D-4794-86FF-156E6729BB56
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8752766572975ef97094a3915446086c903a7fd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099525"
---
# Get-AzureSqlDatabaseCopy

## Sammanfattning
Kontrollerar statusen för kopierings relationer.

## FRÅGESYNTAXEN

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

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureSqlDatabaseCopy** kontrollerar statusen för en eller flera aktiva kopierings relationer.
Kör den här cmdleten när du har kört Start-AzureSqlDatabaseCopy eller Stop-AzureSqlDatabaseCopy cmdlet.
Du kan kontrol lera en specifik kopierings relation, alla kopierings relationer eller en filtrerad lista över kopierings relationer, till exempel alla kopior på en specifik mål server.
Du kan köra denna cmdlet på den server som är värd för käll-eller mål databasen.

Denna cmdlet är synkron.
Cmdleten blockerar Azure PowerShell-konsolen tills den returnerar ett status-objekt.

Parametrarna *PartnerServer* och *PartnerDatabase* är valfria.
Om du inte anger någon parameter returnerar denna cmdlet en tabell med resultat.
Om du vill visa statusen för endast en viss databas anger du båda parametrarna.

## BESKRIVS

### Exempel 1: få kopierings status för en databas
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

Det här kommandot får statusen för databasen order på den server som heter lpqd0zbr8y.
Parametern *PartnerServer* begränsar det här kommandot till bk0b8kf658-servern.

### Exempel 2: få status för alla kopior på en serverGet status för alla kopior på en server
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y"
```

Det här kommandot får statusen för alla aktiva kopior på servern som heter lpqd0zbr8y.

## MALLPARAMETRAR

### -Databas
Anger ett objekt som representerar käll-Azure SQL-databasen.
Denna cmdlet hämtar kopierings statusen för databasen som anges av den här parametern.

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
Denna cmdlet hämtar kopierings statusen för databasen som anges av den här parametern.
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
Anger namnet på käll databasen.
Denna cmdlet får kopierings status för databasen som anges av den här parametern.

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
Om den här databasen inte finns i vyn sys.dm_database_copies dynamisk hantering returnerar denna cmdlet ett tomt status-objekt.

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
Anger namnet på den server som är värd för mål databasen.
Om den här servern inte finns i vyn sys.dm_database_copies dynamisk hantering returnerar denna cmdlet ett tomt status-objekt.

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
Anger namnet på den server där databas kopian finns.

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Microsoft. WindowsAzure. kommandon. SqlDatabase. Model. DatabaseCopy

### Microsoft. WindowsAzure. kommandon. SqlDatabase. Services. Server. Database

## VÄRDEN

### Microsoft. WindowsAzure. kommandon. SqlDatabase. Model. DatabaseCopy

## ANMÄRKNINGAR
* Verifiera: den här cmdleten kräver certifikatbaserad identifiering. Ett exempel på hur certifikatbaserad verifikation används för att ange aktuell prenumeration finns i New-AzureSqlDatabaseServerContext cmdlet.

## RELATERADE LÄNKAR

[Azure SQL-databas](https://azure.microsoft.com/en-us/services/sql-database/)

[Åtgärder för Azure SQL-databaser](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Azure SQL-databas-cmdletar](./Azure.SQLDatabase.md)

[Start-AzureSqlDatabaseCopy](./Start-AzureSqlDatabaseCopy.md)

[Stopp-AzureSqlDatabaseCopy](./Stop-AzureSqlDatabaseCopy.md)


