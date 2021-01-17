---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapsePipeline.md
ms.openlocfilehash: 747658224703a09f98f232deb865adf4bb084682
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424179"
---
# <span data-ttu-id="d411e-101">Remove-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="d411e-101">Remove-AzSynapsePipeline</span></span>

## <span data-ttu-id="d411e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d411e-102">SYNOPSIS</span></span>
<span data-ttu-id="d411e-103">Tar bort en pipeline från arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="d411e-103">Removes a pipeline from workspace.</span></span>

## <span data-ttu-id="d411e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d411e-104">SYNTAX</span></span>

### <span data-ttu-id="d411e-105">RemoveByName (standard)</span><span class="sxs-lookup"><span data-stu-id="d411e-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapsePipeline -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d411e-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="d411e-106">RemoveByObject</span></span>
```
Remove-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d411e-107">NewByInputObject</span><span class="sxs-lookup"><span data-stu-id="d411e-107">NewByInputObject</span></span>
```
Remove-AzSynapsePipeline -Name <String> -InputObject <PSPipelineResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d411e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d411e-108">DESCRIPTION</span></span>
<span data-ttu-id="d411e-109">Cmdleten **Remove-AzSynapsePipeline** tar bort en pipeline från arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="d411e-109">The **Remove-AzSynapsePipeline** cmdlet removes a pipeline from workspace.</span></span>

## <span data-ttu-id="d411e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d411e-110">EXAMPLES</span></span>

### <span data-ttu-id="d411e-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d411e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="d411e-112">Denna cmdlet tar bort pipelinen med namnet ContosoPipeline från arbets ytan med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="d411e-112">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="d411e-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d411e-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="d411e-114">Denna cmdlet tar bort pipelinen med namnet ContosoPipeline från arbets ytan med namnet ContosoWorkspace till pipeline.</span><span class="sxs-lookup"><span data-stu-id="d411e-114">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="d411e-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="d411e-115">Example 3</span></span>
```powershell
PS C:\> $pipeline = Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
PS C:\> $pipeline | Remove-AzSynapsePipeline
```

<span data-ttu-id="d411e-116">Denna cmdlet tar bort pipelinen med namnet ContosoPipeline från arbets ytan med namnet ContosoWorkspace till pipeline.</span><span class="sxs-lookup"><span data-stu-id="d411e-116">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="d411e-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d411e-117">PARAMETERS</span></span>

### <span data-ttu-id="d411e-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d411e-118">-AsJob</span></span>
<span data-ttu-id="d411e-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d411e-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d411e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d411e-120">-DefaultProfile</span></span>
<span data-ttu-id="d411e-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d411e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d411e-122">-Force</span><span class="sxs-lookup"><span data-stu-id="d411e-122">-Force</span></span>
<span data-ttu-id="d411e-123">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="d411e-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d411e-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d411e-124">-InputObject</span></span>
<span data-ttu-id="d411e-125">Pipeline-objektet.</span><span class="sxs-lookup"><span data-stu-id="d411e-125">The pipeline object.</span></span>

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

### <span data-ttu-id="d411e-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="d411e-126">-Name</span></span>
<span data-ttu-id="d411e-127">Förlopps namnet.</span><span class="sxs-lookup"><span data-stu-id="d411e-127">The pipeline name.</span></span>

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

### <span data-ttu-id="d411e-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d411e-128">-PassThru</span></span>
<span data-ttu-id="d411e-129">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="d411e-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="d411e-130">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="d411e-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="d411e-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d411e-131">-WorkspaceName</span></span>
<span data-ttu-id="d411e-132">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="d411e-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d411e-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d411e-133">-WorkspaceObject</span></span>
<span data-ttu-id="d411e-134">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="d411e-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d411e-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d411e-135">-Confirm</span></span>
<span data-ttu-id="d411e-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d411e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d411e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d411e-137">-WhatIf</span></span>
<span data-ttu-id="d411e-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d411e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d411e-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d411e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d411e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d411e-140">CommonParameters</span></span>
<span data-ttu-id="d411e-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d411e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d411e-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d411e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d411e-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d411e-143">INPUTS</span></span>

### <span data-ttu-id="d411e-144">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d411e-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="d411e-145">Microsoft. Azure. commands. Synapse. Models. PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="d411e-145">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="d411e-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d411e-146">OUTPUTS</span></span>

### <span data-ttu-id="d411e-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d411e-147">System.Boolean</span></span>

## <span data-ttu-id="d411e-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d411e-148">NOTES</span></span>

## <span data-ttu-id="d411e-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d411e-149">RELATED LINKS</span></span>
