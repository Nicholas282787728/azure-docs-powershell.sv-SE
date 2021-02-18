---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: a5691b1d8181d210770802c8d3aa4526b6bd72f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100223446"
---
# Get-AzPostgreSqlFirewallRule

## SYNOPSIS
Hämtar information om en serverbrandväggsregel.

## SYNTAX

### Lista (standard)
```
Get-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Skaffa
```
Get-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## BESKRIVNING
Hämtar information om en serverbrandväggsregel.

## EXEMPEL

### Exempel 1: Visar alla brandväggsregler i angiven PostgreSql-server
```powershell
PS C:\> Get-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

Den här cmdleten listar alla brandväggsregel i angiven PostgreSql-server.

### Exempel 2: Hämta brandväggsregeln efter namn
```powershell
PS C:\> Get-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

Den här cmdleten får brandväggsregeln efter namn.

### Exempel 3: Hämta brandväggsregeln efter identitet
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Get-AzPostgreSqlFirewallRule -InputObject $ID

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

Den här cmdleten får en brandväggsregel efter identitet.

## PARAMETERS

### -DefaultProfile
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Identitetsparameter att skapa finns i avsnittet ANTECKNINGAR för INPUTOBJECT-egenskaper och skapa en hash-tabell.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Namnet på regeln för serverbrandväggen.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Namnet på resursgruppen.
Namnet är okänsligt.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Servernamn
Namnet på servern.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
ID för målprenumerationen.

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### Microsoft.Azure.PowerShell.cmdlets.PostgreSql.Models.IPostgreSqlIdentity

## UTDATA

### Microsoft.Azure.PowerShell.cmdlets.PostgreSql.Models.Api20171201.iFirewallRule

## ANTECKNINGAR

ALIAS

KOMPLEXA PARAMETEREGENSKAPER

Skapa de parametrar som beskrivs nedan genom att skapa en hash-tabell som innehåller rätt egenskaper. Om du vill ha information om hash-tabeller kör du Get-Help about_Hash_Tables.


INPUTOBJECT <IPostgreSqlIdentity> : Identity Parameter
  - `[ConfigurationName <String>]`: Namnet på serverkonfigurationen.
  - `[DatabaseName <String>]`: Namnet på databasen.
  - `[FirewallRuleName <String>]`: Namnet på serverns brandväggsregel.
  - `[Id <String>]`: Resursidentitetssökväg
  - `[LocationName <String>]`: Platsens namn.
  - `[ResourceGroupName <String>]`: Namnet på resursgruppen. Namnet är okänsligt.
  - `[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhetsvarningsprincipen.
  - `[ServerName <String>]`: Namnet på servern.
  - `[SubscriptionId <String>]`: ID för målprenumerationen.
  - `[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverksregeln.

## RELATERADE LÄNKAR

