---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchtaskcounts
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTaskCounts.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTaskCounts.md
ms.openlocfilehash: d0b98081675cd11d8d3eb60a6495ac87a1111034
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574423"
---
# Get-AzureBatchTaskCounts

## Sammanfattning
Hämtar antalet aktiviteter för det angivna jobbet.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### Et
```
Get-AzureBatchTaskCounts [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>]
```

### ParentObject
```
Get-AzureBatchTaskCounts [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureBatchTaskCounts** hämtar antalet Azure Batch-uppgifter för ett batchjobb.
Ange ett jobb genom parametern *jobId* eller *jobb* parameter.
Med aktivitets antal får du ett antal aktiviteter som är aktiva, kör eller slutförda aktivitets tillstånd och antalet uppgifter som lyckades eller misslyckades. Uppgifter i tillståndet för att förbereda räknas som körs. Om validationStatus är avverifierat har batch-tjänsten inte kunnat kontrol lera status för de uppgifter som rapporter ATS i API för List aktiviteter. ValidationStatus kan vara avverifierad om jobbet innehåller fler än 200 000 uppgifter.

## BESKRIVS

### Exempel 1: Hämta antal aktiviteter efter ID
```
PS C:\> Get-AzureBatchTaskCounts -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

Det här kommandot får antalet aktiviteter för jobbet Job01.
Använd Get-AzureRmBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.

## MALLPARAMETRAR

### -BatchContext
Den BatchAccountContext-instans som ska användas vid interaktion med kommando tjänsten.
Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.
Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.
När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.
Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Jobb
Anger det jobb som innehåller uppgifter som denna cmdlet får.
För att hämta ett **PSCloudJob** -objekt, Använd cmdleten Get-AzureBatchJob.

```yaml
Type: PSCloudJob
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -JobId
ID för det jobb som du vill hämta aktiviteter för.

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## KOSTNADS

### System. String
Microsoft.Azure.Commands.BatCH. Modeller. PSCloudJob Microsoft.Azure.Commands.Batch.BatchAccountContext


## VÄRDEN

### Microsoft.Azure.Commands.BatCH. Modeller. PSTaskCounts


## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Get-AzureBatchJob](./Get-AzureBatchJob.md)

[Cmdlets för Azure Batch](./AzureRM.Batch.md)
