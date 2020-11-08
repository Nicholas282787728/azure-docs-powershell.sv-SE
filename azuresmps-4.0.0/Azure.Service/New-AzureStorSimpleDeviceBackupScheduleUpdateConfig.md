---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 22C6845E-D7BD-4BBC-B373-394A23488A94
online version: ''
schema: 2.0.0
ms.openlocfilehash: a0695dc42d9c540e30ddf9ac55bd6fc136c84bff
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093250"
---
# New-AzureStorSimpleDeviceBackupScheduleUpdateConfig

## Sammanfattning
Skapar ett schema för uppdatering av säkerhets kopior.

## FRÅGESYNTAXEN

```
New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id <String> -BackupType <String> -RecurrenceType <String>
 -RecurrenceValue <Int32> -RetentionCount <Int64> [-StartFromDateTime <String>] [-Enabled <Boolean>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** skapar ett **BackupScheduleUpdateRequest** -konfigurationsobjekt.
Använd det här konfigurationsobjektet för att uppdatera en säkerhets kopierings princip med cmdleten **set-AzureStorSimpleDeviceBackupPolicy** .

## BESKRIVS

### Exempel 1: skapa en begäran om schemaläggning
```
PS C:\>New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id "147f734d-a31a-4473-8501-6ba38be2cb30" -BackupType CloudSnapshot -RecurrenceType Hourly -RecurrenceValue 1 -RetentionCount 50 -Enabled $True
VERBOSE: ClientRequestId: ef346641-54b4-4273-8898-7f863e7c5b7e_PS


BackupType     : CloudSnapshot
Id             : 147f734d-a31a-4473-8501-6ba38be2cb30
Recurrence     : Microsoft.WindowsAzure.Management.StorSimple.Models.ScheduleRecurrence
RetentionCount : 50
StartTime      : 2014-12-16T00:39:32+05:30
Status         : Enabled
```

Det här kommandot skapar en begäran om uppdatering av säkerhets kopior för schemat med angivet ID.
Begäran är att göra ett schema för säkerhets kopiering av moln ögonblicks bilder som återkommer varje timme.
Säkerhets kopiorna bevaras i 50 dagar.
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

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Anger instans-ID för det säkerhets kopierings schema som ska uppdateras.

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

### BackupScheduleUpdateRequest
Denna cmdlet returnerar ett **BackupScheduleUpdateRequest** -objekt som innehåller information om uppdaterade säkerhets kopior.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzureStorSimpleDeviceBackupScheduleAddConfig](./New-AzureStorSimpleDeviceBackupScheduleAddConfig.md)

[Set-AzureStorSimpleDeviceBackupPolicy](./Set-AzureStorSimpleDeviceBackupPolicy.md)


