---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapsePipeline.md
ms.openlocfilehash: fc8f24cb124194bc2d2acd5ab5f19a4484571079
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424304"
---
# <span data-ttu-id="981af-101">Invoke-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="981af-101">Invoke-AzSynapsePipeline</span></span>

## <span data-ttu-id="981af-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="981af-102">SYNOPSIS</span></span>
<span data-ttu-id="981af-103">Anropar en pipeline för att starta en körning.</span><span class="sxs-lookup"><span data-stu-id="981af-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="981af-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="981af-104">SYNTAX</span></span>

### <span data-ttu-id="981af-105">NewByName (standard)</span><span class="sxs-lookup"><span data-stu-id="981af-105">NewByName (Default)</span></span>
```
Invoke-AzSynapsePipeline -WorkspaceName <String> -PipelineName <String> [-Parameter <Hashtable>]
 [-ParameterFile <String>] [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="981af-106">NewByInputObject</span><span class="sxs-lookup"><span data-stu-id="981af-106">NewByInputObject</span></span>
```
Invoke-AzSynapsePipeline -InputObject <PSPipelineResource> [-Parameter <Hashtable>] [-ParameterFile <String>]
 [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="981af-107">NewByObject</span><span class="sxs-lookup"><span data-stu-id="981af-107">NewByObject</span></span>
```
Invoke-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -PipelineName <String> [-Parameter <Hashtable>]
 [-ParameterFile <String>] [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="981af-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="981af-108">DESCRIPTION</span></span>
<span data-ttu-id="981af-109">Kommandot **Invoke-AzSynapsePipeline** startar en körning på den angivna pipeline och returnerar ett ID för den.</span><span class="sxs-lookup"><span data-stu-id="981af-109">The **Invoke-AzSynapsePipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="981af-110">Detta GUID kan överföras till **Get-AzSynapsePipelineRun** eller **Get-AzSynapseActivityRun** för att få mer information om den här körningen.</span><span class="sxs-lookup"><span data-stu-id="981af-110">This GUID can be passed to **Get-AzSynapsePipelineRun** or **Get-AzSynapseActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="981af-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="981af-111">EXAMPLES</span></span>

### <span data-ttu-id="981af-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="981af-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSynapsePipeline -WorkspaceName ContosoWorkspace -PipelineName ContosoPipeline
```

<span data-ttu-id="981af-113">Det här kommandot startar en körning för pipeline som heter ContosoPipeline i arbets ytans ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="981af-113">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="981af-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="981af-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Invoke-AzSynapsePipeline -PipelineName ContosoPipeline
```

<span data-ttu-id="981af-115">Det här kommandot startar en körning för pipeline som heter ContosoPipeline i arbets ytans ContosoWorkspace via pipeline.</span><span class="sxs-lookup"><span data-stu-id="981af-115">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="981af-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="981af-116">Example 3</span></span>
```powershell
PS C:\> $pipeline = Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
PS C:\> $pipeline | Invoke-AzSynapsePipeline
```

<span data-ttu-id="981af-117">Det här kommandot startar en körning för pipeline som heter ContosoPipeline i arbets ytans ContosoWorkspace via pipeline.</span><span class="sxs-lookup"><span data-stu-id="981af-117">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="981af-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="981af-118">PARAMETERS</span></span>

### <span data-ttu-id="981af-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="981af-119">-AsJob</span></span>
<span data-ttu-id="981af-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="981af-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="981af-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="981af-121">-DefaultProfile</span></span>
<span data-ttu-id="981af-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="981af-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="981af-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="981af-123">-InputObject</span></span>
<span data-ttu-id="981af-124">Information om pipeline-körningen.</span><span class="sxs-lookup"><span data-stu-id="981af-124">The information about the pipeline run.</span></span>

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

### <span data-ttu-id="981af-125">-IsRecovery</span><span class="sxs-lookup"><span data-stu-id="981af-125">-IsRecovery</span></span>
<span data-ttu-id="981af-126">Flagga för återställnings läge.</span><span class="sxs-lookup"><span data-stu-id="981af-126">Recovery mode flag.</span></span>
<span data-ttu-id="981af-127">Om återställnings läget är inställt på True körs den angivna åberopade pipelinen och den nya körningen grupperas under samma inställningar.</span><span class="sxs-lookup"><span data-stu-id="981af-127">If recovery mode is set to true, the specified referenced pipeline run and the new run will be grouped under the same groupId.</span></span>

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

### <span data-ttu-id="981af-128">-Parameter</span><span class="sxs-lookup"><span data-stu-id="981af-128">-Parameter</span></span>
<span data-ttu-id="981af-129">Parametrar för pipeline-körning.</span><span class="sxs-lookup"><span data-stu-id="981af-129">Parameters for pipeline run.</span></span>

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

### <span data-ttu-id="981af-130">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="981af-130">-ParameterFile</span></span>
<span data-ttu-id="981af-131">Namnet på filen med parametrar för pipeline-körning.</span><span class="sxs-lookup"><span data-stu-id="981af-131">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="981af-132">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="981af-132">-PipelineName</span></span>
<span data-ttu-id="981af-133">Förlopps namnet.</span><span class="sxs-lookup"><span data-stu-id="981af-133">The pipeline name.</span></span>

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

### <span data-ttu-id="981af-134">-ReferencePipelineRunId</span><span class="sxs-lookup"><span data-stu-id="981af-134">-ReferencePipelineRunId</span></span>
<span data-ttu-id="981af-135">Kör-ID för pipeline för kör igen.</span><span class="sxs-lookup"><span data-stu-id="981af-135">The pipeline run ID for rerun.</span></span>
<span data-ttu-id="981af-136">Om kör-ID anges används parametrarna för den angivna körningen för att skapa ett nytt kör.</span><span class="sxs-lookup"><span data-stu-id="981af-136">If run ID is specified, the parameters of the specified run will be used to create a new run.</span></span>

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

### <span data-ttu-id="981af-137">-StartActivityName</span><span class="sxs-lookup"><span data-stu-id="981af-137">-StartActivityName</span></span>
<span data-ttu-id="981af-138">I återställnings läget startas kör igen med den här aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="981af-138">In recovery mode, the rerun will start from this activity.</span></span>
<span data-ttu-id="981af-139">Om det inte anges körs alla aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="981af-139">If not specified, all activities will run.</span></span>

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

### <span data-ttu-id="981af-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="981af-140">-WorkspaceName</span></span>
<span data-ttu-id="981af-141">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="981af-141">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="981af-142">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="981af-142">-WorkspaceObject</span></span>
<span data-ttu-id="981af-143">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="981af-143">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="981af-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="981af-144">-Confirm</span></span>
<span data-ttu-id="981af-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="981af-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="981af-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="981af-146">-WhatIf</span></span>
<span data-ttu-id="981af-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="981af-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="981af-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="981af-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="981af-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="981af-149">CommonParameters</span></span>
<span data-ttu-id="981af-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="981af-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="981af-151">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="981af-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="981af-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="981af-152">INPUTS</span></span>

### <span data-ttu-id="981af-153">Microsoft. Azure. commands. Synapse. Models. PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="981af-153">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

### <span data-ttu-id="981af-154">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="981af-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="981af-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="981af-155">OUTPUTS</span></span>

### <span data-ttu-id="981af-156">Microsoft. Azure. commands. Synapse. Models. PSCreateRunResponse</span><span class="sxs-lookup"><span data-stu-id="981af-156">Microsoft.Azure.Commands.Synapse.Models.PSCreateRunResponse</span></span>

## <span data-ttu-id="981af-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="981af-157">NOTES</span></span>

## <span data-ttu-id="981af-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="981af-158">RELATED LINKS</span></span>
