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
ms.locfileid: "93743682"
---
# <span data-ttu-id="34303-101">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="34303-101">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>

## <span data-ttu-id="34303-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="34303-102">SYNOPSIS</span></span>
<span data-ttu-id="34303-103">Kontrollerar om det finns uppdateringar för de system tjänster som är associerade med ett operationalization-kluster.</span><span class="sxs-lookup"><span data-stu-id="34303-103">Checks if there are updates available for the system services associated with an operationalization cluster.</span></span>

## <span data-ttu-id="34303-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="34303-104">SYNTAX</span></span>

### <span data-ttu-id="34303-105">TestByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="34303-105">TestByNameAndResourceGroup</span></span>
```
Test-AzMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34303-106">TestByInputObject</span><span class="sxs-lookup"><span data-stu-id="34303-106">TestByInputObject</span></span>
```
Test-AzMlOpClusterSystemServicesUpdateAvailability -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34303-107">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="34303-107">TestByResourceId</span></span>
```
Test-AzMlOpClusterSystemServicesUpdateAvailability -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34303-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="34303-108">DESCRIPTION</span></span>
<span data-ttu-id="34303-109">System tjänster tar emot uppdateringar oberoende av operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="34303-109">System services receive updates independently from the operationalization cluster.</span></span> <span data-ttu-id="34303-110">Med den här cmdleten får användaren veta om Invoke-AzMlOpClusterSystemServicesUpdate.</span><span class="sxs-lookup"><span data-stu-id="34303-110">Using this cmdlet will let the user know if Invoke-AzMlOpClusterSystemServicesUpdate.</span></span>

## <span data-ttu-id="34303-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="34303-111">EXAMPLES</span></span>

### <span data-ttu-id="34303-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="34303-112">Example 1</span></span>
```
PS C:\> Test-AzMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="34303-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="34303-113">Example 2</span></span>
```
PS C:\> Get-AzMlOpCluster | Test-AzMlOpClusterSystemServicesUpdateAvailability
```

### <span data-ttu-id="34303-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="34303-114">Example 3</span></span>
```
PS C:\> Find-AzResource -ResourceType Microsoft.MachineLearningCompute/operationalizationClusters | Test-AzMlOpClusterSystemServicesUpdateAvailability
```

## <span data-ttu-id="34303-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="34303-115">PARAMETERS</span></span>

### <span data-ttu-id="34303-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34303-116">-DefaultProfile</span></span>
<span data-ttu-id="34303-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="34303-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34303-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34303-118">-InputObject</span></span>
<span data-ttu-id="34303-119">Operationalization.</span><span class="sxs-lookup"><span data-stu-id="34303-119">The operationalization cluster object.</span></span>

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

### <span data-ttu-id="34303-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="34303-120">-Name</span></span>
<span data-ttu-id="34303-121">Namnet på operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="34303-121">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="34303-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34303-122">-ResourceGroupName</span></span>
<span data-ttu-id="34303-123">Namnet på resurs gruppen för operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="34303-123">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="34303-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="34303-124">-ResourceId</span></span>
<span data-ttu-id="34303-125">Azure Resource ID för operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="34303-125">The Azure resource id for the operationalization cluster.</span></span>

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

### <span data-ttu-id="34303-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34303-126">CommonParameters</span></span>
<span data-ttu-id="34303-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34303-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34303-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34303-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34303-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="34303-129">INPUTS</span></span>

### <span data-ttu-id="34303-130">Microsoft. Azure. commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="34303-130">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="34303-131">System. String</span><span class="sxs-lookup"><span data-stu-id="34303-131">System.String</span></span>

## <span data-ttu-id="34303-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="34303-132">OUTPUTS</span></span>

### <span data-ttu-id="34303-133">Microsoft. Azure. commands. MachineLearningCompute. Models. PSCheckSystemServicesUpdatesAvailableResponse</span><span class="sxs-lookup"><span data-stu-id="34303-133">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSCheckSystemServicesUpdatesAvailableResponse</span></span>

## <span data-ttu-id="34303-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="34303-134">NOTES</span></span>

## <span data-ttu-id="34303-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="34303-135">RELATED LINKS</span></span>
