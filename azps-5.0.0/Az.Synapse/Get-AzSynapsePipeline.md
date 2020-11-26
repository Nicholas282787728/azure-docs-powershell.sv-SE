---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
ms.openlocfilehash: 6224a871aebff834693c8eed3026a75f22879ffa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271685"
---
# <span data-ttu-id="579c2-101">Get-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="579c2-101">Get-AzSynapsePipeline</span></span>

## <span data-ttu-id="579c2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="579c2-102">SYNOPSIS</span></span>
<span data-ttu-id="579c2-103">Hämtar information om rörledningar i arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="579c2-103">Gets information about pipelines in workspace.</span></span>

## <span data-ttu-id="579c2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="579c2-104">SYNTAX</span></span>

### <span data-ttu-id="579c2-105">GetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="579c2-105">GetByName (Default)</span></span>
```
Get-AzSynapsePipeline -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="579c2-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="579c2-106">GetByObject</span></span>
```
Get-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="579c2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="579c2-107">DESCRIPTION</span></span>
<span data-ttu-id="579c2-108">Cmdleten **Get-AzSynapsePipeline** hämtar information om rörledningar i arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="579c2-108">The **Get-AzSynapsePipeline** cmdlet gets information about pipelines in workspace.</span></span> <span data-ttu-id="579c2-109">Om du anger namnet på en pipeline får denna cmdlet information om den pipelinen.</span><span class="sxs-lookup"><span data-stu-id="579c2-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span> <span data-ttu-id="579c2-110">Om du inte anger ett namn hämtas den här cmdleten information om alla rörledningar på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="579c2-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the workspace.</span></span>

## <span data-ttu-id="579c2-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="579c2-111">EXAMPLES</span></span>

### <span data-ttu-id="579c2-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="579c2-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="579c2-113">Det här kommandot får information om alla rörledningar i arbets ytan med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="579c2-113">This command gets information about all pipelines in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="579c2-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="579c2-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="579c2-115">Med det här kommandot får du information om pipeline med namnet ContosoPipeline i arbets ytan med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="579c2-115">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="579c2-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="579c2-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="579c2-117">Med det här kommandot får du information om pipeline med namnet ContosoPipeline i arbets ytan som heter ContosoWorkspace via pipeline.</span><span class="sxs-lookup"><span data-stu-id="579c2-117">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="579c2-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="579c2-118">PARAMETERS</span></span>

### <span data-ttu-id="579c2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="579c2-119">-DefaultProfile</span></span>
<span data-ttu-id="579c2-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="579c2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="579c2-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="579c2-121">-Name</span></span>
<span data-ttu-id="579c2-122">Förlopps namnet.</span><span class="sxs-lookup"><span data-stu-id="579c2-122">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="579c2-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="579c2-123">-WorkspaceName</span></span>
<span data-ttu-id="579c2-124">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="579c2-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="579c2-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="579c2-125">-WorkspaceObject</span></span>
<span data-ttu-id="579c2-126">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="579c2-126">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="579c2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="579c2-127">CommonParameters</span></span>
<span data-ttu-id="579c2-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="579c2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="579c2-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="579c2-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="579c2-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="579c2-130">INPUTS</span></span>

### <span data-ttu-id="579c2-131">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="579c2-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="579c2-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="579c2-132">OUTPUTS</span></span>

### <span data-ttu-id="579c2-133">Microsoft. Azure. commands. Synapse. Models. PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="579c2-133">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="579c2-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="579c2-134">NOTES</span></span>

## <span data-ttu-id="579c2-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="579c2-135">RELATED LINKS</span></span>