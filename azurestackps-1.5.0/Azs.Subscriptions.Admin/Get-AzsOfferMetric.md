---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8228a8605462b71fce598c7dc44454a16e1d7c90
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754926"
---
# Get-AzsOfferMetric

## Sammanfattning
Skaffa Mät värden.

## FRÅGESYNTAXEN

```
Get-AzsOfferMetric [-OfferName] <String> [-ResourceGroupName] <String> [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Skaffa Mät värden.

## BESKRIVS

### --------------------------EXEMPEL 1--------------------------
```
Get-AzsOfferMetric -ResourceGroupName rg1 -OfferName offername1
```

Skaffa Mät värden.

## MALLPARAMETRAR

### -OfferName
Namn på ett bud.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Resurs gruppen som resursen finns under.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### Microsoft. AzureStack. Management. abonnemang. admin. Models. Metric

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

