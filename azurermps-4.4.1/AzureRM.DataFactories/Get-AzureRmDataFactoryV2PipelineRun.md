---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2PipelineRun.md
ms.openlocfilehash: 0ecc2025a5c1b1a3ad1c27a8c2a926c6ef0402b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574722"
---
# <span data-ttu-id="90078-101">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="90078-101">Get-AzureRmDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="90078-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="90078-102">SYNOPSIS</span></span>
<span data-ttu-id="90078-103">Hämtar information om rörledningen.</span><span class="sxs-lookup"><span data-stu-id="90078-103">Gets information about pipeline runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90078-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="90078-104">SYNTAX</span></span>

### <span data-ttu-id="90078-105">ByFactoryNameByRunId (standard)</span><span class="sxs-lookup"><span data-stu-id="90078-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90078-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="90078-106">ByFactoryObjectByRunId</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90078-107">ByFactoryObjectByPipeline</span><span class="sxs-lookup"><span data-stu-id="90078-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="90078-108">ByFactoryNameByPipeline</span><span class="sxs-lookup"><span data-stu-id="90078-108">ByFactoryNameByPipeline</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90078-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="90078-109">DESCRIPTION</span></span>
<span data-ttu-id="90078-110">Kommandot **Get-AzureRmDataFactoryV2PipelineRun** returnerar information om körs för den angivna pipeline.</span><span class="sxs-lookup"><span data-stu-id="90078-110">The **Get-AzureRmDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="90078-111">Om PipelineRunId är angivet visas information om det ID som finns i den.</span><span class="sxs-lookup"><span data-stu-id="90078-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="90078-112">Om PipelineRunId inte anges visas information om alla körningar för den angivna pipeline som inträffade mellan värdena för LastUpdatedAfter och LastUpdatedBefore.</span><span class="sxs-lookup"><span data-stu-id="90078-112">If the PipelineRunId is not specified, then it shows information about all runs for the specified pipeline that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="90078-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="90078-113">EXAMPLES</span></span>

### <span data-ttu-id="90078-114">Exempel 1: Hämta information för en pipline-körning</span><span class="sxs-lookup"><span data-stu-id="90078-114">Example 1: Get information for a pipline run</span></span>
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

<span data-ttu-id="90078-115">Det här kommandot får information om pipeline-körningen med ID "61eb095a-FE23-4591-8a97-fade6c65ca72".</span><span class="sxs-lookup"><span data-stu-id="90078-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="90078-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="90078-116">PARAMETERS</span></span>

### <span data-ttu-id="90078-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="90078-117">-DataFactory</span></span>
<span data-ttu-id="90078-118">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="90078-118">The data factory object.</span></span>

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

### <span data-ttu-id="90078-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="90078-119">-DataFactoryName</span></span>
<span data-ttu-id="90078-120">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="90078-120">The data factory name.</span></span>

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

### <span data-ttu-id="90078-121">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="90078-121">-LastUpdatedAfter</span></span>
<span data-ttu-id="90078-122">Klock slaget för eller efter vilken pipeline-körningen uppdaterades i ISO8601-format.</span><span class="sxs-lookup"><span data-stu-id="90078-122">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="90078-123">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="90078-123">-LastUpdatedBefore</span></span>
<span data-ttu-id="90078-124">Tiden då pipelinen senast uppdaterades i ISO8601-format.</span><span class="sxs-lookup"><span data-stu-id="90078-124">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="90078-125">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="90078-125">-PipelineName</span></span>
<span data-ttu-id="90078-126">Förlopps namnet.</span><span class="sxs-lookup"><span data-stu-id="90078-126">The pipeline name.</span></span>

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

### <span data-ttu-id="90078-127">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="90078-127">-PipelineRunId</span></span>
<span data-ttu-id="90078-128">Kör-ID för pipeline.</span><span class="sxs-lookup"><span data-stu-id="90078-128">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="90078-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90078-129">-ResourceGroupName</span></span>
<span data-ttu-id="90078-130">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="90078-130">The resource group name.</span></span>

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

### <span data-ttu-id="90078-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90078-131">-DefaultProfile</span></span>
<span data-ttu-id="90078-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="90078-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90078-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90078-133">CommonParameters</span></span>
<span data-ttu-id="90078-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90078-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90078-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90078-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90078-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="90078-136">INPUTS</span></span>

### <span data-ttu-id="90078-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="90078-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="90078-138">System. String</span><span class="sxs-lookup"><span data-stu-id="90078-138">System.String</span></span>

## <span data-ttu-id="90078-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="90078-139">OUTPUTS</span></span>

### <span data-ttu-id="90078-140">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. DataFactoryV2. Models. PSPipelineRun, Microsoft. Azure. commands. DataFactoryV2, version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="90078-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="90078-141">Microsoft. Azure. commands. DataFactoryV2. Models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="90078-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

## <span data-ttu-id="90078-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="90078-142">NOTES</span></span>

## <span data-ttu-id="90078-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="90078-143">RELATED LINKS</span></span>

[<span data-ttu-id="90078-144">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="90078-144">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="90078-145">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="90078-145">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

