---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A1815E7F-720E-4526-A779-106C181B840D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22b04496d9ce310b58662c62b70a195e8cfa8878
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099261"
---
# Start-AzureEmulator

## Sammanfattning
Startar beräknings-och lagrings emulatorer.

## FRÅGESYNTAXEN

```
Start-AzureEmulator [-Launch] [-Mode <ComputeEmulatorMode>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.
För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .

Cmdleten **Start-AzureEmulator** startar både Compute-och Storage-emulatorerna och är värd för den aktuella tjänsten i Compute-emulatorn.

## BESKRIVS

### Exempel 1: starta emulatorn och starta en webbläsare
```
PS C:\> Start-AzureEmulator -L
```

I det här exemplet körs tjänsten i Azure-emulatorn och ett nytt webbläsarfönster öppnas i den emulerade tjänsten.

## MALLPARAMETRAR

### -Lansera
Öppnar ett nytt webbläsarfönster på tjänsten när det är inloggat i emulatorn.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ln

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Mode
Anger emuleringsläge.
Giltiga värden är: full och Express.
Standardvärdet är uttrycka.

```yaml
Type: ComputeEmulatorMode
Parameter Sets: (All)
Aliases: 

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

[Publicera – AzureServiceProject](./Publish-AzureServiceProject.md)

[Stopp-AzureEmulator](./Stop-AzureEmulator.md)


