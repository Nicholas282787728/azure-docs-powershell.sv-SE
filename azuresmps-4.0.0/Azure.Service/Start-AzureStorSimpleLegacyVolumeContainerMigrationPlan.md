---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 6F31F2B4-6131-4B11-B074-CA05CE3A56F1
online version: ''
schema: 2.0.0
ms.openlocfilehash: f928ecba8f92badc1eb87e47aee16515f1684fce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099003"
---
# Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan

## Sammanfattning
Skapar ett migreringsarkiv.

## FRÅGESYNTAXEN

### MigrateSpecificContainer
```
Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId <String>
 -LegacyContainerNames <String[]> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### MigrateAllContainer
```
Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId <String> [-All]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan** börjar skapa ett migreringsarkiv.
Skapandet av ett migreringsarkiv är asynkront.
Använd cmdleten **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** för att se status för migreringsarkivet.

## BESKRIVS

### Exempel 1: starta ett migreringsarkiv
```
PS C:\>Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud"
Successfully started estimating the Migration Plan. Please check details with Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
```

Det här kommandot börjar skapa ett migreringsarkiv för den äldre behållaren med namnet OneSDKAzureCloud.
Kommandot returnerar ett meddelande om planens status och för att använda cmdleten **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** för uppdaterade uppgifter.

### Exempel 2: starta ett migreringsarkiv för alla volym behållare
```
PS C:\>Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -All
Successfully started estimating the Migration Plan. Please check details with Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
```

Det här kommandot börjar skapa ett migreringsarkiv för alla gamla volym behållare i konfigurations filen som importeras.

## MALLPARAMETRAR

### -Alla
Anger att den här cmdleten ska börja uppskattad migrations tid för alla volym behållare i den importerade konfigurations filen.

```yaml
Type: SwitchParameter
Parameter Sets: MigrateAllContainer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LegacyConfigId
Anger det unika ID: t för den äldre utrustningens konfiguration.

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

### -LegacyContainerNames
Anger en matris med volym behållar namn som du vill skapa ett migreringsarkiv för.

```yaml
Type: String[]
Parameter Sets: MigrateSpecificContainer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Anger den Azure-profil från vilken denna cmdlet läser.
Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.

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

### Strängvärdet
Denna cmdlet returnerar statusen för migreringsjobbet om den har startats.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan](./Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


