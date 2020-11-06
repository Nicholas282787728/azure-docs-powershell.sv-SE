---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 516192dab6d075979a2d78cea72afaedb7a18231
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576608"
---
# New-AzureVMSqlServerAutoPatchingConfig

## Sammanfattning
Skapar ett konfigurations objekt för automatisk korrigering på en virtuell dator.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
New-AzureVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureVMSqlServerAutoPatchingConfig** skapar ett konfigurations objekt för automatisk korrigering på en virtuell dator.

## BESKRIVS

### Exempel 1: skapa ett konfigurations objekt för att konfigurera automatisk korrigering
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

Det här kommandot skapar konfigurations objekt för korrigering.
Kommandot anger vecko dagen och fönstret underhåll.
Denna konfiguration möjliggör en korrigering som använder dessa värden.
Resultatet sparas i $AutoBackupConfig variabel.
Du kan ange det här konfigurationsobjektet för andra cmdlets, till exempel Set-AzureRmVMSqlServerExtension cmdlet.

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
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Everyday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Aktivera
Anger att automatisk korrigering för den virtuella datorn är aktive rad.
Om du aktiverar automatisk korrigering av cmdleten placeras Windows Update i interaktivt läge.
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

### -MaintenanceWindowDuration
Anger längden i minuter för underhålls fönstret.
Automatisk korrigering undvikr att utföra en åtgärd som kan påverka en virtuell dator tillgänglighet utanför det fönstret.
Ange en multipel av 30 minuter.

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
Den här tiden anger när uppdateringar börjar installera.

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
Accepted values: Important

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
Denna cmdlet accepterar inte indata.

## VÄRDEN

### AutoPatchingSettings
Den här cmdleten returnerar objekt som innehåller inställningar för automatisk korrigering.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzureVMSqlServerAutoBackupConfig](./New-AzureVMSqlServerAutoBackupConfig.md)

[Set-AzureRmVMSqlServerExtension](./Set-AzureRMVMSqlServerExtension.md)


