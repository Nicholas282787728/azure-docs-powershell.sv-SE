---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
ms.openlocfilehash: d501faaebcc5e381dc2a7270c8b55b148e2812b4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404163"
---
# Get-AzStorageTable

## Sammanfattning
Visar lagrings tabellerna.

## FRÅGESYNTAXEN

### TableName (standard)
```
Get-AzStorageTable [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### TablePrefix
```
Get-AzStorageTable -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzStorageTable** innehåller lagrings tabeller som är kopplade till lagrings kontot i Azure.

## BESKRIVS

### Exempel 1: lista alla Azure Storage-tabeller
```
PS C:\>Get-AzStorageTable
```

Det här kommandot hämtar alla lagrings tabeller för ett lagrings konto.

### Exempel 2: lista Azure Storage-tabeller med ett jokertecken
```
PS C:\>Get-AzStorageTable -Name table*
```

Det här kommandot använder ett jokertecken för att hämta lagrings tabeller vars namn börjar med tabellen.

### Exempel 3: lista Azure Storage-tabeller med hjälp av tabell namns prefix
```
PS C:\>Get-AzStorageTable -Prefix "table"
```

Det här kommandot använder parametern *prefix* för att hämta lagrings tabeller vars namn börjar med tabellen.

## MALLPARAMETRAR

### -Kontext
Anger lagrings kontexten.
För att skapa den kan du använda New-AzStorageContext cmdlet.

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
Anger tabell namnet.
Om tabell namnet är tomt visar cmdleten alla tabeller.
Annars visas alla tabeller som matchar det angivna namnet eller det vanliga namn mönstret.

```yaml
Type: System.String
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
Type: System.String
Parameter Sets: TablePrefix
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

### Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageTable

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzStorageTable](./New-AzStorageTable.md)

[Remove-AzStorageTable](./Remove-AzStorageTable.md)


