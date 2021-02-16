---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryFilterObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
ms.openlocfilehash: d2adba5ac5c75745c43e0d1ef62fb39d9b867c5e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100230743"
---
# New-AzCostManagementQueryFilterObject

## SYNOPSIS
Skapa ett minnesobjekt för Frågefilter

## SYNTAX

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## BESKRIVNING
Skapa ett minnesobjekt för Frågefilter

## EXEMPEL

### Exempel 1: Skapa ett filterobjekt för en fråga för kostnadshanteringsexport
```powershell
PS C:\> $orDimension = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Value @('East US', 'West Europe')
PS C:\> $orTag = New-AzCostManagementQueryComparisonExpressionObject -Name 'Environment' -Value @('UAT', 'Prod')
PS C:\> New-AzCostManagementQueryFilterObject -or @((New-AzCostManagementQueryFilterObject -Dimension $orDimension), (New-AzCostManagementQueryFilterObject -Tag $orTag))

And       :
Dimension : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
Not       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter
Or        : {Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter, Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter}
Tag       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
```

Med det här kommandot skapas ett filterobjekt för en fråga för export av kostnadshantering.

## PARAMETERS

### Och
Det logiska "OCH"-uttrycket.
Måste innehålla minst 2 objekt.
Skapa genom att gå till avsnittet ANTECKNINGAR för EGENSKAPER OCH och skapa en hash-tabell.

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
Har ett jämförelseuttryck för en dimension.
Skapa genom att gå till avsnittet NOTES för DIMENSIONS-egenskaper och skapa en hash-tabell.

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

### -Not
Det logiska "INTE"-uttrycket.
Skapa genom att gå till avsnittet ANTECKNINGAR för EGENSKAPER INTE och skapa en hash-tabell.

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

### Eller
Det logiska "ELLER"-uttrycket.
Måste innehålla minst 2 objekt.
Skapa genom att gå till avsnittet ANTECKNINGAR för ELLER-egenskaper och skapa en hash-tabell.

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

### -Tag
Har jämförelseuttryck för en tagg.
Skapa genom att gå till avsnittet ANTECKNINGAR för TAG-egenskaper och skapa en hash-tabell.

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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

## UTDATA

### Microsoft.Azure.PowerShell.cmdlets.CostManagement.Models.Api20200601.QueryFilter

## ANTECKNINGAR

ALIAS

KOMPLEXA PARAMETEREGENSKAPER

Skapa de parametrar som beskrivs nedan genom att skapa en hash-tabell som innehåller rätt egenskaper. Om du vill ha information om hash-tabeller kör du Get-Help about_Hash_Tables.


AND <IQueryFilter[]>: Det logiska "OCH"-uttrycket. Måste innehålla minst 2 objekt.
  - `[And <IQueryFilter[]>]`: Det logiska "OCH"-uttrycket. Måste innehålla minst 2 objekt.
  - `[Dimensions <IQueryComparisonExpression>]`: Har jämförelseuttryck för en dimension
    - `Name <String>`: Namnet på kolumnen som ska användas i jämförelse.
    - `Value <String[]>`: Matris med värden som ska användas för jämförelse
  - `[Not <IQueryFilter>]`: Det logiska "INTE"-uttrycket.
  - `[Or <IQueryFilter[]>]`: Det logiska "ELLER"-uttrycket. Måste innehålla minst 2 objekt.
  - `[Tag <IQueryComparisonExpression>]`: Har jämförelseuttryck för en tagg

DIMENSIONS <IQueryComparisonExpression> : Har jämförelseuttryck för en dimension.
  - `Name <String>`: Namnet på kolumnen som ska användas i jämförelse.
  - `Value <String[]>`: Matris med värden som ska användas för jämförelse

NOT: <IQueryFilter> Det logiska "INTE"-uttrycket.
  - `[And <IQueryFilter[]>]`: Det logiska "OCH"-uttrycket. Måste innehålla minst 2 objekt.
  - `[Dimensions <IQueryComparisonExpression>]`: Har jämförelseuttryck för en dimension
    - `Name <String>`: Namnet på kolumnen som ska användas i jämförelse.
    - `Value <String[]>`: Matris med värden som ska användas för jämförelse
  - `[Not <IQueryFilter>]`: Det logiska "INTE"-uttrycket.
  - `[Or <IQueryFilter[]>]`: Det logiska "ELLER"-uttrycket. Måste innehålla minst 2 objekt.
  - `[Tag <IQueryComparisonExpression>]`: Har jämförelseuttryck för en tagg

ELLER <IQueryFilter[]>: Det logiska "ELLER"-uttrycket. Måste innehålla minst 2 objekt.
  - `[And <IQueryFilter[]>]`: Det logiska "OCH"-uttrycket. Måste innehålla minst 2 objekt.
  - `[Dimensions <IQueryComparisonExpression>]`: Har jämförelseuttryck för en dimension
    - `Name <String>`: Namnet på kolumnen som ska användas i jämförelse.
    - `Value <String[]>`: Matris med värden som ska användas för jämförelse
  - `[Not <IQueryFilter>]`: Det logiska "INTE"-uttrycket.
  - `[Or <IQueryFilter[]>]`: Det logiska "ELLER"-uttrycket. Måste innehålla minst 2 objekt.
  - `[Tag <IQueryComparisonExpression>]`: Har jämförelseuttryck för en tagg

TAG <IQueryComparisonExpression> : Har jämförelseuttryck för en tagg.
  - `Name <String>`: Namnet på kolumnen som ska användas i jämförelse.
  - `Value <String[]>`: Matris med värden som ska användas för jämförelse

## RELATERADE LÄNKAR

