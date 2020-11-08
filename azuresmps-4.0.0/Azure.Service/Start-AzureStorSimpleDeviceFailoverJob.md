---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 53580FF1-D905-40FD-A5F0-D5FBCD036E0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: a51fd8210d2fe7fb224ed43650a354e383ed4e54
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099006"
---
# Start-AzureStorSimpleDeviceFailoverJob

## Sammanfattning
Initierar en failover-åtgärd för volym behållar grupper.

## FRÅGESYNTAXEN

### Tom (standard)
```
Start-AzureStorSimpleDeviceFailoverJob
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyById
```
Start-AzureStorSimpleDeviceFailoverJob -DeviceId <String>
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 -TargetDeviceId <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByName
```
Start-AzureStorSimpleDeviceFailoverJob -DeviceName <String>
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 -TargetDeviceName <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Start-AzureStorSimpleDeviceFailoverJob** initierar en redundansväxling av en eller flera volym behållar grupper från en enhet till en annan.

## BESKRIVS

### Exempel 1: starta ett failover-jobb för en namngiven enhet och en namngiven mål enhet
```
PS C:\>(Get-AzureStorSimpleFailoverVolumeContainers -DeviceName "ChewD_App7") | Where-Object {$_.IsDCGroupEligibleForDR -eq $True} | Start-AzureStorSimpleDeviceFailoverJob -DeviceName "ChewD_App7" -TargetDeviceName "Fuller05" -Force
a3d902be-8ffb-42a4-bbf8-0a1b30db71b2_0ee59ae9-0293-46e2-ae56-bc308c8e5520
```

Det här kommandot får volym containrarna för enheten som heter ChewD_App7 genom att använda cmdleten **Get-AzureStorSimpleFailoverVolumeContainers** .
Kommandot skickar resultaten till cmdleten **Where-Object** , som avslutar de behållare som har ett annat värde än $True för egenskapen **IsDCGroupEligibleForDR** .
Om du vill ha mer information skriver du `Get-Help Where-Object` .
Den aktuella cmdleten startar failover-jobb för återstående enheter med växling vid fel.
Kommandot anger enhetens namn och mål enhetens namn.
Kommandot returnerar instans-ID för jobbet som cmdleten startar.

### Exempel 2: starta ett failover-jobb för en enhet och en måldator som anges av ID
```
PS C:\>(Get-AzureStorSimpleFailoverVolumeContainers -DeviceId "3825f272-1efb-4c14-b63f-22605ce3b925") | Where-Object {$_.IsDCGroupEligibleForDR -eq $True} | Select-Object -First 1 | Start-AzureStorSimpleDeviceFailoverJob -DeviceId "3825f272-1efb-4c14-b63f-22605ce3b925" -TargetDeviceId "0ee59ae9-0293-46e2-ae56-bc308c8e5520" -Force
4c5ac0d0-4b66-465c-98f5-aec90505ad12_0ee59ae9-0293-46e2-ae56-bc308c8e5520
```

Det här kommandot får volym containrarna för enheten med namn ChewD_App7 genom att använda **Get-AzureStorSimpleFailoverVolumeContainers**.
Kommandot skickar resultaten till **WHERE-objekt** , som ignorerar dem som har ett annat värde än $True för egenskapen **IsDCGroupEligibleForDR** .
Cmdleten skickar resultaten till cmdleten **Select-Object** , som markerar det första objektet för överföring till den aktuella cmdleten.
Om du vill ha mer information skriver du `Get-Help Select-Object` .
Den aktuella cmdleten startar redundans för den valda volymen.
Kommandot anger enhets-ID och Målprogram-ID.
Kommandot returnerar instans-ID för jobbet som cmdleten startar.

## MALLPARAMETRAR

### -DeviceId
Anger instans-ID för den StorSimple-enhet som volym behållar gruppen finns på.

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
Anger namnet på den StorSimple-enhet som volym behållar grupper finns på.

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -TargetDeviceId
Anger instans-ID för den StorSimple-enhet som cmdleten växlar till över volym behållar grupperna.

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

### -TargetDeviceName
Anger namnet på den StorSimple-enhet som cmdleten växlar till över volym behållar grupperna.

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VolumecontainerGroups
Anger listan över volym behållar grupper som denna cmdlet växlar över till en annan enhet.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Förteckning\<DataContainerGroup\>
Du kan visa en lista med volym behållar grupper för denna cmdlet.

## VÄRDEN

### Strängvärdet

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureStorSimpleFailoverVolumeContainers](./Get-AzureStorSimpleFailoverVolumeContainers.md)


