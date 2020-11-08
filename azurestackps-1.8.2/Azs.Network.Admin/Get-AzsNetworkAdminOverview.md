---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f5fbef7c67676f16793b63a8448517ca24aa7e5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94099845"
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

### EXEMPEL 1
```
Get-AzsNetworkAdminOverview
```

Få översikt över nätverks administratör.

### EXEMPEL 2
```
(Get-AzsNetworkAdminOverview).PublicIpAddressUsage
```

Få offentlig IP-adress.

## MALLPARAMETRAR

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### Microsoft. AzureStack. Management. Network. admin. Models. AdminOverview

## ANMÄRKNINGAR

## RELATERADE LÄNKAR
