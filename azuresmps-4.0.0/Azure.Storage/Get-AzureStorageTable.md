---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f2bccab190fc27b5e97ecf3af502d3488f28998
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572343"
---
# Get-AzureStorageTable

## Sammanfattning
Visar lagrings tabellerna.

## FRÅGESYNTAXEN

### TableName (standard)
```
Get-AzureStorageTable [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### TablePrefix
```
Get-AzureStorageTable -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureStorageTable** innehåller lagrings tabeller som är kopplade till lagrings kontot i Azure.

## BESKRIVS

### Exempel 1: lista alla Azure Storage-tabeller
```
PS C:\>Get-AzureStorageTable
```

Det här kommandot hämtar alla lagrings tabeller för ett lagrings konto.

### Exempel 2: lista Azure Storage-tabeller med ett jokertecken
```
PS C:\>Get-AzureStorageTable -Name table*
```

Det här kommandot använder ett jokertecken för att hämta lagrings tabeller vars namn börjar med tabellen.

### Exempel 3: lista Azure Storage-tabeller med hjälp av tabell namns prefix
```
PS C:\>Get-AzureStorageTable -Prefix "table"
```

Det här kommandot använder parametern *prefix* för att hämta lagrings tabeller vars namn börjar med tabellen.

## MALLPARAMETRAR

### -Kontext
Anger lagrings kontexten.
För att skapa den kan du använda New-AzureStorageContext cmdlet.

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
Anger tabell namnet.
Om tabell namnet är tomt visar cmdleten alla tabeller.
Annars visas alla tabeller som matchar det angivna namnet eller det vanliga namn mönstret.

```yaml
Type: String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Prefix
Anger ett prefix som används i namnet på den eller de tabeller som du vill hämta.
Du kan använda den här för att hitta alla tabeller som börjar med samma sträng, till exempel tabell.

```yaml
Type: String
Parameter Sets: TablePrefix
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

[New-AzureStorageTable](./New-AzureStorageTable.md)

[Remove-AzureStorageTable](./Remove-AzureStorageTable.md)


