---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapsePipeline.md
ms.openlocfilehash: fc8f24cb124194bc2d2acd5ab5f19a4484571079
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416792"
---
# <span data-ttu-id="d475a-101">Invoke-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="d475a-101">Invoke-AzSynapsePipeline</span></span>

## <span data-ttu-id="d475a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d475a-102">SYNOPSIS</span></span>
<span data-ttu-id="d475a-103">Anropar en pipeline för att starta en körning.</span><span class="sxs-lookup"><span data-stu-id="d475a-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="d475a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d475a-104">SYNTAX</span></span>

### <span data-ttu-id="d475a-105">NewByName (standard)</span><span class="sxs-lookup"><span data-stu-id="d475a-105">NewByName (Default)</span></span>
```
Invoke-AzSynapsePipeline -WorkspaceName <String> -PipelineName <String> [-Parameter <Hashtable>]
 [-ParameterFile <String>] [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d475a-106">NewByInputObject</span><span class="sxs-lookup"><span data-stu-id="d475a-106">NewByInputObject</span></span>
```
Invoke-AzSynapsePipeline -InputObject <PSPipelineResource> [-Parameter <Hashtable>] [-ParameterFile <String>]
 [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d475a-107">NewByObject</span><span class="sxs-lookup"><span data-stu-id="d475a-107">NewByObject</span></span>
```
Invoke-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -PipelineName <String> [-Parameter <Hashtable>]
 [-ParameterFile <String>] [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d475a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d475a-108">DESCRIPTION</span></span>
<span data-ttu-id="d475a-109">Kommandot **Invoke-AzSynapsePipeline** startar en körning på den angivna pipeline och returnerar ett ID för den.</span><span class="sxs-lookup"><span data-stu-id="d475a-109">The **Invoke-AzSynapsePipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="d475a-110">Detta GUID kan överföras till **Get-AzSynapsePipelineRun** eller **Get-AzSynapseActivityRun** för att få mer information om den här körningen.</span><span class="sxs-lookup"><span data-stu-id="d475a-110">This GUID can be passed to **Get-AzSynapsePipelineRun** or **Get-AzSynapseActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="d475a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d475a-111">EXAMPLES</span></span>

### <span data-ttu-id="d475a-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d475a-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSynapsePipeline -WorkspaceName ContosoWorkspace -PipelineName ContosoPipeline
```

<span data-ttu-id="d475a-113">Det här kommandot startar en körning för pipeline som heter ContosoPipeline i arbets ytans ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="d475a-113">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="d475a-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d475a-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Invoke-AzSynapsePipeline -PipelineName ContosoPipeline
```

<span data-ttu-id="d475a-115">Det här kommandot startar en körning för pipeline som heter ContosoPipeline i arbets ytans ContosoWorkspace via pipeline.</span><span class="sxs-lookup"><span data-stu-id="d475a-115">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="d475a-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="d475a-116">Example 3</span></span>
```powershell
PS C:\> $pipeline = Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
PS C:\> $pipeline | Invoke-AzSynapsePipeline
```

<span data-ttu-id="d475a-117">Det här kommandot startar en körning för pipeline som heter ContosoPipeline i arbets ytans ContosoWorkspace via pipeline.</span><span class="sxs-lookup"><span data-stu-id="d475a-117">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="d475a-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d475a-118">PARAMETERS</span></span>

### <span data-ttu-id="d475a-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d475a-119">-AsJob</span></span>
<span data-ttu-id="d475a-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d475a-120">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d475a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d475a-121">-DefaultProfile</span></span>
<span data-ttu-id="d475a-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d475a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d475a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d475a-123">-InputObject</span></span>
<span data-ttu-id="d475a-124">Information om pipeline-körningen.</span><span class="sxs-lookup"><span data-stu-id="d475a-124">The information about the pipeline run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource
Parameter Sets: NewByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d475a-125">-IsRecovery</span><span class="sxs-lookup"><span data-stu-id="d475a-125">-IsRecovery</span></span>
<span data-ttu-id="d475a-126">Flagga för återställnings läge.</span><span class="sxs-lookup"><span data-stu-id="d475a-126">Recovery mode flag.</span></span>
<span data-ttu-id="d475a-127">Om återställnings läget är inställt på True körs den angivna åberopade pipelinen och den nya körningen grupperas under samma inställningar.</span><span class="sxs-lookup"><span data-stu-id="d475a-127">If recovery mode is set to true, the specified referenced pipeline run and the new run will be grouped under the same groupId.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d475a-128">-Parameter</span><span class="sxs-lookup"><span data-stu-id="d475a-128">-Parameter</span></span>
<span data-ttu-id="d475a-129">Parametrar för pipeline-körning.</span><span class="sxs-lookup"><span data-stu-id="d475a-129">Parameters for pipeline run.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d475a-130">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="d475a-130">-ParameterFile</span></span>
<span data-ttu-id="d475a-131">Namnet på filen med parametrar för pipeline-körning.</span><span class="sxs-lookup"><span data-stu-id="d475a-131">The name of the file with parameters for pipeline run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d475a-132">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="d475a-132">-PipelineName</span></span>
<span data-ttu-id="d475a-133">Förlopps namnet.</span><span class="sxs-lookup"><span data-stu-id="d475a-133">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByName, NewByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d475a-134">-ReferencePipelineRunId</span><span class="sxs-lookup"><span data-stu-id="d475a-134">-ReferencePipelineRunId</span></span>
<span data-ttu-id="d475a-135">Kör-ID för pipeline för kör igen.</span><span class="sxs-lookup"><span data-stu-id="d475a-135">The pipeline run ID for rerun.</span></span>
<span data-ttu-id="d475a-136">Om kör-ID anges används parametrarna för den angivna körningen för att skapa ett nytt kör.</span><span class="sxs-lookup"><span data-stu-id="d475a-136">If run ID is specified, the parameters of the specified run will be used to create a new run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d475a-137">-StartActivityName</span><span class="sxs-lookup"><span data-stu-id="d475a-137">-StartActivityName</span></span>
<span data-ttu-id="d475a-138">I återställnings läget startas kör igen med den här aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="d475a-138">In recovery mode, the rerun will start from this activity.</span></span>
<span data-ttu-id="d475a-139">Om det inte anges körs alla aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="d475a-139">If not specified, all activities will run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d475a-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d475a-140">-WorkspaceName</span></span>
<span data-ttu-id="d475a-141">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="d475a-141">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d475a-142">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d475a-142">-WorkspaceObject</span></span>
<span data-ttu-id="d475a-143">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="d475a-143">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: NewByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d475a-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d475a-144">-Confirm</span></span>
<span data-ttu-id="d475a-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d475a-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d475a-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d475a-146">-WhatIf</span></span>
<span data-ttu-id="d475a-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d475a-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d475a-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d475a-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d475a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d475a-149">CommonParameters</span></span>
<span data-ttu-id="d475a-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d475a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d475a-151">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d475a-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d475a-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d475a-152">INPUTS</span></span>

### <span data-ttu-id="d475a-153">Microsoft. Azure. commands. Synapse. Models. PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="d475a-153">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

### <span data-ttu-id="d475a-154">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d475a-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="d475a-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d475a-155">OUTPUTS</span></span>

### <span data-ttu-id="d475a-156">Microsoft. Azure. commands. Synapse. Models. PSCreateRunResponse</span><span class="sxs-lookup"><span data-stu-id="d475a-156">Microsoft.Azure.Commands.Synapse.Models.PSCreateRunResponse</span></span>

## <span data-ttu-id="d475a-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d475a-157">NOTES</span></span>

## <span data-ttu-id="d475a-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d475a-158">RELATED LINKS</span></span>
