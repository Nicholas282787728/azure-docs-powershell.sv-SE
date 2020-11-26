---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsepipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapsePipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapsePipelineRun.md
ms.openlocfilehash: f907afbc573d558a08d514c019cbcbe3fa999bf6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269830"
---
# <span data-ttu-id="1f8b9-101">Stop-AzSynapsePipelineRun</span><span class="sxs-lookup"><span data-stu-id="1f8b9-101">Stop-AzSynapsePipelineRun</span></span>

## <span data-ttu-id="1f8b9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1f8b9-102">SYNOPSIS</span></span>
<span data-ttu-id="1f8b9-103">Stoppar en pipeline-körning på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="1f8b9-103">Stops a pipeline run in a workspace.</span></span>

## <span data-ttu-id="1f8b9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1f8b9-104">SYNTAX</span></span>

### <span data-ttu-id="1f8b9-105">RemoveByName (standard)</span><span class="sxs-lookup"><span data-stu-id="1f8b9-105">RemoveByName (Default)</span></span>
```
Stop-AzSynapsePipelineRun -WorkspaceName <String> -PipelineRunId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f8b9-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="1f8b9-106">RemoveByObject</span></span>
```
Stop-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -PipelineRunId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f8b9-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="1f8b9-107">RemoveByInputObject</span></span>
```
Stop-AzSynapsePipelineRun -InputObject <PSPipelineRun> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f8b9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1f8b9-108">DESCRIPTION</span></span>
<span data-ttu-id="1f8b9-109">Cmdleten **Stop-AzSynapsePipelineRun** stoppar en pipeline-körning på en arbets yta som anges med det förvalda kör-ID.</span><span class="sxs-lookup"><span data-stu-id="1f8b9-109">The **Stop-AzSynapsePipelineRun** cmdlet stops a pipeline run in a workspace specified with the pipeline run ID.</span></span>

## <span data-ttu-id="1f8b9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1f8b9-110">EXAMPLES</span></span>

### <span data-ttu-id="1f8b9-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1f8b9-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
```

<span data-ttu-id="1f8b9-112">Det här kommandot stoppar pipeline-körningen med ID-b9730a13-AA12-4926-a8b3-8e3a974ab0bd i arbets ytans ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="1f8b9-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="1f8b9-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="1f8b9-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Stop-AzSynapsePipelineRun -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
```

<span data-ttu-id="1f8b9-114">Det här kommandot stoppar pipeline-körningen med ID-b9730a13-AA12-4926-a8b3-8e3a974ab0bd i arbets ytans ContosoWorkspace genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="1f8b9-114">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="1f8b9-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="1f8b9-115">Example 3</span></span>
```powershell
PS C:\> $pipelineRun = Get-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
PS C:\> $pipelineRun | Stop-AzSynapsePipelineRun
```

<span data-ttu-id="1f8b9-116">Det här kommandot stoppar pipeline-körningen med ID-b9730a13-AA12-4926-a8b3-8e3a974ab0bd i arbets ytans ContosoWorkspace genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="1f8b9-116">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="1f8b9-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1f8b9-117">PARAMETERS</span></span>

### <span data-ttu-id="1f8b9-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f8b9-118">-AsJob</span></span>
<span data-ttu-id="1f8b9-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="1f8b9-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1f8b9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f8b9-120">-DefaultProfile</span></span>
<span data-ttu-id="1f8b9-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1f8b9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f8b9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f8b9-122">-InputObject</span></span>
<span data-ttu-id="1f8b9-123">Information om pipeline-körningen.</span><span class="sxs-lookup"><span data-stu-id="1f8b9-123">The information about the pipeline run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f8b9-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f8b9-124">-PassThru</span></span>
<span data-ttu-id="1f8b9-125">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="1f8b9-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="1f8b9-126">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="1f8b9-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="1f8b9-127">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="1f8b9-127">-PipelineRunId</span></span>
<span data-ttu-id="1f8b9-128">ID för pipeline-körningen.</span><span class="sxs-lookup"><span data-stu-id="1f8b9-128">The pipeline run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f8b9-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1f8b9-129">-WorkspaceName</span></span>
<span data-ttu-id="1f8b9-130">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="1f8b9-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f8b9-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1f8b9-131">-WorkspaceObject</span></span>
<span data-ttu-id="1f8b9-132">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="1f8b9-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f8b9-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1f8b9-133">-Confirm</span></span>
<span data-ttu-id="1f8b9-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1f8b9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f8b9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f8b9-135">-WhatIf</span></span>
<span data-ttu-id="1f8b9-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1f8b9-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f8b9-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1f8b9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f8b9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f8b9-138">CommonParameters</span></span>
<span data-ttu-id="1f8b9-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f8b9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f8b9-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f8b9-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f8b9-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1f8b9-141">INPUTS</span></span>

### <span data-ttu-id="1f8b9-142">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1f8b9-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="1f8b9-143">Microsoft. Azure. commands. Synapse. Models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="1f8b9-143">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span></span>

## <span data-ttu-id="1f8b9-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1f8b9-144">OUTPUTS</span></span>

### <span data-ttu-id="1f8b9-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1f8b9-145">System.Boolean</span></span>

## <span data-ttu-id="1f8b9-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1f8b9-146">NOTES</span></span>

## <span data-ttu-id="1f8b9-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1f8b9-147">RELATED LINKS</span></span>