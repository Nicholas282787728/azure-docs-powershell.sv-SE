---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceMetricsProperty.md
ms.openlocfilehash: 3cbe0a4e0276f2b62a0e0aed5b6168a5b81f8d7f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758244"
---
# Set-AzureStorageServiceMetricsProperty

## Sammanfattning
Ändrar mått för Azure Storage-tjänsten.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Set-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzureStorageServiceMetricsProperty** ändrar måtten för Azure Storage-tjänsten.

## BESKRIVS

### Exempel 1: ändra mått egenskaper för Blob-tjänsten
```
C:\PS>Set-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

Det här kommandot ändrar version 1,0-värden för blob-lagring till en tjänst nivå.
Mått för Azure Storage-tjänsten bevarar poster i 10 dagar.
Eftersom det här kommandot anger parametern *Passthru* visas egenskaperna för de ändrade måtten.

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

### -MetricsLevel
Anger den mått nivå som Azure-lagring använder för tjänsten.
De acceptabla värdena för den här parametern är:

- Ingen
- Serv
- ServiceAndApi

```yaml
Type: MetricsLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Service, ServiceAndApi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MetricsType
Anger en typ av mått.
Den här cmldet ställer in värdet för Azure Storage Service-värden på det värde som den här parametern anger.
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

### -PassThru
Anger att den här cmdleten returnerar de uppdaterade måtten.
Om du inte anger den här parametern returnerar denna cmdlet inte ett värde.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RetentionDays
Anger antalet dagar som Azure Storage-tjänsten behåller statistik information.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceType
Anger typ av lagrings tjänst.
Denna cmdlet ändrar egenskaperna för de tjänst typer som den här parametern anger.
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

### -Version
Anger versionen för Azure lagrings mått.
Standardvärdet är 1,0.

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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

[Get-AzureStorageServiceMetricsProperty](./Get-AzureStorageServiceMetricsProperty.md)

[New-AzureStorageContext](./New-AzureStorageContext.md)


