---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/export-azurermloganalyticrequestratebyinterval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticRequestRateByInterval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticRequestRateByInterval.md
ms.openlocfilehash: c4008e9b6587e0b6c5b8ed56057490b0aad8764f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581748"
---
# Export-AzureRmLogAnalyticRequestRateByInterval

## Sammanfattning
Exportera loggar som visar API-begäranden som gjorts av detta abonnemang i tidsfönstret för att Visa begränsnings aktiviteter.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Export-AzureRmLogAnalyticRequestRateByInterval [-FromTime] <DateTime> [-GroupByOperationName]
 [-IntervalLength] <IntervalInMins> [-GroupByThrottlePolicy] [-BlobContainerSasUri] <String>
 [-GroupByResourceName] [-ToTime] <DateTime> [-Location] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Exporterar statistik information om prenumerationens samtal till Microsoft. Compute API efter framgång, misslyckad eller begränsad status, i fördefinierade tidsintervall. Loggarna kan grupperas ytterligare med tre parametrar: GroupByOperationName, GroupByThrottlePolicy eller GroupByResourceName.
Observera att den här cmdleten endast samlar in en Compute Resource Provider-loggar; Dessutom finns inte data om resurs typerna disk och ögonblicks bild.

En översikt över API-begränsning för Compute Resource Provider finns i https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits . 

## BESKRIVS

### Exempel 1
```
PS C:\> Export-AzureRmLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByOperationName
```

Det här kommandot lagrar de aggregerade numren för Microsoft. Compute API-samtal avgränsade med lyckat, misslyckat eller begränsat mellan 2018 – 02-20T17:54:14 och 2018-02-22T17:54:17 i angiven SAS URI, aggregerad efter åtgärds namn.

## MALLPARAMETRAR

### -AsJob
Kör cmdlet i bakgrunden

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

### -BlobContainerSasUri
SAS URI för den loggnings-BLOB-behållare som LogAnalytics API skriver ut loggar till.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FromTime
Från tiden i frågan

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GroupByOperationName
Gruppens frågeresultat efter åtgärds namn.

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

### -GroupByResourceName
Grupp frågans resultat efter resurs namn.

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

### -GroupByThrottlePolicy
Grupp frågans resultat efter begränsnings princip tillämpas.

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

### -IntervalLength
Intervall värde i minuter som används för att skapa LogAnalytics samtals taxa.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.IntervalInMins
Parameter Sets: (All)
Aliases:
Accepted values: ThreeMins, FiveMins, ThirtyMins, SixtyMins

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Plats
Den plats där loggen för loggning görs.

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

### -ToTime
Till tid i frågan

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

## VÄRDEN

### Microsoft. Azure. commands. Compute. Automation. Models. PSLogAnalyticsOperationResult

## ANMÄRKNINGAR

## RELATERADE LÄNKAR
