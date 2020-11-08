---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataset.md
ms.openlocfilehash: 712aa1012269c6207b078fefa3a04a46bea4c573
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103145"
---
# <span data-ttu-id="277a8-101">Remove-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="277a8-101">Remove-AzSynapseDataset</span></span>

## <span data-ttu-id="277a8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="277a8-102">SYNOPSIS</span></span>
<span data-ttu-id="277a8-103">Tar bort en data uppsättning från arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="277a8-103">Removes a dataset from workspace.</span></span>

## <span data-ttu-id="277a8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="277a8-104">SYNTAX</span></span>

### <span data-ttu-id="277a8-105">RemoveByName (standard)</span><span class="sxs-lookup"><span data-stu-id="277a8-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseDataset -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="277a8-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="277a8-106">RemoveByObject</span></span>
```
Remove-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="277a8-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="277a8-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseDataset -InputObject <PSDatasetResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="277a8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="277a8-108">DESCRIPTION</span></span>
<span data-ttu-id="277a8-109">Cmdleten **Remove-AzSynapseDataset** tar bort en data uppsättning från arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="277a8-109">The **Remove-AzSynapseDataset** cmdlet removes a dataset from workspace.</span></span>

## <span data-ttu-id="277a8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="277a8-110">EXAMPLES</span></span>

### <span data-ttu-id="277a8-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="277a8-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset
```

<span data-ttu-id="277a8-112">Det här kommandot tar bort den data uppsättning som heter ContosoDataset från arbets ytan med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="277a8-112">This command removes the dataset named ContosoDataset from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="277a8-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="277a8-113">PARAMETERS</span></span>

### <span data-ttu-id="277a8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="277a8-114">-AsJob</span></span>
<span data-ttu-id="277a8-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="277a8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="277a8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="277a8-116">-DefaultProfile</span></span>
<span data-ttu-id="277a8-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="277a8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="277a8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="277a8-118">-InputObject</span></span>
<span data-ttu-id="277a8-119">Dataset-objektet.</span><span class="sxs-lookup"><span data-stu-id="277a8-119">The dataset object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="277a8-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="277a8-120">-Name</span></span>
<span data-ttu-id="277a8-121">Dataset-namnet.</span><span class="sxs-lookup"><span data-stu-id="277a8-121">The dataset name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: DatasetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="277a8-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="277a8-122">-PassThru</span></span>
<span data-ttu-id="277a8-123">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="277a8-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="277a8-124">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="277a8-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="277a8-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="277a8-125">-WorkspaceName</span></span>
<span data-ttu-id="277a8-126">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="277a8-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="277a8-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="277a8-127">-WorkspaceObject</span></span>
<span data-ttu-id="277a8-128">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="277a8-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="277a8-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="277a8-129">-Confirm</span></span>
<span data-ttu-id="277a8-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="277a8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="277a8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="277a8-131">-WhatIf</span></span>
<span data-ttu-id="277a8-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="277a8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="277a8-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="277a8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="277a8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="277a8-134">CommonParameters</span></span>
<span data-ttu-id="277a8-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="277a8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="277a8-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="277a8-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="277a8-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="277a8-137">INPUTS</span></span>

### <span data-ttu-id="277a8-138">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="277a8-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="277a8-139">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="277a8-139">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="277a8-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="277a8-140">OUTPUTS</span></span>

### <span data-ttu-id="277a8-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="277a8-141">System.Boolean</span></span>

## <span data-ttu-id="277a8-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="277a8-142">NOTES</span></span>

## <span data-ttu-id="277a8-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="277a8-143">RELATED LINKS</span></span>
