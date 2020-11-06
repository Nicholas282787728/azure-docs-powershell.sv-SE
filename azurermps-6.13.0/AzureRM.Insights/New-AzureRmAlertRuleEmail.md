---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleEmail.md
ms.openlocfilehash: f5936bcbbf12308830fd158baa2c2d20f295694b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576268"
---
# New-AzureRmAlertRuleEmail

## Sammanfattning
Skapar en e-poståtgärd för en notifieringsregel.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
New-AzureRmAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureRmAlertRuleEmail** skapar en e-poståtgärd för en notifieringsregel.

## BESKRIVS

### Exempel 1: skapa en e-poståtgärd för aviserings regeln för tjänst ägare
```
PS C:\>New-AzureRmAlertRuleEmail -SendToServiceOwners
```

Det här kommandot skapar en e-poståtgärd för aviserings regeln för att skicka till sina tjänst ägare när en notifieringsregel utlöses.

### Exempel 2: skapa en e-poståtgärd för aviserings regeln för icke-tjänste ägare
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails pattif@contoso.com,davidchew@contoso.net
```

Det här kommandot skapar en e-poståtgärd för aviserings regeln för de angivna e-postadresserna, men inte för tjänste ägarna.

### Exempel 3: skapa en e-poståtgärd för tjänste ägare och ägare som inte tillhör en aviserings regel
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails pattif@contoso.net -SendToServiceOwners
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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

[Add-AzureRmLogAlertRule](./Add-AzureRmLogAlertRule.md)

[Add-AzureRmMetricAlertRule](./Add-AzureRmMetricAlertRule.md)

[Add-AzureRmWebtestAlertRule](./Add-AzureRmWebtestAlertRule.md)

[New-AzureRmAlertRuleWebhook](./New-AzureRmAlertRuleWebhook.md)


