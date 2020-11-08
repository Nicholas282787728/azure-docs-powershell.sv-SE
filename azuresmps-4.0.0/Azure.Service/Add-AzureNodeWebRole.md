---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: C2DAFB2C-A58B-406C-8349-8728771B279E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 59aef29c27d7eb96834d270c2fce48ff3acb9554
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099622"
---
# Add-AzureNodeWebRole

## Sammanfattning
Skapar nödvändiga filer och mappar för ett Node.js-program.

## FRÅGESYNTAXEN

```
Add-AzureNodeWebRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.
För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .

**AzureNodeWebRole** skapar nödvändiga filer och mappar, som ibland kallas för scaffolding, för ett Node.js-program som ska finnas i molnet via IIS.

## BESKRIVS

### Exempel 1: webb rollen enkel instans
```
PS C:\> Add-AzureNodeWebRole -Name MyWebRole
```

I det här exemplet läggs scaffolding för en webb roll med namnet **MyWebRole** till det aktuella programmet.

### Exempel 2: webb rollen flera instanser
```
PS C:\> Add-AzureNodeWebRole MyWebRole -I 2
```

I det här exemplet läggs scaffolding till för en ny webb roll med namnet **MyWebRole** till det aktuella programmet, med antal roller på en roll instans.

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
Det bestämmer också namnet på den katalog som innehåller scaffolding för det node.js-program som finns i webb rollen.
Standardvärdet för webrole #, där # anger antalet webb roller i tjänsten.

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

[Add-AzureNodeWorkerRole](./Add-AzureNodeWorkerRole.md)

[New-AzureServiceProject](./New-AzureServiceProject.md)


