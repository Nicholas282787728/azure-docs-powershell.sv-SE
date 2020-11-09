---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
ms.openlocfilehash: ad741d955399b355534074737741b153d8d48690
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320579"
---
# Get-AzDataLakeStoreItem

## Sammanfattning
Hämtar information om en fil eller mapp i data Lake Store.

## FRÅGESYNTAXEN

```
Get-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzDataLakeStoreItem** hämtar information om en fil eller mapp i data Lake Store.

## BESKRIVS

### Exempel 1: Hämta information om en fil från data Lake Store
```
PS C:\>Get-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

Det här kommandot får information om filen Test.csv från data Lake Store.

## MALLPARAMETRAR

### -Konto
Anger namnet på data Lake Store-kontot.

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
Anger sökvägen till data Lake Store från vilken du vill få information om ett objekt, från och med rot katalogen (/).

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

### Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance

## VÄRDEN

### Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreItem

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Exportera-AzDataLakeStoreItem](./Export-AzDataLakeStoreItem.md)

[Get-AzDataLakeStoreChildItem](./Get-AzDataLakeStoreChildItem.md)

[Import-AzDataLakeStoreItem](./Import-AzDataLakeStoreItem.md)

[Anslut-AzDataLakeStoreItem](./Join-AzDataLakeStoreItem.md)

[Move-AzDataLakeStoreItem](./Move-AzDataLakeStoreItem.md)

[New-AzDataLakeStoreItem](./New-AzDataLakeStoreItem.md)

[Remove-AzDataLakeStoreItem](./Remove-AzDataLakeStoreItem.md)

[Test-AzDataLakeStoreItem](./Test-AzDataLakeStoreItem.md)


