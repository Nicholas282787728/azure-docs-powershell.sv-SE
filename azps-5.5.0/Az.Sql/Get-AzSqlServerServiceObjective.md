---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: AC2D64B9-5BCD-45D3-8650-538633F5BBBC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverserviceobjective
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerServiceObjective.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerServiceObjective.md
ms.openlocfilehash: e53857533770d6de0040d2d777020f1a2f9f320a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235550"
---
# Get-AzSqlServerServiceObjective

## SYNOPSIS
Får tjänstmål för en Azure SQL Database-server.

## SYNTAX

### ByLocation (standard)
```
Get-AzSqlServerServiceObjective [[-ServiceObjectiveName] <String>] -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByServer
```
Get-AzSqlServerServiceObjective [[-ServiceObjectiveName] <String>] [-ResourceGroupName] <String>
 [-ServerName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Get-AzSqlServerServiceObjective** får de tillgängliga tjänstmålen för en Azure SQL Database-server.

## EXEMPEL

### Exempel 1: Hämta tjänstmål
```
PS C:\>Get-AzSqlServerServiceObjective -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
serviceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
System               System        System                  0        DTU          False
Free                 Free          Free                    5        DTU          True
Basic                Basic         Basic                   5        DTU          True
S0                   Standard      Standard                10       DTU          True
S1                   Standard      Standard                20       DTU          True
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
DW100c               DataWarehouse DataWarehouse           900      DTU          False
GP_Gen4_1            GP_Gen4       GeneralPurpose   Gen4   1        VCores       True
GP_Gen5_2            GP_Gen5       GeneralPurpose   Gen5   2        VCores       True
BC_Gen4_1            BC_Gen4       BusinessCritical Gen4   1        VCores       True
BC_Gen5_4            BC_Gen5       BusinessCritical Gen5   4        VCores       True
```

Det här kommandot får tjänstmål för servern Server01.

### Exempel 2: Få tjänstmål med hjälp av filtrering
```
PS C:\>Get-AzSqlServerServiceObjective -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServiceObjectiveName "P*"
ServiceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
```

Det här kommandot får tjänstmålen för servern Server01 som börjar med "System".

### Exempel 3: Hämta tjänstmål för en plats
```
PS C:\>Get-AzSqlServerServiceObjective -Location "west us"
serviceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
System               System        System                  0        DTU          False
Free                 Free          Free                    5        DTU          True
Basic                Basic         Basic                   5        DTU          True
S0                   Standard      Standard                10       DTU          True
S1                   Standard      Standard                20       DTU          True
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
DW100c               DataWarehouse DataWarehouse           900      DTU          False
GP_Gen4_1            GP_Gen4       GeneralPurpose   Gen4   1        VCores       True
GP_Gen5_2            GP_Gen5       GeneralPurpose   Gen5   2        VCores       True
BC_Gen4_1            BC_Gen4       BusinessCritical Gen4   1        VCores       True
BC_Gen5_4            BC_Gen5       BusinessCritical Gen5   4        VCores       True
```

Det här kommandot får tjänstmålen för en viss Azure-region.

## PARAMETERS

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

### -Plats
Namnet på den plats som du vill få tjänstmål för.

```yaml
Type: System.String
Parameter Sets: ByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på en resursgrupp.
Den här cmdleten får tjänstmål för en SQL Database-server tilldelad den här resursen.

```yaml
Type: System.String
Parameter Sets: ByServer
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Servernamn
Anger namnet på en SQL Database SQL Database-server.

```yaml
Type: System.String
Parameter Sets: ByServer
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceObjectiveName
Anger namnet på ett tjänstmål för en Azure SQL Database-server.
De godtagbara värdena för den här parametern är: Basic, S0, S1, S2, P1, P2 och P3.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
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

### Microsoft.Azure.Commands.Sql.ServiceObjective.Model.AzureSqlServerServiceObjectiveModel

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Dokumentation om SQL-databaser](https://docs.microsoft.com/azure/sql-database/)


