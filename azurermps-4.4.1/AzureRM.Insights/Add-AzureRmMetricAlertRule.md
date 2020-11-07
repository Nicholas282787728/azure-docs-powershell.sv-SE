---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A90564B5-57D7-48EB-976D-38C03D930289
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmMetricAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmMetricAlertRule.md
ms.openlocfilehash: 9a215195ada1d804d2c139ed748eb844df46eed5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758061"
---
# Add-AzureRmMetricAlertRule

## Sammanfattning
Lägger till eller uppdaterar en Metric-baserad notifieringsregel.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Add-AzureRmMetricAlertRule -WindowSize <TimeSpan> -Operator <ConditionOperator> -Threshold <Double>
 -TargetResourceId <String> -MetricName <String> -TimeAggregationOperator <TimeAggregationOperator>
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroup <String> -Name <String>
 [-Actions <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Add-AzureRmMetricAlertRule** lägger till eller uppdaterar en Metric-baserad notifieringsregel.
Den tillagda regeln associeras med en resurs grupp och har ett namn.

## BESKRIVS

### Exempel 1: lägga till en regel för att varna på en webbplats
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -Description "Pura Vida" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
33574ccf-0b01-43b4-aa97-87e6bbcf1c11                                                                         Created
```

Det här kommandot skapar en regel för att varna för en webbplats.

### Exempel 2: inaktivera en regel
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup Default-Web-EastUS -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -TimeAggregationOperator Total 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
96c489f1-8529-46e1-a76d-2c1463ca3116                                                                                 OK
```

Det här kommandot inaktiverar en regel.
Om regeln inte finns skapas den avaktiverad.
Om regeln finns inaktive ras den bara.

### Exempel 3: lägga till en regel med åtgärder
```
PS C:\>Add-AzureRmMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 1 -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -MetricName "Requests" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

Det här kommandot skapar en regel för att varna för en webbplats.

## MALLPARAMETRAR

### -Åtgärder
Anger en kommaavgränsad lista med åtgärder.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Beskrivning
Anger en beskrivning av regeln.

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

### -DisableRule
Inaktiverar regeln.
Om du inte anger den här parametern aktive ras regeln.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Plats
Anger platsen där regeln är definierad.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MetricName
Anger namnet på det mått som regeln övervakar.
Ange endast den här parametern för Metric-baserade regler.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namn
Anger namnet på regeln.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Operatör
Anger Relations operatorn för regelns villkor.
De acceptabla värdena för den här parametern är:

- GreaterThan
- GreaterThanOrEqual
-  Mindreän
- LessThanOrEqual

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ConditionOperator
Parameter Sets: (All)
Aliases: 
Accepted values: GreaterThan, GreaterThanOrEqual, LessThan, LessThanOrEqual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroup
Anger namnet på resurs gruppen för regeln.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TargetResourceId
Anger ID för den resurs som regeln övervakar. Obs! det går inte att uppdatera den här egenskapen för en befintlig notifieringsregel.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tröskel
Anger tröskeln för regeln.

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TimeAggregationOperator
Anger den mängd operator som ska användas för tidsfönstret när regeln utvärderas.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationOperator]
Parameter Sets: (All)
Aliases: 
Accepted values: Average, Minimum, Maximum, Total, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WindowSize
Anger tidsfönstrets storlek för regeln för att beräkna dess data.

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
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

### Microsoft. Azure. commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzureRmLogAlertRule](./Add-AzureRmLogAlertRule.md)

[Add-AzureRmWebtestAlertRule](./Add-AzureRmWebtestAlertRule.md)

[Get-AzureRmAlertHistory](./Get-AzureRmAlertHistory.md)

[Get-AzureRmAlertRule](./Get-AzureRmAlertRule.md)

[New-AzureRmAlertRuleEmail](./New-AzureRmAlertRuleEmail.md)

[New-AzureRmAlertRuleWebhook](./New-AzureRmAlertRuleWebhook.md)

[Remove-AzureRmAlertRule](./Remove-AzureRmAlertRule.md)


