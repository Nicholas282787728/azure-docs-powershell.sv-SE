---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0f8c9192100536a04b664f981a9df9e1508a1f87
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100143"
---
# Get-AzsStorageShare

## Sammanfattning
Returnerar en lista med lagrings resurser.

## FRÅGESYNTAXEN

### Lista (standard)
```
Get-AzsStorageShare -FarmName <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### Lära
```
Get-AzsStorageShare -FarmName <String> -ShareName <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### ID
```
Get-AzsStorageShare -ResourceId <String> [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Returnerar en lista med lagrings resurser.

## BESKRIVS

### EXEMPEL 1
```
Get-AzsStorageShare -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

Hämta listan med lagrings resurser.

## MALLPARAMETRAR

### -FarmName
Server grupp-ID.

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

### -ShareName
Resurs namn.

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

### -ResourceGroupName
Resurs grupps namn.

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### Microsoft. AzureStack. Management. Storage. admin. Models. share

## ANMÄRKNINGAR

## RELATERADE LÄNKAR
