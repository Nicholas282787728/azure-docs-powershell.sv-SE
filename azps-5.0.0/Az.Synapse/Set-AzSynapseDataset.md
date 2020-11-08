---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
ms.openlocfilehash: d2471320a27b1af96dba6b5e2b552a01ff5b50e3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272977"
---
# <span data-ttu-id="0a531-101">Set-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="0a531-101">Set-AzSynapseDataset</span></span>

## <span data-ttu-id="0a531-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0a531-102">SYNOPSIS</span></span>
<span data-ttu-id="0a531-103">Skapar eller uppdaterar en data uppsättning i arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="0a531-103">Creates or updates a dataset in workspace.</span></span>

## <span data-ttu-id="0a531-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0a531-104">SYNTAX</span></span>

### <span data-ttu-id="0a531-105">SetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="0a531-105">SetByName (Default)</span></span>
```
Set-AzSynapseDataset -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a531-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="0a531-106">SetByObject</span></span>
```
Set-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a531-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0a531-107">DESCRIPTION</span></span>
<span data-ttu-id="0a531-108">Cmdleten **set-AzSynapseDataset** skapar en DataSet eller uppdaterar en befintlig data uppsättning i arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="0a531-108">The **Set-AzSynapseDataset** cmdlet creates a dataset or updates an existing dataset in workspace.</span></span>

## <span data-ttu-id="0a531-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0a531-109">EXAMPLES</span></span>

### <span data-ttu-id="0a531-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0a531-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset -DefinitionFile "C:\\samples\\Dataset.json"
```

<span data-ttu-id="0a531-111">Det här kommandot skapar en data mängd som heter ContosoDataset i arbets ytan med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="0a531-111">This command creates a dataset named ContosoDataset in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="0a531-112">Kommandot baserar data uppsättningen på informationen i filen Dataset.js.</span><span class="sxs-lookup"><span data-stu-id="0a531-112">The command bases the dataset on information in the Dataset.json file.</span></span>

## <span data-ttu-id="0a531-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0a531-113">PARAMETERS</span></span>

### <span data-ttu-id="0a531-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a531-114">-AsJob</span></span>
<span data-ttu-id="0a531-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="0a531-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0a531-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a531-116">-DefaultProfile</span></span>
<span data-ttu-id="0a531-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0a531-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a531-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="0a531-118">-DefinitionFile</span></span>
<span data-ttu-id="0a531-119">Sökvägen till JSON-filen.</span><span class="sxs-lookup"><span data-stu-id="0a531-119">The JSON file path.</span></span>

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

### <span data-ttu-id="0a531-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="0a531-120">-Name</span></span>
<span data-ttu-id="0a531-121">Dataset-namnet.</span><span class="sxs-lookup"><span data-stu-id="0a531-121">The dataset name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a531-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0a531-122">-WorkspaceName</span></span>
<span data-ttu-id="0a531-123">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="0a531-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="0a531-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0a531-124">-WorkspaceObject</span></span>
<span data-ttu-id="0a531-125">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="0a531-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="0a531-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0a531-126">-Confirm</span></span>
<span data-ttu-id="0a531-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0a531-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a531-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a531-128">-WhatIf</span></span>
<span data-ttu-id="0a531-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0a531-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a531-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0a531-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a531-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a531-131">CommonParameters</span></span>
<span data-ttu-id="0a531-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a531-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a531-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a531-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a531-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0a531-134">INPUTS</span></span>

### <span data-ttu-id="0a531-135">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0a531-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="0a531-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0a531-136">OUTPUTS</span></span>

### <span data-ttu-id="0a531-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="0a531-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="0a531-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0a531-138">NOTES</span></span>

## <span data-ttu-id="0a531-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0a531-139">RELATED LINKS</span></span>
