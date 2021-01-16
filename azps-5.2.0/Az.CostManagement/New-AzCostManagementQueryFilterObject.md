---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryFilterObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
ms.openlocfilehash: e7b5c605af531bd1c1251a1c615da9498059d43d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395531"
---
# New-AzCostManagementQueryFilterObject

## Sammanfattning
Skapa ett objekt i minnet för QueryFilter

## FRÅGESYNTAXEN

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Skapa ett objekt i minnet för QueryFilter

## BESKRIVS

### Exempel 1: skapa ett filter objekt av fråga för export av kostnads hantering
```powershell
PS C:\> $orDimension = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Operator In -Value @('East US', 'West Europe')
PS C:\> $orTag = New-AzCostManagementQueryComparisonExpressionObject -Name 'Environment' -Operator In -Value @('UAT', 'Prod')
PS C:\> New-AzCostManagementQueryFilterObject -or @((New-AzCostManagementQueryFilterObject -Dimension $orDimension), (New-AzCostManagementQueryFilterObject -Tag $orTag))

And       :
Dimension : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
Not       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter
Or        : {Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter, Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter}
Tag       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
```

Det här kommandot skapar ett filter objekt av fråga för export av kostnads hantering.

## MALLPARAMETRAR

### -Och
Det logiska uttrycket "och".
Måste innehålla minst två objekt.
För att konstruera kan du läsa avsnittet anteckningar och skapa en hash-tabell.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Dimensioner
Har jämförelse uttryck för en dimension.
Om du vill skapa läser du avsnittet anteckningar för egenskaper och skapar en hash-tabell.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryComparisonExpression
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inte
Det logiska uttrycket "inte".
För att konstruera kan du läsa avsnittet anteckningar och skapa en hash-tabell.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Eller
Det logiska uttrycket "eller".
Måste innehålla minst två objekt.
För att konstruera, se avsnittet anteckningar för eller egenskaper och skapa en hash-tabell.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tagg
Har jämförelse uttryck för en tagg.
För att konstruera kan du läsa avsnittet anteckningar för TAGGEGENSKAPER och skapa en hash-tabell.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryComparisonExpression
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

## VÄRDEN

### Microsoft. Azure. PowerShell. cmdletar. CostManagement. Models. Api20200601. QueryFilter

## ANMÄRKNINGAR

ALIAS

KOMPLEXA PARAMETER EGENSKAPER

Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan. Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.


OCH <IQueryFilter [] >: det logiska uttrycket "AND". Måste innehålla minst två objekt.
  - `[And <IQueryFilter[]>]`: Det logiska uttrycket "och". Måste innehålla minst två objekt.
  - `[Dimensions <IQueryComparisonExpression>]`: Jämförelse uttryck för en dimension
    - `Name <String>`: Namnet på den kolumn som ska användas vid jämförelse.
    - `Operator <OperatorType>`: Den operator som ska användas för jämförelse.
    - `Value <String[]>`: Matris med värden som ska användas för jämförelse
  - `[Not <IQueryFilter>]`: Det logiska uttrycket "inte".
  - `[Or <IQueryFilter[]>]`: Det logiska uttrycket "eller". Måste innehålla minst två objekt.
  - `[Tag <IQueryComparisonExpression>]`: Jämförelse uttryck för en tagg

MÅTT <IQueryComparisonExpression> : har jämförelse uttryck för en dimension.
  - `Name <String>`: Namnet på den kolumn som ska användas vid jämförelse.
  - `Operator <OperatorType>`: Den operator som ska användas för jämförelse.
  - `Value <String[]>`: Matris med värden som ska användas för jämförelse

INTE <IQueryFilter> : det logiska uttrycket "inte".
  - `[And <IQueryFilter[]>]`: Det logiska uttrycket "och". Måste innehålla minst två objekt.
  - `[Dimensions <IQueryComparisonExpression>]`: Jämförelse uttryck för en dimension
    - `Name <String>`: Namnet på den kolumn som ska användas vid jämförelse.
    - `Operator <OperatorType>`: Den operator som ska användas för jämförelse.
    - `Value <String[]>`: Matris med värden som ska användas för jämförelse
  - `[Not <IQueryFilter>]`: Det logiska uttrycket "inte".
  - `[Or <IQueryFilter[]>]`: Det logiska uttrycket "eller". Måste innehålla minst två objekt.
  - `[Tag <IQueryComparisonExpression>]`: Jämförelse uttryck för en tagg

ELLER <IQueryFilter [] >: det logiska uttrycket "eller". Måste innehålla minst två objekt.
  - `[And <IQueryFilter[]>]`: Det logiska uttrycket "och". Måste innehålla minst två objekt.
  - `[Dimensions <IQueryComparisonExpression>]`: Jämförelse uttryck för en dimension
    - `Name <String>`: Namnet på den kolumn som ska användas vid jämförelse.
    - `Operator <OperatorType>`: Den operator som ska användas för jämförelse.
    - `Value <String[]>`: Matris med värden som ska användas för jämförelse
  - `[Not <IQueryFilter>]`: Det logiska uttrycket "inte".
  - `[Or <IQueryFilter[]>]`: Det logiska uttrycket "eller". Måste innehålla minst två objekt.
  - `[Tag <IQueryComparisonExpression>]`: Jämförelse uttryck för en tagg

TAGG <IQueryComparisonExpression> : har jämförelse uttryck för en tagg.
  - `Name <String>`: Namnet på den kolumn som ska användas vid jämförelse.
  - `Operator <OperatorType>`: Den operator som ska användas för jämförelse.
  - `Value <String[]>`: Matris med värden som ska användas för jämförelse

## RELATERADE LÄNKAR

