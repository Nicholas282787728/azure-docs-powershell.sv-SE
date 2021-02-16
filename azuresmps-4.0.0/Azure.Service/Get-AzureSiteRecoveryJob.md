---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2957C0DE-3A2F-4337-A778-2B95654972E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8a7c99e2ce307d700e43094ffa9be47e5449acc0
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411661"
---
# Get-AzureSiteRecoveryJob

## SYNOPSIS
Hämtar åtgärdsinformationen för ett valv för webbplatsåterställning.

## SYNTAX

### ByParam (standard)
```
Get-AzureSiteRecoveryJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ById
```
Get-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByObject
```
Get-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Get-AzureSiteRecovery Enl.** får Azure Site Recovery-jobb.
Du kan använda den här cmdleten för att visa åtgärdsinformationen för det aktuella webbplatsåterställningsvalvet.

## EXEMPEL

### Exempel 1: Få ett jobb genom att ange ett ID
```
PS C:\> Get-AzureSiteRecoveryJob -Id "033785cc-9f72-4f07-8e78-e4d1e942a7ae" 
Name             : SaveRecoveryPlan
ID               : 033785cc-9f72-4f07-8e78-e4d1e942a7ae
ClientRequestId  : d604206b-32e1-4d5b-9a23-32b118d14a1e-2015-02-20 07:20:42Z-P
State            : Succeeded
StateDescription : Completed
StartTime        : 20-02-2015 07:20:45 +05:30
EndTime          : 20-02-2015 07:20:46 +05:30
TargetObjectId   : cfb445bf-fd14-4b5d-b9ac-5154e1415ef2
TargetObjectType : RecoveryPlan
TargetObjectName : RP
AllowedActions   : {Cancel}
Tasks            : {Save a recovery plan task}
Errors           : {}
```

Det här kommandot hämtar Azure-webbplatsåterställningsjobbet som har det angivna ID:t.

### Exempel 2: Får ett jobb baserat på tid
```
PS C:\> Get-AzureSiteRecoveryJob -StartTime "20-02-2015 01:00:00" -EndTime "21-02-2015 01:00:00"
Name             : SaveRecoveryPlan
ID               : 033785cc-9f72-4f07-8e78-e4d1e942a7ae
ClientRequestId  : d604206b-32e1-4d5b-9a23-32b118d14a1e-2015-02-20 07:20:42Z-P
State            : Succeeded
StateDescription : Completed
StartTime        : 20-02-2015 07:20:45 +05:30
EndTime          : 20-02-2015 07:20:46 +05:30
TargetObjectId   : cfb445bf-fd14-4b5d-b9ac-5154e1415ef2
TargetObjectType : RecoveryPlan
TargetObjectName : RP
AllowedActions   : {Cancel}
Tasks            : {Save a recovery plan task}
Errors           : {}
```

Med det här kommandot får du Jobb för webbplatsåterställning som faller mellan den angivna starttiden och sluttiden.

## PARAMETERS

### -EndTime
Anger sluttiden för jobben.
Med den här cmdleten får du alla jobb som startats före den angivna tiden.
Om du vill **hämta ett DateTime-objekt** använder du cmdleten **Get-Date.**
Om du vill ha mer information skriver du `Get-Help Get-Date` .

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
Anger ID för ett jobb som ska fås.

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Job
Anger ett jobb som ska fås.

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Profile
Anger den Azure-profil som cmdleten läser upp.
Om du inte anger en profil läser den här cmdleten från den lokala standardprofilen.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartTime
Anger starttiden för jobben.
Med den här cmdleten får du alla jobb som startats efter den angivna tiden.

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Delstat
Anger indatatillståndet för ett Webbplatsåterställning-jobb.
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
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetObjectId
Anger ID för det objekt som jobbet har som mål.

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

## UTDATA

## ANTECKNINGAR

## RELATERADE LÄNKAR



[Restart-AzureSiteRecovery Etti](./Restart-AzureSiteRecoveryJob.md)

[Resume-AzureSiteRecovery Eni](./Resume-AzureSiteRecoveryJob.md)

[Stop-AzureSiteRecovery Etti](./Stop-AzureSiteRecoveryJob.md)


