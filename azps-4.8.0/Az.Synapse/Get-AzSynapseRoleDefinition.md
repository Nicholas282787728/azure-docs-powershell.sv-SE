---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
ms.openlocfilehash: f2ac7efad3c08a351e515eccbe519306a89f06a9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258452"
---
# <span data-ttu-id="3f4ca-101">Get-AzSynapseRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="3f4ca-101">Get-AzSynapseRoleDefinition</span></span>

## <span data-ttu-id="3f4ca-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3f4ca-102">SYNOPSIS</span></span>
<span data-ttu-id="3f4ca-103">Hämtar en Synapse analys.</span><span class="sxs-lookup"><span data-stu-id="3f4ca-103">Gets a Synapse Analytics role definition.</span></span>

## <span data-ttu-id="3f4ca-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3f4ca-104">SYNTAX</span></span>

### <span data-ttu-id="3f4ca-105">GetByWorkspaceNameAndIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3f4ca-105">GetByWorkspaceNameAndIdParameterSet (Default)</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Id <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f4ca-106">GetByWorkspaceNameAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f4ca-106">GetByWorkspaceNameAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f4ca-107">GetByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f4ca-107">GetByWorkspaceObjectAndIdParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> -Id <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f4ca-108">GetByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f4ca-108">GetByWorkspaceObjectAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f4ca-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3f4ca-109">DESCRIPTION</span></span>
<span data-ttu-id="3f4ca-110">Cmdleten **Get-AzSynapseRoleDefinition** hämtar en Azure Synapse Analytics-roll.</span><span class="sxs-lookup"><span data-stu-id="3f4ca-110">The **Get-AzSynapseRoleDefinition** cmdlet gets an Azure Synapse Analytics Role Definition.</span></span>
<span data-ttu-id="3f4ca-111">Om du inte anger ett rollnamn eller ett roll-ID får denna cmdlet alla roll definitioner.</span><span class="sxs-lookup"><span data-stu-id="3f4ca-111">If you do not specify a role name or a role Id, this cmdlet gets all role definitions.</span></span>

## <span data-ttu-id="3f4ca-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3f4ca-112">EXAMPLES</span></span>

### <span data-ttu-id="3f4ca-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3f4ca-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="3f4ca-114">Det här kommandot får alla roll definitioner under en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="3f4ca-114">This command gets all role definitions under a workspace.</span></span>

### <span data-ttu-id="3f4ca-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="3f4ca-115">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace -Name ContosoRole
```

<span data-ttu-id="3f4ca-116">Det här kommandot får roll definitionen under arbets ytans ContosoWorkspace med namnet ContosoRole.</span><span class="sxs-lookup"><span data-stu-id="3f4ca-116">This command gets the role definition under workspace ContosoWorkspace with name ContosoRole.</span></span>

### <span data-ttu-id="3f4ca-117">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="3f4ca-117">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseRoleDefinition
```

<span data-ttu-id="3f4ca-118">Det här kommandot får alla roll definitioner under en arbets yta via pipeline.</span><span class="sxs-lookup"><span data-stu-id="3f4ca-118">This command gets all role definitions under a workspace through pipeline.</span></span>

## <span data-ttu-id="3f4ca-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3f4ca-119">PARAMETERS</span></span>

### <span data-ttu-id="3f4ca-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f4ca-120">-DefaultProfile</span></span>
<span data-ttu-id="3f4ca-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3f4ca-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f4ca-122">-ID</span><span class="sxs-lookup"><span data-stu-id="3f4ca-122">-Id</span></span>
<span data-ttu-id="3f4ca-123">ID för rollen som tilldelats huvudobjektet.</span><span class="sxs-lookup"><span data-stu-id="3f4ca-123">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceObjectAndIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f4ca-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="3f4ca-124">-Name</span></span>
<span data-ttu-id="3f4ca-125">Namn på den roll som tilldelats huvudobjektet.</span><span class="sxs-lookup"><span data-stu-id="3f4ca-125">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet, GetByWorkspaceObjectAndNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f4ca-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3f4ca-126">-WorkspaceName</span></span>
<span data-ttu-id="3f4ca-127">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="3f4ca-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f4ca-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3f4ca-128">-WorkspaceObject</span></span>
<span data-ttu-id="3f4ca-129">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="3f4ca-129">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f4ca-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f4ca-130">CommonParameters</span></span>
<span data-ttu-id="3f4ca-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f4ca-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f4ca-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f4ca-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f4ca-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3f4ca-133">INPUTS</span></span>

### <span data-ttu-id="3f4ca-134">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3f4ca-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="3f4ca-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3f4ca-135">OUTPUTS</span></span>

### <span data-ttu-id="3f4ca-136">Microsoft. Azure. commands. Synapse. Models. PSSynapseRole</span><span class="sxs-lookup"><span data-stu-id="3f4ca-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseRole</span></span>

## <span data-ttu-id="3f4ca-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3f4ca-137">NOTES</span></span>

## <span data-ttu-id="3f4ca-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3f4ca-138">RELATED LINKS</span></span>
