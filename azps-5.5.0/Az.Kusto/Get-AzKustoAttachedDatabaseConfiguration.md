---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: 6b1a042eb96c1fa6acbcc22fbdd33aefd9d4d46b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100219359"
---
# Get-AzKustoAttachedDatabaseConfiguration

## SYNOPSIS
Returnerar en bifogad databaskonfiguration.

## SYNTAX

### Lista (standard)
```
Get-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Skaffa
```
Get-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzKustoAttachedDatabaseConfiguration -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## BESKRIVNING
Returnerar en bifogad databaskonfiguration.

## EXEMPEL

### Exempel 1: Lista alla bifogadeDatabaserConfigurations i ett kluster
```powershell
PS C:\> Get-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf"

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

Kommandot ovan visar alla AttachedDatabaseConfigurations i klustret "testnewkustoclusterf".

### Exempel 2: Hämta en specifik bifogadDatabasKonfiguration i ett kluster
```powershell
PS C:\>  Get-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration" 

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

Kommandot ovan returnerar bifogadeDatabaseConfigurations med namnet "myfollowerconfiguration" i klustret "testnewkustoclusterf".

## PARAMETERS

### -ClusterName
Namnet på Kusto-klustret.

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
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Namnet på den bifogade databaskonfigurationen.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AttachedDatabaseConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Namnet på resursgruppen som innehåller Kusto-klustret.

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
Får prenumerationsuppgifter som unikt identifierar Microsoft Azure-prenumerationen.
Prenumerations-ID:t utgör en del av URI:n för varje servicesamtal.

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

### Microsoft.Azure.PowerShell.cmdlets.Kusto.Models.IKustoIdentity

## UTDATA

### Microsoft.Azure.PowerShell.cmdlets.Kusto.Models.Api20200918.IAttachedDatabaseConfiguration

## ANTECKNINGAR

ALIAS

KOMPLEXA PARAMETEREGENSKAPER

Skapa de parametrar som beskrivs nedan genom att skapa en hash-tabell som innehåller rätt egenskaper. Om du vill ha information om hash-tabeller kör du Get-Help about_Hash_Tables.


INPUTOBJECT <IKustoIdentity> : Identity Parameter
  - `[AttachedDatabaseConfigurationName <String>]`: Namnet på den bifogade databaskonfigurationen.
  - `[ClusterName <String>]`: Namnet på Kusto-klustret.
  - `[DataConnectionName <String>]`: Namnet på dataanslutningen.
  - `[DatabaseName <String>]`: Namnet på databasen i Kusto-klustret.
  - `[Id <String>]`: Resursidentitetssökväg
  - `[Location <String>]`: Azure-plats.
  - `[PrincipalAssignmentName <String>]`: Namnet på Kusto principalAssignment.
  - `[ResourceGroupName <String>]`: Namnet på resursgruppen som innehåller Kusto-klustret.
  - `[SubscriptionId <String>]`: Får prenumerationsuppgifter som unikt identifierar Microsoft Azure-prenumerationen. Prenumerations-ID:t utgör en del av URI:n för varje servicesamtal.

## RELATERADE LÄNKAR

