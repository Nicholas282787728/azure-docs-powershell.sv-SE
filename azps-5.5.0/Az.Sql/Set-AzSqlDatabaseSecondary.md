---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
ms.openlocfilehash: d713675e3e73f32a4579d801a4dc1577cebd4cf0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100212423"
---
# Set-AzSqlDatabaseSecondary

## SYNOPSIS
Växlar till primär sekundär databas för att initiera redundans.

## SYNTAX

### NoOptionsSet (standard)
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByFailoverParams
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Set-AzSqlDatabaseSecondary** växlar en sekundär databas till primär för att initiera redundans.
Den här cmdleten är utformad som ett allmänt konfigurationskommando, men är för närvarande begränsad till att initiera redundans.
Ange *parametern AllowDataLoss* som initierar en force failover vid ett avbrott.
Du behöver inte ange den här parametern när du utför en planerad åtgärd, till exempel återställningsgranskning.
I det senare fallet synkroniseras den sekundära databasen med den primära databasen innan den byts ut.

## EXEMPEL

### Exempel 1: Initiera en planerad redundans
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover
```

### Exempel 2: Initiera en tvingad redundans (med potentiell dataförlust)
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover -AllowDataLoss
```

## PARAMETERS

### -AllowDataLoss
Anger att den här redundansåtgärden medger dataförlust.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -As Ent
Kör cmdleten i bakgrunden

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseName
Anger namnet på Azure SQL Database Secondary.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure

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

### -Failover
Anger att den här åtgärden är en redundans.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerResourceGroupName
Anger namnet på den resursgrupp som partnern Azure SQL Database är tilldelad till.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på den resursgrupp som Azure SQL Database Secondary är tilldelad till.

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

### -Servernamn
Anger namnet på den SQL Server som är värd för Azure SQL Database Secondary.

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
Frågar dig om bekräftelse innan du kör cmdleten.

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
Visar vad som skulle hända om cmdleten körs.
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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### System.String

## UTDATA

### Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel

## ANTECKNINGAR

## RELATERADE LÄNKAR

[New-AzSqlDatabaseSecondary](./New-AzSqlDatabaseSecondary.md)

[Remove-AzSqlDatabaseSecondary](./Remove-AzSqlDatabaseSecondary.md)

[Dokumentation om SQL-databaser](https://docs.microsoft.com/azure/sql-database/)
