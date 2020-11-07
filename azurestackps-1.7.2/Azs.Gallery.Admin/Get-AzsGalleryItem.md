---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2020caba1d7cac4ed1830fbc1b6a3ccdb4c71f27
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921189"
---
# Get-AzsGalleryItem

## Sammanfattning
Visar en lista med Galleri objekt.

## FRÅGESYNTAXEN

### Lista (standard)
```
Get-AzsGalleryItem [<CommonParameters>]
```

### Lära
```
Get-AzsGalleryItem [-Name] <String> [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Få en lista med tillgängliga Galleri objekt i Azure Stack Marketplace

## BESKRIVS

### --------------------------EXEMPEL 1--------------------------
```
Get-AzsGalleryItem
```

List Galleri objekt.

### --------------------------EXEMPEL 2--------------------------
```
Get-AzsGalleryItem -Name 'microsoft.vmss.1.3.6'
```

Hämta ett galleri objekt efter namn.

## MALLPARAMETRAR

### -Namn
Identitet för GALLERYITEM.
Inkluderar Publisher-namn, artikel namn och kan innehålla version avgränsad efter period tecken.

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### Microsoft. AzureStack. Management. Gallery. admin. Models. GalleryItem

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

