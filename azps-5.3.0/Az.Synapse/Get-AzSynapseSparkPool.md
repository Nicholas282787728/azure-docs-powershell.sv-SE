---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
ms.openlocfilehash: fd1dbcc2e70b4d44de0c105af2332a9e4836d3bc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424483"
---
# <span data-ttu-id="36e3a-101">Get-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="36e3a-101">Get-AzSynapseSparkPool</span></span>

## <span data-ttu-id="36e3a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="36e3a-102">SYNOPSIS</span></span>
<span data-ttu-id="36e3a-103">Hämtar en Synapse Analytics Spark-pool.</span><span class="sxs-lookup"><span data-stu-id="36e3a-103">Gets a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="36e3a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="36e3a-104">SYNTAX</span></span>

### <span data-ttu-id="36e3a-105">GetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="36e3a-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36e3a-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="36e3a-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkPool [-Name <String>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36e3a-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="36e3a-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSparkPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36e3a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="36e3a-108">DESCRIPTION</span></span>
<span data-ttu-id="36e3a-109">Cmdleten **Get-AzSynapseSparkPool** hämtar information om en Azure Synapse Analytics Spark-pool.</span><span class="sxs-lookup"><span data-stu-id="36e3a-109">The **Get-AzSynapseSparkPool** cmdlet gets information about an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="36e3a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="36e3a-110">EXAMPLES</span></span>

### <span data-ttu-id="36e3a-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="36e3a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="36e3a-112">Det här kommandot får alla Spark-pooler under en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="36e3a-112">This command gets all Spark pools under a workspace.</span></span>

### <span data-ttu-id="36e3a-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="36e3a-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="36e3a-114">Det här kommandot får Spark-poolen under arbets ytans ContosoWorkspace med namnet ContosoSparkPool.</span><span class="sxs-lookup"><span data-stu-id="36e3a-114">This command gets the Spark pool under workspace ContosoWorkspace with name ContosoSparkPool.</span></span>

### <span data-ttu-id="36e3a-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="36e3a-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSparkPool
```

<span data-ttu-id="36e3a-116">Det här kommandot får alla Spark-pooler under en arbets yta genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="36e3a-116">This command gets all Spark pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="36e3a-117">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="36e3a-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool"
```

<span data-ttu-id="36e3a-118">Det här kommandot får Spark-poolen med angivet resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="36e3a-118">This command gets the Spark pool with the specified resource ID.</span></span>

## <span data-ttu-id="36e3a-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="36e3a-119">PARAMETERS</span></span>

### <span data-ttu-id="36e3a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36e3a-120">-DefaultProfile</span></span>
<span data-ttu-id="36e3a-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="36e3a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36e3a-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="36e3a-122">-Name</span></span>
<span data-ttu-id="36e3a-123">Namn på Synapse Spark-pool.</span><span class="sxs-lookup"><span data-stu-id="36e3a-123">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: SparkPoolName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36e3a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36e3a-124">-ResourceGroupName</span></span>
<span data-ttu-id="36e3a-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="36e3a-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36e3a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36e3a-126">-ResourceId</span></span>
<span data-ttu-id="36e3a-127">Resurs-ID för Synapse Spark-pool.</span><span class="sxs-lookup"><span data-stu-id="36e3a-127">Resource identifier of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36e3a-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="36e3a-128">-WorkspaceName</span></span>
<span data-ttu-id="36e3a-129">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="36e3a-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36e3a-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="36e3a-130">-WorkspaceObject</span></span>
<span data-ttu-id="36e3a-131">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="36e3a-131">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36e3a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36e3a-132">CommonParameters</span></span>
<span data-ttu-id="36e3a-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36e3a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36e3a-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36e3a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36e3a-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="36e3a-135">INPUTS</span></span>

### <span data-ttu-id="36e3a-136">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="36e3a-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="36e3a-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="36e3a-137">OUTPUTS</span></span>

### <span data-ttu-id="36e3a-138">Microsoft. Azure. commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="36e3a-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="36e3a-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="36e3a-139">NOTES</span></span>

## <span data-ttu-id="36e3a-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="36e3a-140">RELATED LINKS</span></span>
