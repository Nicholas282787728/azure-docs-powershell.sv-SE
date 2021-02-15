---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
ms.openlocfilehash: 7d9ed01346c04974fb43d7e3b233badb7a185dc2
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100396038"
---
# New-AzAlertRuleEmail

## SYNOPSIS
Skapar en e-poståtgärd för en aviseringsregel.

## SYNTAX

```
New-AzAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **New-AzAlertRuleEmail** skapar en e-poståtgärd för en aviseringsregel.

## EXEMPEL

### Exempel 1: Skapa en e-poståtgärd för aviseringsregel för tjänstägare
```
PS C:\>New-AzAlertRuleEmail -SendToServiceOwners
```

Med det här kommandot skapas en e-poståtgärd för aviseringsregel som skickas till dess tjänstägare när en aviseringsregel är en aviseringsregel.

### Exempel 2: Skapa en e-poståtgärd för aviseringsregel för ägare som inte är tjänstägare
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.com,davidchew@contoso.net
```

Med det här kommandot skapas en e-poståtgärd för aviseringsregel för de angivna e-postadresserna, men inte för tjänstägarna.

### Exempel 3: Skapa en e-poståtgärd för aviseringsregel för tjänstägare och icke-tjänstägare
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.net -SendToServiceOwners
```

Med det här kommandot skapas en e-poståtgärd för aviseringsregel för den angivna adressen och för dess tjänstägare.

## PARAMETERS

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
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure

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
Anger att den här åtgärden skickar ett e-postmeddelande till tjänstägarna när regeln brandar.

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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### System.String[]

### System.Management.Automation.SwitchParameter

## UTDATA

### Microsoft.Azure.Management.monitor.Management.Models.ruleemailAction

## ANTECKNINGAR

## RELATERADE LÄNKAR


[Add-AzMetricAlertRule](./Add-AzMetricAlertRule.md)

[Add-AzWebtestAlertRule](./Add-AzWebtestAlertRule.md)

[New-AzAlertRuleWebhook](./New-AzAlertRuleWebhook.md)


