---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/get-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExport.md
ms.openlocfilehash: 269a58e57510f6b0945218645ec079b21b606e44
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100230766"
---
# Get-AzCostManagementExport

## SYNOPSIS
Åtgärden för att hämta exporten för den definierade omfattningen efter exportnamn.

## SYNTAX

### Lista (standard)
```
Get-AzCostManagementExport -Scope <String> [-Expand <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### Skaffa
```
Get-AzCostManagementExport -Name <String> -Scope <String> [-Expand <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzCostManagementExport -InputObject <ICostManagementIdentity> [-Expand <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## BESKRIVNING
Åtgärden för att hämta exporten för den definierade omfattningen efter exportnamn.

## EXEMPEL

### Exempel 1: Hämta alla AzCostManagementExports efter omfattning
```powershell
PS C:\> Get-AzCostManagementExport -Scope 'subscriptions/**********'

ETag              Name                               Type
----              ----                               ----
"************" TestExport                         Microsoft.CostManagement/exports
"************" TestExport1                        Microsoft.CostManagement/exports
"************" TestExport2                        Microsoft.CostManagement/exports
```

Hämta alla AzCostManagementExports efter omfattning

### Exempel 2: Hämta AzCostManagementExport efter namn och omfattning
```powershell
PS C:\> Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'

ETag              Name       Type
----              ----       ----
"************" TestExport Microsoft.CostManagement/exports
```

Hämta AzCostManagementExport efter namn och omfattning

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

### -Expand
Kan användas för att expandera egenskaperna i en export.
För närvarande stöds endast "runHistory" och returnerar information för de senaste 10 körningarna av exporten.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Identitetsparameter att skapa finns i avsnittet ANTECKNINGAR för INPUTOBJECT-egenskaper och skapa en hash-tabell.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Exportera namn.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Omfattning
Den här parametern definierar omfattningen av kostnadshantering från olika perspektiv "Prenumeration", "Resursgrupp" och "Tillhandahåll tjänst".

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

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### Microsoft.Azure.PowerShell.cmdlets.CostManagement.Models.ICostManagementIdentity

## UTDATA

### Microsoft.Azure.PowerShell.cmdlets.CostManagement.Models.Api20200601.IExport

## ANTECKNINGAR

ALIAS

KOMPLEXA PARAMETEREGENSKAPER

Skapa de parametrar som beskrivs nedan genom att skapa en hash-tabell som innehåller rätt egenskaper. Om du vill ha information om hash-tabeller kör du Get-Help about_Hash_Tables.


INPUTOBJECT <ICostManagementIdentity> : Identity Parameter
  - `[AlertId <String>]`: Aviserings-ID
  - `[ExportName <String>]`: Exportera namn.
  - `[ExternalCloudProviderId <String>]`: Det kan vara {externalSubscriptionId}' för länkat konto eller {externalBillingAccountId}för konsoliderat konto som används med dimension-/frågeåtgärder.
  - `[ExternalCloudProviderType <ExternalCloudProviderType?>]`: Den externa molnleverantörens typ som associeras med dimension-/frågeåtgärder. Detta inkluderar 'externalSubscriptions' för länkat konto och 'externalBillingAccounts' för konsoliderat konto.
  - `[Id <String>]`: Resursidentitetssökväg
  - `[Scope <String>]`: Omfattningen som associeras med visningsåtgärder. Detta inkluderar "prenumerationer/{subscriptionId}" för prenumerationsomfång, 'prenumerationer/{subscriptionId}/resourceGroups/{resourceGroupName}' för resursgruppomfattning, Leverantörer/Microsoft.Billing/billingAccounts/{billingAccountId}' för faktureringskontoomfattning, leverantörer/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' för avdelningsomfånget, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' för registreringaccountomfattning, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' för BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.' Management/managementGroups/{managementGroupId}' för omfattningen Management Group, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.
  - `[ViewName <String>]`: Vynamn

## RELATERADE LÄNKAR

