---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: cfbe2cc695ceb2db7c498e8ee2750fa0427da114
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270405"
---
# New-AzStorageBlobRangeToRestore

## Sammanfattning
Skapar ett BLOB Range-objekt som återställer ett lagrings konto.

## FRÅGESYNTAXEN

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzStorageBlobRangeToRestore** skapar ett BLOB Range-objekt som kan användas i Återställ-AzStorageBlobRange.

## BESKRIVS

### Exempel 1: skapar ett BLOB-intervall att återställa
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

Det här kommandot skapar ett BLOB-intervall som ska återställas, som börjar på container1/blob1 (include) och slutar på container2/blob2 (exclude).

### Exempel 2: skapar ett BLOB-intervall som återställs från första blobben i alfabetisk ordning till en specifik BLOB (exkludera)
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

Det här kommandot skapar ett BLOB-intervall som återställs från första blobben i alfabetisk ordning till en specifik BLOB-container2/blob2 (exkludera)

### Exempel 3: skapar ett BLOB-intervall som återställs från en specifik BLOB (include) till sista blobben i alfabetisk ordning
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

Det här kommandot skapar ett BLOB-intervall som återställs från en specifik BLOB-container1/blob1 (include) till sista blobben i alfabetisk ordning.

### Exempel 4: skapar ett BLOB-intervall som återställer alla blobbar
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

Det här kommandot skapar ett BLOB-intervall som återställer alla blobbar.

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndRange
Ange slut intervallet för BLOB-återställning.
Slut intervallet utesluts i återställda blobs.
Ange den som Tom Strng för att återställa till slutet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartRange
Ange start intervallet för BLOB-återställning.
Start intervall tas med i återställda blobs.
Ange den som en tom sträng för att återställa från början.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen

## VÄRDEN

### Microsoft. Azure. commands. Management. Storage. Models. PSBlobRestoreRange

## ANMÄRKNINGAR

## RELATERADE LÄNKAR
