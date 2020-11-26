---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/add-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
ms.openlocfilehash: ca5501115b7c75b2e3c1baca368ebaac841e0ae1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271195"
---
# <span data-ttu-id="a1011-101">Add-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="a1011-101">Add-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="a1011-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a1011-102">SYNOPSIS</span></span>
<span data-ttu-id="a1011-103">Abonnera på händelse utlösare för externa tjänst händelser.</span><span class="sxs-lookup"><span data-stu-id="a1011-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="a1011-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a1011-104">SYNTAX</span></span>

### <span data-ttu-id="a1011-105">AddByName (standard)</span><span class="sxs-lookup"><span data-stu-id="a1011-105">AddByName (Default)</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1011-106">AddByObject</span><span class="sxs-lookup"><span data-stu-id="a1011-106">AddByObject</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1011-107">AddByInputObject</span><span class="sxs-lookup"><span data-stu-id="a1011-107">AddByInputObject</span></span>
```
Add-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1011-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a1011-108">DESCRIPTION</span></span>
<span data-ttu-id="a1011-109">Cmdleten **Add-AzSynapseTriggerSubscription** abonnerar på händelse utlösaren för angivna externa tjänst händelser från utlösaren defintion.</span><span class="sxs-lookup"><span data-stu-id="a1011-109">The **Add-AzSynapseTriggerSubscription** cmdlet subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="a1011-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a1011-110">EXAMPLES</span></span>

### <span data-ttu-id="a1011-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a1011-111">Example 1</span></span>
```powershell
PS C:\> Add-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="a1011-112">Det här kommandot abonnerar på utlösaren ContosoTrigger till angivna händelser från utlösaren defintion.</span><span class="sxs-lookup"><span data-stu-id="a1011-112">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="a1011-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a1011-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Add-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="a1011-114">Det här kommandot prenumererar på utlösaren ContosoTrigger till angivna händelser från utlösaren defintion via pipeline.</span><span class="sxs-lookup"><span data-stu-id="a1011-114">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="a1011-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="a1011-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Add-AzSynapseTriggerSubscription
```

<span data-ttu-id="a1011-116">Det här kommandot prenumererar på utlösaren ContosoTrigger till angivna händelser från utlösaren defintion via pipeline.</span><span class="sxs-lookup"><span data-stu-id="a1011-116">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="a1011-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a1011-117">PARAMETERS</span></span>

### <span data-ttu-id="a1011-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1011-118">-AsJob</span></span>
<span data-ttu-id="a1011-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a1011-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a1011-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1011-120">-DefaultProfile</span></span>
<span data-ttu-id="a1011-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a1011-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1011-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1011-122">-InputObject</span></span>
<span data-ttu-id="a1011-123">Utlös ande objekt.</span><span class="sxs-lookup"><span data-stu-id="a1011-123">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: AddByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1011-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="a1011-124">-Name</span></span>
<span data-ttu-id="a1011-125">Utlösarens namn.</span><span class="sxs-lookup"><span data-stu-id="a1011-125">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: AddByName, AddByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1011-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a1011-126">-WorkspaceName</span></span>
<span data-ttu-id="a1011-127">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="a1011-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: AddByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1011-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a1011-128">-WorkspaceObject</span></span>
<span data-ttu-id="a1011-129">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="a1011-129">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: AddByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1011-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a1011-130">-Confirm</span></span>
<span data-ttu-id="a1011-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a1011-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1011-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1011-132">-WhatIf</span></span>
<span data-ttu-id="a1011-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a1011-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1011-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a1011-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1011-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1011-135">CommonParameters</span></span>
<span data-ttu-id="a1011-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1011-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1011-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1011-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1011-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a1011-138">INPUTS</span></span>

### <span data-ttu-id="a1011-139">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a1011-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="a1011-140">Microsoft. Azure. commands. Synapse. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="a1011-140">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="a1011-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a1011-141">OUTPUTS</span></span>

### <span data-ttu-id="a1011-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="a1011-142">System.Object</span></span>
## <span data-ttu-id="a1011-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a1011-143">NOTES</span></span>

## <span data-ttu-id="a1011-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a1011-144">RELATED LINKS</span></span>