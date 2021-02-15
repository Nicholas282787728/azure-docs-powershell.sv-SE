---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E1FC931E-4EB8-4DCA-92BD-8013DDC13219
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationWebhook.md
ms.openlocfilehash: 88881e9ca5869bc2f63f4cec7c3993facc2cb3f6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235063"
---
# New-AzAutomationWebhook

## SYNOPSIS
Skapar en webhook för en automatiseringskörningsbok.

## SYNTAX

```
New-AzAutomationWebhook [-Name] <String> [-RunbookName] <String> [-IsEnabled] <Boolean>
 [-ExpiryTime] <DateTimeOffset> [-Parameters <IDictionary>] [-Force] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESKRIVNING
Den **nya azAutomationWebhook-cmdleten** skapar en webhook för en Azure Automation-runbook.
Se till att spara webhook-URL:en som denna cmdlet returnerar, eftersom den inte kan hämtas igen.

## EXEMPEL

### Exempel 1: Skapa en webhook
```
PS C:\>$Webhook = New-AzAutomationWebhook -Name "Webhook06" -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

Det här kommandot skapar en webhook med namnet Webhook06 för runbooken ContosoRunbook i automatiseringskontot AutomationAccount01.
Kommandot lagrar webhook i variabeln $Webhook variabeln.
Webhook är aktiverat.
Webhook går ut vid den angivna tiden.
Det här kommandot anger inga värden för webhook-parametrar.
Det här kommandot anger *force-parametern.*
Därför uppmanas du inte att bekräfta.

### Exempel 2: Skapa en webhook med parametrar
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> $Webhook = New-AzAutomationWebhook -Name "Webhook11" -Parameters $Params -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

Det första kommandot skapar en ordlista med parametrar och lagrar dem i $Params variabeln.
Det andra kommandot skapar en webhook med namnet Webhook11 för runbooken ContosoRunbook i automatiseringskontot AutomationAccount01.
Kommandot tilldelar parametrarna i $Params till webhook.

## PARAMETERS

### -AutomationAccountName
Anger namnet på ett automatiseringskonto där den här cmdleten skapar en webhook.

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

### -ExpiryTime
Anger utgångstiden för webhook som ett **DateTimeOffset-objekt.**
Du kan ange en sträng eller en **DateTime som** kan konverteras till en giltig **DateTimeOffset.**

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
ps_force

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

### -IsEnabled
Anger om webhook är aktiverat.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Anger ett namn för webhook.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Parametrar
Anger en ordlista med nyckel-/värdepar.
Nycklarna är runbook-parameternamnen.
Värdena är runbook-parametervärdena.
När runbook startar som svar på en webhook överförs dessa parametrar till runbooken.

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på resursgruppen för vilken den här cmdleten skapar en webhook.

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

### -RunbookName
Anger namnet på den runbook som ska associeras med webhook.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RunOn
Valfritt namn på hybrid worker-gruppen som ska köra runbooken

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bekräfta
Frågar dig om bekräftelse innan du kör cmdleten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som skulle hända om cmdleten körs.
Cmdleten körs inte.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### System.String

### System.Boolean

### System.DateTimeOffset

## UTDATA

### Microsoft.Azure.Commands.Automation.Model.Webhook

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzAutomationWebhook](./Get-AzAutomationWebhook.md)

[Remove-AzAutomationWebhook](./Remove-AzAutomationWebhook.md)

[Set-AzAutomationWebhook](./Set-AzAutomationWebhook.md)


