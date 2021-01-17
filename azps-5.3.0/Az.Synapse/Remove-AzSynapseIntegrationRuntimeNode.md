---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: cb2c632b47e512d31a5349be9b6091a9981f5459
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424195"
---
# <span data-ttu-id="d1906-101">Remove-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="d1906-101">Remove-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="d1906-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d1906-102">SYNOPSIS</span></span>
<span data-ttu-id="d1906-103">Ta bort en nod med det angivna namnet i en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="d1906-103">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="d1906-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d1906-104">SYNTAX</span></span>

### <span data-ttu-id="d1906-105">RemoveByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d1906-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1906-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1906-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d1906-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1906-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -ResourceId <String> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1906-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1906-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1906-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d1906-109">DESCRIPTION</span></span>
<span data-ttu-id="d1906-110">Cmdleten **Remove-AzSynapseIntegrationRuntimeNode** tar bort en nod i en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="d1906-110">The **Remove-AzSynapseIntegrationRuntimeNode** cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="d1906-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d1906-111">EXAMPLES</span></span>

### <span data-ttu-id="d1906-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d1906-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="d1906-113">Ta bort en nod med det angivna namnet i en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="d1906-113">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="d1906-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d1906-114">PARAMETERS</span></span>

### <span data-ttu-id="d1906-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1906-115">-DefaultProfile</span></span>
<span data-ttu-id="d1906-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d1906-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1906-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d1906-117">-Force</span></span>
<span data-ttu-id="d1906-118">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="d1906-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="d1906-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1906-119">-InputObject</span></span>
<span data-ttu-id="d1906-120">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="d1906-120">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1906-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="d1906-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="d1906-122">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="d1906-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet, RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1906-123">-Nodnamn</span><span class="sxs-lookup"><span data-stu-id="d1906-123">-NodeName</span></span>
<span data-ttu-id="d1906-124">Integration runtime-nodnamnet.</span><span class="sxs-lookup"><span data-stu-id="d1906-124">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1906-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1906-125">-ResourceGroupName</span></span>
<span data-ttu-id="d1906-126">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="d1906-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1906-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1906-127">-ResourceId</span></span>
<span data-ttu-id="d1906-128">Resurs-ID för Synapse.</span><span class="sxs-lookup"><span data-stu-id="d1906-128">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1906-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d1906-129">-WorkspaceName</span></span>
<span data-ttu-id="d1906-130">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="d1906-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1906-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d1906-131">-WorkspaceObject</span></span>
<span data-ttu-id="d1906-132">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="d1906-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1906-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d1906-133">-Confirm</span></span>
<span data-ttu-id="d1906-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d1906-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1906-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1906-135">-WhatIf</span></span>
<span data-ttu-id="d1906-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d1906-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1906-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d1906-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1906-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1906-138">CommonParameters</span></span>
<span data-ttu-id="d1906-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1906-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1906-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1906-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1906-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d1906-141">INPUTS</span></span>

### <span data-ttu-id="d1906-142">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d1906-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="d1906-143">Microsoft. Azure. commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d1906-143">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="d1906-144">System. String</span><span class="sxs-lookup"><span data-stu-id="d1906-144">System.String</span></span>

## <span data-ttu-id="d1906-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d1906-145">OUTPUTS</span></span>

### <span data-ttu-id="d1906-146">System. Void</span><span class="sxs-lookup"><span data-stu-id="d1906-146">System.Void</span></span>

## <span data-ttu-id="d1906-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d1906-147">NOTES</span></span>

## <span data-ttu-id="d1906-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d1906-148">RELATED LINKS</span></span>
