---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88c19285ee7188dab272eeab7a668f5f5dfe22a4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743550"
---
# Get-AzsDelegatedProvider

## Sammanfattning
Hämta listan med delegatedProviders.

## FRÅGESYNTAXEN

### Lista (standard)
```
Get-AzsDelegatedProvider [<CommonParameters>]
```

### Lära
```
Get-AzsDelegatedProvider [-DelegatedProviderId] <Guid> [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Hämta listan med delegatedProviders.

## BESKRIVS

### --------------------------EXEMPEL 1--------------------------
```
Get-AzsDelegatedProvider
```

Få en lista med delegerade providrar.

### --------------------------EXEMPEL 2--------------------------
```
Get-AzsDelegatedProvider -DelegatedProviderId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

Skaffa en specifik delegerad leverantör.

## MALLPARAMETRAR

### -DelegatedProviderId
DelegatedProvider-ID.

```yaml
Type: Guid
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

### Microsoft. AzureStack. Management. Subscriptions. admin. Models. Subscription

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

