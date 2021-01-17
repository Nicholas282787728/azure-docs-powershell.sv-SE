---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
ms.openlocfilehash: 23bd6186f31199ab9387df5ee78ce3fdbe89032e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424184"
---
# <span data-ttu-id="09985-101">Remove-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="09985-101">Remove-AzSynapseNotebook</span></span>

## <span data-ttu-id="09985-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="09985-102">SYNOPSIS</span></span>
<span data-ttu-id="09985-103">Tar bort en antecknings bok från en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="09985-103">Removes a notebook from a workspace.</span></span>

## <span data-ttu-id="09985-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="09985-104">SYNTAX</span></span>

### <span data-ttu-id="09985-105">RemoveByName (standard)</span><span class="sxs-lookup"><span data-stu-id="09985-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseNotebook -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09985-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="09985-106">RemoveByObject</span></span>
```
Remove-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09985-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="09985-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseNotebook -InputObject <PSNotebookResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09985-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="09985-108">DESCRIPTION</span></span>
<span data-ttu-id="09985-109">Cmdleten **Remove-AzSynapseNotebook** tar bort en antecknings bok från en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="09985-109">The **Remove-AzSynapseNotebook** cmdlet removes a notebook from a workspace.</span></span>

## <span data-ttu-id="09985-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="09985-110">EXAMPLES</span></span>

### <span data-ttu-id="09985-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="09985-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="09985-112">Ta bort en antecknings bok som heter ContosoNotebook från arbets ytans ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="09985-112">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="09985-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="09985-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="09985-114">Ta bort en antecknings bok som heter ContosoNotebook från ContosoWorkspace för arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="09985-114">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="09985-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="09985-115">Example 3</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Remove-AzSynapseNotebook
```

<span data-ttu-id="09985-116">Ta bort en antecknings bok som heter ContosoNotebook från ContosoWorkspace för arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="09985-116">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="09985-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="09985-117">PARAMETERS</span></span>

### <span data-ttu-id="09985-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="09985-118">-AsJob</span></span>
<span data-ttu-id="09985-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="09985-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="09985-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09985-120">-DefaultProfile</span></span>
<span data-ttu-id="09985-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="09985-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09985-122">-Force</span><span class="sxs-lookup"><span data-stu-id="09985-122">-Force</span></span>
<span data-ttu-id="09985-123">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="09985-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="09985-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09985-124">-InputObject</span></span>
<span data-ttu-id="09985-125">Objektet antecknings bok.</span><span class="sxs-lookup"><span data-stu-id="09985-125">The notebook object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09985-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="09985-126">-Name</span></span>
<span data-ttu-id="09985-127">Namnet på antecknings boken.</span><span class="sxs-lookup"><span data-stu-id="09985-127">The notebook name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: NotebookName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09985-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="09985-128">-PassThru</span></span>
<span data-ttu-id="09985-129">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="09985-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="09985-130">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="09985-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="09985-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="09985-131">-WorkspaceName</span></span>
<span data-ttu-id="09985-132">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="09985-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="09985-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="09985-133">-WorkspaceObject</span></span>
<span data-ttu-id="09985-134">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="09985-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="09985-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="09985-135">-Confirm</span></span>
<span data-ttu-id="09985-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="09985-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09985-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09985-137">-WhatIf</span></span>
<span data-ttu-id="09985-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="09985-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="09985-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="09985-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09985-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09985-140">CommonParameters</span></span>
<span data-ttu-id="09985-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09985-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09985-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09985-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09985-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="09985-143">INPUTS</span></span>

### <span data-ttu-id="09985-144">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="09985-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="09985-145">Microsoft. Azure. commands. Synapse. Models. PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="09985-145">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="09985-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="09985-146">OUTPUTS</span></span>

### <span data-ttu-id="09985-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="09985-147">System.Boolean</span></span>

## <span data-ttu-id="09985-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="09985-148">NOTES</span></span>

## <span data-ttu-id="09985-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="09985-149">RELATED LINKS</span></span>
