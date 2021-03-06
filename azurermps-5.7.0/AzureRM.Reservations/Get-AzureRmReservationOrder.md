---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrder.md
ms.openlocfilehash: 0dc5eba8b498be7814ae74eca6953a5cadb01f22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576436"
---
# Get-AzureRmReservationOrder

## Sammanfattning
Lära `ReservationOrder`

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Get-AzureRmReservationOrder [-ReservationOrderId <String>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Lista över alla `ReservationOrder` s som användaren har till gång till i den aktuella klient organisationen. Om ReservationOrderId parameter är aktive rad ska du hämta specifika ReservationOrder.

## BESKRIVS

### Exempel 1
```
PS C:\> Get-AzureRmReservationOrder
```

Visa alla `ReservationOrder` som användaren har åtkomst till i den aktuella klient organisationen

### Exempel 2
```
PS C:\> Get-AzureRmReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

Få `ReservationOrder` med angiven ReservationOrderId

## MALLPARAMETRAR

### -ReservationOrderId
ID för den specifika ReservationOrder som användaren vill se

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen

## VÄRDEN

### Microsoft. Azure. commands. reservations. Models. PSReservationOrderPage
Microsoft. Azure. commands. reservations. Models. PSReservationOrder

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

