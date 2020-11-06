---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
ms.openlocfilehash: fc89ff40c36fc444eec23089288849aa5ffe592c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585468"
---
# <span data-ttu-id="87baf-101">Update-AzureRmMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="87baf-101">Update-AzureRmMlOpClusterSystemService</span></span>

## <span data-ttu-id="87baf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="87baf-102">SYNOPSIS</span></span>
<span data-ttu-id="87baf-103">Startar en uppdatering av operationalization kluster system tjänster.</span><span class="sxs-lookup"><span data-stu-id="87baf-103">Starts an update on the operationalization cluster's system services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87baf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="87baf-104">SYNTAX</span></span>

### <span data-ttu-id="87baf-105">Starta en system tjänst uppdatering från cmdlet input Parameters.</span><span class="sxs-lookup"><span data-stu-id="87baf-105">Start a system services update from cmdlet input parameters.</span></span>
```
Update-AzureRmMlOpClusterSystemService -ResourceGroupName <String> -Name <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="87baf-106">Starta en system tjänst uppdatering från en PSOperationalizationCluster.</span><span class="sxs-lookup"><span data-stu-id="87baf-106">Start a system services update from an PSOperationalizationCluster instance definition.</span></span>
```
Update-AzureRmMlOpClusterSystemService -InputObject <PSOperationalizationCluster> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="87baf-107">Starta en system tjänst uppdatering från ett Azure representations-ID.</span><span class="sxs-lookup"><span data-stu-id="87baf-107">Start a system services update from an Azure resouce id.</span></span>
```
Update-AzureRmMlOpClusterSystemService -ResourceId <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="87baf-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="87baf-108">DESCRIPTION</span></span>
<span data-ttu-id="87baf-109">System tjänsterna kan uppdateras oberoende av operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="87baf-109">The system services can be updated independently from the operationalization cluster.</span></span> <span data-ttu-id="87baf-110">Använd denna cmdlet för att starta en uppdatering av system tjänsterna.</span><span class="sxs-lookup"><span data-stu-id="87baf-110">To start an update on the system services use this cmdlet.</span></span> <span data-ttu-id="87baf-111">Om det inte finns någon uppdatering kommer en uppdatering att påbörjas och kommer att återföras.</span><span class="sxs-lookup"><span data-stu-id="87baf-111">If no update is available an update will still be started and will return successfully.</span></span> <span data-ttu-id="87baf-112">När uppdateringen är klar rapporteras den när den startas, är färdig och om den lyckades.</span><span class="sxs-lookup"><span data-stu-id="87baf-112">Once the update is finished it reports when it started, finished, and if it was successful.</span></span>

## <span data-ttu-id="87baf-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="87baf-113">EXAMPLES</span></span>

### <span data-ttu-id="87baf-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="87baf-114">Example 1</span></span>
```
PS C:\> Update-AzureRmMlOpClusterSystemService -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="87baf-115">Startar en system tjänst uppdatering i angivet kluster.</span><span class="sxs-lookup"><span data-stu-id="87baf-115">Starts a system services update on the specified cluster.</span></span> 

## <span data-ttu-id="87baf-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="87baf-116">PARAMETERS</span></span>

### <span data-ttu-id="87baf-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87baf-117">-InputObject</span></span>
<span data-ttu-id="87baf-118">Operationalization.</span><span class="sxs-lookup"><span data-stu-id="87baf-118">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Start a system services update from an PSOperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87baf-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="87baf-119">-Confirm</span></span>
<span data-ttu-id="87baf-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="87baf-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87baf-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="87baf-121">-Name</span></span>
<span data-ttu-id="87baf-122">Namnet på operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="87baf-122">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Start a system services update from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87baf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87baf-123">-ResourceGroupName</span></span>
<span data-ttu-id="87baf-124">Namnet på resurs gruppen för operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="87baf-124">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Start a system services update from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87baf-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87baf-125">-ResourceId</span></span>
<span data-ttu-id="87baf-126">Azure Resource ID för operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="87baf-126">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Start a system services update from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87baf-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87baf-127">-WhatIf</span></span>
<span data-ttu-id="87baf-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="87baf-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87baf-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="87baf-129">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="87baf-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="87baf-130">INPUTS</span></span>

### <span data-ttu-id="87baf-131">Microsoft. Azure. commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="87baf-131">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
### <span data-ttu-id="87baf-132">System. String</span><span class="sxs-lookup"><span data-stu-id="87baf-132">System.String</span></span>


## <span data-ttu-id="87baf-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="87baf-133">OUTPUTS</span></span>

### <span data-ttu-id="87baf-134">Microsoft. Azure. commands. MachineLearningCompute. Models. PSUpdateSystemServicesResponse</span><span class="sxs-lookup"><span data-stu-id="87baf-134">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSUpdateSystemServicesResponse</span></span>


## <span data-ttu-id="87baf-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="87baf-135">NOTES</span></span>

## <span data-ttu-id="87baf-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="87baf-136">RELATED LINKS</span></span>

