---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueue.md
ms.openlocfilehash: 6363b8030571d6cf3e89b30229395b16cdb5f44b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577312"
---
# New-AzureStorageQueue

## Sammanfattning
Skapar en lagrings kö.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureStorageQueue** skapar en lagrings kö i Azure.

## BESKRIVS

### Exempel 1: skapa en Azure Storage-kö
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

I det här exemplet skapas en lagrings kö med namnet queueabc.

### Exempel 2: skapa flera Azure Storage-köer
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

I det här exemplet skapas flera lagrings köer.
Den använder metoden Split i klassen .NET och skickar sedan namnen i pipeline.

## MALLPARAMETRAR

### -Kontext
Anger Azure Storage-kontexten.
Du kan skapa det med hjälp av New-AzureStorageContext cmdlet.

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
Anger ett namn för kön.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### IStorageContext

Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline

### Strängvärdet

Parametern "name" accepterar värdet för typen String från pipeline

## VÄRDEN

### Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageQueue

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureStorageQueue](./Get-AzureStorageQueue.md)

[Remove-AzureStorageQueue](./Remove-AzureStorageQueue.md)


