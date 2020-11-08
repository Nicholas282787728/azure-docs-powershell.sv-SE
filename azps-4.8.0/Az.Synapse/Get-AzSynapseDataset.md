---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataset.md
ms.openlocfilehash: 8919c554fb32a102991b9c40236e897662709ccb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261504"
---
# <span data-ttu-id="d6273-101">Get-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="d6273-101">Get-AzSynapseDataset</span></span>

## <span data-ttu-id="d6273-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d6273-102">SYNOPSIS</span></span>
<span data-ttu-id="d6273-103">Hämtar information om data mängder i arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="d6273-103">Gets information about datasets in workspace.</span></span>

## <span data-ttu-id="d6273-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d6273-104">SYNTAX</span></span>

### <span data-ttu-id="d6273-105">GetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="d6273-105">GetByName (Default)</span></span>
```
Get-AzSynapseDataset -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d6273-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="d6273-106">GetByObject</span></span>
```
Get-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6273-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d6273-107">DESCRIPTION</span></span>
<span data-ttu-id="d6273-108">Cmdleten **Get-AzSynapseDataset** hämtar information om data mängderna i arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="d6273-108">The **Get-AzSynapseDataset** cmdlet gets information about datasets in workspace.</span></span>
<span data-ttu-id="d6273-109">Om du anger namnet på en data uppsättning får denna cmdlet information om den data uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="d6273-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="d6273-110">Om du inte anger ett namn hämtas den här cmdleten information om alla data uppsättningarna i arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="d6273-110">If you do not specify a name, this cmdlet gets information about all the datasets in the workspace.</span></span>

## <span data-ttu-id="d6273-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d6273-111">EXAMPLES</span></span>

### <span data-ttu-id="d6273-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d6273-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseDataset -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="d6273-113">Det här kommandot får information om alla data mängder i arbets ytan med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="d6273-113">This command gets information about all datasets in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="d6273-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d6273-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset
```

<span data-ttu-id="d6273-115">Med det här kommandot får du information om den data uppsättning som heter ContosoDataset i arbets ytan med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="d6273-115">This command gets information about the dataset named ContosoDataset in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="d6273-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d6273-116">PARAMETERS</span></span>

### <span data-ttu-id="d6273-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6273-117">-DefaultProfile</span></span>
<span data-ttu-id="d6273-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d6273-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6273-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="d6273-119">-Name</span></span>
<span data-ttu-id="d6273-120">Dataset-namnet.</span><span class="sxs-lookup"><span data-stu-id="d6273-120">The dataset name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6273-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d6273-121">-WorkspaceName</span></span>
<span data-ttu-id="d6273-122">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="d6273-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d6273-123">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d6273-123">-WorkspaceObject</span></span>
<span data-ttu-id="d6273-124">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="d6273-124">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d6273-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6273-125">CommonParameters</span></span>
<span data-ttu-id="d6273-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6273-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6273-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6273-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6273-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d6273-128">INPUTS</span></span>

### <span data-ttu-id="d6273-129">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d6273-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="d6273-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d6273-130">OUTPUTS</span></span>

### <span data-ttu-id="d6273-131">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="d6273-131">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="d6273-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d6273-132">NOTES</span></span>

## <span data-ttu-id="d6273-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d6273-133">RELATED LINKS</span></span>
