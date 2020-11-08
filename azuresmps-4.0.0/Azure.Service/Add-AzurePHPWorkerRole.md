---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FEFBF1EF-FBCE-45D8-8455-F3F8662F1F36
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4ddf78f30cb6938571fc967d510e4ab99a0cfc80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099617"
---
# Add-AzurePHPWorkerRole

## Sammanfattning
Skapar nödvändiga filer och konfiguration för ett PHP-program som hanteras i Azure via php.exe.

## FRÅGESYNTAXEN

```
Add-AzurePHPWorkerRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.
För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .

Skapar de filer och den konfiguration som krävs, som ibland kallas scaffolding, för ett PHP-program som hanteras i Azure via php.exe.

## BESKRIVS

### Exempel 1: skapa en arbets roll med en enda instans
```
PS C:\> Add-AzurePHPWorkerRole MyWorkerRole
```

I det här exemplet läggs nödvändiga filer och inställningar till i det aktuella programmet.

### Exempel 2: skapa en arbets roll med flera instanser
```
PS C:\> Add-AzurePHPWorkerRole MyWorkerRole -I 2
```

I det här exemplet läggs nödvändiga filer och inställningar till i det aktuella programmet med hjälp av namnet MyWorkerRole med en roll instans räkning på 2.

## MALLPARAMETRAR

### -Instanser
Anger antalet roll instanser för denna arbets roll.
Standardvärdet är 1.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: i

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Anger namnet på arbets rollen.
Namnet bestämmer mappnamnet som innehåller de filer och den konfiguration för PHP-tjänsten som finns i arbets rollen.
Standardvärdet är WorkerRole1.

```yaml
Type: String
Parameter Sets: (All)
Aliases: n

Required: False
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

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzureServiceProject](./New-AzureServiceProject.md)

[Add-AzurePHPWebRole](./Add-AzurePHPWebRole.md)


