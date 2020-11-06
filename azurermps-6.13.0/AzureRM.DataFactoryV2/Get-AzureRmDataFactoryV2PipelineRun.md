---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2PipelineRun.md
ms.openlocfilehash: ac5735d66a7b44c7183a9af3a32c01445f2b3486
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580200"
---
# <span data-ttu-id="3119d-101">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="3119d-101">Get-AzureRmDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="3119d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3119d-102">SYNOPSIS</span></span>
<span data-ttu-id="3119d-103">Hämtar information om rörledningen.</span><span class="sxs-lookup"><span data-stu-id="3119d-103">Gets information about pipeline runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3119d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3119d-104">SYNTAX</span></span>

### <span data-ttu-id="3119d-105">ByFactoryNameByRunId (standard)</span><span class="sxs-lookup"><span data-stu-id="3119d-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3119d-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="3119d-106">ByFactoryObjectByRunId</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3119d-107">ByFactoryObjectByPipeline</span><span class="sxs-lookup"><span data-stu-id="3119d-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3119d-108">ByFactoryNameByPipeline</span><span class="sxs-lookup"><span data-stu-id="3119d-108">ByFactoryNameByPipeline</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3119d-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3119d-109">DESCRIPTION</span></span>
<span data-ttu-id="3119d-110">Kommandot **Get-AzureRmDataFactoryV2PipelineRun** returnerar information om körs för den angivna pipeline.</span><span class="sxs-lookup"><span data-stu-id="3119d-110">The **Get-AzureRmDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="3119d-111">Om PipelineRunId är angivet visas information om det ID som finns i den.</span><span class="sxs-lookup"><span data-stu-id="3119d-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="3119d-112">Om PipelineRunId inte anges visas information om alla körningar för den angivna pipeline som inträffade mellan värdena för LastUpdatedAfter och LastUpdatedBefore.</span><span class="sxs-lookup"><span data-stu-id="3119d-112">If the PipelineRunId is not specified, then it shows information about all runs for the specified pipeline that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="3119d-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3119d-113">EXAMPLES</span></span>

### <span data-ttu-id="3119d-114">Exempel 1: Hämta information för en pipline-körning</span><span class="sxs-lookup"><span data-stu-id="3119d-114">Example 1: Get information for a pipline run</span></span>
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

<span data-ttu-id="3119d-115">Det här kommandot får information om pipeline-körningen med ID "61eb095a-FE23-4591-8a97-fade6c65ca72".</span><span class="sxs-lookup"><span data-stu-id="3119d-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="3119d-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3119d-116">PARAMETERS</span></span>

### <span data-ttu-id="3119d-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="3119d-117">-DataFactory</span></span>
<span data-ttu-id="3119d-118">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="3119d-118">The data factory object.</span></span>

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

### <span data-ttu-id="3119d-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3119d-119">-DataFactoryName</span></span>
<span data-ttu-id="3119d-120">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="3119d-120">The data factory name.</span></span>

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

### <span data-ttu-id="3119d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3119d-121">-DefaultProfile</span></span>
<span data-ttu-id="3119d-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3119d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3119d-123">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="3119d-123">-LastUpdatedAfter</span></span>
<span data-ttu-id="3119d-124">Klock slaget för eller efter vilken pipeline-körningen uppdaterades i ISO8601-format.</span><span class="sxs-lookup"><span data-stu-id="3119d-124">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="3119d-125">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="3119d-125">-LastUpdatedBefore</span></span>
<span data-ttu-id="3119d-126">Tiden då pipelinen senast uppdaterades i ISO8601-format.</span><span class="sxs-lookup"><span data-stu-id="3119d-126">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="3119d-127">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="3119d-127">-PipelineName</span></span>
<span data-ttu-id="3119d-128">Förlopps namnet.</span><span class="sxs-lookup"><span data-stu-id="3119d-128">The pipeline name.</span></span>

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

### <span data-ttu-id="3119d-129">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="3119d-129">-PipelineRunId</span></span>
<span data-ttu-id="3119d-130">Kör-ID för pipeline.</span><span class="sxs-lookup"><span data-stu-id="3119d-130">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="3119d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3119d-131">-ResourceGroupName</span></span>
<span data-ttu-id="3119d-132">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="3119d-132">The resource group name.</span></span>

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

### <span data-ttu-id="3119d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3119d-133">CommonParameters</span></span>
<span data-ttu-id="3119d-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3119d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3119d-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3119d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3119d-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3119d-136">INPUTS</span></span>

### <span data-ttu-id="3119d-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="3119d-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="3119d-138">Parametrar: DataFactory (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3119d-138">Parameters: DataFactory (ByValue)</span></span>

### <span data-ttu-id="3119d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3119d-139">System.String</span></span>

## <span data-ttu-id="3119d-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3119d-140">OUTPUTS</span></span>

### <span data-ttu-id="3119d-141">Microsoft. Azure. commands. DataFactoryV2. Models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="3119d-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

## <span data-ttu-id="3119d-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3119d-142">NOTES</span></span>

## <span data-ttu-id="3119d-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3119d-143">RELATED LINKS</span></span>

[<span data-ttu-id="3119d-144">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="3119d-144">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="3119d-145">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="3119d-145">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

