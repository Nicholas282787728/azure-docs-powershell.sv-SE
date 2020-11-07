---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9374f8a55beca561afd9ed4bca4320b685349798
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/22/2020
ms.locfileid: "93931661"
---
# Get-AzsAzureBridgeActivation

## Sammanfattning
Returnerar aktiveringen av Azure-bryggan.

## FRÅGESYNTAXEN

### Lista (standard)
```
Get-AzsAzureBridgeActivation -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### Lära
```
Get-AzsAzureBridgeActivation -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### ID
```
Get-AzsAzureBridgeActivation -ResourceId <String> [<CommonParameters>]
```

## PROBLEMBESKRIVNING
När Azure-stacken har registrerats innehåller aktiverings objektet information som länkar en Azure Stack-distribution till dess registrering i Azure, till exempel förfallo datum, namn, etc.

## BESKRIVS

### EXEMPEL 1
```
Get-AzsAzureBridgeActivation -ResourceGroupName 'activationRG'
```

Få en lista med Azure Bridge-aktiveringar under resurs gruppen "activationRG"

### EXEMPEL 2
```
Get-AzsAzureBridgeActivation -Name 'myActivation' -ResourceGroupName 'activationRG'
```

Få en Azure Bridge-aktivering med namn ' aktiveringsbegäran ' under ' activationRG '

## MALLPARAMETRAR

### -Namn
Namn på aktiveringen.

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
Resurs gruppen som används vid registrering av Azure Stack; Du kan också Visa resurs grupp namn i portalen.

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### Microsoft. AzureStack. Management. AzureBridge. admin. Models. ActivationResource

## ANMÄRKNINGAR

## RELATERADE LÄNKAR
