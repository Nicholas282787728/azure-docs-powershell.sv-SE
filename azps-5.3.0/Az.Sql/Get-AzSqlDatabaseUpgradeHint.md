---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
ms.openlocfilehash: b5f94aeb66749fa9bc89a89febb0bc5597241d58
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520367"
---
# Get-AzSqlDatabaseUpgradeHint

## Sammanfattning
Hämtar kodtips för en databas.

## FRÅGESYNTAXEN

```
Get-AzSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzSqlDatabaseUpgradeHint** får pris nivå tips för uppgradering av en Azure SQL-databas.
Databaser som fortfarande finns i webb-och företags pris nivåer är ett tips för att du ska kunna uppgradera till de nya grund klasserna.
Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.

## BESKRIVS

### Exempel 1: få rekommendationer för alla databaser på en server
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

Det här kommandot returnerar uppgraderings tips för alla databaser på servern som heter Server01.

### Exempel 2: få rekommendationer för specifik databas
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

Det här kommandot returnerar ett uppgraderings tips för en viss databas.

### Exempel 3: få rekommendationer för alla databaser som inte är i en elastisk databas
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

Det här kommandot returnerar ett uppgraderings tips för alla databaser som inte är i en elastisk databas.

### Exempel 4: få rekommendationer för alla databaser på en server med hjälp av filtrering
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

Det här kommandot returnerar uppgraderings tips för alla databaser på servern med namnet Server01 som börjar med "databas".

## MALLPARAMETRAR

### -DatabaseName
Anger namnet på den SQL-databas för vilken denna cmdlet får ett uppgraderings tips.
Om du inte anger en databas får denna cmdlet tips för alla databaser på den logiska servern.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExcludeElasticPoolCandidates
Anger om databaser i Elastic Database-pooler exkluderas från de rekommendationer som returneras.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på den resurs grupp som databasen har tilldelats till.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerName
Anger namnet på den server som är värd för databasen för vilken denna cmdlet får ett uppgraderings tips.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### System. String

### System. Boolean

## VÄRDEN

### Microsoft. Azure. Management. SQL. LegacySdk. Models. RecommendedDatabaseProperties

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzSqlDatabaseExpanded](./Get-AzSqlDatabaseExpanded.md)

[Get-AzSqlElasticPoolRecommendation](./Get-AzSqlElasticPoolRecommendation.md)


