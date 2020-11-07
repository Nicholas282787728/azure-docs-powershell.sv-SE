---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 776249a7a474e3918ed29003f631c984111ca25c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754331"
---
# Get-AzDataLakeAnalyticsComputePolicy

## Sammanfattning
Hämtar en beräknings princip för data Lake Analytics eller en lista över beräknings principer.

## FRÅGESYNTAXEN

```
Get-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Funktionen **Get-AzDataLakeAnalyticsComputePolicy** hämtar en beräknings princip för Azure Data Lake Analytics eller en lista med principer.

## BESKRIVS

### Exempel 1: Hämta en angiven beräknings princip
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

Det här kommandot hämtar den angivna beräknings principen med namnet "policy" i kontot ' contosoadla '.

### Exempel 2: Hämta en lista över alla beräknings principer i kontot
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -AccountName "contosoadla"
```

Det här kommandot får en lista över alla beräknings principer i kontot "contosoadla"

## MALLPARAMETRAR

### -Konto
Namnet på kontot som du vill hämta en beräknings princip från.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
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

### -Namn
Namnet på den beräknings princip som ska erhållas.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Namnet på den resurs grupp som du har kontot för.
Valfritt och försöker upptäcka om det inte tillhandahålls.

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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

## VÄRDEN

### Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy

## ANMÄRKNINGAR

## RELATERADE LÄNKAR
