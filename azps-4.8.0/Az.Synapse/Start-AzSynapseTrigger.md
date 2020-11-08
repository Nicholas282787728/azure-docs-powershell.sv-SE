---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/start-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseTrigger.md
ms.openlocfilehash: d2488a99bba1813c192df5ef8561d83c06f2f6e7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260211"
---
# <span data-ttu-id="4d149-101">Start-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="4d149-101">Start-AzSynapseTrigger</span></span>

## <span data-ttu-id="4d149-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4d149-102">SYNOPSIS</span></span>
<span data-ttu-id="4d149-103">Startar en utlösare på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="4d149-103">Starts a trigger in a workspace.</span></span>

## <span data-ttu-id="4d149-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4d149-104">SYNTAX</span></span>

### <span data-ttu-id="4d149-105">StartByName (standard)</span><span class="sxs-lookup"><span data-stu-id="4d149-105">StartByName (Default)</span></span>
```
Start-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d149-106">StartByObject</span><span class="sxs-lookup"><span data-stu-id="4d149-106">StartByObject</span></span>
```
Start-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d149-107">StartByInputObject</span><span class="sxs-lookup"><span data-stu-id="4d149-107">StartByInputObject</span></span>
```
Start-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d149-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4d149-108">DESCRIPTION</span></span>
<span data-ttu-id="4d149-109">Cmdleten **Start-AzSynapseTrigger** startar en utlösare på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="4d149-109">The **Start-AzSynapseTrigger** cmdlet starts a trigger in a workspace.</span></span> <span data-ttu-id="4d149-110">Om utlösaren är i tillståndet "stoppad" startar cmdleten utlösaren och kommer slutligen till att ligga på grund val av dess definition.</span><span class="sxs-lookup"><span data-stu-id="4d149-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="4d149-111">Om utlösaren redan är i tillståndet start har denna cmdlet ingen effekt.</span><span class="sxs-lookup"><span data-stu-id="4d149-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span>

## <span data-ttu-id="4d149-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4d149-112">EXAMPLES</span></span>

### <span data-ttu-id="4d149-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4d149-113">Example 1</span></span>
```powershell
PS C:\> Start-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="4d149-114">Startar en trigger som heter ContosoTrigger i arbets ytans ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="4d149-114">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="4d149-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="4d149-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Start-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="4d149-116">Startar en utlösare som heter ContosoTrigger i arbets ytans ContosoWorkspace via pipeline.</span><span class="sxs-lookup"><span data-stu-id="4d149-116">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="4d149-117">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="4d149-117">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Start-AzSynapseTrigger
```

<span data-ttu-id="4d149-118">Startar en utlösare som heter ContosoTrigger i arbets ytans ContosoWorkspace via pipeline.</span><span class="sxs-lookup"><span data-stu-id="4d149-118">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="4d149-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4d149-119">PARAMETERS</span></span>

### <span data-ttu-id="4d149-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d149-120">-AsJob</span></span>
<span data-ttu-id="4d149-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="4d149-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4d149-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d149-122">-DefaultProfile</span></span>
<span data-ttu-id="4d149-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4d149-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d149-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d149-124">-InputObject</span></span>
<span data-ttu-id="4d149-125">Utlös ande objekt.</span><span class="sxs-lookup"><span data-stu-id="4d149-125">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: StartByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d149-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="4d149-126">-Name</span></span>
<span data-ttu-id="4d149-127">Utlösarens namn.</span><span class="sxs-lookup"><span data-stu-id="4d149-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: StartByName, StartByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d149-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4d149-128">-PassThru</span></span>
<span data-ttu-id="4d149-129">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="4d149-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="4d149-130">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="4d149-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="4d149-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4d149-131">-WorkspaceName</span></span>
<span data-ttu-id="4d149-132">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="4d149-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StartByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d149-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4d149-133">-WorkspaceObject</span></span>
<span data-ttu-id="4d149-134">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="4d149-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: StartByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d149-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4d149-135">-Confirm</span></span>
<span data-ttu-id="4d149-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4d149-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d149-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d149-137">-WhatIf</span></span>
<span data-ttu-id="4d149-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4d149-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4d149-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4d149-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d149-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d149-140">CommonParameters</span></span>
<span data-ttu-id="4d149-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d149-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d149-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d149-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d149-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4d149-143">INPUTS</span></span>

### <span data-ttu-id="4d149-144">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4d149-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="4d149-145">Microsoft. Azure. commands. Synapse. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="4d149-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="4d149-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4d149-146">OUTPUTS</span></span>

### <span data-ttu-id="4d149-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4d149-147">System.Boolean</span></span>

## <span data-ttu-id="4d149-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4d149-148">NOTES</span></span>

## <span data-ttu-id="4d149-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4d149-149">RELATED LINKS</span></span>
