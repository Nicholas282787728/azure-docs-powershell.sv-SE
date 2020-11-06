---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
ms.openlocfilehash: 4dfa855bba7318e85eb855e35227070a55d4ed73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582356"
---
# <span data-ttu-id="bb7bf-101">Get-AzureRmMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="bb7bf-101">Get-AzureRmMlOpClusterKey</span></span>

## <span data-ttu-id="bb7bf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bb7bf-102">SYNOPSIS</span></span>
<span data-ttu-id="bb7bf-103">Hämtar åtkomst nycklar som är kopplade till ett operationalization-kluster.</span><span class="sxs-lookup"><span data-stu-id="bb7bf-103">Gets the access keys associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb7bf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bb7bf-104">SYNTAX</span></span>

### <span data-ttu-id="bb7bf-105">Skaffa operationalization för klustret från cmdlet input Parameters.</span><span class="sxs-lookup"><span data-stu-id="bb7bf-105">Get operationalization cluster's keys from cmdlet input parameters.</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceGroupName <String> -Name <String>
```

### <span data-ttu-id="bb7bf-106">Skaffa operationalization för klustret från en OperationalizationCluster.</span><span class="sxs-lookup"><span data-stu-id="bb7bf-106">Get operationalization cluster's keys from an OperationalizationCluster instance definition.</span></span>
```
Get-AzureRmMlOpClusterKey -Cluster <PSOperationalizationCluster>
```

### <span data-ttu-id="bb7bf-107">Skaffa operationalization kluster nycklar från ett Azure Resource-ID.</span><span class="sxs-lookup"><span data-stu-id="bb7bf-107">Get operationalization cluster's keys from an Azure resource id.</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceId <String>
```

## <span data-ttu-id="bb7bf-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bb7bf-108">DESCRIPTION</span></span>
<span data-ttu-id="bb7bf-109">Nycklarna för lagrings kontot, behållar registret och andra tjänster som är kopplade till operationalization-klustret returneras inte när du hämtar kluster egenskaperna.</span><span class="sxs-lookup"><span data-stu-id="bb7bf-109">The keys for the storage account, container registry, and other services associated with the operationalization cluster are not returned when getting the cluster properties.</span></span> <span data-ttu-id="bb7bf-110">Ett specifikt samtal att hämta nycklar måste göras sedan de är känslig information.</span><span class="sxs-lookup"><span data-stu-id="bb7bf-110">A specific call to retrieve the keys must be made since they are sensitive information.</span></span>

## <span data-ttu-id="bb7bf-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bb7bf-111">EXAMPLES</span></span>

### <span data-ttu-id="bb7bf-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bb7bf-112">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="bb7bf-113">Returnerar hemliga nycklar för de tjänster som är kopplade till operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="bb7bf-113">Returns the secret keys for the services associated with the operationalization cluster.</span></span>

## <span data-ttu-id="bb7bf-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bb7bf-114">PARAMETERS</span></span>

### <span data-ttu-id="bb7bf-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb7bf-115">-InputObject</span></span>
<span data-ttu-id="bb7bf-116">Operationalization.</span><span class="sxs-lookup"><span data-stu-id="bb7bf-116">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Get operationalization cluster's keys from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb7bf-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="bb7bf-117">-Name</span></span>
<span data-ttu-id="bb7bf-118">Namnet på operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="bb7bf-118">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb7bf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb7bf-119">-ResourceGroupName</span></span>
<span data-ttu-id="bb7bf-120">Namnet på resurs gruppen för operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="bb7bf-120">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb7bf-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb7bf-121">-ResourceId</span></span>
<span data-ttu-id="bb7bf-122">Azure Resource ID för operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="bb7bf-122">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="bb7bf-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bb7bf-123">INPUTS</span></span>

### <span data-ttu-id="bb7bf-124">Microsoft. Azure. commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="bb7bf-124">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="bb7bf-125">System. String</span><span class="sxs-lookup"><span data-stu-id="bb7bf-125">System.String</span></span>


## <span data-ttu-id="bb7bf-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bb7bf-126">OUTPUTS</span></span>

### <span data-ttu-id="bb7bf-127">Microsoft. Azure. commands. MachineLearningCompute. Models. PSOperationalizationClusterCredentials</span><span class="sxs-lookup"><span data-stu-id="bb7bf-127">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationClusterCredentials</span></span>


## <span data-ttu-id="bb7bf-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bb7bf-128">NOTES</span></span>

## <span data-ttu-id="bb7bf-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bb7bf-129">RELATED LINKS</span></span>

