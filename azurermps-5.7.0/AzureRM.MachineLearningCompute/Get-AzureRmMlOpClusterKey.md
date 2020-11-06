---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/get-azurermmlopclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
ms.openlocfilehash: cdf8c04a3d3b3b9fc50e571642bc14352d976b84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581124"
---
# <span data-ttu-id="1ff07-101">Get-AzureRmMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="1ff07-101">Get-AzureRmMlOpClusterKey</span></span>

## <span data-ttu-id="1ff07-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1ff07-102">SYNOPSIS</span></span>
<span data-ttu-id="1ff07-103">Hämtar åtkomst nycklar som är kopplade till ett operationalization-kluster.</span><span class="sxs-lookup"><span data-stu-id="1ff07-103">Gets the access keys associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ff07-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1ff07-104">SYNTAX</span></span>

### <span data-ttu-id="1ff07-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1ff07-105">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1ff07-106">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="1ff07-106">GetByInputObject</span></span>
```
Get-AzureRmMlOpClusterKey -InputObject <PSOperationalizationCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1ff07-107">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1ff07-107">GetByResourceId</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ff07-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1ff07-108">DESCRIPTION</span></span>
<span data-ttu-id="1ff07-109">Nycklarna för lagrings kontot, behållar registret och andra tjänster som är kopplade till operationalization-klustret returneras inte när du hämtar kluster egenskaperna.</span><span class="sxs-lookup"><span data-stu-id="1ff07-109">The keys for the storage account, container registry, and other services associated with the operationalization cluster are not returned when getting the cluster properties.</span></span> <span data-ttu-id="1ff07-110">Ett specifikt samtal att hämta nycklar måste göras sedan de är känslig information.</span><span class="sxs-lookup"><span data-stu-id="1ff07-110">A specific call to retrieve the keys must be made since they are sensitive information.</span></span>

## <span data-ttu-id="1ff07-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1ff07-111">EXAMPLES</span></span>

### <span data-ttu-id="1ff07-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1ff07-112">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="1ff07-113">Returnerar hemliga nycklar för de tjänster som är kopplade till operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="1ff07-113">Returns the secret keys for the services associated with the operationalization cluster.</span></span>

## <span data-ttu-id="1ff07-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1ff07-114">PARAMETERS</span></span>

### <span data-ttu-id="1ff07-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ff07-115">-DefaultProfile</span></span>
<span data-ttu-id="1ff07-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1ff07-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ff07-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ff07-117">-InputObject</span></span>
<span data-ttu-id="1ff07-118">Operationalization.</span><span class="sxs-lookup"><span data-stu-id="1ff07-118">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: GetByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ff07-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="1ff07-119">-Name</span></span>
<span data-ttu-id="1ff07-120">Namnet på operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="1ff07-120">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ff07-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ff07-121">-ResourceGroupName</span></span>
<span data-ttu-id="1ff07-122">Namnet på resurs gruppen för operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="1ff07-122">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ff07-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ff07-123">-ResourceId</span></span>
<span data-ttu-id="1ff07-124">Azure Resource ID för operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="1ff07-124">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ff07-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ff07-125">CommonParameters</span></span>
<span data-ttu-id="1ff07-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ff07-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ff07-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ff07-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ff07-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1ff07-128">INPUTS</span></span>

### <span data-ttu-id="1ff07-129">Microsoft. Azure. commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="1ff07-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="1ff07-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1ff07-130">System.String</span></span>

## <span data-ttu-id="1ff07-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1ff07-131">OUTPUTS</span></span>

### <span data-ttu-id="1ff07-132">Microsoft. Azure. commands. MachineLearningCompute. Models. PSOperationalizationClusterCredentials</span><span class="sxs-lookup"><span data-stu-id="1ff07-132">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationClusterCredentials</span></span>

## <span data-ttu-id="1ff07-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1ff07-133">NOTES</span></span>

## <span data-ttu-id="1ff07-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1ff07-134">RELATED LINKS</span></span>

