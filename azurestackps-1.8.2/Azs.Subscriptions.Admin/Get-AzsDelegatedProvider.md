---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: afc99afebed095da96d826918cc6912f197d1899
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100320"
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
{{Fill DelegatedProviderId Description}}

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### Microsoft. AzureStack. Management. Subscriptions. admin. Models. Subscription

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

