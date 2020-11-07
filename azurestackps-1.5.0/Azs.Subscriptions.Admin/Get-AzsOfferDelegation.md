---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6c58e8dedf4f55a9e1fb6451bf7f774b766b6d71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93755031"
---
# Get-AzsOfferDelegation

## Sammanfattning
Hämta listan med ombud.

## FRÅGESYNTAXEN

### Lista (standard)
```
Get-AzsOfferDelegation -OfferName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### Lära
```
Get-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [<CommonParameters>]
```

### ID
```
Get-AzsOfferDelegation -ResourceId <String> [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Hämta listan med ombud.

## BESKRIVS

### --------------------------EXEMPEL 1--------------------------
```
Get-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1
```

Hämta listan med ombud.

## MALLPARAMETRAR

### -Namn
Namn på en ombuds delegering.

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OfferName
Namn på ett bud.

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Resurs gruppen som resursen finns under.

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Resurs-ID.

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Hoppa över
Hoppa över de första N objekten enligt värdet i parametervärdet.

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### -Överst
Returnera de översta N objekten enligt värdet i parametervärdet.
Gäller efter parametern-Skip.

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### Microsoft. AzureStack. Management. abonnemang. admin. Models. OfferDelegation

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

