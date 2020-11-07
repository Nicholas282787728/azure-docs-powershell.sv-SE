---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
ms.openlocfilehash: 892177efebb3a62e40f79b80b1ac67c488e048d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757455"
---
# Test-AzureRmServiceBusName

## Sammanfattning
Kontrollerar tillgänglighet för det angivna namn områdes namnet

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Test-AzureRmServiceBusName [-Namespace] <String>
```

## PROBLEMBESKRIVNING
**Test-AzureRmServiceBusName** cmdlet kontrollerar tillgänglighet för namn områdes namnet

## BESKRIVS

### Exempel 1
```
PS C:\> Test-AzureRmServiceBusName -Namespace TestingtheAvailability
```

### Exempel 2
```
PS C:\> Test-AzureRmServiceBusName -Namespace Testi
```

### Exempel 3
```
PS C:\> Test-AzureRmServiceBusName -Namespace Test123
```

Returnerar statusen för tillgänglighet för namn områdes namnet

## MALLPARAMETRAR

### -Namnrymd
Namn områdes namnet ServiceBus.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```
### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### -Namnrymd
 System. String

## VÄRDEN

### [Microsoft. Azure. kommandon. ServiceBus. Models. CheckNameAvailabilityResultAttributes, Microsoft. Azure. commands. ServiceBus, version = 0.1.0.0, Culture = neutralt, PublicKeyToken = null]

### Exempel 1
NameAvailable skäl
------------- ------ -------
         True   None

### Exempel 2
NameAvailable skäl
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.

### Exempel 3
NameAvailable skäl
-------------    ------ -------
        False NameInUse The specified service namespace is not available.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR
