---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: cfbe2cc695ceb2db7c498e8ee2750fa0427da114
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232542"
---
# New-AzStorageBlobRangeToRestore

## SYNOPSIS
Skapar ett Blob Range-objekt för att återställa ett lagringskonto.

## SYNTAX

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **New-AzStorageBlobRangeToRestore** skapar ett Blob range-objekt som kan användas i Restore-AzStorageBlobRange.

## EXEMPEL

### Exempel 1: Skapar ett blob-intervall för återställning
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

Det här kommandot skapar ett blob-område att återställa, som börjar med container1/blob1 (inkludera) och slutar vid container2/blob2 (exkludera).

### Exempel 2: Skapar ett blob-intervall som återställer från första blob i alfabetisk ordning till en viss blob (exkluderas)
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

Det här kommandot skapar ett blob-intervall som återställer från första blob i alfabetisk ordning till en specifik blob-behållare2/blob2 (exkludera)

### Exempel 3: Skapar ett blob-intervall som återställer från en specifik blob (inkludera) till den sista blob i alfabetisk ordning
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

Det här kommandot skapar ett blob-intervall som återställer från en specifik blob-behållare1/blob1 (inkludera) till den sista blob i alfabetisk ordning.

### Exempel 4: Skapar ett blob-intervall som återställer alla blobbar
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

Det här kommandot skapar ett blob-intervall som återställer alla blobbar.

## PARAMETERS

### -DefaultProfile
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

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
Ange blob-återställningens slutområde.
Slutområde exkluderas i återställ blobbar.
Ange den som tom om du vill återställa till slutet.

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
Ange blob-återställningens startområde.
Startintervallet inkluderas i återställ blobbar.
Ange det som en tom sträng att återställa från början.

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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### Ingen

## UTDATA

### Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange

## ANTECKNINGAR

## RELATERADE LÄNKAR
