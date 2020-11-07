---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 889cffd16c836c5f895a9eb587c14cfbe66a45b3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927857"
---
# <span data-ttu-id="33e05-101">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="33e05-101">Get-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="33e05-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="33e05-102">SYNOPSIS</span></span>
<span data-ttu-id="33e05-103">Hämtar information om rörledningen.</span><span class="sxs-lookup"><span data-stu-id="33e05-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="33e05-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="33e05-104">SYNTAX</span></span>

### <span data-ttu-id="33e05-105">ByFactoryNameByRunId (standard)</span><span class="sxs-lookup"><span data-stu-id="33e05-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33e05-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="33e05-106">ByFactoryObjectByRunId</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33e05-107">ByFactoryObjectByPipeline</span><span class="sxs-lookup"><span data-stu-id="33e05-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="33e05-108">ByFactoryNameByPipeline</span><span class="sxs-lookup"><span data-stu-id="33e05-108">ByFactoryNameByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33e05-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="33e05-109">DESCRIPTION</span></span>
<span data-ttu-id="33e05-110">Kommandot **Get-AzDataFactoryV2PipelineRun** returnerar information om körs för den angivna pipeline.</span><span class="sxs-lookup"><span data-stu-id="33e05-110">The **Get-AzDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="33e05-111">Om PipelineRunId är angivet visas information om det ID som finns i den.</span><span class="sxs-lookup"><span data-stu-id="33e05-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="33e05-112">Om PipelineRunId inte anges visas information om alla körningar för de rörledningar som inträffade mellan värdena för LastUpdatedAfter och LastUpdatedBefore.</span><span class="sxs-lookup"><span data-stu-id="33e05-112">If the PipelineRunId is not specified, then it shows information about all runs for the pipelines that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="33e05-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="33e05-113">EXAMPLES</span></span>

### <span data-ttu-id="33e05-114">Exempel 1: Hämta information för en pipeline-körning</span><span class="sxs-lookup"><span data-stu-id="33e05-114">Example 1: Get information for a pipeline run</span></span>
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

<span data-ttu-id="33e05-115">Det här kommandot får information om pipeline-körningen med ID "61eb095a-FE23-4591-8a97-fade6c65ca72".</span><span class="sxs-lookup"><span data-stu-id="33e05-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="33e05-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="33e05-116">PARAMETERS</span></span>

### <span data-ttu-id="33e05-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="33e05-117">-DataFactory</span></span>
<span data-ttu-id="33e05-118">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="33e05-118">The data factory object.</span></span>

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

### <span data-ttu-id="33e05-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="33e05-119">-DataFactoryName</span></span>
<span data-ttu-id="33e05-120">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="33e05-120">The data factory name.</span></span>

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

### <span data-ttu-id="33e05-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33e05-121">-DefaultProfile</span></span>
<span data-ttu-id="33e05-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="33e05-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33e05-123">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="33e05-123">-LastUpdatedAfter</span></span>
<span data-ttu-id="33e05-124">Klock slaget för eller efter vilken pipeline-körningen uppdaterades i ISO8601-format.</span><span class="sxs-lookup"><span data-stu-id="33e05-124">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="33e05-125">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="33e05-125">-LastUpdatedBefore</span></span>
<span data-ttu-id="33e05-126">Tiden då pipelinen senast uppdaterades i ISO8601-format.</span><span class="sxs-lookup"><span data-stu-id="33e05-126">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="33e05-127">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="33e05-127">-PipelineName</span></span>
<span data-ttu-id="33e05-128">Förlopps namnet.</span><span class="sxs-lookup"><span data-stu-id="33e05-128">The pipeline name.</span></span>

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

### <span data-ttu-id="33e05-129">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="33e05-129">-PipelineRunId</span></span>
<span data-ttu-id="33e05-130">Kör-ID för pipeline.</span><span class="sxs-lookup"><span data-stu-id="33e05-130">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="33e05-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33e05-131">-ResourceGroupName</span></span>
<span data-ttu-id="33e05-132">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="33e05-132">The resource group name.</span></span>

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

### <span data-ttu-id="33e05-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33e05-133">CommonParameters</span></span>
<span data-ttu-id="33e05-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33e05-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33e05-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33e05-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33e05-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="33e05-136">INPUTS</span></span>

### <span data-ttu-id="33e05-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="33e05-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="33e05-138">System. String</span><span class="sxs-lookup"><span data-stu-id="33e05-138">System.String</span></span>

## <span data-ttu-id="33e05-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="33e05-139">OUTPUTS</span></span>

### <span data-ttu-id="33e05-140">Microsoft. Azure. commands. DataFactoryV2. Models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="33e05-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

## <span data-ttu-id="33e05-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="33e05-141">NOTES</span></span>

## <span data-ttu-id="33e05-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="33e05-142">RELATED LINKS</span></span>

[<span data-ttu-id="33e05-143">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="33e05-143">Invoke-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="33e05-144">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="33e05-144">Get-AzDataFactoryV2ActivityRun</span></span>]()

