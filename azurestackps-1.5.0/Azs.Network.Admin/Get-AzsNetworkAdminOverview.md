---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d3c564a004c006a9fd77c6fb5cef034b402b0b1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571695"
---
# Get-AzsNetworkAdminOverview

## Sammanfattning
Få en översikt över statusen för nätverks resurs leverantören.

## FRÅGESYNTAXEN

```
Get-AzsNetworkAdminOverview [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Få en översikt över statusen för nätverks resurs leverantören. Enskilda egenskaper ger detaljerad information om resursanvändning och hälsa efter komponent.

## BESKRIVS

### --------------------------EXEMPEL 1--------------------------
```
Get-AzsNetworkAdminOverview
```

Få översikt över nätverks administratör.

### --------------------------EXEMPEL 2--------------------------
```
(Get-AzsNetworkAdminOverview).PublicIpAddressUsage
```

Få offentlig IP-adress.

## MALLPARAMETRAR

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### Microsoft. AzureStack. Management. Network. admin. Models. AdminOverview

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

