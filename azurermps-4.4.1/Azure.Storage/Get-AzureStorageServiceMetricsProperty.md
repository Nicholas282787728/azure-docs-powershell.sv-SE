---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceMetricsProperty.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: f3930216e93f13004d7d2e8b149867cf511e3708
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573810"
---
# Get-AzureStorageServiceMetricsProperty

## Sammanfattning
Hämtar mått för Azure Storage-tjänsten.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Get-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureStorageServiceMetricsProperty** hämtar mått för Azure Storage-tjänsten.

## BESKRIVS

### Exempel 1: Hämta mått egenskaper för Blob-tjänsten
```
C:\PS>Get-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

Det här kommandot får Metric-egenskaper för blob-lagring för typen timme.

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

### -MetricsType
Anger en typ av mått.
Med den här cmdleten hämtas mått för Azure Storage-tjänsten för de mått typer som den här parametern anger.
De acceptabla värdena för den här parametern är: timme och minut.

```yaml
Type: ServiceMetricsType
Parameter Sets: (All)
Aliases: 
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceType
Anger typ av lagrings tjänst.
Denna cmdlet hämtar måtten för den typ som den här parametern anger.
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

### Microsoft. WindowsAzure. Storage. Shared. Protocol. MetricsProperties

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzureStorageContext](./New-AzureStorageContext.md)

[Set-AzureStorageServiceMetricsProperty](./Set-AzureStorageServiceMetricsProperty.md)


