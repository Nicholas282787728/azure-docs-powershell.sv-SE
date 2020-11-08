---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapseintegrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseIntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseIntegrationRuntimeUpgrade.md
ms.openlocfilehash: 59630bd0ffcf5bebfc68f647cff444466727a990
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258449"
---
# <span data-ttu-id="35586-101">Invoke-AzSynapseIntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="35586-101">Invoke-AzSynapseIntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="35586-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="35586-102">SYNOPSIS</span></span>
<span data-ttu-id="35586-103">Uppgraderar integrerings körning med egen värd.</span><span class="sxs-lookup"><span data-stu-id="35586-103">Upgrades self-hosted integration runtime.</span></span>

## <span data-ttu-id="35586-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="35586-104">SYNTAX</span></span>

### <span data-ttu-id="35586-105">InvokeByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="35586-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35586-106">InvokeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="35586-106">InvokeByParentObjectParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35586-107">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="35586-107">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35586-108">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="35586-108">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35586-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="35586-109">DESCRIPTION</span></span>
<span data-ttu-id="35586-110">Cmdleten **Invoke-AzSynapseIntegrationRuntimeUpgrade** uppgraderar den självvärdbaserade integrerings miljön om den nya versionen är tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="35586-110">The **Invoke-AzSynapseIntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="35586-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="35586-111">EXAMPLES</span></span>

### <span data-ttu-id="35586-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="35586-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSynapseIntegrationRuntimeUpgrade -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="35586-113">Cmdleten uppgraderar den självvärdbaserade integrations körningen "test-selfhost-IR" i arbets ytans ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="35586-113">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in workspace ContosoWorkspace.</span></span>

## <span data-ttu-id="35586-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="35586-114">PARAMETERS</span></span>

### <span data-ttu-id="35586-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35586-115">-DefaultProfile</span></span>
<span data-ttu-id="35586-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="35586-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35586-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35586-117">-InputObject</span></span>
<span data-ttu-id="35586-118">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="35586-118">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: InvokeByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35586-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="35586-119">-Name</span></span>
<span data-ttu-id="35586-120">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="35586-120">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet, InvokeByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35586-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35586-121">-ResourceGroupName</span></span>
<span data-ttu-id="35586-122">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="35586-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35586-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35586-123">-ResourceId</span></span>
<span data-ttu-id="35586-124">Resurs-ID för Synapse.</span><span class="sxs-lookup"><span data-stu-id="35586-124">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35586-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="35586-125">-WorkspaceName</span></span>
<span data-ttu-id="35586-126">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="35586-126">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35586-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="35586-127">-WorkspaceObject</span></span>
<span data-ttu-id="35586-128">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="35586-128">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: InvokeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35586-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="35586-129">-Confirm</span></span>
<span data-ttu-id="35586-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="35586-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35586-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35586-131">-WhatIf</span></span>
<span data-ttu-id="35586-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="35586-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35586-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="35586-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35586-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35586-134">CommonParameters</span></span>
<span data-ttu-id="35586-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35586-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35586-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35586-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35586-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="35586-137">INPUTS</span></span>

### <span data-ttu-id="35586-138">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="35586-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="35586-139">Microsoft. Azure. commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="35586-139">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="35586-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="35586-140">OUTPUTS</span></span>

### <span data-ttu-id="35586-141">System. Void</span><span class="sxs-lookup"><span data-stu-id="35586-141">System.Void</span></span>

## <span data-ttu-id="35586-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="35586-142">NOTES</span></span>

## <span data-ttu-id="35586-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="35586-143">RELATED LINKS</span></span>
