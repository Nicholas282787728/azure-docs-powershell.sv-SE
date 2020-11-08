---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 76826524-480F-458E-A996-A9DBACB8BA9E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4aa220334c75d3e6832698ec10fbad71896473d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099257"
---
# Start-AzureStorSimpleDeviceBackupJob

## Sammanfattning
Startar ett nytt jobb som skapar en säkerhets kopia från en befintlig säkerhets kopierings princip.

## FRÅGESYNTAXEN

### Tom (standard)
```
Start-AzureStorSimpleDeviceBackupJob -DeviceName <String> -BackupPolicyId <String> [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BackupTypeGiven
```
Start-AzureStorSimpleDeviceBackupJob -DeviceName <String> -BackupPolicyId <String> -BackupType <String>
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Start-AzureStorSimpleDeviceBackupJob** startar ett nytt jobb med en säkerhets kopia från en befintlig säkerhets kopierings princip på en StorSimple-enhet.
Denna cmdlet skapar som standard en säkerhets kopia av en lokal ögonblicks bild.
Om du vill skapa en säkerhets kopia av molnet anger du ett värde för CloudSnapshot för parametern *BackupType* .

## BESKRIVS

### Exempel 1: skapa en lokal säkerhets kopia av ögonblicks bild
```
PS C:\>Start-AzureStorSimpleDeviceBackupJob -DeviceName "Contoso63-AppVm" -BackupPolicyId "de088eac-b283-4d92-b501-a759845fdf3f"
JobId                                                                StatusCode RequestId
-----                                                                ---------- ---------
fb9acdca-ed6f-4b69-93f2-5c0bce0a1e08                                 Accepted   456cf6bafd427103b71c07145e26d35c

VERBOSE: Your backup operation has been submitted for processing. Use commandlet "Get-AzureStorSimpleJob -JobId
fb9acdca-ed6f-4b69-93f2-5c0bce0a1e08" to track status.
```

Det här kommandot skapar en lokal säkerhets kopia av den angivna princip-ID: t.
Det här kommandot startar jobbet och returnerar sedan ett **TaskResponse** -objekt.
Använd cmdleten **Get-AzureStorSimpleTask** för att se status för jobbet.

### Exempel 2: skapa en säkerhets kopia av en moln ögonblicks bild och vänta tills den är klar
```
PS C:\>Start-AzureStorSimpleDeviceBackupJob -DeviceName "Contoso63-AppVm" -BackupPolicyId "de088eac-b283-4d92-b501-a759845fdf3f" -BackupType CloudSnapshot -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : fb9acdca-ed6f-4b69-93f2-5c0bce0a1e08
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : f28ecf6cf75a7f128ca18e6ae14f9003
```

Det här kommandot skapar en säkerhets kopia av en moln ögonblicks bild för angivet princip-ID.
Det här kommandot anger parametern *WaitForComplete* så att kommandot slutför uppgiften och returnerar sedan ett **TaskStatusInfo** -objekt för jobbet.

## MALLPARAMETRAR

### -BackupPolicyId
Anger ID för säkerhets kopierings principen som ska användas för att skapa säkerhets kopian.

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

### -BackupType
Anger säkerhets kopierings typen.
Giltiga värden är: LocalSnapshot och CloudSnapshot.

```yaml
Type: String
Parameter Sets: BackupTypeGiven
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Enhets namn
Anger namnet på den StorSimple-enhet som du vill starta säkerhets kopierings jobbet på.

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

[Start-AzureStorSimpleDeviceBackupRestoreJob](./Start-AzureStorSimpleDeviceBackupRestoreJob.md)


