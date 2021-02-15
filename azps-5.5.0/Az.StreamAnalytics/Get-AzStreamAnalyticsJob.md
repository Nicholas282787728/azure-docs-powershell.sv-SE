---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
ms.openlocfilehash: 826089ca0db48e89138e9df78f0aa483b110ba30
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217094"
---
# Get-AzStreamAnalyticsJob

## SYNOPSIS
Hämtar information om Stream Analytics-jobb.

## SYNTAX

### ByResourceGroup
```
Get-AzStreamAnalyticsJob [-ResourceGroupName] <String> [[-Name] <String>] [-NoExpand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### BySubscription
```
Get-AzStreamAnalyticsJob [-NoExpand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Get-AzStreamAnalytics En** lista över alla Stream Analytics-jobb som definierats i Azure-prenumerationen eller den angivna resursgruppen eller får jobbinformation om ett visst jobb inom en resursgrupp.

## EXEMPEL

### EXEMPEL 1: Få information om alla jobb i en prenumeration
```
PS C:\>Get-AzStreamAnalyticsJob
```

Det här kommandot returnerar information om alla Stream Analytics-jobb i Azure-prenumerationen.

### EXEMPEL 2: Få information om alla jobb i en resursgrupp
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

Det här kommandot returnerar information om alla Stream Analytics-jobb i resursgruppen StreamAnalytics-Default-West-US.

### EXEMPEL 3: Få information om ett visst jobb i en resursgrupp
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

Det här kommandot returnerar information om Stream Analytics-jobbet Streaming En i resursgruppen StreamAnalytics-Default-West-US.

## PARAMETERS

### -DefaultProfile
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

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
Anger namnet på Azure Stream Analytics-jobbet som ska hämtas.

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NoExpand
Anger att cmdleten hämtar Azure Stream Analytics-jobbet, men inte returnerar information om dess indata, utdata och transformation.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på den resursgrupp som Azure Stream Analytics-jobbet tillhör.

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
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

### System.Management.Automation.SwitchParameter

## UTDATA

### Microsoft.Azure.Commands.StreamAnalytics.Models.PS Engström

## ANTECKNINGAR

## RELATERADE LÄNKAR

[New-AzStreamAnalytics Till exempel](./New-AzStreamAnalyticsJob.md)

[Remove-AzStreamAnalytics Till exempel](./Remove-AzStreamAnalyticsJob.md)

[Start-AzStreamAnalytics Till exempel](./Start-AzStreamAnalyticsJob.md)

[Stop-AzStreamAnalytics Till exempel](./Stop-AzStreamAnalyticsJob.md)


