---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/test-azmlopclustersystemservicesupdateavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Test-AzMlOpClusterSystemServicesUpdateAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Test-AzMlOpClusterSystemServicesUpdateAvailability.md
ms.openlocfilehash: d05f8b746dbd212c834e3554639340fa6075c216
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915846"
---
# <span data-ttu-id="5fc9a-101">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="5fc9a-101">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>

## <span data-ttu-id="5fc9a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5fc9a-102">SYNOPSIS</span></span>
<span data-ttu-id="5fc9a-103">Kontrollerar om det finns uppdateringar för de system tjänster som är associerade med ett operationalization-kluster.</span><span class="sxs-lookup"><span data-stu-id="5fc9a-103">Checks if there are updates available for the system services associated with an operationalization cluster.</span></span>

## <span data-ttu-id="5fc9a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5fc9a-104">SYNTAX</span></span>

### <span data-ttu-id="5fc9a-105">TestByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5fc9a-105">TestByNameAndResourceGroup</span></span>
```
Test-AzMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5fc9a-106">TestByInputObject</span><span class="sxs-lookup"><span data-stu-id="5fc9a-106">TestByInputObject</span></span>
```
Test-AzMlOpClusterSystemServicesUpdateAvailability -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5fc9a-107">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="5fc9a-107">TestByResourceId</span></span>
```
Test-AzMlOpClusterSystemServicesUpdateAvailability -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5fc9a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5fc9a-108">DESCRIPTION</span></span>
<span data-ttu-id="5fc9a-109">System tjänster tar emot uppdateringar oberoende av operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="5fc9a-109">System services receive updates independently from the operationalization cluster.</span></span> <span data-ttu-id="5fc9a-110">Med den här cmdleten får användaren veta om Invoke-AzMlOpClusterSystemServicesUpdate.</span><span class="sxs-lookup"><span data-stu-id="5fc9a-110">Using this cmdlet will let the user know if Invoke-AzMlOpClusterSystemServicesUpdate.</span></span>

## <span data-ttu-id="5fc9a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5fc9a-111">EXAMPLES</span></span>

### <span data-ttu-id="5fc9a-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5fc9a-112">Example 1</span></span>
```
PS C:\> Test-AzMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="5fc9a-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="5fc9a-113">Example 2</span></span>
```
PS C:\> Get-AzMlOpCluster | Test-AzMlOpClusterSystemServicesUpdateAvailability
```

### <span data-ttu-id="5fc9a-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="5fc9a-114">Example 3</span></span>
```
PS C:\> Find-AzResource -ResourceType Microsoft.MachineLearningCompute/operationalizationClusters | Test-AzMlOpClusterSystemServicesUpdateAvailability
```

## <span data-ttu-id="5fc9a-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5fc9a-115">PARAMETERS</span></span>

### <span data-ttu-id="5fc9a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fc9a-116">-DefaultProfile</span></span>
<span data-ttu-id="5fc9a-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5fc9a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fc9a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5fc9a-118">-InputObject</span></span>
<span data-ttu-id="5fc9a-119">Operationalization.</span><span class="sxs-lookup"><span data-stu-id="5fc9a-119">The operationalization cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: TestByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5fc9a-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="5fc9a-120">-Name</span></span>
<span data-ttu-id="5fc9a-121">Namnet på operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="5fc9a-121">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fc9a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fc9a-122">-ResourceGroupName</span></span>
<span data-ttu-id="5fc9a-123">Namnet på resurs gruppen för operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="5fc9a-123">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fc9a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5fc9a-124">-ResourceId</span></span>
<span data-ttu-id="5fc9a-125">Azure Resource ID för operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="5fc9a-125">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fc9a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fc9a-126">CommonParameters</span></span>
<span data-ttu-id="5fc9a-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fc9a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fc9a-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fc9a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fc9a-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5fc9a-129">INPUTS</span></span>

### <span data-ttu-id="5fc9a-130">Microsoft. Azure. commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="5fc9a-130">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="5fc9a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="5fc9a-131">System.String</span></span>

## <span data-ttu-id="5fc9a-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5fc9a-132">OUTPUTS</span></span>

### <span data-ttu-id="5fc9a-133">Microsoft. Azure. commands. MachineLearningCompute. Models. PSCheckSystemServicesUpdatesAvailableResponse</span><span class="sxs-lookup"><span data-stu-id="5fc9a-133">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSCheckSystemServicesUpdatesAvailableResponse</span></span>

## <span data-ttu-id="5fc9a-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5fc9a-134">NOTES</span></span>

## <span data-ttu-id="5fc9a-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5fc9a-135">RELATED LINKS</span></span>
