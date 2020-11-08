---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: EFAE7117-9B8B-4CB9-B4D9-3F08DCE1816E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 405b9d427c7e59dfb3628806a878d57a281a6b4e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099438"
---
# New-AzureStorSimpleDeviceBackupPolicy

## Sammanfattning
Skapar en säkerhets kopierings princip.

## FRÅGESYNTAXEN

```
New-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicyName <String>
 -BackupSchedulesToAdd <PSObject[]> -VolumeIdsToAdd <PSObject[]> [-WaitForComplete] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureStorSimpleDeviceBackupPolicy** skapar en säkerhets kopierings princip.
En säkerhets kopierings princip innehåller minst ett schema för säkerhets kopior som kan köras på en eller flera volymer.
Använd cmdleten **New-AzureStorSimpleDeviceBackupScheduleAddConfig** för att skapa ett schema för säkerhets kopiering.

## BESKRIVS

### Exempel 1: skapa en säkerhets kopierings princip
```
PS C:\>$Schedule01 = New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType LocalSnapshot -RecurrenceType Daily -RecurrenceValue 10 -RetentionCount 5 -Enabled $True
PS C:\> $Schedule02 = New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType CloudSnapshot -RecurrenceType Hourly -RecurrenceValue 1 -RetentionCount 5 -Enabled $True
PS C:\> $ScheduleArray = @()
PS C:\> $ScheduleArray += $Schedule01
PS C:\> $ScheduleArray += $Schedule02
PS C:\> $DeviceContainer = Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm"
PS C:\> $Volume = $(Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeContainer $DeviceContainer[0])
PS C:\> $VolumeArray = @()
PS C:\> $VolumeArray += $Volume[0].InstanceId
PS C:\> New-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "GeneralPolicy07" -BackupSchedulesToAdd $ScheduleArray -VolumeIdsToAdd $VolumeArray
VERBOSE: ClientRequestId: e9d6771e-c323-47b9-b424-cb98f8ed0273_PS
VERBOSE: ClientRequestId: db0e7c86-d0d2-4a5a-b1cb-182494cba027_PS
VERBOSE: ClientRequestId: 77708dfd-a386-4999-b7ed-5d53e288ae83_PS


JobId        : d4ce5340-d5d1-4471-9cc8-013193f021b3
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your add operation has completed successfully. 
VERBOSE: ClientRequestId: bbf7e9b9-b493-40b3-8348-f15bcfc4da8a_PS
BackupSchedules          : {36d21096-bbd1-47b7-91b5-40ad1792d992, 505fc91f-deb5-4dca-bfcb-98c20b75ebcc}
Volumes                  : {volume03}
BackupPolicyCreationType : BySaaS
LastBackup               : 01-01-2010 05:30:00
NextBackup               : 16-12-2014 01:13:43
SchedulesCount           : 2
SSMHostName              : 
VolumesCount             : 1
InstanceId               : 8799c2f0-8850-4e91-aa23-ee18c67da8bd
Name                     : GeneralPolicy07
OperationInProgress      : None
```

Det första kommandot skapar ett schema för säkerhets kopierings schemaläggning med hjälp av **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet och lagrar sedan objektet i variabeln $Schedule 01.

Det andra kommandot skapar ett annat konfigurations objekt för säkerhets kopior med hjälp av **New-AzureStorSimpleDeviceBackupScheduleAddConfig** och lagrar sedan objektet i $Schedule 02-variabeln.

Det tredje kommandot skapar en tom mat ris variabel, namngiven $ScheduleArray.
Nästa två kommandon lägger till de objekt som skapats i de två första kommandona för att $ScheduleArray.

Det sjätte kommandot får en volym behållare för enheten som heter Contoso63-AppVm med hjälp av cmdleten **Get-AzureStorSimpleDeviceVolumeContainer** och lagrar sedan det behållar-objekt i $DeviceContainer-variabeln.

Med det sjunde kommandot får du en volym för volymen som lagras i den första medlemmen i $DeviceContainer genom att använda cmdleten **Get-AzureStorSimpleDeviceVolume** och sedan lagra den volymen i $Volume variabeln.

Med kommandot åtto skapas en tom mat ris variabel som heter $VolumeArray.
Med nästa kommando läggs ett volym-ID till $VolumeArray.
Det här värdet identifierar volymen, som är lagrad i $Volume, där säkerhets kopierings principen körs.
Du kan lägga till ytterligare volym-ID: n för $VolumeArray.

Det sista kommandot skapar säkerhets kopierings principen med namnet GeneralPolicy07 för enheten som heter Contoso63-AppVm.
Kommandot anger de schema konfigurations objekt som lagras i $ScheduleArray.
Kommandot anger volymen eller volymerna som du vill tillämpa principen på i $VolumeArray.
Du kan verifiera säkerhets kopierings principen genom att använda cmdleten **Get-AzureStorSimpleDeviceBackupPolicy** .

## MALLPARAMETRAR

### -BackupPolicyName
Anger namnet på säkerhets kopierings principen.

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

### -BackupSchedulesToAdd
Anger en matris med **BackupScheduleBase** -objekt som ska läggas till i principen.
Varje objekt representerar ett schema.
En säkerhets kopierings princip innehåller ett eller flera scheman.
För att få ett **BackupScheduleBase** -objekt, Använd cmdleten **New-AzureStorSimpleDeviceBackupScheduleAddConfig** .

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Enhets namn
Anger namnet på den StorSimple-enhet där säkerhets kopierings principen ska skapas.

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

### -VolumeIdsToAdd
Anger en matris med ID-numren för volymer som ska läggas till i säkerhets kopierings principen.

```yaml
Type: PSObject[]
Parameter Sets: (All)
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

### BackupPolicy
Denna cmdlet returnerar ett **BackupPolicy** -objekt som innehåller de nya scheman och volymer.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureStorSimpleDeviceBackupPolicy](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[Get-AzureStorSimpleDeviceVolume](./Get-AzureStorSimpleDeviceVolume.md)

[Get-AzureStorSimpleDeviceVolumeContainer](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[Remove-AzureStorSimpleDeviceBackupPolicy](./Remove-AzureStorSimpleDeviceBackupPolicy.md)

[Set-AzureStorSimpleDeviceBackupPolicy](./Set-AzureStorSimpleDeviceBackupPolicy.md)

[New-AzureStorSimpleDeviceBackupScheduleAddConfig](./New-AzureStorSimpleDeviceBackupScheduleAddConfig.md)


