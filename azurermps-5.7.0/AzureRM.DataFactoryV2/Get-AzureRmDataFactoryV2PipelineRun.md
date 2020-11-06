---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2PipelineRun.md
ms.openlocfilehash: 05adb3533604188aa5331d0d4b3f41a2aeba292d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584380"
---
# <span data-ttu-id="1583f-101">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="1583f-101">Get-AzureRmDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="1583f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1583f-102">SYNOPSIS</span></span>
<span data-ttu-id="1583f-103">Hämtar information om rörledningen.</span><span class="sxs-lookup"><span data-stu-id="1583f-103">Gets information about pipeline runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1583f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1583f-104">SYNTAX</span></span>

### <span data-ttu-id="1583f-105">ByFactoryNameByRunId (standard)</span><span class="sxs-lookup"><span data-stu-id="1583f-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1583f-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="1583f-106">ByFactoryObjectByRunId</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1583f-107">ByFactoryObjectByPipeline</span><span class="sxs-lookup"><span data-stu-id="1583f-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1583f-108">ByFactoryNameByPipeline</span><span class="sxs-lookup"><span data-stu-id="1583f-108">ByFactoryNameByPipeline</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1583f-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1583f-109">DESCRIPTION</span></span>
<span data-ttu-id="1583f-110">Kommandot **Get-AzureRmDataFactoryV2PipelineRun** returnerar information om körs för den angivna pipeline.</span><span class="sxs-lookup"><span data-stu-id="1583f-110">The **Get-AzureRmDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="1583f-111">Om PipelineRunId är angivet visas information om det ID som finns i den.</span><span class="sxs-lookup"><span data-stu-id="1583f-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="1583f-112">Om PipelineRunId inte anges visas information om alla körningar för den angivna pipeline som inträffade mellan värdena för LastUpdatedAfter och LastUpdatedBefore.</span><span class="sxs-lookup"><span data-stu-id="1583f-112">If the PipelineRunId is not specified, then it shows information about all runs for the specified pipeline that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="1583f-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1583f-113">EXAMPLES</span></span>

### <span data-ttu-id="1583f-114">Exempel 1: Hämta information för en pipline-körning</span><span class="sxs-lookup"><span data-stu-id="1583f-114">Example 1: Get information for a pipline run</span></span>
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

<span data-ttu-id="1583f-115">Det här kommandot får information om pipeline-körningen med ID "61eb095a-FE23-4591-8a97-fade6c65ca72".</span><span class="sxs-lookup"><span data-stu-id="1583f-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="1583f-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1583f-116">PARAMETERS</span></span>

### <span data-ttu-id="1583f-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="1583f-117">-DataFactory</span></span>
<span data-ttu-id="1583f-118">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="1583f-118">The data factory object.</span></span>

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

### <span data-ttu-id="1583f-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1583f-119">-DataFactoryName</span></span>
<span data-ttu-id="1583f-120">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="1583f-120">The data factory name.</span></span>

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

### <span data-ttu-id="1583f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1583f-121">-DefaultProfile</span></span>
<span data-ttu-id="1583f-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1583f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1583f-123">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="1583f-123">-LastUpdatedAfter</span></span>
<span data-ttu-id="1583f-124">Klock slaget för eller efter vilken pipeline-körningen uppdaterades i ISO8601-format.</span><span class="sxs-lookup"><span data-stu-id="1583f-124">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="1583f-125">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="1583f-125">-LastUpdatedBefore</span></span>
<span data-ttu-id="1583f-126">Tiden då pipelinen senast uppdaterades i ISO8601-format.</span><span class="sxs-lookup"><span data-stu-id="1583f-126">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="1583f-127">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="1583f-127">-PipelineName</span></span>
<span data-ttu-id="1583f-128">Förlopps namnet.</span><span class="sxs-lookup"><span data-stu-id="1583f-128">The pipeline name.</span></span>

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

### <span data-ttu-id="1583f-129">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="1583f-129">-PipelineRunId</span></span>
<span data-ttu-id="1583f-130">Kör-ID för pipeline.</span><span class="sxs-lookup"><span data-stu-id="1583f-130">The Run ID of the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByRunId, ByFactoryObjectByRunId
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1583f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1583f-131">-ResourceGroupName</span></span>
<span data-ttu-id="1583f-132">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="1583f-132">The resource group name.</span></span>

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

### <span data-ttu-id="1583f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1583f-133">CommonParameters</span></span>
<span data-ttu-id="1583f-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1583f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1583f-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1583f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1583f-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1583f-136">INPUTS</span></span>

### <span data-ttu-id="1583f-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1583f-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="1583f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1583f-138">System.String</span></span>

## <span data-ttu-id="1583f-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1583f-139">OUTPUTS</span></span>

### <span data-ttu-id="1583f-140">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. DataFactoryV2. Models. PSPipelineRun, Microsoft. Azure. commands. DataFactoryV2, version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1583f-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="1583f-141">Microsoft. Azure. commands. DataFactoryV2. Models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="1583f-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

## <span data-ttu-id="1583f-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1583f-142">NOTES</span></span>

## <span data-ttu-id="1583f-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1583f-143">RELATED LINKS</span></span>

[<span data-ttu-id="1583f-144">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="1583f-144">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="1583f-145">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="1583f-145">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

