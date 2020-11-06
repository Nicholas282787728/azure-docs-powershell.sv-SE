---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/test-azurermmlopclustersystemservicesupdateavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
ms.openlocfilehash: 9f531b67d2dc3cc6010a7677c96dc4ecf10fb5a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577185"
---
# <span data-ttu-id="7be73-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="7be73-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span></span>

## <span data-ttu-id="7be73-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7be73-102">SYNOPSIS</span></span>
<span data-ttu-id="7be73-103">Kontrollerar om det finns uppdateringar för de system tjänster som är associerade med ett operationalization-kluster.</span><span class="sxs-lookup"><span data-stu-id="7be73-103">Checks if there are updates available for the system services associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7be73-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7be73-104">SYNTAX</span></span>

### <span data-ttu-id="7be73-105">TestByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7be73-105">TestByNameAndResourceGroup</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7be73-106">TestByInputObject</span><span class="sxs-lookup"><span data-stu-id="7be73-106">TestByInputObject</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7be73-107">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="7be73-107">TestByResourceId</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7be73-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7be73-108">DESCRIPTION</span></span>
<span data-ttu-id="7be73-109">System tjänster tar emot uppdateringar oberoende av operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="7be73-109">System services receive updates independently from the operationalization cluster.</span></span> <span data-ttu-id="7be73-110">Med den här cmdleten får användaren veta om Invoke-AzureRmMlOpClusterSystemServicesUpdate.</span><span class="sxs-lookup"><span data-stu-id="7be73-110">Using this cmdlet will let the user know if Invoke-AzureRmMlOpClusterSystemServicesUpdate.</span></span>

## <span data-ttu-id="7be73-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7be73-111">EXAMPLES</span></span>

### <span data-ttu-id="7be73-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7be73-112">Example 1</span></span>
```
PS C:\> Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="7be73-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="7be73-113">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

### <span data-ttu-id="7be73-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="7be73-114">Example 3</span></span>
```
PS C:\> Find-AzureRmResource -ResourceType Microsoft.MachineLearningCompute/operationalizationClusters | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

## <span data-ttu-id="7be73-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7be73-115">PARAMETERS</span></span>

### <span data-ttu-id="7be73-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7be73-116">-DefaultProfile</span></span>
<span data-ttu-id="7be73-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7be73-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7be73-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7be73-118">-InputObject</span></span>
<span data-ttu-id="7be73-119">Operationalization.</span><span class="sxs-lookup"><span data-stu-id="7be73-119">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: TestByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7be73-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="7be73-120">-Name</span></span>
<span data-ttu-id="7be73-121">Namnet på operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="7be73-121">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: TestByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7be73-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7be73-122">-ResourceGroupName</span></span>
<span data-ttu-id="7be73-123">Namnet på resurs gruppen för operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="7be73-123">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: TestByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7be73-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7be73-124">-ResourceId</span></span>
<span data-ttu-id="7be73-125">Azure Resource ID för operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="7be73-125">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: TestByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7be73-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7be73-126">CommonParameters</span></span>
<span data-ttu-id="7be73-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7be73-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7be73-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7be73-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7be73-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7be73-129">INPUTS</span></span>

### <span data-ttu-id="7be73-130">Microsoft. Azure. commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="7be73-130">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="7be73-131">System. String</span><span class="sxs-lookup"><span data-stu-id="7be73-131">System.String</span></span>

## <span data-ttu-id="7be73-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7be73-132">OUTPUTS</span></span>

### <span data-ttu-id="7be73-133">Microsoft. Azure. commands. MachineLearningCompute. Models. PSCheckSystemServicesUpdatesAvailableResponse</span><span class="sxs-lookup"><span data-stu-id="7be73-133">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSCheckSystemServicesUpdatesAvailableResponse</span></span>

## <span data-ttu-id="7be73-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7be73-134">NOTES</span></span>

## <span data-ttu-id="7be73-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7be73-135">RELATED LINKS</span></span>

