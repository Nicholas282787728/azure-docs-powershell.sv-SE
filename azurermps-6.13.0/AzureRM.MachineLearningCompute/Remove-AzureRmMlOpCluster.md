---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/remove-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
ms.openlocfilehash: 5619b9ca4e7f5593a20baf04951d0d5594b31215
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574834"
---
# <span data-ttu-id="0f7ea-101">Remove-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="0f7ea-101">Remove-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="0f7ea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0f7ea-102">SYNOPSIS</span></span>
<span data-ttu-id="0f7ea-103">Tar bort ett operationalization-kluster.</span><span class="sxs-lookup"><span data-stu-id="0f7ea-103">Removes an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f7ea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0f7ea-104">SYNTAX</span></span>

### <span data-ttu-id="0f7ea-105">RemoveByNameAndResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="0f7ea-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-IncludeAllResources]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f7ea-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="0f7ea-106">RemoveByInputObject</span></span>
```
Remove-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-IncludeAllResources]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f7ea-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="0f7ea-107">RemoveByResourceId</span></span>
```
Remove-AzureRmMlOpCluster -ResourceId <String> [-IncludeAllResources]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f7ea-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0f7ea-108">DESCRIPTION</span></span>
<span data-ttu-id="0f7ea-109">Tar bort ett operationalization-kluster.</span><span class="sxs-lookup"><span data-stu-id="0f7ea-109">Removes an operationalization cluster.</span></span> <span data-ttu-id="0f7ea-110">Vissa resurser som är kopplade till klustret kanske inte tas bort.</span><span class="sxs-lookup"><span data-stu-id="0f7ea-110">Some resources associated with the cluster might not all be removed.</span></span> <span data-ttu-id="0f7ea-111">Tjänsten Azure Container tar till exempel bort, men de tillhör ande datorerna är inte det.</span><span class="sxs-lookup"><span data-stu-id="0f7ea-111">For example, the Azure container service will get removed, but the associated VMs do not.</span></span> <span data-ttu-id="0f7ea-112">Lagrings kontot, behållar registret och program insikter tas inte bort för diagnostikinformation.</span><span class="sxs-lookup"><span data-stu-id="0f7ea-112">The storage account, container registry, and application insights are not removed for diagnostic information.</span></span>

## <span data-ttu-id="0f7ea-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0f7ea-113">EXAMPLES</span></span>

### <span data-ttu-id="0f7ea-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0f7ea-114">Example 1</span></span>
```
PS C:\> Remove-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="0f7ea-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="0f7ea-115">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster | Remove-AzureRmMlOpCluster
```

## <span data-ttu-id="0f7ea-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0f7ea-116">PARAMETERS</span></span>

### <span data-ttu-id="0f7ea-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f7ea-117">-DefaultProfile</span></span>
<span data-ttu-id="0f7ea-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0f7ea-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f7ea-119">-IncludeAllResources</span><span class="sxs-lookup"><span data-stu-id="0f7ea-119">-IncludeAllResources</span></span>
<span data-ttu-id="0f7ea-120">Tar bort alla resurser som har skapats med klustret.</span><span class="sxs-lookup"><span data-stu-id="0f7ea-120">Removes all resources that were created with the cluster.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f7ea-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f7ea-121">-InputObject</span></span>
<span data-ttu-id="0f7ea-122">Operationalization.</span><span class="sxs-lookup"><span data-stu-id="0f7ea-122">The operationalization cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: RemoveByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f7ea-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="0f7ea-123">-Name</span></span>
<span data-ttu-id="0f7ea-124">Namnet på operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="0f7ea-124">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f7ea-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f7ea-125">-ResourceGroupName</span></span>
<span data-ttu-id="0f7ea-126">Namnet på resurs gruppen för operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="0f7ea-126">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f7ea-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f7ea-127">-ResourceId</span></span>
<span data-ttu-id="0f7ea-128">Azure Resource ID för operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="0f7ea-128">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f7ea-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0f7ea-129">-Confirm</span></span>
<span data-ttu-id="0f7ea-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0f7ea-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f7ea-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f7ea-131">-WhatIf</span></span>
<span data-ttu-id="0f7ea-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0f7ea-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f7ea-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0f7ea-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f7ea-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f7ea-134">CommonParameters</span></span>
<span data-ttu-id="0f7ea-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f7ea-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f7ea-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f7ea-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f7ea-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0f7ea-137">INPUTS</span></span>

### <span data-ttu-id="0f7ea-138">Microsoft. Azure. commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="0f7ea-138">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="0f7ea-139">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0f7ea-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="0f7ea-140">System. String</span><span class="sxs-lookup"><span data-stu-id="0f7ea-140">System.String</span></span>

## <span data-ttu-id="0f7ea-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0f7ea-141">OUTPUTS</span></span>

### <span data-ttu-id="0f7ea-142">System. Void</span><span class="sxs-lookup"><span data-stu-id="0f7ea-142">System.Void</span></span>

## <span data-ttu-id="0f7ea-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0f7ea-143">NOTES</span></span>

## <span data-ttu-id="0f7ea-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0f7ea-144">RELATED LINKS</span></span>