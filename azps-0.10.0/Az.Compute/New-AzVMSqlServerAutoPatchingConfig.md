---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 3ba7ab00076a3a0634a0d4394270fe4a83ec8ede
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398265"
---
# New-AzVMSqlServerAutoPatchingConfig

## SYNOPSIS
Skapar ett konfigurationsobjekt för automatisk korrigering på en virtuell dator.

## SYNTAX

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>]
 [-MaintenanceWindowStartingHour <Int32>] [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>]
 [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **New-AzVMSqlServerAutoPatchingConfig** skapar ett konfigurationsobjekt för automatisk korrigering på en virtuell dator.

## EXEMPEL

### Exempel 1: Skapa ett konfigurationsobjekt för att konfigurera automatisk korrigering
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

Det här kommandot skapar konfigurationsobjekt för korrigeringar.
Kommandot anger veckodagen och definierar underhållsfönstret.
Den här konfigurationen aktiverar korrigeringar som använder dessa värden.
Kommandot lagrar resultatet i den $AutoBackupConfig variabeln.
Du kan ange det här konfigurationsobjektet för andra cmdlets, till exempel Set-AzVMSqlServerExtension cmdlet.

## PARAMETERS

### -DayOfWeek
Anger den dag i veckan då uppdateringar ska installeras.

De godtagbara värdena för den här parametern är:

- söndag
- Måndag
- Tisdag
- Onsdag
- Torsdag
- Fredag
- Lördag
- Varje dag

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

### -Enable
Anger att automatisk korrigering för den virtuella datorn är aktiverad.
Om du aktiverar automatisk korrigering placerar cmdleten Windows Update i interaktivt läge.
Om du inaktiverar automatisk korrigering ändras inte Windows Update-inställningarna.

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
Anger underhållsfönstrets varaktighet i minuter.
Med automatiska korrigeringar undviker du att utföra en åtgärd som kan påverka tillgängligheten för virtuella maskiner utanför fönstret.
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
Anger vilken timme under dagen som underhållsfönstret startar.
Den här gången definieras när uppdateringar ska installeras.

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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### Ingen
Den här cmdleten accepterar inte några indata.

## UTDATA

### AutoPatchingSettings
Den här cmdleten returnerar objektet innehåller inställningar för automatisk korrigering.

## ANTECKNINGAR

## RELATERADE LÄNKAR

[New-AzureVMSqlServerAutoBackupConfig](./New-AzVMSqlServerAutoBackupConfig.md)

[Set-AzVMSqlServerExtension](./Set-AzVMSqlServerExtension.md)


