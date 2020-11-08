---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
ms.openlocfilehash: df4d31c1a90808e4d289cab60c5edf9785de1182
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269575"
---
# Get-AzStorageQueue

## Sammanfattning
Visar lagrings köer.

## FRÅGESYNTAXEN

### QueueName (standard)
```
Get-AzStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### QueuePrefix
```
Get-AzStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzStorageQueue** innehåller alla lagrings köer som är associerade med ett Azure Storage-konto.

## BESKRIVS

### Exempel 1: lista alla köer för Azure-lagring
```
PS C:\>Get-AzStorageQueue
```

Det här kommandot får en lista över alla lagrings köer för det aktuella lagrings kontot.

### Exempel 2: lista Azure Storage-köer med ett jokertecken
```
PS C:\>Get-AzStorageQueue -Name queue*
```

Det här kommandot använder ett jokertecken för att hämta en lista med lagrings köer vars namn börjar med kön.

### Exempel 3: lista Azure Storage köer med prefixet könamn
```
PS C:\>Get-AzStorageQueue -Prefix "queue"
```

I det här exemplet används parametern *prefix* för att hämta en lista med lagrings köer vars namn börjar med kön.

## MALLPARAMETRAR

### -Kontext
Anger Azure Storage-kontexten.
Du kan skapa det med hjälp av **New-AzStorageContext** cmdlet.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Anger ett namn.
Om du inte anger något namn visas en lista över alla köer i cmdleten.
Om ett fullständigt eller delvis namn anges får cmdleten alla köer som matchar namn mönstret.

```yaml
Type: System.String
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
Type: System.String
Parameter Sets: QueuePrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

### Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext

## VÄRDEN

### Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageQueue

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzStorageQueue](./New-AzStorageQueue.md)

[Remove-AzStorageQueue](./Remove-AzStorageQueue.md)


