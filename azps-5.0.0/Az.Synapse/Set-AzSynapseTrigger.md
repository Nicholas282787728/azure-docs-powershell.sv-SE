---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseTrigger.md
ms.openlocfilehash: 289e601ab80e4842b493cd6852839bec544bcc36
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324858"
---
# <span data-ttu-id="50499-101">Set-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="50499-101">Set-AzSynapseTrigger</span></span>

## <span data-ttu-id="50499-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="50499-102">SYNOPSIS</span></span>
<span data-ttu-id="50499-103">Skapar en utlösare på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="50499-103">Creates a trigger in a workspace.</span></span>

## <span data-ttu-id="50499-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="50499-104">SYNTAX</span></span>

### <span data-ttu-id="50499-105">SetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="50499-105">SetByName (Default)</span></span>
```
Set-AzSynapseTrigger -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50499-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="50499-106">SetByObject</span></span>
```
Set-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50499-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="50499-107">DESCRIPTION</span></span>
<span data-ttu-id="50499-108">Cmdleten **set-AzSynapseTrigger** skapar en utlösare på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="50499-108">The **Set-AzSynapseTrigger** cmdlet creates a trigger in a workspace.</span></span> <span data-ttu-id="50499-109">Utlösare skapas i tillståndet "stoppad", vilket innebär att de inte omedelbart påbörjar samtals ledningar som de refererar till.</span><span class="sxs-lookup"><span data-stu-id="50499-109">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="50499-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="50499-110">EXAMPLES</span></span>

### <span data-ttu-id="50499-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="50499-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger -DefinitionFile ".\scheduledTrigger.json"
```

<span data-ttu-id="50499-112">Skapa en ny utlösare som heter ContosoTrigger i arbets ytans ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="50499-112">Create a new trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span> <span data-ttu-id="50499-113">Utlösaren skapas i tillståndet "stoppad", vilket innebär att den inte startas omedelbart.</span><span class="sxs-lookup"><span data-stu-id="50499-113">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="50499-114">En utlösare kan börja använda `Start-AzDataFactoryV2Trigger` cmdleten.</span><span class="sxs-lookup"><span data-stu-id="50499-114">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

### <span data-ttu-id="50499-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="50499-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseTrigger -Name ContosoTrigger -DefinitionFile ".\scheduledTrigger.json"
```

<span data-ttu-id="50499-116">Skapa en ny utlösare som heter ContosoTrigger i arbets ytans ContosoWorkspace via pipeline.</span><span class="sxs-lookup"><span data-stu-id="50499-116">Create a new trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span> <span data-ttu-id="50499-117">Utlösaren skapas i tillståndet "stoppad", vilket innebär att den inte startas omedelbart.</span><span class="sxs-lookup"><span data-stu-id="50499-117">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="50499-118">En utlösare kan börja använda `Start-AzDataFactoryV2Trigger` cmdleten.</span><span class="sxs-lookup"><span data-stu-id="50499-118">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="50499-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="50499-119">PARAMETERS</span></span>

### <span data-ttu-id="50499-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50499-120">-AsJob</span></span>
<span data-ttu-id="50499-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="50499-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="50499-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50499-122">-DefaultProfile</span></span>
<span data-ttu-id="50499-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="50499-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50499-124">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="50499-124">-DefinitionFile</span></span>
<span data-ttu-id="50499-125">Sökvägen till JSON-filen.</span><span class="sxs-lookup"><span data-stu-id="50499-125">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50499-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="50499-126">-Name</span></span>
<span data-ttu-id="50499-127">Utlösarens namn.</span><span class="sxs-lookup"><span data-stu-id="50499-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50499-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="50499-128">-WorkspaceName</span></span>
<span data-ttu-id="50499-129">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="50499-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50499-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="50499-130">-WorkspaceObject</span></span>
<span data-ttu-id="50499-131">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="50499-131">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50499-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="50499-132">-Confirm</span></span>
<span data-ttu-id="50499-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="50499-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50499-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50499-134">-WhatIf</span></span>
<span data-ttu-id="50499-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="50499-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50499-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="50499-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50499-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50499-137">CommonParameters</span></span>
<span data-ttu-id="50499-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50499-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50499-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50499-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50499-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="50499-140">INPUTS</span></span>

### <span data-ttu-id="50499-141">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="50499-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="50499-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="50499-142">OUTPUTS</span></span>

### <span data-ttu-id="50499-143">Microsoft. Azure. commands. Synapse. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="50499-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="50499-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="50499-144">NOTES</span></span>

## <span data-ttu-id="50499-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="50499-145">RELATED LINKS</span></span>
