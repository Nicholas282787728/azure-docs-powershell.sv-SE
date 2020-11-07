---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageTable.md
ms.openlocfilehash: 29b2bb0c6a9c6e8e34c08a7ce04ca1c3ed071c84
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923553"
---
# New-AzStorageTable

## Sammanfattning
Skapar en lagrings tabell.

## FRÅGESYNTAXEN

```
New-AzStorageTable [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzStorageTable** skapar en lagrings tabell som är kopplad till lagrings kontot i Azure.

## BESKRIVS

### Exempel 1: skapa en Azure Storage-tabell
```
PS C:\>New-AzStorageTable -Name "tableabc"
```

Det här kommandot skapar en lagrings tabell med namnet tableabc.

### Exempel 2: skapa flera Azure Storage-tabeller
```
PS C:\>"table1 table2 table3".split() | New-AzStorageTable
```

Det här kommandot skapar flera tabeller.
Den använder metoden **Split** i **klassen .net och** skickar sedan namnen i pipeline.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Anger ett namn för den nya tabellen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

[Get-AzStorageTable](./Get-AzStorageTable.md)

[Remove-AzStorageTable](./Remove-AzStorageTable.md)


