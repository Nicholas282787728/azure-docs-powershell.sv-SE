---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 31647da87319ca6be90962f34d128f5e2c922d47
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102568"
---
# <span data-ttu-id="c6876-101">Update-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c6876-101">Update-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="c6876-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c6876-102">SYNOPSIS</span></span>
<span data-ttu-id="c6876-103">Uppdaterar en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="c6876-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="c6876-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c6876-104">SYNTAX</span></span>

### <span data-ttu-id="c6876-105">UpdateByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c6876-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6876-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6876-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6876-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6876-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -ResourceId <String> [-AutoUpdate <String>]
 [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c6876-108">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6876-108">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-AutoUpdate <String>]
 [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c6876-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c6876-109">DESCRIPTION</span></span>
<span data-ttu-id="c6876-110">**Update-AzSynapseIntegrationRuntime** cmdlet uppdaterar egenskaperna för integrations körning.</span><span class="sxs-lookup"><span data-stu-id="c6876-110">The **Update-AzSynapseIntegrationRuntime** cmdlet updates integration runtime properties.</span></span> <span data-ttu-id="c6876-111">För närvarande stöds endast cmdleten för uppdatering av "AutoUpdate" och "AutoUpdateDelayOffset" för integrations körning med egen värd.</span><span class="sxs-lookup"><span data-stu-id="c6876-111">Currently the cmdlet only supports updating 'AutoUpdate' and 'AutoUpdateDelayOffset' for self-hosted integration runtime.</span></span>

## <span data-ttu-id="c6876-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c6876-112">EXAMPLES</span></span>

### <span data-ttu-id="c6876-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c6876-113">Example 1</span></span>
```powershell
PS C:\> $ts = New-TimeSpan -Hours 3
PS C:\> Update-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -AutoUpdate Off -AutoUpdateDelayOffset $ts
```

<span data-ttu-id="c6876-114">Cmdleten uppdaterar den självvärdbaserade integrations körningen "test-selfhost-IR".</span><span class="sxs-lookup"><span data-stu-id="c6876-114">The cmdlet updates self-hosted integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="c6876-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c6876-115">PARAMETERS</span></span>

### <span data-ttu-id="c6876-116">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="c6876-116">-AutoUpdate</span></span>
<span data-ttu-id="c6876-117">Aktivera eller inaktivera automatisk uppdatering för integrering med automatisk värd.</span><span class="sxs-lookup"><span data-stu-id="c6876-117">Enable or disable the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: On, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6876-118">-AutoUpdateDelayOffset</span><span class="sxs-lookup"><span data-stu-id="c6876-118">-AutoUpdateDelayOffset</span></span>
<span data-ttu-id="c6876-119">Tiden på dagen för automatisk uppdatering av integrations körning med självvärd.</span><span class="sxs-lookup"><span data-stu-id="c6876-119">The time of the day for the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6876-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6876-120">-DefaultProfile</span></span>
<span data-ttu-id="c6876-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c6876-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6876-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6876-122">-InputObject</span></span>
<span data-ttu-id="c6876-123">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="c6876-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="c6876-124">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="c6876-124">-IntegrationRuntimeName</span></span>
<span data-ttu-id="c6876-125">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="c6876-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="c6876-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6876-126">-ResourceGroupName</span></span>
<span data-ttu-id="c6876-127">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="c6876-127">Resource group name.</span></span>

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

### <span data-ttu-id="c6876-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6876-128">-ResourceId</span></span>
<span data-ttu-id="c6876-129">Resurs-ID för Synapse.</span><span class="sxs-lookup"><span data-stu-id="c6876-129">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="c6876-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c6876-130">-WorkspaceName</span></span>
<span data-ttu-id="c6876-131">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="c6876-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="c6876-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c6876-132">-WorkspaceObject</span></span>
<span data-ttu-id="c6876-133">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="c6876-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="c6876-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c6876-134">-Confirm</span></span>
<span data-ttu-id="c6876-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c6876-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6876-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6876-136">-WhatIf</span></span>
<span data-ttu-id="c6876-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c6876-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6876-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c6876-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6876-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6876-139">CommonParameters</span></span>
<span data-ttu-id="c6876-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6876-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6876-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6876-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6876-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c6876-142">INPUTS</span></span>

### <span data-ttu-id="c6876-143">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c6876-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="c6876-144">Microsoft. Azure. commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c6876-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="c6876-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c6876-145">OUTPUTS</span></span>

### <span data-ttu-id="c6876-146">Microsoft. Azure. commands. Synapse. Models. PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="c6876-146">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="c6876-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c6876-147">NOTES</span></span>

## <span data-ttu-id="c6876-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c6876-148">RELATED LINKS</span></span>
