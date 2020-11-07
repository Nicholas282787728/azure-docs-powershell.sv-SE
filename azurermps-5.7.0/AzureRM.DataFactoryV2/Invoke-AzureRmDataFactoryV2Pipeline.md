---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/invoke-azurermdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: 1503d7307c38c72eece2eb7cb3d6e9f1543be8bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757693"
---
# <span data-ttu-id="78f6b-101">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="78f6b-101">Invoke-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="78f6b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="78f6b-102">SYNOPSIS</span></span>
  <span data-ttu-id="78f6b-103">Anropar en pipeline för att starta en körning.</span><span class="sxs-lookup"><span data-stu-id="78f6b-103">Invokes a pipeline to start a run for it.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78f6b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="78f6b-104">SYNTAX</span></span>

### <span data-ttu-id="78f6b-105">ByFactoryNameByParameterFile (standard)</span><span class="sxs-lookup"><span data-stu-id="78f6b-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78f6b-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="78f6b-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78f6b-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="78f6b-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78f6b-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="78f6b-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78f6b-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="78f6b-109">DESCRIPTION</span></span>
<span data-ttu-id="78f6b-110">Kommandot **Invoke-AzureRmDataFactoryV2Pipeline** startar en körning på den angivna pipeline och returnerar ett ID för den.</span><span class="sxs-lookup"><span data-stu-id="78f6b-110">The **Invoke-AzureRmDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="78f6b-111">Detta GUID kan överföras till **Get-AzureRmDataFactoryV2PipelineRun** eller **Get-AzureRmDataFactoryV2ActivityRun** för att få mer information om den här körningen.</span><span class="sxs-lookup"><span data-stu-id="78f6b-111">This GUID can be passed to **Get-AzureRmDataFactoryV2PipelineRun** or **Get-AzureRmDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="78f6b-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="78f6b-112">EXAMPLES</span></span>

### <span data-ttu-id="78f6b-113">Exempel 1: starta en pipeline för att starta en körning</span><span class="sxs-lookup"><span data-stu-id="78f6b-113">Example 1: Invoke a pipeline to start a run</span></span>
```
PS C:\> Invoke-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="78f6b-114">Det här kommandot startar en körning för "DPWikisample"-pipeline i fabriken "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="78f6b-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

## <span data-ttu-id="78f6b-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="78f6b-115">PARAMETERS</span></span>

### <span data-ttu-id="78f6b-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="78f6b-116">-DataFactoryName</span></span>
<span data-ttu-id="78f6b-117">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="78f6b-117">The data factory name.</span></span>

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

### <span data-ttu-id="78f6b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78f6b-118">-DefaultProfile</span></span>
<span data-ttu-id="78f6b-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="78f6b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78f6b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78f6b-120">-InputObject</span></span>
<span data-ttu-id="78f6b-121">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="78f6b-121">The data factory object.</span></span>

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

### <span data-ttu-id="78f6b-122">-Parameter</span><span class="sxs-lookup"><span data-stu-id="78f6b-122">-Parameter</span></span>
<span data-ttu-id="78f6b-123">Parametrar för pipeline-körning.</span><span class="sxs-lookup"><span data-stu-id="78f6b-123">Parameters for pipeline run.</span></span>

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

### <span data-ttu-id="78f6b-124">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="78f6b-124">-ParameterFile</span></span>
<span data-ttu-id="78f6b-125">Namnet på filen med parametrar för pipeline-körning.</span><span class="sxs-lookup"><span data-stu-id="78f6b-125">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="78f6b-126">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="78f6b-126">-PipelineName</span></span>
<span data-ttu-id="78f6b-127">Förlopps namnet.</span><span class="sxs-lookup"><span data-stu-id="78f6b-127">The pipeline name.</span></span>

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

### <span data-ttu-id="78f6b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78f6b-128">-ResourceGroupName</span></span>
<span data-ttu-id="78f6b-129">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="78f6b-129">The resource group name.</span></span>

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

### <span data-ttu-id="78f6b-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="78f6b-130">-Confirm</span></span>
<span data-ttu-id="78f6b-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="78f6b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78f6b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78f6b-132">-WhatIf</span></span>
<span data-ttu-id="78f6b-133">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="78f6b-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="78f6b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78f6b-134">CommonParameters</span></span>
<span data-ttu-id="78f6b-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78f6b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78f6b-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78f6b-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78f6b-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="78f6b-137">INPUTS</span></span>

### <span data-ttu-id="78f6b-138">Microsoft. Azure. commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="78f6b-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="78f6b-139">System. String system. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="78f6b-139">System.String System.Collections.Hashtable</span></span>

## <span data-ttu-id="78f6b-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="78f6b-140">OUTPUTS</span></span>

### <span data-ttu-id="78f6b-141">Microsoft. Azure. commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="78f6b-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="78f6b-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="78f6b-142">NOTES</span></span>

## <span data-ttu-id="78f6b-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="78f6b-143">RELATED LINKS</span></span>

[<span data-ttu-id="78f6b-144">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="78f6b-144">Get-AzureRmDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="78f6b-145">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="78f6b-145">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

