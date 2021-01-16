---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseNotebook.md
ms.openlocfilehash: 28a4742b2e744fb41bca9402a8c48b830554e231
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397248"
---
# <span data-ttu-id="a26f9-101">Get-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="a26f9-101">Get-AzSynapseNotebook</span></span>

## <span data-ttu-id="a26f9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a26f9-102">SYNOPSIS</span></span>
<span data-ttu-id="a26f9-103">Hämtar information om antecknings böcker på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="a26f9-103">Gets information about notebooks in a workspace.</span></span>

## <span data-ttu-id="a26f9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a26f9-104">SYNTAX</span></span>

### <span data-ttu-id="a26f9-105">GetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="a26f9-105">GetByName (Default)</span></span>
```
Get-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a26f9-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="a26f9-106">GetByObject</span></span>
```
Get-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a26f9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a26f9-107">DESCRIPTION</span></span>
<span data-ttu-id="a26f9-108">Cmdleten **Get-AzSynapseNotebook** hämtar information om antecknings böcker på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="a26f9-108">The **Get-AzSynapseNotebook** cmdlet gets information about notebooks in a workspace.</span></span> <span data-ttu-id="a26f9-109">Om du anger namnet på en antecknings bok får cmdleten information om den antecknings boken.</span><span class="sxs-lookup"><span data-stu-id="a26f9-109">If you specify the name of a notebook, the cmdlet gets information about that notebook.</span></span> <span data-ttu-id="a26f9-110">Om du inte anger ett namn får cmdleten information om alla antecknings böcker i arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="a26f9-110">If you do not specify a name, the cmdlet gets information about all notebooks in the workspace.</span></span>

## <span data-ttu-id="a26f9-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a26f9-111">EXAMPLES</span></span>

### <span data-ttu-id="a26f9-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a26f9-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace | Format-Table

WorkspaceName    Properties                                         Name
-------------    ----------                                         --
ContosoWorkspace Microsoft.Azure.Commands.Synapse.Models.PSNotebook ContosoNotebook1
ContosoWorkspace Microsoft.Azure.Commands.Synapse.Models.PSNotebook ContosoNotebook2
```

<span data-ttu-id="a26f9-113">Hämtar en lista över alla antecknings böcker i arbets ytans ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a26f9-113">Gets a list of all notebooks in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="a26f9-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a26f9-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="a26f9-115">Hämtar en enskild antecknings bok med namnet ContosoNotebook i arbets ytans ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a26f9-115">Gets a single notebook called ContosoNotebook in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="a26f9-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="a26f9-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="a26f9-117">Hämtar en enskild antecknings bok som heter ContosoNotebook i arbets ytan ContosoWorkspace via pipeline.</span><span class="sxs-lookup"><span data-stu-id="a26f9-117">Gets a single notebook called ContosoNotebook in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="a26f9-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a26f9-118">PARAMETERS</span></span>

### <span data-ttu-id="a26f9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a26f9-119">-DefaultProfile</span></span>
<span data-ttu-id="a26f9-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a26f9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a26f9-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="a26f9-121">-Name</span></span>
<span data-ttu-id="a26f9-122">Namnet på antecknings boken.</span><span class="sxs-lookup"><span data-stu-id="a26f9-122">The notebook name.</span></span>

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

### <span data-ttu-id="a26f9-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a26f9-123">-WorkspaceName</span></span>
<span data-ttu-id="a26f9-124">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="a26f9-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a26f9-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a26f9-125">-WorkspaceObject</span></span>
<span data-ttu-id="a26f9-126">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="a26f9-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a26f9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a26f9-127">CommonParameters</span></span>
<span data-ttu-id="a26f9-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a26f9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a26f9-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a26f9-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a26f9-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a26f9-130">INPUTS</span></span>

### <span data-ttu-id="a26f9-131">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a26f9-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a26f9-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a26f9-132">OUTPUTS</span></span>

### <span data-ttu-id="a26f9-133">Microsoft. Azure. commands. Synapse. Models. PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="a26f9-133">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="a26f9-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a26f9-134">NOTES</span></span>

## <span data-ttu-id="a26f9-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a26f9-135">RELATED LINKS</span></span>
