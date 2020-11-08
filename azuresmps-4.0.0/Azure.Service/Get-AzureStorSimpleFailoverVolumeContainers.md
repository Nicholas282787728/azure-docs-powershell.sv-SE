---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BABBA19E-5833-452C-9E36-811EAE7C20F9
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb326281058f0ff9280c4b87c0530241ece801e0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093287"
---
# Get-AzureStorSimpleFailoverVolumeContainers

## Sammanfattning
Hämtar volym behållar grupperna för redundanstestning.

## FRÅGESYNTAXEN

### IdentifyById
```
Get-AzureStorSimpleFailoverVolumeContainers -DeviceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByName
```
Get-AzureStorSimpleFailoverVolumeContainers -DeviceName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureStorSimpleFailoverVolumeContainers** hämtar volym behållar grupperna för redundanstestning.
Skicka en enda **VolumeContainer** -grupp eller en matris med **VolumeContainer** -grupper till cmdleten **Start-AzureStorSimpleDeviceFailover** .
Endast grupper som har ett värde för $True för egenskapen **IsDCGroupEligibleForDR** är berättigade till redundans.

## BESKRIVS

### Exempel 1: Hämta volym behållare för redundans
```
PS C:\>Get-AzureStorSimpleFailoverVolumeContainers -DeviceName "ChewD_App7"

DCGroup                    IneligibilityMessage          IsDCGroupEligibleForDR
-------                    --------------------          ----------------------
{VolumeContainer1889078...                                                 True
{VC_01}                    No cloud snapshot found                        False
{VolumeContainer7306959}   No cloud snapshot found                        False
{VolumeContainer407850151} No cloud snapshot found                        False
```

Det här kommandot får volym behållare för redundans.
Endast DCGroups som har ett $True värde för egenskapen **IsDCGroupEligibleForDR** kan användas för redundanstestning.

## MALLPARAMETRAR

### -DeviceId
Anger instans-ID för den StorSimple-enhet som cmdleten ska köras på.

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
Anger namnet på den StorSimple-enhet som cmdleten ska köras på.

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

## VÄRDEN

### IList\<DataContainerGroup\>
Denna cmdlet returnerar en lista med **VolumeContainer** Groups.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Start-AzureStorSimpleDeviceFailoverJob](./Start-AzureStorSimpleDeviceFailoverJob.md)

[Get-AzureStorSimpleDeviceVolumeContainer](./Get-AzureStorSimpleDeviceVolumeContainer.md)


