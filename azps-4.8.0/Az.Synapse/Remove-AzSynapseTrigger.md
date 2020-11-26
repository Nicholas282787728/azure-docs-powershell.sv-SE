---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTrigger.md
ms.openlocfilehash: 0882789e230c012fe9f23dcdbeeb5378e9b91781
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261191"
---
# <span data-ttu-id="7081b-101">Remove-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="7081b-101">Remove-AzSynapseTrigger</span></span>

## <span data-ttu-id="7081b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7081b-102">SYNOPSIS</span></span>
<span data-ttu-id="7081b-103">Tar bort en utlösare från en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="7081b-103">Removes a trigger from a workspace.</span></span>

## <span data-ttu-id="7081b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7081b-104">SYNTAX</span></span>

### <span data-ttu-id="7081b-105">RemoveByName (standard)</span><span class="sxs-lookup"><span data-stu-id="7081b-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7081b-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="7081b-106">RemoveByObject</span></span>
```
Remove-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7081b-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="7081b-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7081b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7081b-108">DESCRIPTION</span></span>
<span data-ttu-id="7081b-109">Cmdleten **Remove-AzSynapseTrigger** tar bort en utlösare från en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="7081b-109">The **Remove-AzSynapseTrigger** cmdlet removes a trigger from a workspace.</span></span>

## <span data-ttu-id="7081b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7081b-110">EXAMPLES</span></span>

### <span data-ttu-id="7081b-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7081b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="7081b-112">Ta bort en trigger som heter ContosoTrigger från arbets ytans ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="7081b-112">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="7081b-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="7081b-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="7081b-114">Ta bort en utlösare som heter ContosoTrigger från arbets ytan ContosoWorkspace via pipeline.</span><span class="sxs-lookup"><span data-stu-id="7081b-114">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="7081b-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="7081b-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Remove-AzSynapseTrigger
```

<span data-ttu-id="7081b-116">Ta bort en utlösare som heter ContosoTrigger från arbets ytan ContosoWorkspace via pipeline.</span><span class="sxs-lookup"><span data-stu-id="7081b-116">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="7081b-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7081b-117">PARAMETERS</span></span>

### <span data-ttu-id="7081b-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7081b-118">-AsJob</span></span>
<span data-ttu-id="7081b-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="7081b-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7081b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7081b-120">-DefaultProfile</span></span>
<span data-ttu-id="7081b-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7081b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7081b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7081b-122">-InputObject</span></span>
<span data-ttu-id="7081b-123">Utlös ande objekt.</span><span class="sxs-lookup"><span data-stu-id="7081b-123">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7081b-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="7081b-124">-Name</span></span>
<span data-ttu-id="7081b-125">Utlösarens namn.</span><span class="sxs-lookup"><span data-stu-id="7081b-125">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7081b-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7081b-126">-PassThru</span></span>
<span data-ttu-id="7081b-127">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="7081b-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="7081b-128">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="7081b-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="7081b-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7081b-129">-WorkspaceName</span></span>
<span data-ttu-id="7081b-130">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="7081b-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="7081b-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7081b-131">-WorkspaceObject</span></span>
<span data-ttu-id="7081b-132">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="7081b-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="7081b-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7081b-133">-Confirm</span></span>
<span data-ttu-id="7081b-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7081b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7081b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7081b-135">-WhatIf</span></span>
<span data-ttu-id="7081b-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7081b-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7081b-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7081b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7081b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7081b-138">CommonParameters</span></span>
<span data-ttu-id="7081b-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7081b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7081b-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7081b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7081b-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7081b-141">INPUTS</span></span>

### <span data-ttu-id="7081b-142">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7081b-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="7081b-143">Microsoft. Azure. commands. Synapse. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="7081b-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="7081b-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7081b-144">OUTPUTS</span></span>

### <span data-ttu-id="7081b-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7081b-145">System.Boolean</span></span>

## <span data-ttu-id="7081b-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7081b-146">NOTES</span></span>

## <span data-ttu-id="7081b-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7081b-147">RELATED LINKS</span></span>