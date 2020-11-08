---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 0ACEDE22-1C2B-4846-A949-710AF6C148D0
online version: ''
schema: 2.0.0
ms.openlocfilehash: d513d6d019c84984923541624063e657e2250b61
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093297"
---
# Get-AzureSqlDatabaseServer

## Sammanfattning
Hämtar information om Azure SQL Database-servrar.

## FRÅGESYNTAXEN

```
Get-AzureSqlDatabaseServer [-ServerName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureSqlDatabaseServer** hämtar information om instanser av Azure SQL Database Server i det aktuella abonnemanget.
Om du anger en server med namn, returnerar denna cmdlet ett objekt som innehåller information om den servern.
Annars returnerar cmdleten information om alla servrar.

## BESKRIVS

### Exempel 1: få information om alla servrar
```
PS C:\> Get-AzureSqlDatabaseServer
```

Det här kommandot returnerar information om alla instanser av Azure SQL Database Server i det aktuella abonnemanget.

### Exempel 2: Hämta information om en viss server
```
PS C:\> Get-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y"
```

Det här kommandot returnerar information om den server som heter lpqd0zbr8y.

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

### -ServerName
Anger namnet på den server som cmdleten tar bort.
Ange Server namnet, inte det fullständigt kvalificerade DNS-namnet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Microsoft. WindowsAzure. kommandon. SqlDatabase. Model. SqlDatabaseServerContext

## VÄRDEN

### IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext\>

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Azure SQL-databas](https://azure.microsoft.com/en-us/services/sql-database/)

[List servrar](https://msdn.microsoft.com/en-us/library/azure/dn505702.aspx)

[Åtgärder för Azure SQL-databaser](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[New-AzureSqlDatabaseServer](./New-AzureSqlDatabaseServer.md)

[Remove-AzureSqlDatabaseServer](./Remove-AzureSqlDatabaseServer.md)

[Set-AzureSqlDatabaseServer](./Set-AzureSqlDatabaseServer.md)


