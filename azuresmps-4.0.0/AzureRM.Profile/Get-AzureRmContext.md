---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 914b75e3952f7841aaf3ff505f51f7b4ebdc6044
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571751"
---
# Get-AzureRmContext

## Sammanfattning
Hämtar de metadata som används för att autentisera Azure Resource Manager-begäranden.

## FRÅGESYNTAXEN

```
Get-AzureRmContext [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Den Get-AzureRmContext cmdleten hämtar de aktuella metadata som används för att autentisera Azure Resource Manager-begäranden.

Denna cmdlet hämtar Active Directory-kontot, Active Directory-klienten, Azure-prenumerationen och mål Azure-miljön.
Azure Resource Manager-cmdlets använder de här inställningarna som standard när du gör Azure Resource Manager-begäranden.

## BESKRIVS

### Exempel 1: hämta den aktuella kontexten
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmContext

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

I det här exemplet loggar vi in på vårt konto med ett Azure-abonnemang med hjälp av Add-AzureRmAccount och sedan hämtas den aktuella sessionens kontext genom att ringa get-AzureRmContext.

## MALLPARAMETRAR

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### PSAzureContext
Denna cmdlet returnerar det konto, den klient organisation och det abonnemang som används av Azure Resource Manager-cmdletar.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Set-AzureRMContext]()

