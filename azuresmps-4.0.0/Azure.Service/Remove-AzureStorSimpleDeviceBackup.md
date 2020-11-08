---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 47650E39-758C-4D3C-9653-B70576CA0979
online version: ''
schema: 2.0.0
ms.openlocfilehash: a93791e3184fcabacbf90caebcb2170746922b36
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099697"
---
# Remove-AzureStorSimpleDeviceBackup

## Sammanfattning
Tar bort ett säkerhets kopie objekt.

## FRÅGESYNTAXEN

### IdentifyById (standard)
```
Remove-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupId <String> [-Force] [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByObject
```
Remove-AzureStorSimpleDeviceBackup -DeviceName <String> -Backup <Backup> [-Force] [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Remove-AzureStorSimpleDeviceBackup** tar bort ett enda säkerhets kopie objekt.
Om du försöker ta bort en säkerhets kopia som redan har tagits bort returnerar denna cmdlet ett fel.

## BESKRIVS

### Exempel 1: ta bort en säkerhets kopia för en enhet
```
PS C:\>Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupId "dcb5c991-0485-400f-8d0a-03a1341ee989" -Force
The remove job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId 6c73aff2-f5a1-4b5e-
9a4e-857e128dc216 for tracking the job status
```

Det här kommandot tar bort den säkerhets kopia som har angivet ID för enheten som heter Contoso63-AppVm.
Kommandot startar åtgärden som tar bort **säkerhetskopierade** objekt och returnerar sedan ett **TaskResponse** -objekt.
Använd cmdleten **Get-AzureStorSimpleTask** för att se uppgiftens status.

### Exempel 2: ta bort den första säkerhets kopian för en enhet med hjälp av dess ID
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm"
PS C:\> Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupId $Backup[0].InstanceId -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 53a656c3-c082-4e1f-afb7-bff3db45c791
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : f4411f38d07f68b88095682dbeedd9e9
```

Det första kommandot får säkerhets kopiorna för enheten som heter Contoso63-AppVm och lagrar dem sedan i $Backup variabel.

Det andra kommandot tar bort en säkerhets kopia från enheten med namnet Contoso63-AppVm.
Kommandot använder standard punkt notation för att referera till **InstanceID** -egenskapen för det första elementet i $Backup matrisen.
Det här kommandot anger parametern *WaitForComplete* och därför väntar du tills åtgärden är slutförd och returnerar sedan ett **TaskStatusInfo** -objekt.

### Exempel 3: ta bort den första säkerhets kopian för en enhet med hjälp av pipeline
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso-AppVm" -WaitForComplete
PS C:\> $Backup[0] | Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso-AppVm" -Force -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 48059fd8-e355-4b91-9385-630d24f31df6
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e1753f3bf68e6e44ab719436b5111e41
```

Det första kommandot får säkerhets kopiorna för enheten som heter Contoso63-AppVm och lagrar dem sedan i $Backup variabel.

Det andra kommandot skickar det första objektet som lagras i $Backup matris till den aktuella cmdleten.
Denna cmdlet tar bort den säkerhets kopian från enheten med namnet Contoso63-AppVm.
Det här kommandot anger parametern *WaitForComplete* och därför väntar du tills åtgärden är slutförd och returnerar sedan ett **TaskStatusInfo** -objekt.

## MALLPARAMETRAR

### -Säkerhets kopiering
Anger det **säkerhetskopierade** objekt som ska tas bort.
Använd cmdleten **Get-AzureStorSimpleDeviceBackup** för att få ett **säkerhets kopie** objekt.

```yaml
Type: Backup
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -BackupId
Anger instans-ID för en säkerhets kopia som ska tas bort.

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

### -Enhets namn
Anger namnet på den StorSimple-enhet där du vill ta bort en säkerhets kopia.

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

### Reservdomänkontrollant

## VÄRDEN

### TaskStatusInfo, TaskResponse
Denna cmdlet returnerar ett **TaskStatusInfo** -objekt om du anger parametern *WaitForComplete* om du inte anger den parametern, returnerar den ett **TaskResponse** -objekt.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureStorSimpleDeviceBackup](./Get-AzureStorSimpleDeviceBackup.md)


