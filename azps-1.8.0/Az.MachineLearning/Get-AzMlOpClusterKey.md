---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlopclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlOpClusterKey.md
ms.openlocfilehash: d8b8a333b4d009ee1b40a8b4ddc6ed49850f1a11
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915890"
---
# <span data-ttu-id="0e298-101">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="0e298-101">Get-AzMlOpClusterKey</span></span>

## <span data-ttu-id="0e298-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0e298-102">SYNOPSIS</span></span>
<span data-ttu-id="0e298-103">Hämtar åtkomst nycklar som är kopplade till ett operationalization-kluster.</span><span class="sxs-lookup"><span data-stu-id="0e298-103">Gets the access keys associated with an operationalization cluster.</span></span>

## <span data-ttu-id="0e298-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0e298-104">SYNTAX</span></span>

### <span data-ttu-id="0e298-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0e298-105">GetByNameAndResourceGroup</span></span>
```
Get-AzMlOpClusterKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0e298-106">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="0e298-106">GetByInputObject</span></span>
```
Get-AzMlOpClusterKey -InputObject <PSOperationalizationCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0e298-107">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0e298-107">GetByResourceId</span></span>
```
Get-AzMlOpClusterKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e298-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0e298-108">DESCRIPTION</span></span>
<span data-ttu-id="0e298-109">Nycklarna för lagrings kontot, behållar registret och andra tjänster som är kopplade till operationalization-klustret returneras inte när du hämtar kluster egenskaperna.</span><span class="sxs-lookup"><span data-stu-id="0e298-109">The keys for the storage account, container registry, and other services associated with the operationalization cluster are not returned when getting the cluster properties.</span></span> <span data-ttu-id="0e298-110">Ett specifikt samtal att hämta nycklar måste göras sedan de är känslig information.</span><span class="sxs-lookup"><span data-stu-id="0e298-110">A specific call to retrieve the keys must be made since they are sensitive information.</span></span>

## <span data-ttu-id="0e298-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0e298-111">EXAMPLES</span></span>

### <span data-ttu-id="0e298-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0e298-112">Example 1</span></span>
```
PS C:\> Get-AzMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="0e298-113">Returnerar hemliga nycklar för de tjänster som är kopplade till operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="0e298-113">Returns the secret keys for the services associated with the operationalization cluster.</span></span>

## <span data-ttu-id="0e298-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0e298-114">PARAMETERS</span></span>

### <span data-ttu-id="0e298-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e298-115">-DefaultProfile</span></span>
<span data-ttu-id="0e298-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0e298-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e298-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0e298-117">-InputObject</span></span>
<span data-ttu-id="0e298-118">Operationalization.</span><span class="sxs-lookup"><span data-stu-id="0e298-118">The operationalization cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: GetByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e298-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="0e298-119">-Name</span></span>
<span data-ttu-id="0e298-120">Namnet på operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="0e298-120">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e298-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e298-121">-ResourceGroupName</span></span>
<span data-ttu-id="0e298-122">Namnet på resurs gruppen för operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="0e298-122">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e298-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e298-123">-ResourceId</span></span>
<span data-ttu-id="0e298-124">Azure Resource ID för operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="0e298-124">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e298-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e298-125">CommonParameters</span></span>
<span data-ttu-id="0e298-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e298-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e298-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e298-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e298-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0e298-128">INPUTS</span></span>

### <span data-ttu-id="0e298-129">Microsoft. Azure. commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="0e298-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="0e298-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0e298-130">System.String</span></span>

## <span data-ttu-id="0e298-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0e298-131">OUTPUTS</span></span>

### <span data-ttu-id="0e298-132">Microsoft. Azure. commands. MachineLearningCompute. Models. PSOperationalizationClusterCredentials</span><span class="sxs-lookup"><span data-stu-id="0e298-132">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationClusterCredentials</span></span>

## <span data-ttu-id="0e298-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0e298-133">NOTES</span></span>

## <span data-ttu-id="0e298-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0e298-134">RELATED LINKS</span></span>
