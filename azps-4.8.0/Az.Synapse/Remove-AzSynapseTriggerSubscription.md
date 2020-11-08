---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTriggerSubscription.md
ms.openlocfilehash: 69e7c17d28c94ce00f054a0e5b71eadc4d8ade76
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260215"
---
# <span data-ttu-id="23aa9-101">Remove-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="23aa9-101">Remove-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="23aa9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="23aa9-102">SYNOPSIS</span></span>
<span data-ttu-id="23aa9-103">Avabonnera händelse utlösaren för externa tjänst händelser.</span><span class="sxs-lookup"><span data-stu-id="23aa9-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="23aa9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="23aa9-104">SYNTAX</span></span>

### <span data-ttu-id="23aa9-105">RemoveByName (standard)</span><span class="sxs-lookup"><span data-stu-id="23aa9-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23aa9-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="23aa9-106">RemoveByObject</span></span>
```
Remove-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23aa9-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="23aa9-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23aa9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="23aa9-108">DESCRIPTION</span></span>
<span data-ttu-id="23aa9-109">Cmdleten **Remove-AzSynapseTriggerSubscription** avabonnerar händelse utlösaren för angivna externa tjänst händelser från utlösaren defintion.</span><span class="sxs-lookup"><span data-stu-id="23aa9-109">The **Remove-AzSynapseTriggerSubscription** cmdlet unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="23aa9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="23aa9-110">EXAMPLES</span></span>

### <span data-ttu-id="23aa9-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="23aa9-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="23aa9-112">Det här kommandot avbryter prenumerations utlösaren som heter ContosoTrigger till angivna händelser från utlösaren defintion.</span><span class="sxs-lookup"><span data-stu-id="23aa9-112">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="23aa9-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="23aa9-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="23aa9-114">Det här kommandot avbryter prenumerations utlösaren som heter ContosoTrigger till angivna händelser från utlösaren defintion via pipeline.</span><span class="sxs-lookup"><span data-stu-id="23aa9-114">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="23aa9-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="23aa9-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Remove-AzSynapseTriggerSubscription
```

<span data-ttu-id="23aa9-116">Det här kommandot avbryter prenumerations utlösaren som heter ContosoTrigger till angivna händelser från utlösaren defintion via pipeline.</span><span class="sxs-lookup"><span data-stu-id="23aa9-116">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="23aa9-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="23aa9-117">PARAMETERS</span></span>

### <span data-ttu-id="23aa9-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23aa9-118">-AsJob</span></span>
<span data-ttu-id="23aa9-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="23aa9-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="23aa9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23aa9-120">-DefaultProfile</span></span>
<span data-ttu-id="23aa9-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="23aa9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23aa9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23aa9-122">-InputObject</span></span>
<span data-ttu-id="23aa9-123">Utlös ande objekt.</span><span class="sxs-lookup"><span data-stu-id="23aa9-123">The trigger object.</span></span>

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

### <span data-ttu-id="23aa9-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="23aa9-124">-Name</span></span>
<span data-ttu-id="23aa9-125">Utlösarens namn.</span><span class="sxs-lookup"><span data-stu-id="23aa9-125">The trigger name.</span></span>

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

### <span data-ttu-id="23aa9-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="23aa9-126">-PassThru</span></span>
<span data-ttu-id="23aa9-127">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="23aa9-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="23aa9-128">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="23aa9-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="23aa9-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="23aa9-129">-WorkspaceName</span></span>
<span data-ttu-id="23aa9-130">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="23aa9-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="23aa9-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="23aa9-131">-WorkspaceObject</span></span>
<span data-ttu-id="23aa9-132">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="23aa9-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="23aa9-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="23aa9-133">-Confirm</span></span>
<span data-ttu-id="23aa9-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="23aa9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23aa9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23aa9-135">-WhatIf</span></span>
<span data-ttu-id="23aa9-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="23aa9-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="23aa9-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="23aa9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23aa9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23aa9-138">CommonParameters</span></span>
<span data-ttu-id="23aa9-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23aa9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23aa9-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23aa9-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23aa9-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="23aa9-141">INPUTS</span></span>

### <span data-ttu-id="23aa9-142">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="23aa9-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="23aa9-143">Microsoft. Azure. commands. Synapse. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="23aa9-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="23aa9-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="23aa9-144">OUTPUTS</span></span>

### <span data-ttu-id="23aa9-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="23aa9-145">System.Boolean</span></span>

## <span data-ttu-id="23aa9-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="23aa9-146">NOTES</span></span>

## <span data-ttu-id="23aa9-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="23aa9-147">RELATED LINKS</span></span>
