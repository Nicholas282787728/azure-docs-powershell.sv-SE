---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 1EC96B4E-7731-4EE3-A0C1-EA0793F0FE5C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Stop-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Stop-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 990cd9d10dd90ee68c179fa65ea4d0575bdda1d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574467"
---
# Stop-AzureRmStreamAnalyticsJob

## Sammanfattning
Stoppar ett ström analys jobb.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Stop-AzureRmStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Stop-AzureRmStreamAnalyticsJob** asynkront stoppar ett ström analys jobb som körs i Azure och avallokerar resurser som användes.
Jobb definitionen och metadata är tillgängliga i ditt abonnemang via både Azure Portal och Management API: er, så att jobbet kan redige ras och startas om.
Du kommer inte att debiteras för ett jobb i stoppat tillstånd.

## BESKRIVS

### EXEMPEL 1: stoppa ett pågående jobb
```
PS C:\>Stop-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

Det här kommandot stoppar jobbets StreamingJob.

## MALLPARAMETRAR

### -Namn
Anger namnet på Azure Stream Analytics-jobbet som ska stoppas.

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

### -ResourceGroupName
Anger namnet på den resurs grupp som Azure Stream Analytics-jobbet tillhör.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### System. Object

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmStreamAnalyticsJob](./Get-AzureRmStreamAnalyticsJob.md)

[Get-AzureRmStreamAnalyticsJob](./Get-AzureRmStreamAnalyticsJob.md)

[New-AzureRmStreamAnalyticsJob](./New-AzureRmStreamAnalyticsJob.md)

[Remove-AzureRmStreamAnalyticsJob](./Remove-AzureRmStreamAnalyticsJob.md)

[Start-AzureRmStreamAnalyticsJob](./Start-AzureRmStreamAnalyticsJob.md)


