---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsjobpipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobPipeline.md
ms.openlocfilehash: c17a58cee2b5f13345997b97ce00792a8b9c9a0f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582716"
---
# Get-AzureRmDataLakeAnalyticsJobPipeline

## Sammanfattning
Hämtar en pipeline för data Lake Analytics-jobb eller-rörledningar.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### GetAllInAccount (standard)
```
Get-AzureRmDataLakeAnalyticsJobPipeline [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetBySpecificJobPipeline
```
Get-AzureRmDataLakeAnalyticsJobPipeline [-Account] <String> [-PipelineId] <Guid>
 [-SubmittedAfter <DateTimeOffset>] [-SubmittedBefore <DateTimeOffset>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
**Get-AzureRmDataLakeAnalyticsJobPipeline** får ett angivet Azure Data Lake Analytics-jobbs pipeline eller en lista över rörledningar.

## BESKRIVS

### Exempel 1: skaffa en angiven rörledning
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobPipeline -Account "contosoadla" -PipelineId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

Det här kommandot hämtar pipeline med ID ' 83cb7ad2-3523-4b82-b909-d478b0d8aea3 ' i kontot ' contosoadla '.

### Exempel 2: Hämta en lista över alla rörledningar i kontot
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobPipeline -AccountName "contosoadla"
```

Det här kommandot får en lista över alla rörledningar i kontot "contosoadla"

## MALLPARAMETRAR

### -Konto
Namnet på det data Lake Analytics-konto namn som du vill hämta jobb pipeline för.

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
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

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

### -PipelineId
ID för det specifika jobb försäljnings förlopp du vill returnera information om.

```yaml
Type: System.Guid
Parameter Sets: GetBySpecificJobPipeline
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -SubmittedAfter
Ett valfritt filter som returnerar jobb ledning (ar) som skickas efter den angivna tiden.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubmittedBefore
Ett valfritt filter som returnerar jobbets pipeline (ar) som skickas före angiven tid.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

### System. GUID

### System. Nullable ' 1 [[system. DateTimeOffset, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]

## VÄRDEN

### Microsoft. Azure. commands. DataLakeAnalytics. Models. PSJobPipelineInformation

## ANMÄRKNINGAR

## RELATERADE LÄNKAR
