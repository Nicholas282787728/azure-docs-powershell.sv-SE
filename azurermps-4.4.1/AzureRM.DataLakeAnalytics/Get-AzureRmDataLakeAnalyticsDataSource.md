---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0377C4E9-C1DC-49BA-BBC4-5598C83234F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: b7f2c6f2077d0b7e9c7510f6984ada15a65d6ef2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758096"
---
# Get-AzureRmDataLakeAnalyticsDataSource

## Sammanfattning
Hämtar data källan data Lake Analytics.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### Lista alla data källor (standard)
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Skaffa ett data Lake Store-konto
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Skaffa ett Blob Storage-konto
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmDataLakeAnalyticsDataSource** får en Azure Data Lake Analytics-datakälla.

## BESKRIVS

### Exempel 1: Hämta en data Källa från ett konto
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataLakeStore "ContosoAdls"
```

Det här kommandot hämtar data källan för data Lake Store som heter ContosoAdls från ett data Lake Analytics-konto.

### Exempel 2: hämta listan över data Lake Store-konton i ett data Lake Analytics-konto
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataSource "DataLakeStore"
```

Det här kommandot får alla data Lake Store-konton från ett data Lake Analytics-konto.

## MALLPARAMETRAR

### -Konto
Anger det data Lake Analytics-konto som denna cmdlet hämtar data källor.

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

### -BLOB
Anger namnet på din källa för Azure Blob Storage.

```yaml
Type: System.String
Parameter Sets: Get a Blob storage account
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataLakeStore
Anger namnet på data Lake Store-kontot.

```yaml
Type: System.String
Parameter Sets: Get a Data Lake Store account
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på resurs gruppen som innehåller data källan.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### PSStorageAccountInfo
De angivna Azure Storage-konto uppgifterna.

### PSDataLakeStoreAccountInfo
De angivna konto uppgifterna för data Lake Store

### Förteckning<AdlDataSource>
Listan över både Azure Storage-konton och data Lake Store-konton i det angivna data Lake Analytics-kontot.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzureRmDataLakeAnalyticsDataSource](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[Remove-AzureRmDataLakeAnalyticsDataSource](./Remove-AzureRmDataLakeAnalyticsDataSource.md)

[Set-AzureRmDataLakeAnalyticsDataSource](./Set-AzureRmDataLakeAnalyticsDataSource.md)


