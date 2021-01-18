---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/get-azcostmanagementexportexecutionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExportExecutionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExportExecutionHistory.md
ms.openlocfilehash: 7bb337837f9bd2be532c4eead8d8379b7cf04fe9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524284"
---
# Get-AzCostManagementExportExecutionHistory

## Sammanfattning
Åtgärden för att hämta körnings historiken för en export för det definierade scopet och export namnet.

## FRÅGESYNTAXEN

### Skaffa (standard)
```
Get-AzCostManagementExportExecutionHistory -ExportName <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzCostManagementExportExecutionHistory -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Åtgärden för att hämta körnings historiken för en export för det definierade scopet och export namnet.

## BESKRIVS

### Exempel 1: skaffa AzCostManagementExportExecutionHistory
```powershell
PS C:\> Get-AzCostManagementExportExecutionHistory -ExportName 'TestExport' -Scope 'subscriptions/**********'

ExecutionType ProcessingStartTime ProcessingEndTime  Status    FileName
------------- ------------------- -----------------  ------    --------
Scheduled     2020/6/11 12:03:20  2020/6/11 12:03:43 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
Scheduled     2020/6/12 12:03:37  2020/6/12 12:03:48 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
```

Få AzCostManagementExportExecutionHistory via ExportName och omfattning

### Exempel 2: get AzCostManagementExportExecutionHistory by InputObject
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'
Get-AzCostManagementExportExecutionHistory -InputObject $getExport

ExecutionType ProcessingStartTime ProcessingEndTime  Status    FileName
------------- ------------------- -----------------  ------    --------
Scheduled     2020/6/11 12:03:20  2020/6/11 12:03:43 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
Scheduled     2020/6/12 12:03:37  2020/6/12 12:03:48 Completed ad-hoc/TestExport/20200601-20200630/
```

Få AzCostManagementExportExecutionHistory via InputObject

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

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

### -ExportName
Exportera namn.

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.

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

### -Omfattning
Den här parametern definierar omfattningen av costmanagement från olika perspektiv, "ResourceGroup" och "tillhandahåller tjänst".

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### Microsoft. Azure. PowerShell. cmdletar. CostManagement. Models. ICostManagementIdentity

## VÄRDEN

### Microsoft. Azure. PowerShell. cmdletar. CostManagement. Models. Api20200601. IExportExecution

## ANMÄRKNINGAR

ALIAS

KOMPLEXA PARAMETER EGENSKAPER

Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan. Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.


INPUTOBJECT <ICostManagementIdentity> : identitets parameter
  - `[AlertId <String>]`: ID
  - `[ExportName <String>]`: Exportera namn.
  - `[ExternalCloudProviderId <String>]`: Det kan vara ' {externalSubscriptionId} ' för det länkade kontot eller ' {externalBillingAccountId} ' för det konsoliderade kontot som används med dimension/frågor.
  - `[ExternalCloudProviderType <ExternalCloudProviderType?>]`: Typen av extern moln leverantör som är associerad med dimension/frågor. Detta inkluderar ' externalSubscriptions ' för det länkade kontot och ' externalBillingAccounts ' för konsoliderat konto.
  - `[Id <String>]`: Sökväg till resurs identitet
  - `[Scope <String>]`: Omfattningen som är associerad med vyn View. Här ingår "prenumerationer/{subscriptionId}" för abonnemangs omfattningen, "prenumerationer/{subscriptionId}/resourceGroups/{resourceGroupName}" för resourceGroup omfattning "leverantörer/Microsoft. fakturering/billingAccounts/{billingAccountId} ' för fakturerings konto omfattning," leverantörer/Microsoft. fakturering/billingAccounts/{billingAccountId}/avdelningar/{departmentId} "för avdelningens omfattning," leverantörer/Microsoft. fakturering/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId} "för EnrollmentAccount omfattning" providers/Microsoft. fakturering/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId} ' for BillingProfile scope "providers/Microsoft. fakturering/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId} ' för InvoiceSection omfattning" providers/Microsoft. Management/managementGroups/{managementGroupId} "for Management Group scope," providers/Microsoft. CostManagement/externalBillingAccounts/{externalBillingAccountName} "för externa scope för fakturerings konto och" leverantörer/Microsoft. CostManagement/externalSubscriptions/{externalSubscriptionName} "för extern abonnemangs omfattning.
  - `[ViewName <String>]`: Vynamn

## RELATERADE LÄNKAR

