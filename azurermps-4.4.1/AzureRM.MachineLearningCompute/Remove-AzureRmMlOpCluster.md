---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
ms.openlocfilehash: 63e401c09a2d224b53d260855990198a409d4846
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756337"
---
# <span data-ttu-id="62897-101">Remove-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="62897-101">Remove-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="62897-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="62897-102">SYNOPSIS</span></span>
<span data-ttu-id="62897-103">Tar bort ett operationalization-kluster.</span><span class="sxs-lookup"><span data-stu-id="62897-103">Removes an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62897-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="62897-104">SYNTAX</span></span>

### <span data-ttu-id="62897-105">Ta bort ett operationalization-kluster från en cmdlet input Parameters.</span><span class="sxs-lookup"><span data-stu-id="62897-105">Remove an operationalization cluster from cmdlet input parameters.</span></span>
```
Remove-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="62897-106">Ta bort ett operationalization-kluster från en OperationalizationCluster-instans.</span><span class="sxs-lookup"><span data-stu-id="62897-106">Remove an operationalization cluster from an OperationalizationCluster instance definition.</span></span>
```
Remove-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="62897-107">Ta bort ett operationalization-kluster från ett Azure reresurspool-ID.</span><span class="sxs-lookup"><span data-stu-id="62897-107">Remove an operationalization cluster from an Azure resouce id.</span></span>
```
Remove-AzureRmMlOpCluster -ResourceId <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="62897-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="62897-108">DESCRIPTION</span></span>
<span data-ttu-id="62897-109">Tar bort ett operationalization-kluster.</span><span class="sxs-lookup"><span data-stu-id="62897-109">Removes an operationalization cluster.</span></span> <span data-ttu-id="62897-110">Vissa resurser som är kopplade till klustret kanske inte tas bort.</span><span class="sxs-lookup"><span data-stu-id="62897-110">Some resources associated with the cluster might not all be removed.</span></span> <span data-ttu-id="62897-111">Tjänsten Azure Container tar till exempel bort, men de tillhör ande datorerna är inte det.</span><span class="sxs-lookup"><span data-stu-id="62897-111">For example, the Azure container service will get removed, but the associated VMs do not.</span></span> <span data-ttu-id="62897-112">Lagrings kontot, behållar registret och program insikter tas inte bort för diagnostikinformation.</span><span class="sxs-lookup"><span data-stu-id="62897-112">The storage account, container registry, and application insights are not removed for diagnostic information.</span></span>

## <span data-ttu-id="62897-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="62897-113">EXAMPLES</span></span>

### <span data-ttu-id="62897-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="62897-114">Example 1</span></span>
```
PS C:\> Remove-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="62897-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="62897-115">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster | Remove-AzureRmMlOpCluster 
```

## <span data-ttu-id="62897-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="62897-116">PARAMETERS</span></span>

### <span data-ttu-id="62897-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62897-117">-InputObject</span></span>
<span data-ttu-id="62897-118">Operationalization.</span><span class="sxs-lookup"><span data-stu-id="62897-118">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Remove an operationalization cluster from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62897-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="62897-119">-Confirm</span></span>
<span data-ttu-id="62897-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="62897-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62897-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="62897-121">-Name</span></span>
<span data-ttu-id="62897-122">Namnet på operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="62897-122">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Remove an operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62897-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62897-123">-ResourceGroupName</span></span>
<span data-ttu-id="62897-124">Namnet på resurs gruppen för operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="62897-124">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Remove an operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62897-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62897-125">-ResourceId</span></span>
<span data-ttu-id="62897-126">Azure Resource ID för operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="62897-126">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Remove an operationalization cluster from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62897-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62897-127">-WhatIf</span></span>
<span data-ttu-id="62897-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="62897-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62897-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="62897-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="62897-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="62897-130">INPUTS</span></span>

### <span data-ttu-id="62897-131">Microsoft. Azure. commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="62897-131">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
### <span data-ttu-id="62897-132">System. String</span><span class="sxs-lookup"><span data-stu-id="62897-132">System.String</span></span>


## <span data-ttu-id="62897-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="62897-133">OUTPUTS</span></span>

### <span data-ttu-id="62897-134">System. Void</span><span class="sxs-lookup"><span data-stu-id="62897-134">System.Void</span></span>


## <span data-ttu-id="62897-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="62897-135">NOTES</span></span>

## <span data-ttu-id="62897-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="62897-136">RELATED LINKS</span></span>

