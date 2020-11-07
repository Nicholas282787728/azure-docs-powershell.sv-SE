---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88ba307bb9232176d4900b80856e0e08b3dc445b
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921783"
---
# Get-AzsSubscription

## Sammanfattning
Hämta listan med prenumerationer.

## FRÅGESYNTAXEN

### Lista (standard)
```
Get-AzsSubscription [<CommonParameters>]
```

### Lära
```
Get-AzsSubscription [-SubscriptionId] <String> [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Hämta listan med prenumerationer.

## BESKRIVS

### EXEMPEL 1
```
Get-AzsSubscription
```

Hämta listan med prenumerationer.

## MALLPARAMETRAR

### -SubscriptionId
ID för abonnemanget.

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### Microsoft. AzureStack. Management. Subscription. Models. SubscriptionModel

## ANMÄRKNINGAR

## RELATERADE LÄNKAR
