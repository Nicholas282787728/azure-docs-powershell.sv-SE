---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5ff90957a655837dbdf75ce3f4242222615f2a73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921242"
---
# Get-AzsUserSubscription

## Sammanfattning
Hämta listan med användar abonnemang som operator.

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
Hämta listan med användar abonnemang som operator.

## BESKRIVS

### --------------------------EXEMPEL 1--------------------------
```
Get-AzsUserSubscription
```

Hämta listan med användar abonnemang som operator.

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### Microsoft. AzureStack. Management. Subscriptions. admin. Models. Subscription

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

