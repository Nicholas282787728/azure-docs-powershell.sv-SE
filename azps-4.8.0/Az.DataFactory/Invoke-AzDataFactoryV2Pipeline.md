---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: e4204068b12a21732cca1802dcc20a770d74d5e0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262765"
---
# <span data-ttu-id="1cb8c-101">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="1cb8c-101">Invoke-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="1cb8c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1cb8c-102">SYNOPSIS</span></span>
  <span data-ttu-id="1cb8c-103">Anropar en pipeline för att starta en körning.</span><span class="sxs-lookup"><span data-stu-id="1cb8c-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="1cb8c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1cb8c-104">SYNTAX</span></span>

### <span data-ttu-id="1cb8c-105">ByFactoryNameByParameterFile (standard)</span><span class="sxs-lookup"><span data-stu-id="1cb8c-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [[-ReferencePipelineRunId] <String>] [-IsRecovery]
 [[-StartActivityName] <String>] [-StartFromFailure] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cb8c-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="1cb8c-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>]
 [[-ReferencePipelineRunId] <String>] [-IsRecovery] [[-StartActivityName] <String>] [-StartFromFailure]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cb8c-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="1cb8c-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>]
 [[-ReferencePipelineRunId] <String>] [-IsRecovery] [[-StartActivityName] <String>] [-StartFromFailure]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cb8c-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="1cb8c-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [[-ReferencePipelineRunId] <String>] [-IsRecovery]
 [[-StartActivityName] <String>] [-StartFromFailure] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cb8c-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1cb8c-109">DESCRIPTION</span></span>
<span data-ttu-id="1cb8c-110">Kommandot **Invoke-AzDataFactoryV2Pipeline** startar en körning på den angivna pipeline och returnerar ett ID för den.</span><span class="sxs-lookup"><span data-stu-id="1cb8c-110">The **Invoke-AzDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="1cb8c-111">Detta GUID kan överföras till **Get-AzDataFactoryV2PipelineRun** eller **Get-AzDataFactoryV2ActivityRun** för att få mer information om den här körningen.</span><span class="sxs-lookup"><span data-stu-id="1cb8c-111">This GUID can be passed to **Get-AzDataFactoryV2PipelineRun** or **Get-AzDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="1cb8c-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1cb8c-112">EXAMPLES</span></span>

### <span data-ttu-id="1cb8c-113">Exempel 1: starta en pipeline för att starta en körning</span><span class="sxs-lookup"><span data-stu-id="1cb8c-113">Example 1: Invoke a pipeline to start a run</span></span>
```powershell
PS C:\> Invoke-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="1cb8c-114">Det här kommandot startar en körning för "DPWikisample"-pipeline i fabriken "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="1cb8c-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

### <span data-ttu-id="1cb8c-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="1cb8c-115">Example 2</span></span>

<span data-ttu-id="1cb8c-116">Anropar en pipeline för att starta en körning.</span><span class="sxs-lookup"><span data-stu-id="1cb8c-116">Invokes a pipeline to start a run for it.</span></span> <span data-ttu-id="1cb8c-117">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="1cb8c-117">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Invoke-AzDataFactoryV2Pipeline -DataFactoryName 'WikiADF' -Parameter <Hashtable> -PipelineName 'DPWikisample' -ResourceGroupName 'ADF'
```

## <span data-ttu-id="1cb8c-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1cb8c-118">PARAMETERS</span></span>

### <span data-ttu-id="1cb8c-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1cb8c-119">-DataFactoryName</span></span>
<span data-ttu-id="1cb8c-120">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="1cb8c-120">The data factory name.</span></span>

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

### <span data-ttu-id="1cb8c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cb8c-121">-DefaultProfile</span></span>
<span data-ttu-id="1cb8c-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1cb8c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1cb8c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1cb8c-123">-InputObject</span></span>
<span data-ttu-id="1cb8c-124">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="1cb8c-124">The data factory object.</span></span>

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

### <span data-ttu-id="1cb8c-125">-IsRecovery</span><span class="sxs-lookup"><span data-stu-id="1cb8c-125">-IsRecovery</span></span>
<span data-ttu-id="1cb8c-126">Flagga för återställnings läge.</span><span class="sxs-lookup"><span data-stu-id="1cb8c-126">Recovery mode flag.</span></span> <span data-ttu-id="1cb8c-127">Om återställnings läget är inställt på True körs den angivna åberopade pipelinen och den nya körningen grupperas under samma inställningar.</span><span class="sxs-lookup"><span data-stu-id="1cb8c-127">If recovery mode is set to true, the specified referenced pipeline run and the new run will be grouped under the same groupId.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cb8c-128">-Parameter</span><span class="sxs-lookup"><span data-stu-id="1cb8c-128">-Parameter</span></span>
<span data-ttu-id="1cb8c-129">Parametrar för pipeline-körning.</span><span class="sxs-lookup"><span data-stu-id="1cb8c-129">Parameters for pipeline run.</span></span>

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

### <span data-ttu-id="1cb8c-130">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="1cb8c-130">-ParameterFile</span></span>
<span data-ttu-id="1cb8c-131">Namnet på filen med parametrar för pipeline-körning.</span><span class="sxs-lookup"><span data-stu-id="1cb8c-131">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="1cb8c-132">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="1cb8c-132">-PipelineName</span></span>
<span data-ttu-id="1cb8c-133">Förlopps namnet.</span><span class="sxs-lookup"><span data-stu-id="1cb8c-133">The pipeline name.</span></span>

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

### <span data-ttu-id="1cb8c-134">-ReferencePipelineRunId</span><span class="sxs-lookup"><span data-stu-id="1cb8c-134">-ReferencePipelineRunId</span></span>
<span data-ttu-id="1cb8c-135">Kör-ID för pipeline för kör igen.</span><span class="sxs-lookup"><span data-stu-id="1cb8c-135">The pipeline run ID for rerun.</span></span> <span data-ttu-id="1cb8c-136">Om kör-ID anges används parametrarna för den angivna körningen för att skapa ett nytt kör.</span><span class="sxs-lookup"><span data-stu-id="1cb8c-136">If run ID is specified, the parameters of the specified run will be used to create a new run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cb8c-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cb8c-137">-ResourceGroupName</span></span>
<span data-ttu-id="1cb8c-138">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="1cb8c-138">The resource group name.</span></span>

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

### <span data-ttu-id="1cb8c-139">-StartActivityName</span><span class="sxs-lookup"><span data-stu-id="1cb8c-139">-StartActivityName</span></span>
<span data-ttu-id="1cb8c-140">I återställnings läget startas kör igen med den här aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="1cb8c-140">In recovery mode, the rerun will start from this activity.</span></span> <span data-ttu-id="1cb8c-141">Om det inte anges körs alla aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="1cb8c-141">If not specified, all activities will run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cb8c-142">-StartFromFailure</span><span class="sxs-lookup"><span data-stu-id="1cb8c-142">-StartFromFailure</span></span>
<span data-ttu-id="1cb8c-143">Starta om från flaggan misslyckade aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="1cb8c-143">Start rerun from failed activities flag.</span></span> <span data-ttu-id="1cb8c-144">I återställnings läge kommer kör igen att starta från misslyckade aktiviteter om du anger det.</span><span class="sxs-lookup"><span data-stu-id="1cb8c-144">In recovery mode, if specified, the rerun will start from failed activities.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cb8c-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1cb8c-145">-Confirm</span></span>
<span data-ttu-id="1cb8c-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1cb8c-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cb8c-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cb8c-147">-WhatIf</span></span>
<span data-ttu-id="1cb8c-148">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1cb8c-148">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="1cb8c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cb8c-149">CommonParameters</span></span>
<span data-ttu-id="1cb8c-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cb8c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cb8c-151">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1cb8c-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cb8c-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1cb8c-152">INPUTS</span></span>

### <span data-ttu-id="1cb8c-153">Microsoft. Azure. commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="1cb8c-153">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="1cb8c-154">System. String</span><span class="sxs-lookup"><span data-stu-id="1cb8c-154">System.String</span></span>

### <span data-ttu-id="1cb8c-155">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="1cb8c-155">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1cb8c-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1cb8c-156">OUTPUTS</span></span>

### <span data-ttu-id="1cb8c-157">Microsoft. Azure. commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="1cb8c-157">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="1cb8c-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1cb8c-158">NOTES</span></span>

## <span data-ttu-id="1cb8c-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1cb8c-159">RELATED LINKS</span></span>

[<span data-ttu-id="1cb8c-160">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="1cb8c-160">Get-AzDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="1cb8c-161">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="1cb8c-161">Get-AzDataFactoryV2ActivityRun</span></span>]()

