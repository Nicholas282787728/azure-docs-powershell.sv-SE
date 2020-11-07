---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
ms.openlocfilehash: cfdd18a02a5e0507e86a37dee1e1662bb5094f37
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915634"
---
# New-AzAlertRuleEmail

## Sammanfattning
Skapar en e-poståtgärd för en notifieringsregel.

## FRÅGESYNTAXEN

```
New-AzAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzAlertRuleEmail** skapar en e-poståtgärd för en notifieringsregel.

## BESKRIVS

### Exempel 1: skapa en e-poståtgärd för aviserings regeln för tjänst ägare
```
PS C:\>New-AzAlertRuleEmail -SendToServiceOwners
```

Det här kommandot skapar en e-poståtgärd för aviserings regeln för att skicka till sina tjänst ägare när en notifieringsregel utlöses.

### Exempel 2: skapa en e-poståtgärd för aviserings regeln för icke-tjänste ägare
```
PS C:\>New-AzAlertRuleEmail -CustomEmails pattif@contoso.com,davidchew@contoso.net
```

Det här kommandot skapar en e-poståtgärd för aviserings regeln för de angivna e-postadresserna, men inte för tjänste ägarna.

### Exempel 3: skapa en e-poståtgärd för tjänste ägare och ägare som inte tillhör en aviserings regel
```
PS C:\>New-AzAlertRuleEmail -CustomEmails pattif@contoso.net -SendToServiceOwners
```

Det här kommandot skapar en e-poståtgärd för aviserings regeln för den angivna adressen och dess tjänste ägare.

## MALLPARAMETRAR

### -CustomEmail
Anger en lista med kommaavgränsade e-postadresser.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
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

### -SendToServiceOwner
Anger att den här åtgärden skickar ett e-postmeddelande till tjänste ägarna när regeln utlöses.

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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. string []

### System. Management. Automation. SwitchParameter

## VÄRDEN

### Microsoft. Azure. Management. Monitoring. Management. Models. RuleEmailAction

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzLogAlertRule](./Add-AzLogAlertRule.md)

[Add-AzMetricAlertRule](./Add-AzMetricAlertRule.md)

[Add-AzWebtestAlertRule](./Add-AzWebtestAlertRule.md)

[New-AzAlertRuleWebhook](./New-AzAlertRuleWebhook.md)


