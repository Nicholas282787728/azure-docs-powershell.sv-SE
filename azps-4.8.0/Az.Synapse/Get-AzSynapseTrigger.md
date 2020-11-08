---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTrigger.md
ms.openlocfilehash: 9e39d6458ca330909e500a45532d0a9d66f404af
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258946"
---
# <span data-ttu-id="0a4de-101">Get-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="0a4de-101">Get-AzSynapseTrigger</span></span>

## <span data-ttu-id="0a4de-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0a4de-102">SYNOPSIS</span></span>
<span data-ttu-id="0a4de-103">Hämtar information om utlösare på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="0a4de-103">Gets information about triggers in a workspace.</span></span>

## <span data-ttu-id="0a4de-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0a4de-104">SYNTAX</span></span>

### <span data-ttu-id="0a4de-105">GetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="0a4de-105">GetByName (Default)</span></span>
```
Get-AzSynapseTrigger -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0a4de-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="0a4de-106">GetByObject</span></span>
```
Get-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a4de-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0a4de-107">DESCRIPTION</span></span>
<span data-ttu-id="0a4de-108">Cmdleten **Get-AzSynapseTrigger** hämtar information om utlösare på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="0a4de-108">The **Get-AzSynapseTrigger** cmdlet gets information about triggers in a workspace.</span></span> <span data-ttu-id="0a4de-109">Om du anger namnet på en utlösare får cmdleten information om den utlösaren.</span><span class="sxs-lookup"><span data-stu-id="0a4de-109">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="0a4de-110">Om du inte anger ett namn får cmdleten information om alla utlösare i arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="0a4de-110">If you do not specify a name, the cmdlet gets information about all triggers in the workspace.</span></span>

## <span data-ttu-id="0a4de-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0a4de-111">EXAMPLES</span></span>

### <span data-ttu-id="0a4de-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0a4de-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="0a4de-113">Hämtar en lista över alla utlösare som har skapats i arbets ytans ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="0a4de-113">Gets a list of all triggers that have been created in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="0a4de-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="0a4de-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="0a4de-115">Hämtar en enskild utlösare som heter ContosoTrigger i arbets ytans ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="0a4de-115">Gets a single trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="0a4de-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="0a4de-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="0a4de-117">Hämtar en enda utlösare som heter ContosoTrigger i arbets ytans ContosoWorkspace via pipeline.</span><span class="sxs-lookup"><span data-stu-id="0a4de-117">Gets a single trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="0a4de-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0a4de-118">PARAMETERS</span></span>

### <span data-ttu-id="0a4de-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a4de-119">-DefaultProfile</span></span>
<span data-ttu-id="0a4de-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0a4de-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a4de-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="0a4de-121">-Name</span></span>
<span data-ttu-id="0a4de-122">Utlösarens namn.</span><span class="sxs-lookup"><span data-stu-id="0a4de-122">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a4de-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0a4de-123">-WorkspaceName</span></span>
<span data-ttu-id="0a4de-124">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="0a4de-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="0a4de-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0a4de-125">-WorkspaceObject</span></span>
<span data-ttu-id="0a4de-126">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="0a4de-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="0a4de-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a4de-127">CommonParameters</span></span>
<span data-ttu-id="0a4de-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a4de-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a4de-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a4de-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a4de-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0a4de-130">INPUTS</span></span>

### <span data-ttu-id="0a4de-131">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0a4de-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="0a4de-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0a4de-132">OUTPUTS</span></span>

### <span data-ttu-id="0a4de-133">Microsoft. Azure. commands. Synapse. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="0a4de-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="0a4de-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0a4de-134">NOTES</span></span>

## <span data-ttu-id="0a4de-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0a4de-135">RELATED LINKS</span></span>
