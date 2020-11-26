---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/export-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Export-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Export-AzSynapseNotebook.md
ms.openlocfilehash: d61038add8ded9f697bfef551e00aec24c8aaf3e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269394"
---
# <span data-ttu-id="97c35-101">Export-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="97c35-101">Export-AzSynapseNotebook</span></span>

## <span data-ttu-id="97c35-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="97c35-102">SYNOPSIS</span></span>
<span data-ttu-id="97c35-103">Exporterar notbooks.</span><span class="sxs-lookup"><span data-stu-id="97c35-103">Exports notbooks.</span></span>

## <span data-ttu-id="97c35-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="97c35-104">SYNTAX</span></span>

### <span data-ttu-id="97c35-105">ExportByName (standard)</span><span class="sxs-lookup"><span data-stu-id="97c35-105">ExportByName (Default)</span></span>
```
Export-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97c35-106">ExportByObject</span><span class="sxs-lookup"><span data-stu-id="97c35-106">ExportByObject</span></span>
```
Export-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97c35-107">ExportByInputObject</span><span class="sxs-lookup"><span data-stu-id="97c35-107">ExportByInputObject</span></span>
```
Export-AzSynapseNotebook -InputObject <PSNotebookResource> -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97c35-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="97c35-108">DESCRIPTION</span></span>
<span data-ttu-id="97c35-109">Cmdleten **export-AzSynapseNotebook** exporterar en Azure Synapse-anteckningsbok till en antecknings bok (. ipynb).</span><span class="sxs-lookup"><span data-stu-id="97c35-109">The **Export-AzSynapseNotebook** cmdlet exports an Azure Synapse notebook to a notebook (.ipynb) file.</span></span> <span data-ttu-id="97c35-110">Namnet på antecknings boken blir namnet på den exporterade filen.</span><span class="sxs-lookup"><span data-stu-id="97c35-110">The name of the notebook becomes the name of the exported file.</span></span> <span data-ttu-id="97c35-111">Om du anger namnet på en antecknings bok exporterar cmdleten till antecknings boken.</span><span class="sxs-lookup"><span data-stu-id="97c35-111">If you specify the name of a notebook, the cmdlet exports that notebook.</span></span> <span data-ttu-id="97c35-112">Om du inte anger ett namn exporterar cmdleten alla antecknings böcker i arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="97c35-112">If you do not specify a name, the cmdlet export all notebooks in the workspace.</span></span>

## <span data-ttu-id="97c35-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="97c35-113">EXAMPLES</span></span>

### <span data-ttu-id="97c35-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="97c35-114">Example 1</span></span>
```powershell
PS C:\> Export-AzSynapseNotebook -WorkspaceName ContosoWorkspace -OutputFolder "C:\Notebook"
```

<span data-ttu-id="97c35-115">Exporterar alla antecknings böcker i ContosoWorkspace till mappen "C:\Notebook".</span><span class="sxs-lookup"><span data-stu-id="97c35-115">Exports all notebooks in the workspace ContosoWorkspace to the folder "C:\Notebook".</span></span>

### <span data-ttu-id="97c35-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="97c35-116">Example 2</span></span>
```powershell
PS C:\> Export-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="97c35-117">Exporterar en enskild antecknings bok som heter ContosoNotebook i arbets ytan ContosoWorkspace till mappen "C:\Notebook".</span><span class="sxs-lookup"><span data-stu-id="97c35-117">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook".</span></span>

### <span data-ttu-id="97c35-118">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="97c35-118">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Export-AzSynapseNotebook -Name ContosoNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="97c35-119">Exporterar en enskild antecknings bok som heter ContosoNotebook i arbets ytan ContosoWorkspace till mappen "C:\Notebook" genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="97c35-119">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook" through pipeline.</span></span>

### <span data-ttu-id="97c35-120">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="97c35-120">Example 4</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Export-AzSynapseNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="97c35-121">Exporterar en enskild antecknings bok som heter ContosoNotebook i arbets ytan ContosoWorkspace till mappen "C:\Notebook" genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="97c35-121">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook" through pipeline.</span></span>

## <span data-ttu-id="97c35-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="97c35-122">PARAMETERS</span></span>

### <span data-ttu-id="97c35-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97c35-123">-AsJob</span></span>
<span data-ttu-id="97c35-124">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="97c35-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="97c35-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97c35-125">-DefaultProfile</span></span>
<span data-ttu-id="97c35-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="97c35-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97c35-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97c35-127">-InputObject</span></span>
<span data-ttu-id="97c35-128">Objektet antecknings bok.</span><span class="sxs-lookup"><span data-stu-id="97c35-128">The notebook object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource
Parameter Sets: ExportByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97c35-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="97c35-129">-Name</span></span>
<span data-ttu-id="97c35-130">Namnet på antecknings boken.</span><span class="sxs-lookup"><span data-stu-id="97c35-130">The notebook name.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByName, ExportByObject
Aliases: NotebookName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97c35-131">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="97c35-131">-OutputFolder</span></span>
<span data-ttu-id="97c35-132">Den mapp där antecknings boken ska placeras.</span><span class="sxs-lookup"><span data-stu-id="97c35-132">The folder where the notebook should be placed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97c35-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="97c35-133">-WorkspaceName</span></span>
<span data-ttu-id="97c35-134">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="97c35-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97c35-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="97c35-135">-WorkspaceObject</span></span>
<span data-ttu-id="97c35-136">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="97c35-136">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ExportByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97c35-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97c35-137">CommonParameters</span></span>
<span data-ttu-id="97c35-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97c35-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97c35-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97c35-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97c35-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="97c35-140">INPUTS</span></span>

### <span data-ttu-id="97c35-141">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="97c35-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="97c35-142">Microsoft. Azure. commands. Synapse. Models. PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="97c35-142">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="97c35-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="97c35-143">OUTPUTS</span></span>

### <span data-ttu-id="97c35-144">System. IO. FileInfo</span><span class="sxs-lookup"><span data-stu-id="97c35-144">System.IO.FileInfo</span></span>

## <span data-ttu-id="97c35-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="97c35-145">NOTES</span></span>

## <span data-ttu-id="97c35-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="97c35-146">RELATED LINKS</span></span>