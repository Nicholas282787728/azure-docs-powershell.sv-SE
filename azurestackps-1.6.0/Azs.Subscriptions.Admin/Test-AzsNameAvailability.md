---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 267a5bf4c3f864c987c0bc747eefce9dd3ffe6b0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571787"
---
# Test-AzsNameAvailability

## Sammanfattning
Returnerar avaialbility för angiven prenumerations resurs typ och namn

## FRÅGESYNTAXEN

```
Test-AzsNameAvailability -Name <String> -ResourceType <String> [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Returnerar avaialbility för angiven prenumerations resurs typ och namn

## BESKRIVS

### --------------------------EXEMPEL 1--------------------------
```
Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name offername1
```

Returnerar avaialbility för angiven prenumerations resurs typ och namn

## MALLPARAMETRAR

### -Namn
Resurs namn som ska verifieras.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceType
Resurs typen för att verifiera.

```yaml
Type: String
Parameter Sets: (All)
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

### Microsoft. AzureStack. Management. abonnemang. admin. Models. CheckNameAvailabilityResponse

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

