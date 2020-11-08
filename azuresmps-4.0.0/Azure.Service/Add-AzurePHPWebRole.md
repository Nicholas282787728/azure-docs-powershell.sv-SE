---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: F9A06B8B-55DB-48A5-B246-53347E759E64
online version: ''
schema: 2.0.0
ms.openlocfilehash: 050c05f2cdad546388744bcebca4f28a12a03038
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099620"
---
# Add-AzurePHPWebRole

## Sammanfattning
Skapar nödvändiga filer och konfiguration för ett PHP-program.

## FRÅGESYNTAXEN

```
Add-AzurePHPWebRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.
För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .

Cmdleten **Add-AzurePHPWebRole** skapar filer och konfigurationer, som ibland kallas för scaffolding, för ett PHP-program som hanteras i Azure via IIS.

## BESKRIVS

### Exempel 1: lägga till en webb roll med standardvärden
```
PS C:\> Add-AzurePHPWebRole
```

I det här exemplet läggs nödvändiga filer och konfiguration för ny webb roll till med standardvärdena för en tjänst med namnet "WebRole1" med 1 instans.

### Exempel 2: lägga till en webb roll med flera instanser
```
PS C:\> Add-AzurePHPWebRole MyWebRole -I 2
```

I det här exemplet läggs nödvändiga filer och inställningar till för den nya webb rollen till det aktuella programmet, med namnet "MyWebRole" och en roll instans räkning på 2.

## MALLPARAMETRAR

### -Instanser
Anger antalet roll instanser för webb rollen.
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
Anger namnet på webb rollen.
Namnet bestämmer namnet på den katalog som innehåller de nödvändiga filerna och konfigurationen för PHP-programmet.
Standardvärdet för webrole #, där # är antalet webb roller i tjänsten.

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

[Add-AzurePHPWorkerRole](./Add-AzurePHPWorkerRole.md)

[New-AzureServiceProject](./New-AzureServiceProject.md)


