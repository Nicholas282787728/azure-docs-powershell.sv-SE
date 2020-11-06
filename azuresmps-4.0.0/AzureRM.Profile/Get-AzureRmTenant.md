---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2cabb88c490c7fdea56fd5ffde280cfd55bc8f3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571744"
---
# Get-AzureRmTenant

## Sammanfattning
Får klient organisationer som har behörighet för den aktuella användaren.

## FRÅGESYNTAXEN

```
Get-AzureRmTenant [[-TenantId] <String>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Get-AzureRmTenant-cmdleten får innehavare som är auktoriserade för den aktuella användaren.

## BESKRIVS

### Exempel 1: Hämta alla innehavare
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com

TenantId : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Domain   : microsoft.com
```

Det här exemplet visar hur du får alla auktoriserade klient organisationer för ett Azure-konto.

### Exempel 2: skaffa en speciell klient organisation
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com
```

Det här exemplet visar hur du får en viss auktoriserad klient organisation för ett Azure-konto.

## MALLPARAMETRAR

### -TenantId
Anger ID för den klient organisation som denna cmdlet får.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Domain, Tenant

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### PSAzureTenant
Denna cmdlet returnerar klient-ID och associerad domän information för klient organisationer som har behörighet för det aktuella kontot.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

