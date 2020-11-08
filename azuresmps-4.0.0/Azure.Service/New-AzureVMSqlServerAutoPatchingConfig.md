---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7317DAC1-B535-4650-86BF-73E96F61EECD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23bb8e09fac8ec4fe0e8ff5b3c23ab995f03694c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099421"
---
# New-AzureVMSqlServerAutoPatchingConfig

## Sammanfattning
Skapar ett konfigurations objekt för automatisk korrigering av virtuell dator.

## FRÅGESYNTAXEN

```
New-AzureVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureVMSqlServerAutoPatchingConfig** skapar ett konfigurations objekt för automatisk korrigering av virtuell dator.

## BESKRIVS

### Exempel 1: skapa ett konfigurations objekt för att konfigurera automatisk korrigering
```
PS C:\> $APS = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
          Enable                        : True
          DayOfWeek                     : Thursday
          MaintenanceWindowStartingHour : 11
          MaintenanceWindowDuration     : 120
          PatchCategory                 : Important
```

Det här kommandot skapar ett konfigurations objekt som kan användas för att konfigurera automatisk uppdatering med set-AzureVMSqlServerExtension.

## MALLPARAMETRAR

### -DayOfWeek
Anger den dag i veckan då uppdateringar ska installeras.

De acceptabla värdena för den här parametern är:

- Lördag
- Dagarna
- Torsdag
- Onsdagen
- Torsdag
- Fredag
- Afton
- Vardaglig

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

### -Aktivera
Anger att automatisk korrigering för den virtuella datorn är aktive rad.
Om du aktiverar automatisk korrigering av cmdleten kommer Windows Update till interaktivt läge.
Om du inaktiverar automatisk uppdatering ändras inte Windows Update-inställningarna.

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

### -InformationAction
Anger hur den här cmdleten svarar på en informations händelse.

De acceptabla värdena för den här parametern är:

- Vidare
- Över
- Inquire
- SilentlyContinue
- Stanna
- Avbryt

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Anger en informations variabel.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaintenanceWindowDuration
Anger underhålls fönstrets längd.
Automatisk korrigering gör att det inte går att utföra en åtgärd som kan påverka en virtuell dators tillgänglighet utanför det fönstret.
Endast 30 minuters ökningar är tillåtna.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaintenanceWindowStartingHour
Anger den timme i dag då underhålls fönstret startar.
Den här tiden anger när uppdateringar börjar installeras och avrundas till timmen.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PatchCategory
Anger om viktiga uppdateringar ska ingå.

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

## VÄRDEN

### AutoPatchingSettings
Den här cmdleten returnerar objekt som innehåller inställningar för automatisk korrigering.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Set-AzureVMSqlServerExtension](./Set-AzureVMSqlServerExtension.md)

[Remove-AzureVMSqlServerExtension](./Remove-AzureVMSqlServerExtension.md)

[Set-AzureVMSqlServerExtension](./Set-AzureVMSqlServerExtension.md)


