---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 2001E040-5551-40C3-81D2-9A8334DE02BF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7692d4407df8fb4af8647ee0b4490abe73b2c937
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093284"
---
# Get-AzureStorSimpleJob

## Sammanfattning
Hämtar StorSimple-jobb.

## FRÅGESYNTAXEN

```
Get-AzureStorSimpleJob [-DeviceName <String>] [-InstanceId <String>] [-Status <String>] [-Type <String>]
 [-From <DateTime>] [-To <DateTime>] [-Skip <Int32>] [-First <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureStorSimpleJob** får Azure StorSimple-jobb.
Ange ett instans-ID för att hämta ett specifikt jobb.
Ange andra parametrar för att begränsa vilka jobb som denna cmdlet får.

Denna cmdlet returnerar maximalt 200-jobb.
Om det finns fler än 200 jobb kan du hämta de återstående utskrifterna med hjälp av parametrarna *First* och *Skip* .
Om du anger ett värde på 100 för *Skip* och 50 för *First* returnerar denna cmdlet inte de första 100-resultaten.
Den returnerar nästföljande 50-resultat efter 100.

## BESKRIVS

### Exempel 1: Hämta ett jobb genom att använda ett ID
```
PS C:\>Get-AzureStorSimpleJob -InstanceId "574f47e0-44e9-495c-b8a5-0203c57ebf6d"
BackupPolicy             : 
BackupTimeStamp          : 1/1/0001 12:00:00 AM
BackupType               : CloudSnapshot
DataStats                : Microsoft.WindowsAzure.Management.StorSimple.Models.DataStatistics
Device                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
Entity                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
ErrorDetails             : {}
HideProgressDetails      : False
InstanceId               : 574f47e0-44e9-495c-b8a5-0203c57ebf6d
IsInstantRestoreComplete : False
IsJobCancellable         : True
JobDetails               : Microsoft.WindowsAzure.Management.StorSimple.Models.JobStatusInfo
Name                     : 26447caf-59bb-41c9-a028-3224d296c7dc
Progress                 : 100
SourceDevice             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
SourceEntity             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
SourceVolume             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
Status                   : Completed
TimeStats                : Microsoft.WindowsAzure.Management.StorSimple.Models.TimeStatistics
Type                     : Backup
Volume                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
```

Med det här kommandot får du information om det jobb som har angivet ID.

### Exempel 2: Hämta jobb genom att använda ett enhets namn
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "8600-Bravo 001" -First 2
InstanceId                           Type                         Status                                          DeviceName                                      StartTime                                       Progress                                       
----------                           ----                         ------                                          ----------                                      ---------                                       --------                                       
1997c33f-bfcc-4d08-9aba-28068340a1f9 Backup                       Running                                         8600-Bravo 001                                  4/15/2015 1:30:02 PM                            92                                             
85074062-ef6a-408a-b6c9-2a0904bb99ca Backup                       Completed                                       8600-Bravo 001                                  4/15/2015 1:30:02 PM                            100
```

Med det här kommandot får du information om jobben för enheten som heter 8600-Bravo 001.
Kommandot får de två första jobben för enheten.

### Exempel 3: Hämta färdiga jobb
```
PS C:\>Get-AzureStorSimpleJob -Status "Completed" -Skip 10 -First 2
```

Det här kommandot får färdiga jobb.
Kommandot får bara de två första jobben när de hoppat över de tio första jobben.

### Exempel 4: Hämta manuella säkerhets kopierings jobb
```
PS C:\>Get-AzureStorSimpleJob -Type "ManualBackup"
```

Det här kommandot hämtar utskrifts typen manuell säkerhets kopiering.

### Exempel 5: Hämta jobb mellan angivna tider
```
PS C:\>$StartTime = Get-Date -Year 2015 -Month 3 -Day 10
PS C:\> $EndTime = Get-Date -Year 2015 -Month 3 -Day 11 -Hour 12 -Minute 15
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" -From $StartTime -To $EndTime
```

De två första kommandona skapar **datetime** -objekt med hjälp av Get-Date cmdlet.
I kommandona lagras de nya tiderna i $StartTime och $EndTime variabler.
Om du vill ha mer information skriver du `Get-Help Get-Date` .

Med kommandot slut hämtas jobb för enheten som heter Device07 mellan tiderna som lagras i $StartTime och $EndTime.

## MALLPARAMETRAR

### -Enhets namn
Anger namnet på en StorSimple-enhet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Först
Hämtar bara angivet antal objekt.
Ange antalet objekt som ska visas.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Från
Anger start datum och-tid för de jobb som denna cmdlet får.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceId
Anger ID för det jobb som ska visas.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Anger den Azure-profil från vilken denna cmdlet läser.
Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.

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

### -Hoppa över
Ignorerar angivet antal objekt och hämtar sedan återstående objekt.
Ange antalet objekt som ska hoppas över.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Status
Anger status.
De acceptabla värdena för den här parametern är:

- Aktiv
- Rätta
- Annullerats
- Startade
- Avbryta
- CompletedWithErrors

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -För att
Anger slutdatum och slut tid för de jobb som denna cmdlet får.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Skriv
Anger jobb typen.
De acceptabla värdena för den här parametern är:

- Reservdomänkontrollant
- ManualBackup
- Terställa
- CloneWorkflow
- DeviceRestore
- Uppdatera
- SupportPackage
- VirtualApplianceProvisioning

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen
Det går inte att pipe in i denna cmdlet.

## VÄRDEN

### IList \<DeviceJobDetails\> , DeviceJobDetails
Denna cmdlet returnerar en lista med jobb informations objekt, eller om du anger *InstanceID* -parametern, returnerar den ett enskilt jobb informations objekt.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Stopp-AzureStorSimpleJob](./Stop-AzureStorSimpleJob.md)


