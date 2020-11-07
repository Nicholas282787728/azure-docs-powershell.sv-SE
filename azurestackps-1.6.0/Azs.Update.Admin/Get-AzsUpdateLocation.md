---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a9234cb73b1f9c3652827293ae2813f78d7ce336
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93755014"
---
# Get-AzsUpdateLocation

## Sammanfattning
Hämta listan med uppdateringar.

## FRÅGESYNTAXEN

### Lista (standard)
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [<CommonParameters>]
```

### Lära
```
Get-AzsUpdateLocation [-Name <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### ID
```
Get-AzsUpdateLocation -ResourceId <String> [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Hämta listan med uppdateringar. Platserna som returneras kan användas för att hämta tillgängliga uppdateringar på en viss plats med Get-AzsUpdate.

## BESKRIVS

### --------------------------EXEMPEL 1--------------------------
```
Get-AzsUpdateLocation
```

Hämta listan med uppdateringar.

## MALLPARAMETRAR

### -Namn
Namnet på uppdaterings platsen.

```yaml
Type: String
Parameter Sets: Get
Aliases: Location

Required: False
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

Required: False
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
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### Microsoft. AzureStack. Management. Update. admin. Models. UpdateLocation

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

