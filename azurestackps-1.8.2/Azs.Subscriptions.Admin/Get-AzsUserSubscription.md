---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4403232b45b2a1e69d6148a118e69ccaf80e4a1e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100215"
---
# Get-AzsUserSubscription

## Sammanfattning
Hämta listan med användar abonnemang som administratör.

## FRÅGESYNTAXEN

### Lista (standard)
```
Get-AzsUserSubscription [-Filter <String>] [<CommonParameters>]
```

### Lära
```
Get-AzsUserSubscription -SubscriptionId <Guid> [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Hämta listan med användar abonnemang som administratör.

## BESKRIVS

### --------------------------EXEMPEL 1--------------------------
```
Get-AzsUserSubscription
```

Hämta listan med användar abonnemang som administratör.

## MALLPARAMETRAR

### -Filter
Parametern OData filter.

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Parametern prenumerations-ID.

```yaml
Type: Guid
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### Microsoft. AzureStack. Management. Subscriptions. admin. Models. Subscription

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

