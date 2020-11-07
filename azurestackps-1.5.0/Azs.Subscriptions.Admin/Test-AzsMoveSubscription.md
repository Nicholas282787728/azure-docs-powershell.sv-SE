---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 24108a767ec1e423d544fa4fb3eaf8bc419f62d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754975"
---
# Test-AzsMoveSubscription

## Sammanfattning
Verifiera att användar prenumerationer kan flyttas mellan erbjudna leverantörs erbjudanden.

## FRÅGESYNTAXEN

```
Test-AzsMoveSubscription [[-DestinationDelegatedProviderOffer] <String>] [-ResourceId] <String[]> [-AsJob]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Verifiera att användar prenumerationer kan flyttas mellan erbjudna leverantörs erbjudanden.

## BESKRIVS

### --------------------------EXEMPEL 1--------------------------
```
Test that user subscriptions can be moved to a delegated provider offer.
```

Test-MoveSubscription \` -DestinationDelegatedProviderOffer "/Subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1"-ResourceID "/Subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.admin/Subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6", "/Subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.admin/Subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"

### --------------------------EXEMPEL 2--------------------------
```
Test that user subscriptions can be moved from a delegated provider to the Default Provider.
```

$resourceIds = Get-AzsUserSubscription-filter "offerName EQ ' O1 ' | Select-ExpandProperty ID Test-MoveSubscription-ResoruceId $resourceIds

## MALLPARAMETRAR

### -AsJob
Anger om flytt åtgärden ska utföras som ett jobb.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationDelegatedProviderOffer
Anger det fullständigt kvalificerade delegerade leverantörs offerter som den här cmdleten flyttar abonnemang till.
NULL om prenumerationen ska flyttas tillbaka till standardprovidern.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Anger en matris med fullständigt kvalificerade prenumerations resurs-ID som denna cmdlet flyttar.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

