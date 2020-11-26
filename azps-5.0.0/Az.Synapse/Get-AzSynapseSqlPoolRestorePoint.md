---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: f9f921368f55b5901657ca4e366927a284302745
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263475"
---
# <span data-ttu-id="c7aeb-101">Get-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="c7aeb-101">Get-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="c7aeb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c7aeb-102">SYNOPSIS</span></span>
<span data-ttu-id="c7aeb-103">Hämtar de distinkta återställnings punkter från vilka en Synapse Analytics SQL-pool kan återställas.</span><span class="sxs-lookup"><span data-stu-id="c7aeb-103">Retrieves the distinct restore points from which a Synapse Analytics SQL pool can be restored.</span></span>

## <span data-ttu-id="c7aeb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c7aeb-104">SYNTAX</span></span>

### <span data-ttu-id="c7aeb-105">GetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c7aeb-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7aeb-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7aeb-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7aeb-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7aeb-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -InputObject <PSSynapseSqlPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c7aeb-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7aeb-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c7aeb-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c7aeb-109">DESCRIPTION</span></span>
<span data-ttu-id="c7aeb-110">Cmdleten **Get-AzSynapseSqlPoolRestorePoint** hämtar de distinkta återställnings punkter som en Azure SYNAPSE Analytics SQL-pool kan återställas från.</span><span class="sxs-lookup"><span data-stu-id="c7aeb-110">The **Get-AzSynapseSqlPoolRestorePoint** cmdlet retrieves the distinct restore points that an Azure Synapse Analytics SQL pool can be restored from.</span></span>

## <span data-ttu-id="c7aeb-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c7aeb-111">EXAMPLES</span></span>

### <span data-ttu-id="c7aeb-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c7aeb-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolRestorePoint -WorkspaceName -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="c7aeb-113">Det här kommandot returnerar alla tillgängliga återställnings punkter för Azure Synapse Analytics SQL-poolen med namnet ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="c7aeb-113">This command returns all available restore points for the Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

## <span data-ttu-id="c7aeb-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c7aeb-114">PARAMETERS</span></span>

### <span data-ttu-id="c7aeb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7aeb-115">-DefaultProfile</span></span>
<span data-ttu-id="c7aeb-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c7aeb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7aeb-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7aeb-117">-InputObject</span></span>
<span data-ttu-id="c7aeb-118">Objekt i SQL-pool, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="c7aeb-118">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7aeb-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="c7aeb-119">-Name</span></span>
<span data-ttu-id="c7aeb-120">Namn på SQL-poolen Synapse.</span><span class="sxs-lookup"><span data-stu-id="c7aeb-120">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7aeb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7aeb-121">-ResourceGroupName</span></span>
<span data-ttu-id="c7aeb-122">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="c7aeb-122">Resource group name.</span></span>

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

### <span data-ttu-id="c7aeb-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7aeb-123">-ResourceId</span></span>
<span data-ttu-id="c7aeb-124">Resurs-ID för Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="c7aeb-124">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="c7aeb-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c7aeb-125">-WorkspaceName</span></span>
<span data-ttu-id="c7aeb-126">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="c7aeb-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="c7aeb-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c7aeb-127">-WorkspaceObject</span></span>
<span data-ttu-id="c7aeb-128">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="c7aeb-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="c7aeb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7aeb-129">CommonParameters</span></span>
<span data-ttu-id="c7aeb-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7aeb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7aeb-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7aeb-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7aeb-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c7aeb-132">INPUTS</span></span>

### <span data-ttu-id="c7aeb-133">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c7aeb-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="c7aeb-134">Microsoft. Azure. commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="c7aeb-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="c7aeb-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c7aeb-135">OUTPUTS</span></span>

### <span data-ttu-id="c7aeb-136">Microsoft. Azure. Management. Synapse. Models. RestorePoint</span><span class="sxs-lookup"><span data-stu-id="c7aeb-136">Microsoft.Azure.Management.Synapse.Models.RestorePoint</span></span>

## <span data-ttu-id="c7aeb-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c7aeb-137">NOTES</span></span>

## <span data-ttu-id="c7aeb-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c7aeb-138">RELATED LINKS</span></span>