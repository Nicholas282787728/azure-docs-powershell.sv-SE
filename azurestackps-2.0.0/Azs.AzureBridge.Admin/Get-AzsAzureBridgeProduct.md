---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: edcc9bea35e1675b42a04c2b4e804c48ba052742
ms.sourcegitcommit: 5fcf17330d6f335561640a5ee3d98c59f7baab94
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/26/2020
ms.locfileid: "94100549"
---
# Get-AzsAzureBridgeProduct

## Sammanfattning
Returnerar en lista med tillgängliga produkter att ladda ned från Azure Marketplace.

## FRÅGESYNTAXEN

### Lista (standard)
```
Get-AzsAzureBridgeProduct -ActivationName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### Lära
```
Get-AzsAzureBridgeProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [<CommonParameters>]
```

### ID
```
Get-AzsAzureBridgeProduct -ResourceId <String> [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Returnerar en lista med tillgängliga produkter att ladda ned från Azure Marketplace.

## BESKRIVS

### --------------------------EXEMPEL 1--------------------------
```
Get-AzsAzureBridgeProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

Få en lista med tillgängliga produkter att ladda ned från Azure Marketplace.

### --------------------------EXEMPEL 2--------------------------
```
Get-AzsAzureBridgeProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG' -Name 'microsoft.docker-arm.1.1.0'
```

Skaffa en produkt information som kan laddas ner från Azure Marketplace med namn.

## MALLPARAMETRAR

### -ActivationName
Namn på aktiveringen.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Namnet på produkten.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Resurs gruppen som resursen finns under.

```yaml
Type: System.Management.Automation.PSObject
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
Type: System.Management.Automation.PSObject
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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### Microsoft. AzureStack. Management. AzureBridge. admin. Models. ProductResource

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

