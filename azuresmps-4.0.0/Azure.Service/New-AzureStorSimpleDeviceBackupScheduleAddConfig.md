---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: EE7EC812-640B-4672-B23C-673F912F0EDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 945d06ddc1be6d2b0864b0421a5a087e14d98218
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093254"
---
# New-AzureStorSimpleDeviceBackupScheduleAddConfig

## Sammanfattning
Skapar ett konfigurations objekt för säkerhets kopierings schema.

## FRÅGESYNTAXEN

```
New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType <String> -RecurrenceType <String>
 -RecurrenceValue <Int32> -RetentionCount <Int64> [-StartFromDateTime <String>] -Enabled <Boolean>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureStorSimpleDeviceBackupScheduleAddConfig** skapar ett **BackupScheduleBase** -konfigurationsobjekt.
Använd det här konfigurationsobjektet för att skapa en ny säkerhets kopierings princip genom att använda cmdlet **New-AzureStorSimpleDeviceBackupPolicy** .

## BESKRIVS

### Exempel 1: skapa ett konfigurations objekt för säkerhets kopior
```
PS C:\>New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType CloudSnapshot -RecurrenceType Daily -RecurrenceValue 1 -RetentionCount 100 -Enabled $True
VERBOSE: ClientRequestId: 426a79ee-fed3-4d3d-9123-e371f83222b3_PS


BackupType     : CloudSnapshot
Recurrence     : Microsoft.WindowsAzure.Management.StorSimple.Models.ScheduleRecurrence
RetentionCount : 100
StartTime      : 2014-12-16T00:37:19+05:30
Status         : Enabled
```

Det här kommandot skapar ett bas objekt för säkerhets kopierings schema för säkerhets kopiering av moln ögonblick.
Säkerhets kopian sker varje dag och säkerhets kopiorna behålls i 100 dagar.
Detta schema är aktiverat från standard tiden, vilket är den aktuella tiden.

## MALLPARAMETRAR

### -BackupType
Anger säkerhets kopierings typen.
Giltiga värden är: LocalSnapshot och CloudSnapshot.

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

### -Aktiverad
Anger om säkerhets kopierings schema ska aktive ras.

```yaml
Type: Boolean
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

### -RecurrenceType
Anger den återkommande typen för detta säkerhets kopierings schema.
Giltiga värden är: 

- Protokoll
- Tim
- Vardag
- Vecko

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

### -RecurrenceValue
Anger hur ofta du vill göra en säkerhets kopia.
Den här parametern använder enheten som anges av parametern *RecurrenceType* .

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RetentionCount
Anger antalet dagar som en säkerhets kopia ska behållas.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartFromDateTime
Anger det datum från vilket du vill börja skapa säkerhets kopior.
Standardvärdet är den aktuella tiden.

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

## VÄRDEN

### BackupScheduleBase
Denna cmdlet returnerar ett **BackupScheduleBase** -objekt.
Använd en **BackupScheduleBase** för att skapa en ny säkerhets kopierings princip.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzureStorSimpleDeviceBackupScheduleUpdateConfig](./New-AzureStorSimpleDeviceBackupScheduleUpdateConfig.md)

[New-AzureStorSimpleDeviceBackupPolicy](./New-AzureStorSimpleDeviceBackupPolicy.md)


