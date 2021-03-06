---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchjobpreparationandreleasetaskstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobPreparationAndReleaseTaskStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobPreparationAndReleaseTaskStatus.md
ms.openlocfilehash: 5f24e55042a8be7f36b1a9946c4bd5b87209a0f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583199"
---
# Get-AzureBatchJobPreparationAndReleaseTaskStatus

## Sammanfattning
Hämtar och släpper aktivitets status.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### ID (standard)
```
Get-AzureBatchJobPreparationAndReleaseTaskStatus [-Id] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Get-AzureBatchJobPreparationAndReleaseTaskStatus [-InputObject] <PSCloudJob> [-Filter <String>]
 [-MaxCount <Int32>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureBatchJobPreparationAndReleaseTaskStatus** får Azure Batch-jobbet förberedelse och utgivnings aktivitets status för ett batchjobb.
Du måste ange *ID-* parametern eller en **PSCloudJob** -instans till denna cmdlet.

## BESKRIVS

### Exempel 1: få jobb förberedelsen och utgivnings status för ett jobb
```
PS C:\> Get-AzureBatchJobPreparationAndReleaseTaskStatus -BatchContext $Context -Id Test

ComputeNodeId                          : tvm-2316545714_1-20170613t201733z
ComputeNodeUrl                         : https://account.westus.batch.azure.com/pools/test/nodes/tvm-2316545714_1-20170613t201733z
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 : test
```

Det här kommandot får jobbet förberedelser och aktivitets status för jobbet "test".
Använd Get-AzureRmBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.

### Exempel 2: få jobbet Preparation och utgivnings status för ett jobb med filter och välj angiven
```
PS C:\> Get-AzureBatchJobPreparationAndReleaseTaskStatus -BatchContext $context -Id Test -Filter "nodeId eq 'tvm-2316545714_1-20170613t201733z'" -Select "jobPreparationTaskExecutionInfo"

ComputeNodeId                          :
ComputeNodeUrl                         :
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 :
```

Det här kommandot får jobb förberedelsen och aktivitets status för jobbet "test" på noden "TVM-2316545714_1-20170613t201733z" och använder SELECT-satsen för att ange att endast JobPreparationTaskExecutionInformation-informationen ska returneras

## MALLPARAMETRAR

### -BatchContext
Den BatchAccountContext-instans som ska användas vid interaktion med kommando tjänsten.
Använd Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.

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

### -Expandera
Anger en Open data Protocol (OData) Expand-sats.
Ange ett värde för den här parametern för att hämta associerade enheter för huvud enheten som du får.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Filter
Anger en OData filter-sats.
Om du inte anger något filter returnerar denna cmdlet all jobb förberedelse och utgivnings status för jobbet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Anger ID för det jobb vars förberedelse-och utgivnings aktiviteter ska hämtas.
Du kan inte ange jokertecken.

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Anger ett **PSCloudJob** -objekt som representerar jobbet för att få statusen förberedelse-och utgivnings aktivitet från.
För att hämta ett **PSCloudJob** -objekt, Använd cmdleten Get-AzureBatchJob.

```yaml
Type: PSCloudJob
Parameter Sets: InputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MaxCount
Anger det högsta antalet förberedelser och status för aktivitets statusen för att återgå.
Om du anger ett värde som är noll (0) eller mindre används ingen övre gräns av cmdleten.
Standardvärdet är 1000.

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

### -Välj
Anger en OData SELECT-sats.
Ange ett värde för den här parametern för att få specifika egenskaper i stället för alla objekt egenskaper.

```yaml
Type: String
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

### System. String
Microsoft.Azure.Commands.BatCH. Modeller. PSCloudJob Microsoft.Azure.Commands.Batch.BatchAccountContext

## VÄRDEN

### Microsoft.Azure.Commands.BatCH. Modeller. PSJobPreparationAndReleaseTaskExecutionInformation

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureBatchJob](./Get-AzureBatchJob.md)

[Cmdlets för Azure Batch](./AzureRM.Batch.md)
