---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4bd00dc1709a3060da9777ab4755ae1c6a28ec4
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921302"
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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### Microsoft. AzureStack. Management. abonnemang. admin. Models. CheckNameAvailabilityResponse

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

