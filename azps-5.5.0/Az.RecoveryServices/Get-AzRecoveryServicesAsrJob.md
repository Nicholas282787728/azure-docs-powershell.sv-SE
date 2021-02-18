---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: a367fd8643dc29901f8dfafdbecd59a8386320a7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100252093"
---
# Get-AzRecoveryServicesAsrJob

## SYNOPSIS
Hämtar information om det angivna ASR-jobbet eller listan med de senaste ASR-jobben i valv för Recovery Services.

## SYNTAX

### ByParam (standard)
```
Get-AzRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Get-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObject
```
Get-AzRecoveryServicesAsrJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Get-AzRecoveryServicesAsr Engström** får Azure Site Recovery-jobb.
Du kan använda den här cmdleten för att visa ASR-jobben i Recovery Services-valvet.

## EXEMPEL

### Exempel 1
```powershell
PS C:\> $jobs = Get-AzRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

Returnerar alla jobb på ett visst ASR-objekt (referera till ASR-objektet, till exempel replikerat objekt eller återställningsplan efter dess ID.) 

### Exempel 2

Hämtar information om det angivna ASR-jobbet eller listan med de senaste ASR-jobben i valv för Recovery Services. (autogenererat)

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesAsrJob -Job $Job
```

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

### -EndTime
Anger sluttiden för jobben.
Med den här cmdleten får du alla jobb som startats före den angivna tiden.
Använd cmdleten Get-Date för att hämta ett **DateTime-objekt** för den här parametern.
Om du vill ha mer information skriver du `Get-Help Get-Date` .

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Job
Anger ASR-jobbobjektet som du vill få uppdaterad information om.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Ange ASR-jobbet efter namn.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartTime
Anger starttiden för jobben.
Med den här cmdleten får du alla jobb som startats efter den angivna tiden.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Delstat
Anger statusen för ett ASR-jobb.
Den här cmdleten hämtar alla jobb som matchar det angivna tillståndet.
De godtagbara värdena för den här parametern är:

- NotStarted
- InProgress
- Lyckades
- Annat
- Misslyckades
- Annullerad
- Pausad

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetObjectId
Anger objektets ID. Används för att söka efter jobb på det angivna objektet.

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRLow

## UTDATA

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRLow

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Restart-AzRecoveryServicesAsr Eng](./Restart-AzRecoveryServicesAsrJob.md)

[Resume-AzRecoveryServicesAsr Eng](./Resume-AzRecoveryServicesAsrJob.md)

[Stop-AzRecoveryServicesAsr Eng](./Stop-AzRecoveryServicesAsrJob.md)
