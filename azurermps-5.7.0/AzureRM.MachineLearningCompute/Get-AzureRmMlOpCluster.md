---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/get-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
ms.openlocfilehash: 0e9eecf16a26be5367df5d8ad8b45a40e0050da3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755870"
---
# <span data-ttu-id="bebe1-101">Get-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="bebe1-101">Get-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="bebe1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bebe1-102">SYNOPSIS</span></span>
<span data-ttu-id="bebe1-103">Hämtar ett operationalization.</span><span class="sxs-lookup"><span data-stu-id="bebe1-103">Gets an operationalization cluster object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bebe1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bebe1-104">SYNTAX</span></span>

### <span data-ttu-id="bebe1-105">GetByName</span><span class="sxs-lookup"><span data-stu-id="bebe1-105">GetByName</span></span>
```
Get-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bebe1-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bebe1-106">GetByResourceGroup</span></span>
```
Get-AzureRmMlOpCluster [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bebe1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bebe1-107">DESCRIPTION</span></span>
<span data-ttu-id="bebe1-108">Hämtar ett operationalization-kluster objekt efter namn eller resurs grupp eller efter abonnemang.</span><span class="sxs-lookup"><span data-stu-id="bebe1-108">Gets an operationalization cluster object by name, or by resource group, or by subscription.</span></span>

## <span data-ttu-id="bebe1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bebe1-109">EXAMPLES</span></span>

### <span data-ttu-id="bebe1-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bebe1-110">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="bebe1-111">Hämtar ett specifikt operationalization-kluster efter namn.</span><span class="sxs-lookup"><span data-stu-id="bebe1-111">Gets a specific operationalization cluster by name.</span></span>

### <span data-ttu-id="bebe1-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="bebe1-112">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group
```

<span data-ttu-id="bebe1-113">Hämtar alla operationalization-kluster i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="bebe1-113">Gets all the operationalization clusters in a resource group.</span></span>

### <span data-ttu-id="bebe1-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="bebe1-114">Example 3</span></span>
```
PS C:\> Get-AzureRmMlOpCluster
```

<span data-ttu-id="bebe1-115">Hämtar alla operationalization-kluster i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="bebe1-115">Gets all the operationalization clusters in a subscription.</span></span>

## <span data-ttu-id="bebe1-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bebe1-116">PARAMETERS</span></span>

### <span data-ttu-id="bebe1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bebe1-117">-DefaultProfile</span></span>
<span data-ttu-id="bebe1-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bebe1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bebe1-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="bebe1-119">-Name</span></span>
<span data-ttu-id="bebe1-120">Namnet på operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="bebe1-120">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bebe1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bebe1-121">-ResourceGroupName</span></span>
<span data-ttu-id="bebe1-122">Namnet på resurs gruppen för operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="bebe1-122">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetByResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bebe1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bebe1-123">CommonParameters</span></span>
<span data-ttu-id="bebe1-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bebe1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bebe1-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bebe1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bebe1-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bebe1-126">INPUTS</span></span>

### <span data-ttu-id="bebe1-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="bebe1-127">None</span></span>

## <span data-ttu-id="bebe1-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bebe1-128">OUTPUTS</span></span>

### <span data-ttu-id="bebe1-129">Microsoft. Azure. commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="bebe1-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="bebe1-130">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. MachineLearningCompute. Models. PSOperationalizationCluster, Microsoft. Azure. commands. MachineLearningCompute, version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="bebe1-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster, Microsoft.Azure.Commands.MachineLearningCompute, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="bebe1-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bebe1-131">NOTES</span></span>

## <span data-ttu-id="bebe1-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bebe1-132">RELATED LINKS</span></span>

