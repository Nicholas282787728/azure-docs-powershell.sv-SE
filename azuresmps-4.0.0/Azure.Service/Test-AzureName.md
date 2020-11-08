---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 0DF54C9D-7A19-4591-A1FC-33C6A4C9BF33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 05a99e1a4965329c0eeb29fe0e014814fd1807b2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099167"
---
# Test-AzureName

## Sammanfattning
Testar om ett namn på Microsoft Azure Cloud-tjänsten, lagrings tjänstens namn eller Service Bus-namnutrymmet finns eller inte.

## FRÅGESYNTAXEN

### Serv
```
Test-AzureName [-Service] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Lagringsrelaterade
```
Test-AzureName [-Storage] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ServiceBusNamespace
```
Test-AzureName [-ServiceBusNamespace] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Webbplats
```
Test-AzureName [-Website] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Om namnet finns returnerar cmdleten $True.
Om namnet inte existerar returneras $False.

## BESKRIVS

### Exempel 1
```
PS C:\> Test-AzureName -Service "MyNameService1"
```

Det här kommandot testar för att se om "MyNameService1" är ett befintligt namn på Microsoft Azure Cloud-tjänsten.

### Exempel 2
```
PS C:\> Test-AzureName -Storage "mystorename1"
```

Det här kommandot testar för att se om "mystorename1" är ett befintligt Microsoft Azure Storage Service-namn.

### Exempel 3
```
PS C:\> Test-AzureName -ServiceBusNamespace "mynamespace"
```

Det här kommandot testar för att se om "multinamespace" är en befintlig Microsoft Azure Service Bus-namnrymd.

## MALLPARAMETRAR

### -Namn
Anger namnet på det tjänst-eller lagrings konto som ska testas.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profil
Anger den Azure-profil från vilken denna cmdlet läser.
Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.

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

### -Service
Anger att du vill testa ett befintligt tjänst konto.

```yaml
Type: SwitchParameter
Parameter Sets: Service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceBusNamespace
Anger att du vill testa ett befintligt Service Bus-namnområde.

```yaml
Type: SwitchParameter
Parameter Sets: ServiceBusNamespace
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Lagring
Anger att du vill testa ett befintligt lagrings konto.

```yaml
Type: SwitchParameter
Parameter Sets: Storage
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Webbplats
Anger att du vill testa en befintlig webbplats.

```yaml
Type: SwitchParameter
Parameter Sets: Website
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

## ANMÄRKNINGAR
* nod-dev, php-dev, python-dev

## RELATERADE LÄNKAR

