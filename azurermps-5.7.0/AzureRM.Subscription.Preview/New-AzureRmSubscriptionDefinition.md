---
external help file: Microsoft.Azure.Commands.SubscriptionDefinition.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.subscription.preview/new-azurermsubscriptiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/New-AzureRmSubscriptionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/New-AzureRmSubscriptionDefinition.md
ms.openlocfilehash: 7acaca4977114a1a57f88f5050f658753a9b6214
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581895"
---
# New-AzureRmSubscriptionDefinition

## Sammanfattning
Skapar en prenumerations definition.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### Skapa abonnemangs definition
```
New-AzureRmSubscriptionDefinition -Name <String> -OfferType <String> [-SubscriptionDisplayName <String>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureRmSubscriptionDefinition** skapar en prenumerations definition.

## BESKRIVS

### Exempel 1
```
PS C:\> New-AzureRmSubscriptionDefinition -Name MySubDef -OfferType MS-AZR-0017P

Name                    : MySubDef
SubscriptionId          : 86869d42-1782-4337-98b0-c905fb937d46
SubscriptionDisplayName : MySubDef
OfferType               : MS-AZR-0017P
```

Skapar en prenumerations definition med ett förvalt visnings namn för abonnemanget.

### Exempel 2
```
PS C:\> New-AzureRmSubscriptionDefinition -Name MySubDef -OfferType MS-AZR-0017P -SubscriptionDisplayName MyPaygoSub

Name                    : MySubDef
SubscriptionId          : 86869d42-1782-4337-98b0-c905fb937d46
SubscriptionDisplayName : MyPaygoSub
OfferType               : MS-AZR-0017P
```

Skapar en prenumerations definition med ett anpassat abonnemangs visnings namn.

## MALLPARAMETRAR

### -Namn
Namnet på den prenumerations definition som ska skapas.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OfferType
Den typ av erbjudande som ska användas när det underliggande abonnemanget skapas.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionDisplayName
Visnings namnet som ska användas när prenumerations definitionen för ett underliggande abonnemang skapas.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen

## VÄRDEN

### Microsoft. Azure. commands. SubscriptionDefinition. Models. PSSubscriptionDefinition

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

