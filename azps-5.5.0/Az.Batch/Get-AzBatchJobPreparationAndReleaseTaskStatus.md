---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobpreparationandreleasetaskstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
ms.openlocfilehash: ffc89f298715f9e878bb3283c99e794f92662e84
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100251640"
---
# Get-AzBatchJobPreparationAndReleaseTaskStatus

## SYNOPSIS
Hämtar förberedelse av batchjobb och släpper aktivitetsstatus.

## SYNTAX

### ID (standard)
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-Id] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-InputObject] <PSCloudJob> [-Filter <String>]
 [-MaxCount <Int32>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Get-AzBatch EntligPreparationAndReleaseTaskStatus** får Azure Batch-jobbet förberedelse och släpper aktivitetsstatus för ett batchjobb.
Du måste ange *Id-parametern* eller en **PSCloudCloud-instans** till den här cmdleten.

## EXEMPEL

### Exempel 1: Hämta jobbförberedelser och status för ett jobb
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $Context -Id Test

ComputeNodeId                          : tvm-2316545714_1-20170613t201733z
ComputeNodeUrl                         : https://account.westus.batch.azure.com/pools/test/nodes/tvm-2316545714_1-20170613t201733z
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 : test
```

Det här kommandot hämtar jobbet som förberedelse och släpper aktivitetsstatus för jobbet "Test".
Använd cmdlet Get-AzBatchAccountKey-cmdleten för att tilldela en kontext till $Context variabeln.

### Exempel 2: Hämta jobbets förberedelse och släppstatus för ett jobb med Filter och Välj angivet
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $context -Id Test -Filter "nodeId eq 'tvm-2316545714_1-20170613t201733z'" -Select "jobPreparationTaskExecutionInfo"

ComputeNodeId                          :
ComputeNodeUrl                         :
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 :
```

Det här kommandot hämtar jobbförberedelsen och släpper aktivitetsstatusen för jobbet "Test" på noden "tvm-2316545714_1-20170613t201733z" och använder Select-satsen för att ange att endast returnera jobpreparationTaskExecutionInformation-information

## PARAMETERS

### -BatchContext
BatchAccountContext-instansen som ska användas när du interagerar med batchtjänsten.
Använd cmdleten Get-AzBatchAccountKey ett BatchAccountContext-objekt med dess snabbtangenter ifyllda.

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifterna, kontot, klientorganisationen och prenumerationen som används för kommunikation med Azure.

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

### -Expand
Anger en utöka-sats med öppet dataprotokoll (OData).
Ange ett värde för den här parametern för att få associerade enheter i huvudenheten som du får.

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

### -Filter
Anger en OData-filtersats.
Om du inte anger ett filter returnerar den här cmdleten alla jobbförberedelser och aktivitetsstatus för jobbet.

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

### -Id
Anger ID för jobbet vars förberedelse- och utgivningsaktiviteter ska hämtas.
Du kan inte ange jokertecken.

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Anger ett **PSCloudCloud-objekt** som representerar jobbet som förberedelsen och aktivitetsstatusen ska frigöras från.
Om du vill hämta **ett PSCloudCloudCloud-objekt** använder du Get-AzBatchJob-cmdleten.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MaxCount
Anger det maximala antalet förberedelsejobb och aktivitetsstatus som ska returneras.
Om du anger värdet noll (0) eller mindre används ingen övre gräns för cmdleten.
Standardvärdet är 1 000.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Select
Anger en OData Select-sats.
Ange ett värde för den här parametern för att få specifika egenskaper i stället för alla objektegenskaper.

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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### Microsoft.Azure.Commands.Batkap. Models.PSCloudCloud

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## UTDATA

### Microsoft.Azure.Commands.Batkap. Models.PS EngströmPreparationAndReleaseTaskExecutionInformation

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzBatch Ent](./Get-AzBatchJob.md)

[Azure-batch-cmdlets](/powershell/module/Az.Batch/)
