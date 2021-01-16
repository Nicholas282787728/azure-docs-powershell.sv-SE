---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
ms.openlocfilehash: 87627738967a5c3174020932e5c9e7b996980ee9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397304"
---
# <span data-ttu-id="a5a37-101">Get-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="a5a37-101">Get-AzSynapseDataFlow</span></span>

## <span data-ttu-id="a5a37-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a5a37-102">SYNOPSIS</span></span>
<span data-ttu-id="a5a37-103">Hämtar information om data flöden i arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="a5a37-103">Gets information about data flows in workspace.</span></span>

## <span data-ttu-id="a5a37-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a5a37-104">SYNTAX</span></span>

### <span data-ttu-id="a5a37-105">GetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="a5a37-105">GetByName (Default)</span></span>
```
Get-AzSynapseDataFlow -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a5a37-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="a5a37-106">GetByObject</span></span>
```
Get-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5a37-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a5a37-107">DESCRIPTION</span></span>
<span data-ttu-id="a5a37-108">Cmdleten **Get-AzSynapseDataFlow** hämtar information om data flöden i arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="a5a37-108">The **Get-AzSynapseDataFlow** cmdlet gets information about data flows in workspace.</span></span>
<span data-ttu-id="a5a37-109">Om du anger namnet på ett data flöde får denna cmdlet information om det data flödet.</span><span class="sxs-lookup"><span data-stu-id="a5a37-109">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="a5a37-110">Om du inte anger ett namn hämtas den här cmdleten information om alla data flöden i arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="a5a37-110">If you do not specify a name, this cmdlet gets information about all the data flows in the workspace.</span></span>

## <span data-ttu-id="a5a37-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a5a37-111">EXAMPLES</span></span>

### <span data-ttu-id="a5a37-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a5a37-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="a5a37-113">Det här kommandot får information om alla data flöden i arbets ytan med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a5a37-113">This command gets information about all data flows in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="a5a37-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a5a37-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow
```

<span data-ttu-id="a5a37-115">Med det här kommandot får du information om data flödet med namnet ContosoDataFlow i arbets ytan med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a5a37-115">This command gets information about the data flow named ContosoDataFlow in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="a5a37-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a5a37-116">PARAMETERS</span></span>

### <span data-ttu-id="a5a37-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5a37-117">-DefaultProfile</span></span>
<span data-ttu-id="a5a37-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a5a37-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5a37-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="a5a37-119">-Name</span></span>
<span data-ttu-id="a5a37-120">Data flödes namn.</span><span class="sxs-lookup"><span data-stu-id="a5a37-120">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFlowName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a37-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a5a37-121">-WorkspaceName</span></span>
<span data-ttu-id="a5a37-122">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="a5a37-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a5a37-123">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a5a37-123">-WorkspaceObject</span></span>
<span data-ttu-id="a5a37-124">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="a5a37-124">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a5a37-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5a37-125">CommonParameters</span></span>
<span data-ttu-id="a5a37-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5a37-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5a37-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5a37-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5a37-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a5a37-128">INPUTS</span></span>

### <span data-ttu-id="a5a37-129">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a5a37-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a5a37-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a5a37-130">OUTPUTS</span></span>

### <span data-ttu-id="a5a37-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="a5a37-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="a5a37-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a5a37-132">NOTES</span></span>

## <span data-ttu-id="a5a37-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a5a37-133">RELATED LINKS</span></span>
