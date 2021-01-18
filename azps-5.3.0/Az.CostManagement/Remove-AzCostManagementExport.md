---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/remove-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Remove-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Remove-AzCostManagementExport.md
ms.openlocfilehash: 75c1f01730d4dfe3e9769a430f874887fd2d2090
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524277"
---
# Remove-AzCostManagementExport

## Sammanfattning
Åtgärden att ta bort en export.

## FRÅGESYNTAXEN

### Ta bort (standard)
```
Remove-AzCostManagementExport -Name <String> -Scope <String> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### DeleteViaIdentity
```
Remove-AzCostManagementExport -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Åtgärden att ta bort en export.

## BESKRIVS

### Exempel 1: ta bort AzCostManagementExport efter omfattning och namn
```powershell
PS C:\> Remove-AzCostManagementExport -Scope 'subscriptions/********' -name 'TestExportDatasetAggregationInfoYouri'


```

Ta bort AzCostManagementExport efter omfattning och ExportName

### Exempel 2: ta bort AzCostManagementExport efter Exportera-objekt
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Scope 'subscriptions/*********' -name 'TestExportDatasetAggregationYouori'
Remove-AzCostManagementExport -InputObject $getExport


```

Ta bort AzCostManagementExport med InputObject

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

### -InputObject
Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Namn
Exportera namn.

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Returnerar true när kommandot lyckas

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

### -Omfattning
Den här parametern definierar omfattningen av costmanagement från olika perspektiv, "ResourceGroup" och "tillhandahåller tjänst".

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### Microsoft. Azure. PowerShell. cmdletar. CostManagement. Models. ICostManagementIdentity

## VÄRDEN

### System. Boolean

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

