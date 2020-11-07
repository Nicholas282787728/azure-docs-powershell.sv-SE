---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
ms.openlocfilehash: 067fdf88b7a7b29007f81ab26590ffaa542ac7e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756590"
---
# <span data-ttu-id="19843-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="19843-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span></span>

## <span data-ttu-id="19843-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="19843-102">SYNOPSIS</span></span>
<span data-ttu-id="19843-103">Kontrollerar om det finns uppdateringar för de system tjänster som är associerade med ett operationalization-kluster.</span><span class="sxs-lookup"><span data-stu-id="19843-103">Checks if there are updates available for the system services associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19843-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="19843-104">SYNTAX</span></span>

### <span data-ttu-id="19843-105">Testa uppdaterings tillgänglighet från cmdlet-indataparametrar.</span><span class="sxs-lookup"><span data-stu-id="19843-105">Test for update availability from cmdlet input parameters.</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName <String> -Name <String>
```

### <span data-ttu-id="19843-106">Testa uppdaterings tillgänglighet från en OperationalizationCluster.</span><span class="sxs-lookup"><span data-stu-id="19843-106">Test for update availability from an OperationalizationCluster instance definition.</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -InputObject <PSOperationalizationCluster>
```

### <span data-ttu-id="19843-107">Testa uppdaterings tillgänglighet från ett Azure replan-ID.</span><span class="sxs-lookup"><span data-stu-id="19843-107">Test for update availability from an Azure resouce id.</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceId <String>
```

## <span data-ttu-id="19843-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="19843-108">DESCRIPTION</span></span>
<span data-ttu-id="19843-109">System tjänster tar emot uppdateringar oberoende av operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="19843-109">System services receive updates independently from the operationalization cluster.</span></span> <span data-ttu-id="19843-110">Med den här cmdleten får användaren veta om Invoke-AzureRmMlOpClusterSystemServicesUpdate.</span><span class="sxs-lookup"><span data-stu-id="19843-110">Using this cmdlet will let the user know if Invoke-AzureRmMlOpClusterSystemServicesUpdate.</span></span>

## <span data-ttu-id="19843-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="19843-111">EXAMPLES</span></span>

### <span data-ttu-id="19843-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="19843-112">Example 1</span></span>
```
PS C:\> Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="19843-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="19843-113">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

### <span data-ttu-id="19843-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="19843-114">Example 3</span></span>
```
PS C:\> Find-AzureRmResource -ResourceType Microsoft.MachineLearningCompute/operationalizationClusters | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

## <span data-ttu-id="19843-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="19843-115">PARAMETERS</span></span>

### <span data-ttu-id="19843-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19843-116">-InputObject</span></span>
<span data-ttu-id="19843-117">Operationalization.</span><span class="sxs-lookup"><span data-stu-id="19843-117">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Test for update availability from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19843-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="19843-118">-Name</span></span>
<span data-ttu-id="19843-119">Namnet på operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="19843-119">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Test for update availability from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19843-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19843-120">-ResourceGroupName</span></span>
<span data-ttu-id="19843-121">Namnet på resurs gruppen för operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="19843-121">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Test for update availability from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19843-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="19843-122">-ResourceId</span></span>
<span data-ttu-id="19843-123">Azure Resource ID för operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="19843-123">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Test for update availability from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="19843-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="19843-124">INPUTS</span></span>

### <span data-ttu-id="19843-125">Microsoft. Azure. commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="19843-125">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
### <span data-ttu-id="19843-126">System. String</span><span class="sxs-lookup"><span data-stu-id="19843-126">System.String</span></span>


## <span data-ttu-id="19843-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="19843-127">OUTPUTS</span></span>

### <span data-ttu-id="19843-128">Microsoft. Azure. commands. MachineLearningCompute. Models. PSCheckSystemServicesUpdatesAvailableResponse</span><span class="sxs-lookup"><span data-stu-id="19843-128">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSCheckSystemServicesUpdatesAvailableResponse</span></span>


## <span data-ttu-id="19843-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="19843-129">NOTES</span></span>

## <span data-ttu-id="19843-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="19843-130">RELATED LINKS</span></span>

