---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 45095fefa0d4866a40b59c61ca02a98c118cf37a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757304"
---
# <span data-ttu-id="a69ab-101">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="a69ab-101">Invoke-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="a69ab-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a69ab-102">SYNOPSIS</span></span>
  <span data-ttu-id="a69ab-103">Anropar en pipeline för att starta en körning.</span><span class="sxs-lookup"><span data-stu-id="a69ab-103">Invokes a pipeline to start a run for it.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a69ab-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a69ab-104">SYNTAX</span></span>

### <span data-ttu-id="a69ab-105">ByFactoryNameByParameterFile (standard)</span><span class="sxs-lookup"><span data-stu-id="a69ab-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a69ab-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="a69ab-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a69ab-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="a69ab-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a69ab-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="a69ab-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="a69ab-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a69ab-109">DESCRIPTION</span></span>
<span data-ttu-id="a69ab-110">Kommandot **Invoke-AzureRmDataFactoryV2Pipeline** startar en körning på den angivna pipeline och returnerar ett ID för den.</span><span class="sxs-lookup"><span data-stu-id="a69ab-110">The **Invoke-AzureRmDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="a69ab-111">Detta GUID kan överföras till **Get-AzureRmDataFactoryV2PipelineRun** eller **Get-AzureRmDataFactoryV2ActivityRun** för att få mer information om den här körningen.</span><span class="sxs-lookup"><span data-stu-id="a69ab-111">This GUID can be passed to **Get-AzureRmDataFactoryV2PipelineRun** or **Get-AzureRmDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="a69ab-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a69ab-112">EXAMPLES</span></span>

### <span data-ttu-id="a69ab-113">Exempel 1: starta en pipeline för att starta en körning</span><span class="sxs-lookup"><span data-stu-id="a69ab-113">Example 1: Invoke a pipeline to start a run</span></span>
```
PS C:\> Invoke-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="a69ab-114">Det här kommandot startar en körning för "DPWikisample"-pipeline i fabriken "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="a69ab-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

## <span data-ttu-id="a69ab-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a69ab-115">PARAMETERS</span></span>

### <span data-ttu-id="a69ab-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a69ab-116">-Confirm</span></span>
<span data-ttu-id="a69ab-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a69ab-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a69ab-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a69ab-118">-DataFactoryName</span></span>
<span data-ttu-id="a69ab-119">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="a69ab-119">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a69ab-120">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="a69ab-120">-ParameterFile</span></span>
<span data-ttu-id="a69ab-121">Namnet på filen med parametrar för pipeline-körning.</span><span class="sxs-lookup"><span data-stu-id="a69ab-121">The name of the file with parameters for pipeline run.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByPipelineObjectByParameterFile
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a69ab-122">-Parameter</span><span class="sxs-lookup"><span data-stu-id="a69ab-122">-Parameter</span></span>
<span data-ttu-id="a69ab-123">Parametrar för pipeline-körning.</span><span class="sxs-lookup"><span data-stu-id="a69ab-123">Parameters for pipeline run.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByPipelineObjectByParameterObject, ByFactoryNameByParameterObject
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a69ab-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a69ab-124">-InputObject</span></span>
<span data-ttu-id="a69ab-125">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="a69ab-125">The data factory object.</span></span>

```yaml
Type: PSPipeline
Parameter Sets: ByPipelineObjectByParameterFile, ByPipelineObjectByParameterObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a69ab-126">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="a69ab-126">-PipelineName</span></span>
<span data-ttu-id="a69ab-127">Förlopps namnet.</span><span class="sxs-lookup"><span data-stu-id="a69ab-127">The pipeline name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a69ab-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a69ab-128">-ResourceGroupName</span></span>
<span data-ttu-id="a69ab-129">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="a69ab-129">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a69ab-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a69ab-130">-WhatIf</span></span>
<span data-ttu-id="a69ab-131">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a69ab-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="a69ab-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a69ab-132">INPUTS</span></span>

### <span data-ttu-id="a69ab-133">Microsoft. Azure. commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="a69ab-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="a69ab-134">System. String system. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="a69ab-134">System.String System.Collections.Hashtable</span></span>


## <span data-ttu-id="a69ab-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a69ab-135">OUTPUTS</span></span>

### <span data-ttu-id="a69ab-136">Microsoft. Azure. commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="a69ab-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>


## <span data-ttu-id="a69ab-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a69ab-137">NOTES</span></span>

## <span data-ttu-id="a69ab-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a69ab-138">RELATED LINKS</span></span>
[<span data-ttu-id="a69ab-139">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="a69ab-139">Get-AzureRmDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="a69ab-140">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="a69ab-140">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

