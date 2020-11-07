---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPredefinedPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPredefinedPolicy.md
ms.openlocfilehash: 03d47278681cbba23895c00b124cc3a2fc2cc6e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758388"
---
# Get-AzureRmApplicationGatewaySslPredefinedPolicy

## Sammanfattning
Hämtar fördefinierade SSL-principer från Application Gateway.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Get-AzureRmApplicationGatewaySslPredefinedPolicy [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmApplicationGatewaySslPredefinedPolicy** hämtar fördefinierade SSL-principer från Application Gateway.

## BESKRIVS

### Exempel 1
```
PS C:\>$policies = Get-AzureRmApplicationGatewaySslPredefinedPolicy
```

Dessa kommandon returnerar alla fördefinierade SSL-principer.

### Exempel 2
```
PS C:\>$policy = Get-AzureRmApplicationGatewaySslPredefinedPolicy -Name AppGwSslPolicy20170401
```

Det här kommandot returnerar en fördefinierad princip med namnet AppGwSslPolicy20170401.

## MALLPARAMETRAR

### -Namn
Namn på den fördefinierade SSL-principen

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### Ingen

## VÄRDEN

### Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySslPredefinedPolicy
System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. Network. Models. PSApplicationGatewaySslPredefinedPolicy, Microsoft. Azure. commands. Network, version = 4.1.0.0, Culture = neutralt, PublicKeyToken = null]]

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

