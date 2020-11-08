---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 819cdc45e75c15c38c9ae28c583ac3c73e54f4ac
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94099926"
---
# Get-AzsComputeQuota

## Sammanfattning
Returnerar kvoter som anger kvot gränser för beräkning av objekt.

## FRÅGESYNTAXEN

### Lista (standard)
```
Get-AzsComputeQuota [-Location <String>] [<CommonParameters>]
```

### Lära
```
Get-AzsComputeQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### ID
```
Get-AzsComputeQuota -ResourceId <String> [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Få en lista över befintliga kvoter.

## BESKRIVS

### --------------------------EXEMPEL 1--------------------------
```
Get-AzsComputeQuota -Location 'local'
```

Hämta alla beräknings kvoter på den angivna platsen.

### --------------------------EXEMPEL 2--------------------------
```
Get-AzsComputeQuota 'Default Quota'
```

Skaffa en specifik kvot.

## MALLPARAMETRAR

### -Plats
{{Fill location Description}}

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

### -Namn
Namn på kvoten.

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### ComputeQuotaObject

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

