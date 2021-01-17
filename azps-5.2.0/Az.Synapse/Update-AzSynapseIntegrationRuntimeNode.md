---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: 4192350397a9ba23e57b77b017ff7409afac7a39
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98390899"
---
# <span data-ttu-id="5f84c-101">Update-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="5f84c-101">Update-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="5f84c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5f84c-102">SYNOPSIS</span></span>
<span data-ttu-id="5f84c-103">Uppdaterar noden för integrering med egen värd.</span><span class="sxs-lookup"><span data-stu-id="5f84c-103">Updates self-hosted integration runtime node.</span></span>

## <span data-ttu-id="5f84c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5f84c-104">SYNTAX</span></span>

### <span data-ttu-id="5f84c-105">UpdateByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5f84c-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -Name <String> -ConcurrentJobsLimit <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f84c-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f84c-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -Name <String> -ConcurrentJobsLimit <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5f84c-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f84c-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -ResourceId <String> -Name <String> -ConcurrentJobsLimit <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f84c-108">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f84c-108">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -Name <String>
 -ConcurrentJobsLimit <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5f84c-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5f84c-109">DESCRIPTION</span></span>
<span data-ttu-id="5f84c-110">Cmdleten **Update-AzSynapseIntegrationRuntimeNode** uppdaterar egenskaper för den självvärdbaserade integrations körnings platsen på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="5f84c-110">The **Update-AzSynapseIntegrationRuntimeNode** cmdlet updates properties of self-hosted integration runtime node in a workspace.</span></span> <span data-ttu-id="5f84c-111">För närvarande stöds endast uppdatering av ' ConcurrentJobsLimit '.</span><span class="sxs-lookup"><span data-stu-id="5f84c-111">Currently only supports updating 'ConcurrentJobsLimit'.</span></span>

## <span data-ttu-id="5f84c-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5f84c-112">EXAMPLES</span></span>

### <span data-ttu-id="5f84c-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5f84c-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -ConcurrentJobsLimit 3
```

<span data-ttu-id="5f84c-114">Cmdleten uppdaterar ' ConcurrentJobsLimit ' till 3 för nod ' Node_1 ' i test-selfhost-IR för självvärdisk integrering.</span><span class="sxs-lookup"><span data-stu-id="5f84c-114">The cmdlet updates 'ConcurrentJobsLimit' to 3 for node 'Node_1' in self-hosted integration runtime 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="5f84c-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5f84c-115">PARAMETERS</span></span>

### <span data-ttu-id="5f84c-116">-ConcurrentJobsLimit</span><span class="sxs-lookup"><span data-stu-id="5f84c-116">-ConcurrentJobsLimit</span></span>
<span data-ttu-id="5f84c-117">Antalet samtidiga jobb som får köras på integration runtime-noden.</span><span class="sxs-lookup"><span data-stu-id="5f84c-117">The number of concurrent jobs permitted to run on the integration runtime node.</span></span>
<span data-ttu-id="5f84c-118">Värden mellan 1 och maxConcurrentJobs är tillåtna.</span><span class="sxs-lookup"><span data-stu-id="5f84c-118">Values between 1 and maxConcurrentJobs are allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f84c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f84c-119">-DefaultProfile</span></span>
<span data-ttu-id="5f84c-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5f84c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f84c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5f84c-121">-InputObject</span></span>
<span data-ttu-id="5f84c-122">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="5f84c-122">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f84c-123">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="5f84c-123">-IntegrationRuntimeName</span></span>
<span data-ttu-id="5f84c-124">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="5f84c-124">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f84c-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="5f84c-125">-Name</span></span>
<span data-ttu-id="5f84c-126">Integration runtime-nodnamnet.</span><span class="sxs-lookup"><span data-stu-id="5f84c-126">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f84c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f84c-127">-ResourceGroupName</span></span>
<span data-ttu-id="5f84c-128">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="5f84c-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f84c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f84c-129">-ResourceId</span></span>
<span data-ttu-id="5f84c-130">Resurs-ID för Synapse.</span><span class="sxs-lookup"><span data-stu-id="5f84c-130">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f84c-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5f84c-131">-WorkspaceName</span></span>
<span data-ttu-id="5f84c-132">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="5f84c-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f84c-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5f84c-133">-WorkspaceObject</span></span>
<span data-ttu-id="5f84c-134">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="5f84c-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f84c-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5f84c-135">-Confirm</span></span>
<span data-ttu-id="5f84c-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5f84c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f84c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f84c-137">-WhatIf</span></span>
<span data-ttu-id="5f84c-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5f84c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f84c-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5f84c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f84c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f84c-140">CommonParameters</span></span>
<span data-ttu-id="5f84c-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f84c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f84c-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f84c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f84c-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5f84c-143">INPUTS</span></span>

### <span data-ttu-id="5f84c-144">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5f84c-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="5f84c-145">Microsoft. Azure. commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5f84c-145">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="5f84c-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5f84c-146">OUTPUTS</span></span>

### <span data-ttu-id="5f84c-147">Microsoft. Azure. commands. Synapse. Models. PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="5f84c-147">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="5f84c-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5f84c-148">NOTES</span></span>

## <span data-ttu-id="5f84c-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5f84c-149">RELATED LINKS</span></span>
