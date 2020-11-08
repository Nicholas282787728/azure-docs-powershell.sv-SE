---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 8F00099A-042A-4450-B6CF-9EDA2350CBFC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94e1711bc42745b872a8e2abc8cf82e5e0e67db9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099559"
---
# Get-AzureRemoteAppCollection

## Sammanfattning
Hämtar information om en Azure RemoteApp-samling.

## FRÅGESYNTAXEN

```
Get-AzureRemoteAppCollection [[-CollectionName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRemoteAppCollection** hämtar information om Azure RemoteApp-samlingar i Microsoft Azure.
Den returnerar ett objekt med information om en viss samling, eller om ingen samling anges för alla samlingar i den aktuella prenumerationen.

## BESKRIVS

### Exempel 1: Visa en lista över alla samlingar
```
PS C:\> Get-AzureRemoteAppCollection
```

Det här kommandot returnerar en lista över alla Azure RemoteApp-samlingar i prenumerationen.

### Exempel 2: Hämta information om en viss samling
```
PS C:\> Get-AzureRemoteAppCollection ContosoApps
```

Det här kommandot returnerar information om Azure RemoteApp-samlingen med namnet ContosoApps.

### Exempel 3: Hämta en lista med samlingar med hjälp av jokertecken
```
PS C:\> Get-AzureRemoteAppCollection Finance*
```

Det här kommandot returnerar en lista över alla Azure RemoteApp-samlingar som matchar finansierings *.

## MALLPARAMETRAR

### -Samlings namn
Anger namnet på Azure RemoteApp-samlingen.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzureRemoteAppCollection](./New-AzureRemoteAppCollection.md)

[Remove-AzureRemoteAppCollection](./Remove-AzureRemoteAppCollection.md)

[Set-AzureRemoteAppCollection](./Set-AzureRemoteAppCollection.md)

[Update-AzureRemoteAppCollection](./Update-AzureRemoteAppCollection.md)


