---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslpredefinedpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySslPredefinedPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySslPredefinedPolicy.md
ms.openlocfilehash: 2c55da6b7193d02de51e273df4626152d6d088fb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922303"
---
# Get-AzApplicationGatewaySslPredefinedPolicy

## Sammanfattning
Hämtar fördefinierade SSL-principer från Application Gateway.

## FRÅGESYNTAXEN

```
Get-AzApplicationGatewaySslPredefinedPolicy [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzApplicationGatewaySslPredefinedPolicy** hämtar fördefinierade SSL-principer från Application Gateway.

## BESKRIVS

### Exempel 1
```
PS C:\>$policies = Get-AzApplicationGatewaySslPredefinedPolicy
```

Dessa kommandon returnerar alla fördefinierade SSL-principer.

### Exempel 2
```
PS C:\>$policy = Get-AzApplicationGatewaySslPredefinedPolicy -Name AppGwSslPolicy20170401
```

Det här kommandot returnerar en fördefinierad princip med namnet AppGwSslPolicy20170401.

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Namn på den fördefinierade SSL-principen

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen

## VÄRDEN

### Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySslPredefinedPolicy
System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. Network. Models. PSApplicationGatewaySslPredefinedPolicy, Microsoft. Azure. commands. Network, version = 4.1.0.0, Culture = neutralt, PublicKeyToken = null]]

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

