---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: ED6CDEA3-0A5D-47E6-B9D7-47D1862212DF
online version: ''
schema: 2.0.0
ms.openlocfilehash: b907627200ec2463d997ebb4faa834e2821b1c7b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099440"
---
# New-AzureStorSimpleAccessControlRecord

## Sammanfattning
Skapar en åtkomst kontroll post.

## FRÅGESYNTAXEN

```
New-AzureStorSimpleAccessControlRecord -ACRName <String> -IQNInitiatorName <String> [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureStorSimpleAccessControlRecord** skapar en åtkomst kontroll post.
Du kan använda ett **AccessControlRecord** -objekt för att konfigurera volymer.

## BESKRIVS

### Exempel 1: skapa en Access-Controlaccess kontroll post och vänta tills resultaccess-kontrollen
```
PS C:\>New-AzureStorSimpleAccessControlRecord -ACRName "Acr10" -IQNInitiatorName "Iqn10" -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 08719243-3a76-43a5-a88b-e5f2b63ed3d9
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e12362c2c06615108ba8436cf85fcd40
```

Det här kommandot skapar en åtkomst kontroll post med namnet Acr10 för iSCSI Initiator med namnet Iqn10.
Det här kommandot anger parametern *WaitForComplete* och därför väntar du tills åtgärden är slutförd och returnerar sedan ett **TaskStatusInfo** -objekt.

### Exempel 2: skapa en kontroll recordaccess kontroll för Access-Controlaccess
```
PS C:\>New-AzureStorSimpleAccessControlRecord -ACRName "Acr11" -IQNInitiatorName "Iqn11"
VERBOSE: The create job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
2bd56fbb-4b95-4f2c-b99f-6321231a018d for tracking the job status
```

Det här kommandot skapar en åtkomst kontroll post med namnet Acr11 för iSCSI Initiator med namnet Iqn11.
Det här kommandot anger inte parametern *WaitForComplete* , och därför startas uppgiften av kommandot och sedan returneras ett **TaskResponse** -objekt.
Använd cmdleten **Get-AzureStorSimpleTask** för att se uppgiftens status.

## MALLPARAMETRAR

### -ACRName
Anger ett namn för åtkomst kontroll posten.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IQNInitiatorName
Anger iSCSI-kvalificerat namn (IQN) för den iSCSI-initierare som denna cmdlet tillhandahåller åtkomst för volymen.

```yaml
Type: String
Parameter Sets: (All)
Aliases: IQN

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

[Get-AzureStorSimpleAccessControlRecord](./Get-AzureStorSimpleAccessControlRecord.md)

[Remove-AzureStorSimpleAccessControlRecord](./Remove-AzureStorSimpleAccessControlRecord.md)

[Set-AzureStorSimpleAccessControlRecord](./Set-AzureStorSimpleAccessControlRecord.md)

[Get-AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)


