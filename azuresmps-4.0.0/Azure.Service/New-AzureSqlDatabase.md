---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F4FE79DB-B481-49BD-A33B-7C642A136890
online version: ''
schema: 2.0.0
ms.openlocfilehash: 588fcf73c258364e41117eed05c62de7eaa231e9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099203"
---
# New-AzureSqlDatabase

## Sammanfattning
Skapar en Azure SQL-databas.

## FRÅGESYNTAXEN

### ByConnectionContext
```
New-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String>
 [-Collation <String>] [-Edition <DatabaseEdition>] [-ServiceObjective <ServiceObjective>] [-MaxSizeGB <Int32>]
 [-MaxSizeBytes <Int64>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByServerName
```
New-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-Collation <String>]
 [-Edition <DatabaseEdition>] [-ServiceObjective <ServiceObjective>] [-MaxSizeGB <Int32>]
 [-MaxSizeBytes <Int64>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureSqlDatabase** skapar en Azure SQL-databas.
Du kan ange servern genom att använda en kontext för Server anslutning i Azure SQL som du skapar med den nya cmdleten **New-AzureSqlDatabaseServerContext** .
Om du anger Server namnet används den aktuella Azure-prenumerations informationen för att autentisera begäran om att få åtkomst till servern.

När du skapar en ny databas genom att ange en Azure SQL Database-Server skapar cmdlet **New-AzureSqlDatabase** en tillfällig anslutnings kontext med det angivna Server namnet och den aktuella Azure-prenumerations informationen för att utföra åtgärden.

## BESKRIVS

### Exempel 1: skapa en databas
```
PS C:\> $Database01 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01" -Edition "Business" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

Det här kommandot skapar en Azure SQL-databas med namnet database1 för $Context för Azure SQL Database-servern.

### Exempel 2: skapa en databas i det aktuella abonnemanget
```
PS C:\> $Database01 = New-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01" -Edition "Business" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

I det här exemplet skapas en databas med namnet database1 i den angivna Azure SQL-databas servern med namnet lpqd0zbr8y.
Cmdleten använder den aktuella Azure-prenumerationen för att autentisera begäran om att få åtkomst till servern.

## MALLPARAMETRAR

### -Sortering
Anger en sortering för den nya databasen.

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

### -ConnectionContext
Anger den anslutnings kontext för en server där denna cmdlet skapar en databas.

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
Anger namnet på den nya databasen.

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

### -Utgåva
Anger versionen för den nya Azure SQL-databasen.
Giltiga värden är: 

- Ingen
- Webben
- Uppmana
- Basisk
- Standar
-  Beta

Standardvärdet är Web.

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Gör att åtgärden kan slutföras utan att användaren uppmanas att bekräfta.

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

### -MaxSizeBytes
Anger den maximala storleken på databasen i byte.
Du kan ange antingen den här parametern eller parametern *MaxSizeGB* .
Se beskrivningen av *MaxSizeGB* -parametern för acceptabla värden baserat på Edition.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxSizeGB
Anger den maximala storleken på databasen i gigabyte.
Du kan ange antingen den här parametern eller parametern *MaxSizeBytes* .
De acceptabla värdena varierar beroende på utgåva.

Grundläggande Edition-värden: 1 eller 2

Standard Edition-värden: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200 eller 250

Premium Edition-värden: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400 eller 500

Web Edition-värden: 1 eller 5

Business Edition-värden: 10, 20, 30, 40, 50, 100 eller 150

```yaml
Type: Int32
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

### -ServerName
Anger namnet på den Azure SQL-databasserver som ska innehålla den nya databasen.

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

### -ServiceObjective
Anger ett objekt som representerar den nya tjänstens mål (prestanda nivå) för den här databasen.
Det här värdet representerar den resurs nivå som är kopplad till den här databasen.
Giltiga värden är: 

Grundläggande: dd6d99bb-f193-4EC1-86f2-43d3bccbc49c (S0): f1173c43-91bd-4AAA-973c-54e79e15235b standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928 standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7 * standard (S3): 789681b8-ca10-4eb0-bdf2-e0b050601b40 Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0 Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446

* Standard (S3) är en del av den senaste SQL-V12 (för hands version).
Mer information finns i Nyheter i för hands versionen av V12 för Azure SQL Database https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/ .

```yaml
Type: ServiceObjective
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

## VÄRDEN

### Microsoft. WindowsAzure. kommandon. SqlDatabase. Services. Server. Database

## ANMÄRKNINGAR
* Använd Remove-AzureSqlDatabase cmdlet för att ta bort en databas som har skapats av **New-AzureSqlDatabase**.

## RELATERADE LÄNKAR

[Azure SQL-databas](https://azure.microsoft.com/en-us/services/sql-database/)

[Skapa databas](https://msdn.microsoft.com/en-us/library/azure/dn505701.aspx)

[Åtgärder för Azure SQL-databaser](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[New-AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)

[Remove-AzureSqlDatabase](./Remove-AzureSqlDatabase.md)

[Set-AzureSqlDatabase](./Set-AzureSqlDatabase.md)


