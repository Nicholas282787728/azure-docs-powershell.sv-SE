---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapsePipeline.md
ms.openlocfilehash: 2bce821f55b5f8ff39f56fa8a6960cb1f99b47d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271135"
---
# <span data-ttu-id="e595c-101">Set-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="e595c-101">Set-AzSynapsePipeline</span></span>

## <span data-ttu-id="e595c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e595c-102">SYNOPSIS</span></span>
<span data-ttu-id="e595c-103">Skapar en pipeline på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="e595c-103">Creates a pipeline in workspace.</span></span>

## <span data-ttu-id="e595c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e595c-104">SYNTAX</span></span>

### <span data-ttu-id="e595c-105">SetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="e595c-105">SetByName (Default)</span></span>
```
Set-AzSynapsePipeline -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e595c-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="e595c-106">SetByObject</span></span>
```
Set-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e595c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e595c-107">DESCRIPTION</span></span>
<span data-ttu-id="e595c-108">Cmdleten **set-AzSynapsePipeline** skapar en pipeline i arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="e595c-108">The **Set-AzSynapsePipeline** cmdlet creates a pipeline in workspace.</span></span>

## <span data-ttu-id="e595c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e595c-109">EXAMPLES</span></span>

### <span data-ttu-id="e595c-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e595c-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline -DefinitionFile "C:\pipeline.json"
```

<span data-ttu-id="e595c-111">Det här kommandot skapar en pipeline med namnet ContosoPipeline i arbets ytan med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="e595c-111">This command creates a pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="e595c-112">Kommandot baserar sig på informationen i pipeline.jsi filen.</span><span class="sxs-lookup"><span data-stu-id="e595c-112">The command bases the pipeline on information in the pipeline.json file.</span></span>
<span data-ttu-id="e595c-113">Filen innehåller information om aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="e595c-113">This file includes information about activities.</span></span>

### <span data-ttu-id="e595c-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="e595c-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapsePipeline -Name ContosoPipeline -DefinitionFile "C:\pipeline.json"
```

<span data-ttu-id="e595c-115">Det här kommandot skapar en pipeline med namnet ContosoPipeline i arbets ytan med namnet ContosoWorkspace till pipeline.</span><span class="sxs-lookup"><span data-stu-id="e595c-115">This command creates a pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>
<span data-ttu-id="e595c-116">Kommandot baserar sig på informationen i pipeline.jsi filen.</span><span class="sxs-lookup"><span data-stu-id="e595c-116">The command bases the pipeline on information in the pipeline.json file.</span></span>
<span data-ttu-id="e595c-117">Filen innehåller information om aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="e595c-117">This file includes information about activities.</span></span>

## <span data-ttu-id="e595c-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e595c-118">PARAMETERS</span></span>

### <span data-ttu-id="e595c-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e595c-119">-AsJob</span></span>
<span data-ttu-id="e595c-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="e595c-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e595c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e595c-121">-DefaultProfile</span></span>
<span data-ttu-id="e595c-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e595c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e595c-123">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="e595c-123">-DefinitionFile</span></span>
<span data-ttu-id="e595c-124">Sökvägen till JSON-filen.</span><span class="sxs-lookup"><span data-stu-id="e595c-124">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e595c-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="e595c-125">-Name</span></span>
<span data-ttu-id="e595c-126">Förlopps namnet.</span><span class="sxs-lookup"><span data-stu-id="e595c-126">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e595c-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e595c-127">-WorkspaceName</span></span>
<span data-ttu-id="e595c-128">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="e595c-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e595c-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e595c-129">-WorkspaceObject</span></span>
<span data-ttu-id="e595c-130">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="e595c-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e595c-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e595c-131">-Confirm</span></span>
<span data-ttu-id="e595c-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e595c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e595c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e595c-133">-WhatIf</span></span>
<span data-ttu-id="e595c-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e595c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e595c-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e595c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e595c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e595c-136">CommonParameters</span></span>
<span data-ttu-id="e595c-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e595c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e595c-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e595c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e595c-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e595c-139">INPUTS</span></span>

### <span data-ttu-id="e595c-140">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e595c-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="e595c-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e595c-141">OUTPUTS</span></span>

### <span data-ttu-id="e595c-142">Microsoft. Azure. commands. Synapse. Models. PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="e595c-142">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="e595c-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e595c-143">NOTES</span></span>

## <span data-ttu-id="e595c-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e595c-144">RELATED LINKS</span></span>