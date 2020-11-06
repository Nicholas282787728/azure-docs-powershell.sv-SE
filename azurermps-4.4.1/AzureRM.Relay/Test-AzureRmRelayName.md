---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
ms.openlocfilehash: 4b3afc0b41f6eaf68e7ec0c4f8ed976b36267c97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574539"
---
# Test-AzureRmRelayName

## Sammanfattning
Kontrollerar tillgänglighet för det angivna namn områdes namnet

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Test-AzureRmRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
**Test-AzureRmRelayName** cmdlet kontrollerar tillgänglighet för namn områdes namnet

## BESKRIVS

### Exempel 1
```
PS C:\> Test-AzureRmRelayName -Namespace TestingtheAvailability
```

### Exempel 2
```
PS C:\> Test-AzureRmRelayName -Namespace Testi
```

### Exempel 3
```
PS C:\> Test-AzureRmRelayName -Namespace Test123
```

Returnerar statusen för tillgänglighet för namn områdes namnet

## MALLPARAMETRAR

### -Namnrymd
Namn på relä området.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### -Namnrymd
 System. String

## VÄRDEN

### [Microsoft. Azure. commands. Relay. Models. CheckNameAvailabilityResultAttributes, Microsoft. Azure. commands. Relay, version = 0.1.0.0, Culture = neutralt, PublicKeyToken = null]

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

