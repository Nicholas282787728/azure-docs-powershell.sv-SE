---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseNotebook.md
ms.openlocfilehash: da4907200bef198afa1d57b51069c6379d28c8f1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260880"
---
# <span data-ttu-id="9a1bc-101">Set-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="9a1bc-101">Set-AzSynapseNotebook</span></span>

## <span data-ttu-id="9a1bc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9a1bc-102">SYNOPSIS</span></span>
<span data-ttu-id="9a1bc-103">Skapar eller uppdaterar en antecknings bok på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="9a1bc-103">Creates or updates a notebook in a workspace.</span></span>

## <span data-ttu-id="9a1bc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9a1bc-104">SYNTAX</span></span>

### <span data-ttu-id="9a1bc-105">SetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="9a1bc-105">SetByName (Default)</span></span>
```
Set-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a1bc-106">SetByNameAndSparkPool</span><span class="sxs-lookup"><span data-stu-id="9a1bc-106">SetByNameAndSparkPool</span></span>
```
Set-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -SparkPoolName <String> [-ExecutorSize <String>]
 -ExecutorCount <Int32> -DefinitionFile <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a1bc-107">SetByObject</span><span class="sxs-lookup"><span data-stu-id="9a1bc-107">SetByObject</span></span>
```
Set-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a1bc-108">SetByObjectAndSparkPool</span><span class="sxs-lookup"><span data-stu-id="9a1bc-108">SetByObjectAndSparkPool</span></span>
```
Set-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -SparkPoolName <String>
 [-ExecutorSize <String>] -ExecutorCount <Int32> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a1bc-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9a1bc-109">DESCRIPTION</span></span>
<span data-ttu-id="9a1bc-110">Cmdleten **set-AzSynapseNotebook** skapar eller uppdaterar en antecknings bok på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="9a1bc-110">The **Set-AzSynapseNotebook** cmdlet creates or updates a notebook in a workspace.</span></span>

## <span data-ttu-id="9a1bc-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9a1bc-111">EXAMPLES</span></span>

### <span data-ttu-id="9a1bc-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9a1bc-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseNotebook -WorkspaceName ContosoWorkspace -DefinitionFile "C:\\samples\\notebook.ipynb"

    WorkspaceName : ContosoWorkspace
    Properties    : Microsoft.Azure.Commands.Synapse.Models.PSNotebook
    Name          : notebook
```

<span data-ttu-id="9a1bc-113">Det här kommandot skapar eller uppdaterar en antecknings bok från anteckningsbok för antecknings boken. ipynb i arbets ytan med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="9a1bc-113">This command creates or updates a notebook from notebook file notebook.ipynb in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="9a1bc-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="9a1bc-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseNotebook -DefinitionFile "C:\\samples\\notebook.ipynb"
```

<span data-ttu-id="9a1bc-115">Det här kommandot skapar eller uppdaterar en antecknings bok från fil antecknings boken för antecknings böcker. ipynb i arbets ytan ContosoWorkspace via pipeline.</span><span class="sxs-lookup"><span data-stu-id="9a1bc-115">This command creates or updates a notebook from notebook file notebook.ipynb in the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="9a1bc-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="9a1bc-116">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseNotebook -WorkspaceName ContosoWorkspace -DefinitionFile "C:\\samples\\notebook.ipynb" -SparkPoolName ContosoSparkPool -ExecutorCount 2
```

<span data-ttu-id="9a1bc-117">Det här kommandot skapar eller uppdaterar en antecknings bok från antecknings bok för bifogad fil</span><span class="sxs-lookup"><span data-stu-id="9a1bc-117">This command creates or updates a notebook from notebook file notebook.ipynb which attaches to ContosoSparkPool and uses 2 executors in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="9a1bc-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9a1bc-118">PARAMETERS</span></span>

### <span data-ttu-id="9a1bc-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a1bc-119">-AsJob</span></span>
<span data-ttu-id="9a1bc-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="9a1bc-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9a1bc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a1bc-121">-DefaultProfile</span></span>
<span data-ttu-id="9a1bc-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9a1bc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a1bc-123">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="9a1bc-123">-DefinitionFile</span></span>
<span data-ttu-id="9a1bc-124">Sökvägen till JSON-filen.</span><span class="sxs-lookup"><span data-stu-id="9a1bc-124">The JSON file path.</span></span>

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

### <span data-ttu-id="9a1bc-125">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="9a1bc-125">-ExecutorCount</span></span>
<span data-ttu-id="9a1bc-126">Antal exekverare som ska tilldelas i den angivna Spark-poolen för jobbet.</span><span class="sxs-lookup"><span data-stu-id="9a1bc-126">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByNameAndSparkPool, SetByObjectAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a1bc-127">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="9a1bc-127">-ExecutorSize</span></span>
<span data-ttu-id="9a1bc-128">Antal kärnor och minne som ska användas för utförare som tilldelats till det angivna Spark-poolen för jobbet.</span><span class="sxs-lookup"><span data-stu-id="9a1bc-128">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndSparkPool, SetByObjectAndSparkPool
Aliases:
Accepted values: Small, Medium, Large

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a1bc-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="9a1bc-129">-Name</span></span>
<span data-ttu-id="9a1bc-130">Namnet på antecknings boken.</span><span class="sxs-lookup"><span data-stu-id="9a1bc-130">The notebook name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NotebookName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a1bc-131">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="9a1bc-131">-SparkPoolName</span></span>
<span data-ttu-id="9a1bc-132">Namn på Synapse Spark-pool.</span><span class="sxs-lookup"><span data-stu-id="9a1bc-132">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndSparkPool, SetByObjectAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a1bc-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9a1bc-133">-WorkspaceName</span></span>
<span data-ttu-id="9a1bc-134">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="9a1bc-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByNameAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a1bc-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9a1bc-135">-WorkspaceObject</span></span>
<span data-ttu-id="9a1bc-136">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="9a1bc-136">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject, SetByObjectAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a1bc-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9a1bc-137">-Confirm</span></span>
<span data-ttu-id="9a1bc-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9a1bc-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a1bc-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a1bc-139">-WhatIf</span></span>
<span data-ttu-id="9a1bc-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9a1bc-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a1bc-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9a1bc-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a1bc-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a1bc-142">CommonParameters</span></span>
<span data-ttu-id="9a1bc-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a1bc-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a1bc-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a1bc-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a1bc-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9a1bc-145">INPUTS</span></span>

### <span data-ttu-id="9a1bc-146">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9a1bc-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="9a1bc-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9a1bc-147">OUTPUTS</span></span>

### <span data-ttu-id="9a1bc-148">Microsoft. Azure. commands. Synapse. Models. PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="9a1bc-148">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="9a1bc-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9a1bc-149">NOTES</span></span>

## <span data-ttu-id="9a1bc-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9a1bc-150">RELATED LINKS</span></span>
