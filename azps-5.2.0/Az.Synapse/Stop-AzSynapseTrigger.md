---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseTrigger.md
ms.openlocfilehash: 4e35814be14c2be3b5ba0fd1ca5960d297590dca
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98389916"
---
# <span data-ttu-id="35fbf-101">Stop-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="35fbf-101">Stop-AzSynapseTrigger</span></span>

## <span data-ttu-id="35fbf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="35fbf-102">SYNOPSIS</span></span>
<span data-ttu-id="35fbf-103">Stoppar en utlösare på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="35fbf-103">Stops a trigger in a workspace.</span></span>

## <span data-ttu-id="35fbf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="35fbf-104">SYNTAX</span></span>

### <span data-ttu-id="35fbf-105">StopByName (standard)</span><span class="sxs-lookup"><span data-stu-id="35fbf-105">StopByName (Default)</span></span>
```
Stop-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35fbf-106">StopByObject</span><span class="sxs-lookup"><span data-stu-id="35fbf-106">StopByObject</span></span>
```
Stop-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35fbf-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="35fbf-107">StopByInputObject</span></span>
```
Stop-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35fbf-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="35fbf-108">DESCRIPTION</span></span>
<span data-ttu-id="35fbf-109">Cmdleten **Stop-AzSynapseTrigger** stoppar en trigger på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="35fbf-109">The **Stop-AzSynapseTrigger** cmdlet stops a trigger in a workspace.</span></span> <span data-ttu-id="35fbf-110">Om utlösaren är i läget startat stoppar cmdleten utlösaren och är inte längre aktive rad.</span><span class="sxs-lookup"><span data-stu-id="35fbf-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="35fbf-111">Om utlösaren redan är i tillståndet ' stoppad har denna cmdlet ingen effekt.</span><span class="sxs-lookup"><span data-stu-id="35fbf-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span>

## <span data-ttu-id="35fbf-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="35fbf-112">EXAMPLES</span></span>

### <span data-ttu-id="35fbf-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="35fbf-113">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="35fbf-114">Stoppar en utlösare som heter ContosoTrigger i arbets ytans ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="35fbf-114">Stops a trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="35fbf-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="35fbf-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Stop-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="35fbf-116">Stoppar en utlösare som heter ContosoTrigger i arbets ytans ContosoWorkspace genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="35fbf-116">Stops a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="35fbf-117">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="35fbf-117">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Stop-AzSynapseTrigger
```

<span data-ttu-id="35fbf-118">Stoppa en utlösare som heter ContosoTrigger i arbets ytan ContosoWorkspace via pipeline.</span><span class="sxs-lookup"><span data-stu-id="35fbf-118">Stop a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="35fbf-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="35fbf-119">PARAMETERS</span></span>

### <span data-ttu-id="35fbf-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35fbf-120">-AsJob</span></span>
<span data-ttu-id="35fbf-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="35fbf-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="35fbf-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35fbf-122">-DefaultProfile</span></span>
<span data-ttu-id="35fbf-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="35fbf-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35fbf-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35fbf-124">-InputObject</span></span>
<span data-ttu-id="35fbf-125">Utlös ande objekt.</span><span class="sxs-lookup"><span data-stu-id="35fbf-125">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: StopByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35fbf-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="35fbf-126">-Name</span></span>
<span data-ttu-id="35fbf-127">Utlösarens namn.</span><span class="sxs-lookup"><span data-stu-id="35fbf-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByName, StopByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35fbf-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35fbf-128">-PassThru</span></span>
<span data-ttu-id="35fbf-129">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="35fbf-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="35fbf-130">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="35fbf-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="35fbf-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="35fbf-131">-WorkspaceName</span></span>
<span data-ttu-id="35fbf-132">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="35fbf-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35fbf-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="35fbf-133">-WorkspaceObject</span></span>
<span data-ttu-id="35fbf-134">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="35fbf-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: StopByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35fbf-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="35fbf-135">-Confirm</span></span>
<span data-ttu-id="35fbf-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="35fbf-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35fbf-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35fbf-137">-WhatIf</span></span>
<span data-ttu-id="35fbf-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="35fbf-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="35fbf-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="35fbf-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35fbf-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35fbf-140">CommonParameters</span></span>
<span data-ttu-id="35fbf-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35fbf-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35fbf-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35fbf-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35fbf-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="35fbf-143">INPUTS</span></span>

### <span data-ttu-id="35fbf-144">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="35fbf-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="35fbf-145">Microsoft. Azure. commands. Synapse. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="35fbf-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="35fbf-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="35fbf-146">OUTPUTS</span></span>

### <span data-ttu-id="35fbf-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="35fbf-147">System.Boolean</span></span>

## <span data-ttu-id="35fbf-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="35fbf-148">NOTES</span></span>

## <span data-ttu-id="35fbf-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="35fbf-149">RELATED LINKS</span></span>
