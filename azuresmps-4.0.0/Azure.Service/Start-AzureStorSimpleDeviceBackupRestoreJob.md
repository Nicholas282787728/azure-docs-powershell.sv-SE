---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F9C8D0AA-ED97-43E8-ADB1-5AE1A4517666
online version: ''
schema: 2.0.0
ms.openlocfilehash: c524bb90d84df6ad3e37b552b957dac2d75b6a6c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093473"
---
# Start-AzureStorSimpleDeviceBackupRestoreJob

## Sammanfattning
Startar ett jobb som återställer en säkerhets kopia på en StorSimple-enhet.

## FRÅGESYNTAXEN

### Tom (standard)
```
Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName <String> -BackupId <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyById
```
Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName <String> -BackupId <String> -SnapshotId <String>
 [-WaitForComplete] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Start-AzureStorSimpleDeviceBackupRestoreJob** startar ett jobb som återställer en säkerhets kopia på en StorSimple-enhet.
Ange ett säkerhets kopie-ID och valfritt ögonblicks bild-ID.

## BESKRIVS

### Exempel 1: starta ett jobb för att återställa en säkerhets kopia
```
PS C:\>Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName "Contoso63-AppVm" -BackupId "b3b50534-763c-4b05-9724-5ecf62bde721" -WaitForComplete
Confirm
Are you sure you want to restore the backup with backupId b3b50534-763c-4b05-9724-5ecf62bde721? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y


Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 217d0647-c001-4f43-9833-f8155a458e95
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e0aa2dcd2f197a8588c40a067fe0e519
```

Det här kommandot startar ett jobb som återställer det säkerhetskopierade objekt som har det angivna ID: t och dess tillhör ande stillbilder på den enhet som heter Contoso63-AppVm.
Kommandot anger parametern *WaitForComplete* , så jobbet slutar innan cmdleten returnerar kontrollen till konsolen.

### Exempel 2: starta ett jobb för att återställa en viss ögonblicks bild
```
PS C:\>Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName "Contoso63-AppVm" -BackupId "b3b50534-763c-4b05-9724-5ecf62bde721" -SnapshotId "2d0cfad7-46bf-4266-8859-96549646e947_0000000000000000" -Force

The start job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId 9102ed9a-078f-4648-a
721-3cffbba31336 for tracking the job status
```

Det här kommandot startar ett jobb som återställer ögonblicks bilden med det angivna ID: t.
Kommandot anger säkerhetskopierat objekt efter ID på enheten med namnet Contoso63-AppVm.
Kommandot anger parametern *Force* , så start jobbet startas utan att du behöver bekräfta.

## MALLPARAMETRAR

### -BackupId
Anger instans-ID för säkerhets kopian som ska återställas.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Enhets namn
Anger namnet på den StorSimple-enhet där säkerhets kopian finns.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Anger att du inte behöver bekräfta med den här cmdleten.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Anger en Azure-profil.

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

### -SnapshotId
Anger instans-ID för den ögonblicks bild som ska återställas.

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WaitForComplete
Anger att denna cmdlet väntar på att åtgärden ska slutföras innan den återfår kontroll till Windows PowerShell-konsolen.

```yaml
Type: SwitchParameter
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

## VÄRDEN

### TaskStatusInfo, TaskResponse
Denna cmdlet returnerar ett **TaskStatusInfo** -objekt om du anger parametern *WaitForComplete* .
Om du inte anger den parametern returnerar den ett **TaskResponse** -objekt.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)

[Start-AzureStorSimpleDeviceBackupJob](./Start-AzureStorSimpleDeviceBackupJob.md)


