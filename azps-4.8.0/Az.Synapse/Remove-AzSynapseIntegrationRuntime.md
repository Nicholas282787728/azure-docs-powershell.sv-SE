---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 57b6c6619a45e515c7aff2e30edc346ff39af9ac
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103143"
---
# <span data-ttu-id="99ca3-101">Remove-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="99ca3-101">Remove-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="99ca3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="99ca3-102">SYNOPSIS</span></span>
<span data-ttu-id="99ca3-103">Tar bort en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="99ca3-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="99ca3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="99ca3-104">SYNTAX</span></span>

### <span data-ttu-id="99ca3-105">RemoveByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="99ca3-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99ca3-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="99ca3-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99ca3-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="99ca3-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -ResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99ca3-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="99ca3-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99ca3-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="99ca3-109">DESCRIPTION</span></span>
<span data-ttu-id="99ca3-110">Cmdleten **Remove-AzSynapseIntegrationRuntime** tar bort en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="99ca3-110">The **Remove-AzSynapseIntegrationRuntime** cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="99ca3-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="99ca3-111">EXAMPLES</span></span>

### <span data-ttu-id="99ca3-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="99ca3-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="99ca3-113">Det här kommandot tar bort integrations körningen "test-reserverad-IR" från arbets ytan med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="99ca3-113">This command removes the integration runtime named 'test-reserved-ir' from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="99ca3-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="99ca3-114">PARAMETERS</span></span>

### <span data-ttu-id="99ca3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99ca3-115">-DefaultProfile</span></span>
<span data-ttu-id="99ca3-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="99ca3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99ca3-117">-Force</span><span class="sxs-lookup"><span data-stu-id="99ca3-117">-Force</span></span>
<span data-ttu-id="99ca3-118">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="99ca3-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="99ca3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99ca3-119">-InputObject</span></span>
<span data-ttu-id="99ca3-120">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="99ca3-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="99ca3-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="99ca3-121">-Name</span></span>
<span data-ttu-id="99ca3-122">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="99ca3-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet, RemoveByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99ca3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99ca3-123">-ResourceGroupName</span></span>
<span data-ttu-id="99ca3-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="99ca3-124">Resource group name.</span></span>

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

### <span data-ttu-id="99ca3-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99ca3-125">-ResourceId</span></span>
<span data-ttu-id="99ca3-126">Resurs-ID för Synapse.</span><span class="sxs-lookup"><span data-stu-id="99ca3-126">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="99ca3-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="99ca3-127">-WorkspaceName</span></span>
<span data-ttu-id="99ca3-128">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="99ca3-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="99ca3-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="99ca3-129">-WorkspaceObject</span></span>
<span data-ttu-id="99ca3-130">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="99ca3-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="99ca3-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="99ca3-131">-Confirm</span></span>
<span data-ttu-id="99ca3-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="99ca3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99ca3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99ca3-133">-WhatIf</span></span>
<span data-ttu-id="99ca3-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="99ca3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99ca3-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="99ca3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99ca3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99ca3-136">CommonParameters</span></span>
<span data-ttu-id="99ca3-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99ca3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99ca3-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99ca3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99ca3-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="99ca3-139">INPUTS</span></span>

### <span data-ttu-id="99ca3-140">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="99ca3-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="99ca3-141">Microsoft. Azure. commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="99ca3-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="99ca3-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="99ca3-142">OUTPUTS</span></span>

### <span data-ttu-id="99ca3-143">System. Void</span><span class="sxs-lookup"><span data-stu-id="99ca3-143">System.Void</span></span>

## <span data-ttu-id="99ca3-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="99ca3-144">NOTES</span></span>

## <span data-ttu-id="99ca3-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="99ca3-145">RELATED LINKS</span></span>
