---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: 5270d77a9f9cd05b8075011e3fc002ac47d5c3a6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744567"
---
# Get-AzDataLakeStoreItemPermission

## Sammanfattning
Får behörigheten oktalt för en fil eller mapp i data Lake Store.

## FRÅGESYNTAXEN

```
Get-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzDataLakeStoreItemPermission** får behörigheten oktalt för en fil eller mapp i data Lake Store.

## BESKRIVS

### Exempel 1: Ange behörigheten oktalt för en fil
```
PS C:\>Get-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

Det här kommandot får behörigheten oktalt för en fil.

## MALLPARAMETRAR

### -Konto
Anger namnet på data Lake Store-butiken.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -Path
Anger data Lake Store-sökvägen till filen eller mappen, med början med rot katalogen (/).

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

### Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance

## VÄRDEN

### System. String

## ANMÄRKNINGAR
* Alias: Get-AdlStoreItemPermission

## RELATERADE LÄNKAR

[Set-AzDataLakeStoreItemPermission](./Set-AzDataLakeStoreItemPermission.md)


