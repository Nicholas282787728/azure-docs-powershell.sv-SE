---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2PipelineRun.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: 6042b62bb7c641cef335834645f29d73b3d4c53a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585672"
---
# <span data-ttu-id="e23d9-101">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="e23d9-101">Get-AzureRmDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="e23d9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e23d9-102">SYNOPSIS</span></span>
<span data-ttu-id="e23d9-103">Hämtar information om rörledningen.</span><span class="sxs-lookup"><span data-stu-id="e23d9-103">Gets information about pipeline runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e23d9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e23d9-104">SYNTAX</span></span>

### <span data-ttu-id="e23d9-105">ByFactoryNameByRunId (standard)</span><span class="sxs-lookup"><span data-stu-id="e23d9-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String>
```

### <span data-ttu-id="e23d9-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="e23d9-106">ByFactoryObjectByRunId</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
```

### <span data-ttu-id="e23d9-107">ByFactoryObjectByPipeline</span><span class="sxs-lookup"><span data-stu-id="e23d9-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
```

### <span data-ttu-id="e23d9-108">ByFactoryNameByPipeline</span><span class="sxs-lookup"><span data-stu-id="e23d9-108">ByFactoryNameByPipeline</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
```

## <span data-ttu-id="e23d9-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e23d9-109">DESCRIPTION</span></span>
<span data-ttu-id="e23d9-110">Kommandot **Get-AzureRmDataFactoryV2PipelineRun** returnerar information om körs för den angivna pipeline.</span><span class="sxs-lookup"><span data-stu-id="e23d9-110">The **Get-AzureRmDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="e23d9-111">Om PipelineRunId är angivet visas information om det ID som finns i den.</span><span class="sxs-lookup"><span data-stu-id="e23d9-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="e23d9-112">Om PipelineRunId inte anges visas information om alla körningar för den angivna pipeline som inträffade mellan värdena för LastUpdatedAfter och LastUpdatedBefore.</span><span class="sxs-lookup"><span data-stu-id="e23d9-112">If the PipelineRunId is not specified, then it shows information about all runs for the specified pipeline that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="e23d9-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e23d9-113">EXAMPLES</span></span>

### <span data-ttu-id="e23d9-114">Exempel 1: Hämta information för en pipline-körning</span><span class="sxs-lookup"><span data-stu-id="e23d9-114">Example 1: Get information for a pipline run</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"

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

<span data-ttu-id="e23d9-115">Det här kommandot får information om pipeline-körningen med ID "61eb095a-FE23-4591-8a97-fade6c65ca72".</span><span class="sxs-lookup"><span data-stu-id="e23d9-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>


## <span data-ttu-id="e23d9-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e23d9-116">PARAMETERS</span></span>

### <span data-ttu-id="e23d9-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="e23d9-117">-DataFactory</span></span>
<span data-ttu-id="e23d9-118">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="e23d9-118">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObjectByRunId, ByFactoryObjectByPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e23d9-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e23d9-119">-DataFactoryName</span></span>
<span data-ttu-id="e23d9-120">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="e23d9-120">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByRunId, ByFactoryNameByPipeline
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e23d9-121">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="e23d9-121">-LastUpdatedAfter</span></span>
<span data-ttu-id="e23d9-122">Klock slaget för eller efter vilken pipeline-körningen uppdaterades i ISO8601-format.</span><span class="sxs-lookup"><span data-stu-id="e23d9-122">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e23d9-123">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="e23d9-123">-LastUpdatedBefore</span></span>
<span data-ttu-id="e23d9-124">Tiden då pipelinen senast uppdaterades i ISO8601-format.</span><span class="sxs-lookup"><span data-stu-id="e23d9-124">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e23d9-125">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="e23d9-125">-PipelineName</span></span>
<span data-ttu-id="e23d9-126">Förlopps namnet.</span><span class="sxs-lookup"><span data-stu-id="e23d9-126">The pipeline name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e23d9-127">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="e23d9-127">-PipelineRunId</span></span>
<span data-ttu-id="e23d9-128">Kör-ID för pipeline.</span><span class="sxs-lookup"><span data-stu-id="e23d9-128">The Run ID of the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryObjectByRunId, ByFactoryNameByRunId
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e23d9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e23d9-129">-ResourceGroupName</span></span>
<span data-ttu-id="e23d9-130">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="e23d9-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByRunId, ByFactoryNameByPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="e23d9-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e23d9-131">INPUTS</span></span>

### <span data-ttu-id="e23d9-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e23d9-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="e23d9-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e23d9-133">System.String</span></span>


## <span data-ttu-id="e23d9-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e23d9-134">OUTPUTS</span></span>

### <span data-ttu-id="e23d9-135">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. DataFactoryV2. Models. PSPipelineRun, Microsoft. Azure. commands. DataFactoryV2, version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e23d9-135">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="e23d9-136">Microsoft. Azure. commands. DataFactoryV2. Models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="e23d9-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>


## <span data-ttu-id="e23d9-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e23d9-137">NOTES</span></span>

## <span data-ttu-id="e23d9-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e23d9-138">RELATED LINKS</span></span>
[<span data-ttu-id="e23d9-139">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="e23d9-139">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="e23d9-140">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="e23d9-140">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

