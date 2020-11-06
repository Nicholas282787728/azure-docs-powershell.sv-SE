---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceLoggingProperty.md
ms.openlocfilehash: d0edbcc3b519f9600a2ad36832dee0305ce49be7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575744"
---
# Get-AzureStorageServiceLoggingProperty

## Sammanfattning
Hämtar loggnings egenskaper för Azure Storage-tjänsterna.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Get-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureStorageServiceLoggingProperty** hämtar loggnings egenskaper för Azure Storage-tjänsterna.

## BESKRIVS

### Exempel 1: Hämta loggnings egenskaper för Blob-tjänsten
```
C:\PS>Get-AzureStorageServiceLoggingProperty -ServiceType Blob
```

Det här kommandot får loggnings egenskaper för blob-lagring.

## MALLPARAMETRAR

### -Kontext
Anger en Azure Storage-kontext.
Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.

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

### -ServiceType
Anger typ av lagrings tjänst.
Med den här cmdleten får du loggnings egenskaper för den typ av tjänst som den här parametern anger.
De acceptabla värdena för den här parametern är:

- Object 
- Tabell
- Svarskö
- Fil

Värdet för File stöds inte för närvarande.

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### IStorageContext

Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline

## VÄRDEN

### Microsoft. WindowsAzure. Storage. Shared. Protocol. LoggingProperties

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzureStorageContext](./New-AzureStorageContext.md)

[Set-AzureStorageServiceLoggingProperty](./Set-AzureStorageServiceLoggingProperty.md)


