---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 889cffd16c836c5f895a9eb587c14cfbe66a45b3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524195"
---
# Get-AzDataFactoryV2PipelineRun

## Sammanfattning
Hämtar information om rörledningen.

## FRÅGESYNTAXEN

### ByFactoryNameByRunId (standard)
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObjectByRunId
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObjectByPipeline
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByFactoryNameByPipeline
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Kommandot **Get-AzDataFactoryV2PipelineRun** returnerar information om körs för den angivna pipeline. Om PipelineRunId är angivet visas information om det ID som finns i den. Om PipelineRunId inte anges visas information om alla körningar för de rörledningar som inträffade mellan värdena för LastUpdatedAfter och LastUpdatedBefore.

## BESKRIVS

### Exempel 1: Hämta information för en pipeline-körning
```
PS C:\> Get-AzDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"

    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    RunId             : 61eb095a-fe23-4591-8a97-fade6c65ca72
    PipelineName      : DPWikisample
    LastUpdated       : 9/14/2017 12:21:02 AM
    Parameters        : {[url, http://adfsamplewebapi.azurewebsites.net/api/execute/sample]}
    RunStart          : 9/14/2017 12:20:54 AM
    RunEnd            : 9/14/2017 12:21:02 AM
    DurationInMs      : 8246
    Status            : Succeeded
    Message           :
```

Det här kommandot får information om pipeline-körningen med ID "61eb095a-FE23-4591-8a97-fade6c65ca72".

## MALLPARAMETRAR

### -DataFactory
Data fabriks objekt.

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObjectByRunId, ByFactoryObjectByPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DataFactoryName
Namnet på data fabriken.

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByRunId, ByFactoryNameByPipeline
Aliases:

Required: True
Position: 1
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

### -LastUpdatedAfter
Klock slaget för eller efter vilken pipeline-körningen uppdaterades i ISO8601-format.

```yaml
Type: System.DateTime
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LastUpdatedBefore
Tiden då pipelinen senast uppdaterades i ISO8601-format.

```yaml
Type: System.DateTime
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PipelineName
Förlopps namnet.

```yaml
Type: System.String
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PipelineRunId
Kör-ID för pipeline.

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByRunId, ByFactoryObjectByRunId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Resurs gruppens namn.

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByRunId, ByFactoryNameByPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory

### System. String

## VÄRDEN

### Microsoft. Azure. commands. DataFactoryV2. Models. PSPipelineRun

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Invoke-AzDataFactoryV2Pipeline]()

[Get-AzDataFactoryV2ActivityRun]()

