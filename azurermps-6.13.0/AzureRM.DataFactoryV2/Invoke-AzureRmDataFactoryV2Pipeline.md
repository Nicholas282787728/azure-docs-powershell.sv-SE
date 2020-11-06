---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/invoke-azurermdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: e7bfd0b72f5dffe4e5ff4d7e52394846d5f17afa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575246"
---
# <span data-ttu-id="2ea45-101">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="2ea45-101">Invoke-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="2ea45-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2ea45-102">SYNOPSIS</span></span>
  <span data-ttu-id="2ea45-103">Anropar en pipeline för att starta en körning.</span><span class="sxs-lookup"><span data-stu-id="2ea45-103">Invokes a pipeline to start a run for it.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ea45-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2ea45-104">SYNTAX</span></span>

### <span data-ttu-id="2ea45-105">ByFactoryNameByParameterFile (standard)</span><span class="sxs-lookup"><span data-stu-id="2ea45-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ea45-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="2ea45-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ea45-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="2ea45-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ea45-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="2ea45-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ea45-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2ea45-109">DESCRIPTION</span></span>
<span data-ttu-id="2ea45-110">Kommandot **Invoke-AzureRmDataFactoryV2Pipeline** startar en körning på den angivna pipeline och returnerar ett ID för den.</span><span class="sxs-lookup"><span data-stu-id="2ea45-110">The **Invoke-AzureRmDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="2ea45-111">Detta GUID kan överföras till **Get-AzureRmDataFactoryV2PipelineRun** eller **Get-AzureRmDataFactoryV2ActivityRun** för att få mer information om den här körningen.</span><span class="sxs-lookup"><span data-stu-id="2ea45-111">This GUID can be passed to **Get-AzureRmDataFactoryV2PipelineRun** or **Get-AzureRmDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="2ea45-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2ea45-112">EXAMPLES</span></span>

### <span data-ttu-id="2ea45-113">Exempel 1: starta en pipeline för att starta en körning</span><span class="sxs-lookup"><span data-stu-id="2ea45-113">Example 1: Invoke a pipeline to start a run</span></span>
```
PS C:\> Invoke-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="2ea45-114">Det här kommandot startar en körning för "DPWikisample"-pipeline i fabriken "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="2ea45-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

## <span data-ttu-id="2ea45-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2ea45-115">PARAMETERS</span></span>

### <span data-ttu-id="2ea45-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2ea45-116">-DataFactoryName</span></span>
<span data-ttu-id="2ea45-117">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="2ea45-117">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ea45-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ea45-118">-DefaultProfile</span></span>
<span data-ttu-id="2ea45-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2ea45-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ea45-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ea45-120">-InputObject</span></span>
<span data-ttu-id="2ea45-121">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="2ea45-121">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline
Parameter Sets: ByPipelineObjectByParameterFile, ByPipelineObjectByParameterObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ea45-122">-Parameter</span><span class="sxs-lookup"><span data-stu-id="2ea45-122">-Parameter</span></span>
<span data-ttu-id="2ea45-123">Parametrar för pipeline-körning.</span><span class="sxs-lookup"><span data-stu-id="2ea45-123">Parameters for pipeline run.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByPipelineObjectByParameterObject, ByFactoryNameByParameterObject
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ea45-124">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="2ea45-124">-ParameterFile</span></span>
<span data-ttu-id="2ea45-125">Namnet på filen med parametrar för pipeline-körning.</span><span class="sxs-lookup"><span data-stu-id="2ea45-125">The name of the file with parameters for pipeline run.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByPipelineObjectByParameterFile
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ea45-126">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="2ea45-126">-PipelineName</span></span>
<span data-ttu-id="2ea45-127">Förlopps namnet.</span><span class="sxs-lookup"><span data-stu-id="2ea45-127">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ea45-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ea45-128">-ResourceGroupName</span></span>
<span data-ttu-id="2ea45-129">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="2ea45-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ea45-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2ea45-130">-Confirm</span></span>
<span data-ttu-id="2ea45-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2ea45-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ea45-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ea45-132">-WhatIf</span></span>
<span data-ttu-id="2ea45-133">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2ea45-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ea45-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ea45-134">CommonParameters</span></span>
<span data-ttu-id="2ea45-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ea45-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ea45-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ea45-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ea45-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2ea45-137">INPUTS</span></span>

### <span data-ttu-id="2ea45-138">Microsoft. Azure. commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="2ea45-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="2ea45-139">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2ea45-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="2ea45-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2ea45-140">System.String</span></span>

### <span data-ttu-id="2ea45-141">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="2ea45-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2ea45-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2ea45-142">OUTPUTS</span></span>

### <span data-ttu-id="2ea45-143">Microsoft. Azure. commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="2ea45-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="2ea45-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2ea45-144">NOTES</span></span>

## <span data-ttu-id="2ea45-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2ea45-145">RELATED LINKS</span></span>

[<span data-ttu-id="2ea45-146">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="2ea45-146">Get-AzureRmDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="2ea45-147">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="2ea45-147">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

