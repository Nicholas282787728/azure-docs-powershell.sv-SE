---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataFlow.md
ms.openlocfilehash: 2d0bec0c86f51771e971ca2c6b5a22c32f8ee687
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523926"
---
# <span data-ttu-id="e6780-101">Remove-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="e6780-101">Remove-AzSynapseDataFlow</span></span>

## <span data-ttu-id="e6780-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e6780-102">SYNOPSIS</span></span>
<span data-ttu-id="e6780-103">Tar bort ett data flöde från arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="e6780-103">Removes a data flow from workspace.</span></span>

## <span data-ttu-id="e6780-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e6780-104">SYNTAX</span></span>

### <span data-ttu-id="e6780-105">RemoveByName (standard)</span><span class="sxs-lookup"><span data-stu-id="e6780-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseDataFlow -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6780-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="e6780-106">RemoveByObject</span></span>
```
Remove-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6780-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="e6780-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseDataFlow -InputObject <PSDataFlowResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6780-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e6780-108">DESCRIPTION</span></span>
<span data-ttu-id="e6780-109">Cmdleten **Remove-AzSynapseDataFlow** tar bort ett data flöde från arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="e6780-109">The **Remove-AzSynapseDataFlow** cmdlet removes a data flow from workspace.</span></span>

## <span data-ttu-id="e6780-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e6780-110">EXAMPLES</span></span>

### <span data-ttu-id="e6780-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e6780-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow
```

<span data-ttu-id="e6780-112">Det här kommandot tar bort data flödet med namnet ContosoDataFlow från arbets ytan med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="e6780-112">This command removes the data flow named ContosoDataFlow from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="e6780-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e6780-113">PARAMETERS</span></span>

### <span data-ttu-id="e6780-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6780-114">-AsJob</span></span>
<span data-ttu-id="e6780-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="e6780-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e6780-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6780-116">-DefaultProfile</span></span>
<span data-ttu-id="e6780-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e6780-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6780-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e6780-118">-Force</span></span>
<span data-ttu-id="e6780-119">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="e6780-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e6780-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6780-120">-InputObject</span></span>
<span data-ttu-id="e6780-121">Data flödes objekt.</span><span class="sxs-lookup"><span data-stu-id="e6780-121">The data flow object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6780-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="e6780-122">-Name</span></span>
<span data-ttu-id="e6780-123">Data flödes namn.</span><span class="sxs-lookup"><span data-stu-id="e6780-123">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: DataFlowName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6780-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6780-124">-PassThru</span></span>
<span data-ttu-id="e6780-125">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="e6780-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="e6780-126">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="e6780-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="e6780-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e6780-127">-WorkspaceName</span></span>
<span data-ttu-id="e6780-128">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="e6780-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e6780-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e6780-129">-WorkspaceObject</span></span>
<span data-ttu-id="e6780-130">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="e6780-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e6780-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e6780-131">-Confirm</span></span>
<span data-ttu-id="e6780-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e6780-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6780-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6780-133">-WhatIf</span></span>
<span data-ttu-id="e6780-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e6780-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6780-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e6780-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6780-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6780-136">CommonParameters</span></span>
<span data-ttu-id="e6780-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6780-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6780-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6780-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6780-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e6780-139">INPUTS</span></span>

### <span data-ttu-id="e6780-140">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e6780-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e6780-141">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="e6780-141">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="e6780-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e6780-142">OUTPUTS</span></span>

### <span data-ttu-id="e6780-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e6780-143">System.Boolean</span></span>

## <span data-ttu-id="e6780-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e6780-144">NOTES</span></span>

## <span data-ttu-id="e6780-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e6780-145">RELATED LINKS</span></span>
