---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A1E143A8-70F2-4158-9A10-F2082AD62A73
online version: ''
schema: 2.0.0
ms.openlocfilehash: 371291f4bd33809bc2f5880e4380c448219ed37a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099242"
---
# Stop-AzureStorSimpleJob

## Sammanfattning
Stoppar ett StorSimple jobb.

## FRÅGESYNTAXEN

```
Stop-AzureStorSimpleJob -InstanceId <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Stop-AzureStorSimpleJob** stoppar ett pågående StorSimple-jobb.
Du kan ange ett instans-ID eller ett jobbnamn.

## BESKRIVS

### Exempel 1: stoppa jobb för en enhet
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" | Stop-AzureStorSimpleJob -Force
```

Det här kommandot får jobbet för enheten som heter Device07 med hjälp av cmdleten **Get-AzureStorSimpleJob** .
Kommandot skickar jobben till den aktuella cmdleten med hjälp av pipeline-operatorn.
Den aktuella cmdleten stoppar alla jobb som kommandot skickar till det.
Kommandot anger parametern *Force* och ber dig inte att få en bekräftelse innan den stoppar ett jobb.

### Exempel 2: stoppa ett visst jobb
```
PS C:\>Stop-AzureStorSimpleJob -InstanceId "574f47e0-44e9-495c-b8a5-0203c57ebf6d" -Force
```

Det här kommandot stoppar det jobb som har angivet instans-ID.

## MALLPARAMETRAR

### -Force
Tvingar kommandot att köras utan att fråga efter bekräftelse.

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

### -InstanceId
Anger ID för det enhets jobb som ska stoppas.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen

## VÄRDEN

### DeviceJobDetails
Denna cmdlet hämtar information om **DeviceJob** som denna cmdlet slutar.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)


