---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 11a8ffe26a65bf2ecabab7807d8e54bc23b629fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572371"
---
# Get-AzureStorageQueue

## Sammanfattning
Visar lagrings köer.

## FRÅGESYNTAXEN

### QueueName (standard)
```
Get-AzureStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### QueuePrefix
```
Get-AzureStorageQueue -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureStorageQueue** innehåller alla lagrings köer som är associerade med ett Azure Storage-konto.

## BESKRIVS

### Exempel 1: lista alla köer för Azure-lagring
```
PS C:\>Get-AzureStorageQueue
```

Det här kommandot får en lista över alla lagrings köer för det aktuella lagrings kontot.

### Exempel 2: lista Azure Storage-köer med ett jokertecken
```
PS C:\>Get-AzureStorageQueue -Name queue*
```

Det här kommandot använder ett jokertecken för att hämta en lista med lagrings köer vars namn börjar med kön.

### Exempel 3: lista Azure Storage köer med prefixet könamn
```
PS C:\>Get-AzureStorageQueue -Prefix "queue"
```

I det här exemplet används parametern *prefix* för att hämta en lista med lagrings köer vars namn börjar med kön.

## MALLPARAMETRAR

### -Kontext
Anger Azure Storage-kontexten.
Du kan skapa det med hjälp av **New-AzureStorageContext** cmdlet.

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Namn
Anger ett namn.
Om du inte anger något namn visas en lista över alla köer i cmdleten.
Om ett fullständigt eller delvis namn anges får cmdleten alla köer som matchar namn mönstret.

```yaml
Type: String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Prefix
Anger ett prefix som används i namnet på de köer som du vill hämta.

```yaml
Type: String
Parameter Sets: QueuePrefix
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

## RELATERADE LÄNKAR

[New-AzureStorageQueue](./New-AzureStorageQueue.md)

[Remove-AzureStorageQueue](./Remove-AzureStorageQueue.md)


