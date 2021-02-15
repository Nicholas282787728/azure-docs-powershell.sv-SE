---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F281B351-F7C7-47D1-9745-FFE4BAA840FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsJob.md
ms.openlocfilehash: ed5b11684fdb8701343c9390962e95942f4075e9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217046"
---
# New-AzStreamAnalyticsJob

## SYNOPSIS
Skapar eller uppdaterar ett Stream Analytics-jobb.

## SYNTAX

```
New-AzStreamAnalyticsJob [[-Name] <String>] [-File] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **New-AzStreamAnalytics En** cmdlet skapar ett nytt Stream Analytics-jobb i Azure eller uppdaterar definitionen av ett befintligt angivet jobb.
Du kan ange namnet på jobbet i . JSON-fil eller på kommandoraden.
Om båda har angetts måste namnet på kommandoraden matcha namnet i filen.
Om du anger ett jobbnamn som redan finns och inte anger *force-parametern* frågar cmdleten om det befintliga jobbet ska ersättas.
Om du anger *force-parametern* och anger ett befintligt jobbnamn ersätts jobbdefinitionen utan bekräftelse.

## EXEMPEL

### EXEMPEL 1: Skapa ett jobb
```
PS C:\>New-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json"
```

Det här kommandot skapar ett jobb från definitionen i JobDefinition.jspå.
Om ett befintligt jobb med det angivna namnet i jobbdefinitionsfilen redan har definierats frågar cmdleten om den ska ersätta den.

### EXEMPEL 2: Ersätta en jobbdefinition
```
PS C:\>New-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json" -Name "StreamingJob" -Force
```

Det här kommandot ersätter jobbdefinitionen för Streaming Streaming Streaming utan bekräftelse.

## PARAMETERS

### -DefaultProfile
Autentiseringsuppgifterna, kontot, klientorganisationen och prenumerationen som används för kommunikation med Azure.

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

### -Arkiv
Anger sökvägen till en JSON-fil som innehåller JSON-representationen av Azure Stream Analytics-jobbet som ska skapas.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Tvingar kommandot att köras utan att användaren uppmanas att bekräfta.

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

### -Name
Anger namnet på Azure Stream Analytics-jobbet som ska skapas.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på den resursgrupp som Azure Stream Analytics-jobbet ska tillhöra.

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

## UTDATA

### Microsoft.Azure.Commands.StreamAnalytics.Models.PS Engström

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzStreamAnalytics Till exempel](./Get-AzStreamAnalyticsJob.md)

[Remove-AzStreamAnalytics Till exempel](./Remove-AzStreamAnalyticsJob.md)

[Start-AzStreamAnalytics Till exempel](./Start-AzStreamAnalyticsJob.md)

[Stop-AzStreamAnalytics Till exempel](./Stop-AzStreamAnalyticsJob.md)

[Stop-AzStreamAnalytics Till exempel](./Stop-AzStreamAnalyticsJob.md)


