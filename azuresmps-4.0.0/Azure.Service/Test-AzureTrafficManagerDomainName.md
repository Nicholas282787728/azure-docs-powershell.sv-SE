---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 92E2409B-14BC-428F-8BAF-60D8DAFA5F57
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1adaafdfdd4331bbba86530eb532964430ed7c69
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099165"
---
# Test-AzureTrafficManagerDomainName

## Sammanfattning
Kontrollerar om ett domän namn är tillgängligt som Traffic Manager-profil.

## FRÅGESYNTAXEN

```
Test-AzureTrafficManagerDomainName -DomainName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
**Test-AzureTrafficManagerDomainName** cmdlet kontrollerar om ett domän namn är tillgängligt som en Microsoft Azure Traffic Manager-profil.
Om domän namnet är tillgängligt returnerar denna cmdlet ett värde för $True.

## BESKRIVS

### Exempel 1: kontrol lera om ett domän namn är tillgängligt
```
PS C:\>Test-AzureTrafficManagerDomainName -DomainName "ContosoApp.trafficmanager.net"
$True
```

Det här kommandot kontrollerar om domän namnet ContosoApp.trafficmanager.net är tillgängligt som Traffic Manager-profil.

## MALLPARAMETRAR

### -Domän namn
Anger det domän namn som ska testas.
Du måste ta med följande sträng: 

. trafficmanager.net

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

### -Profil
Anger den Azure-profil från vilken denna cmdlet läser. Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.

```yaml
Type: AzureSMProfile
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

## VÄRDEN

### System. Boolean
Denna cmdlet skapar $True eller $False.
Om domän namnet är tillgängligt returnerar denna cmdlet ett värde för $True.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

