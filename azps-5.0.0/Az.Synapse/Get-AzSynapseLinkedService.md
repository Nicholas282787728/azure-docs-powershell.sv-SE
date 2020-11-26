---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseLinkedService.md
ms.openlocfilehash: d7f494b6ba943214106363a5b7dfe4dfb5cdd877
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324192"
---
# <span data-ttu-id="a04ab-101">Get-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="a04ab-101">Get-AzSynapseLinkedService</span></span>

## <span data-ttu-id="a04ab-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a04ab-102">SYNOPSIS</span></span>
<span data-ttu-id="a04ab-103">Hämtar information om de länkade tjänsterna på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="a04ab-103">Gets information about linked services in workspace.</span></span>

## <span data-ttu-id="a04ab-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a04ab-104">SYNTAX</span></span>

### <span data-ttu-id="a04ab-105">GetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="a04ab-105">GetByName (Default)</span></span>
```
Get-AzSynapseLinkedService -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a04ab-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="a04ab-106">GetByObject</span></span>
```
Get-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a04ab-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a04ab-107">DESCRIPTION</span></span>
<span data-ttu-id="a04ab-108">Cmdleten **Get-AzSynapseLinkedService** hämtar information om de länkade tjänsterna i arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="a04ab-108">The **Get-AzSynapseLinkedService** cmdlet gets information about linked services in workspace.</span></span>
<span data-ttu-id="a04ab-109">Om du anger namnet på en länkad tjänst får denna cmdlet information om den länkade tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a04ab-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="a04ab-110">Om du inte anger ett namn hämtas den här cmdleten information om alla de länkade tjänsterna i arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="a04ab-110">If you do not specify a name, this cmdlet gets information about all the linked services in the workspace.</span></span>

## <span data-ttu-id="a04ab-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a04ab-111">EXAMPLES</span></span>

### <span data-ttu-id="a04ab-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a04ab-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="a04ab-113">Det här kommandot får information om alla länkade tjänster i arbets ytan med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a04ab-113">This command gets information about all linked services in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="a04ab-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a04ab-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
```

<span data-ttu-id="a04ab-115">Med det här kommandot får du information om den länkade tjänsten som heter ContosoLinkedService i arbets ytan med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a04ab-115">This command gets information about the linked service named ContosoLinkedService in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="a04ab-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="a04ab-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseLinkedService -Name ContosoLinkedService
```

<span data-ttu-id="a04ab-117">Med det här kommandot får du information om den länkade tjänsten som heter ContosoLinkedService i arbets ytan ContosoWorkspace via pipeline.</span><span class="sxs-lookup"><span data-stu-id="a04ab-117">This command gets information about the linked service named ContosoLinkedService in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="a04ab-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a04ab-118">PARAMETERS</span></span>

### <span data-ttu-id="a04ab-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a04ab-119">-DefaultProfile</span></span>
<span data-ttu-id="a04ab-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a04ab-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a04ab-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="a04ab-121">-Name</span></span>
<span data-ttu-id="a04ab-122">Namnet på den länkade tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a04ab-122">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a04ab-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a04ab-123">-WorkspaceName</span></span>
<span data-ttu-id="a04ab-124">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="a04ab-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a04ab-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a04ab-125">-WorkspaceObject</span></span>
<span data-ttu-id="a04ab-126">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="a04ab-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a04ab-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a04ab-127">CommonParameters</span></span>
<span data-ttu-id="a04ab-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a04ab-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a04ab-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a04ab-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a04ab-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a04ab-130">INPUTS</span></span>

### <span data-ttu-id="a04ab-131">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a04ab-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a04ab-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a04ab-132">OUTPUTS</span></span>

### <span data-ttu-id="a04ab-133">Microsoft. Azure. commands. Synapse. Models. PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="a04ab-133">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="a04ab-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a04ab-134">NOTES</span></span>

## <span data-ttu-id="a04ab-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a04ab-135">RELATED LINKS</span></span>