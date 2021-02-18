---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: B5914F65-CAF8-4647-BA78-49B65DD6D67A
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/start-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
ms.openlocfilehash: 1194a730293d6f0f7b4aca58f508f808a2c6193e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100216983"
---
# Start-AzStreamAnalyticsJob

## SYNOPSIS
Startar ett Stream Analytics-jobb.

## SYNTAX

```
Start-AzStreamAnalyticsJob [-Name] <String> [[-OutputStartMode] <String>] [[-OutputStartTime] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
**Start-AzStreamAnalytics** Streaming-cmdleten asynkront distribuerar och startar ett Stream Analytics-jobb i Azure.

## EXEMPEL

### Exempel 1: Starta ett Stream Analytics-jobb
```powershell
PS C:\> Start-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob" -OutputStartMode "CustomTime" -OutputStartTime "2014-07-03T01:00Z"
```

Det här kommandot startar jobbet Streaming En Streaming En och anger att utdatahändelseströmmen ska starta vid tidsstämpel 2014-07-03T01:00Z.

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

### -Name
Anger namnet på Azure Stream Analytics-jobbet som ska startas.

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

### -OutputStartMode
Anger startläget för jobbet.
Giltiga värden är: 
- JobStartTime – Det här värdet anger att startpunkten för utdatahändelseströmmen ska starta när jobbet startas.
- CustomTime – Det här värdet anger att utgångspunkten för utdatahändelseströmmen ska starta vid en anpassad tidpunkt som anges i *parametern OutputStartTime.* 
 - LastOutputEventTime – Det här värdet anger att startpunkten för utdatahändelseströmmen ska starta från den senaste utdatatiden för händelsen.
Om egenskapen inte är det är JobStartTime som standard.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OutputStartTime
Anger starttiden för utdata.
Det här värdet är antingen en ISO-8601-formaterad tidsstämpel som anger startpunkten för utdatahändelseströmmen eller $Null för att ange att utdatahändelseströmmen startar när direktuppspelningsjobbet startas.
Den här egenskapen måste ha ett värde *om OutputStartMode* är inställt på CustomTime.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på den resursgrupp som Azure Stream Analytics-jobbet tillhör.

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

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### System.String

### System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## UTDATA

### System.Boolean

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzStreamAnalytics Till exempel](./Get-AzStreamAnalyticsJob.md)

[New-AzStreamAnalytics Till exempel](./New-AzStreamAnalyticsJob.md)

[Remove-AzStreamAnalytics Till exempel](./Remove-AzStreamAnalyticsJob.md)

[Stop-AzStreamAnalytics Till exempel](./Stop-AzStreamAnalyticsJob.md)


