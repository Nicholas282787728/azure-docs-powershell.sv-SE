---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
ms.openlocfilehash: e37aff4f6f79a3aa0420c98811bc47b951bb4d3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581411"
---
# <span data-ttu-id="e9512-101">Get-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="e9512-101">Get-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="e9512-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e9512-102">SYNOPSIS</span></span>
<span data-ttu-id="e9512-103">Hämtar ett operationalization.</span><span class="sxs-lookup"><span data-stu-id="e9512-103">Gets an operationalization cluster object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9512-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e9512-104">SYNTAX</span></span>

```
Get-AzureRmMlOpCluster [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9512-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e9512-105">DESCRIPTION</span></span>
<span data-ttu-id="e9512-106">Hämtar ett operationalization-kluster objekt efter namn eller resurs grupp eller efter abonnemang.</span><span class="sxs-lookup"><span data-stu-id="e9512-106">Gets an operationalization cluster object by name, or by resource group, or by subscription.</span></span>

## <span data-ttu-id="e9512-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e9512-107">EXAMPLES</span></span>

### <span data-ttu-id="e9512-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e9512-108">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="e9512-109">Hämtar ett specifikt operationalization-kluster efter namn.</span><span class="sxs-lookup"><span data-stu-id="e9512-109">Gets a specific operationalization cluster by name.</span></span>

### <span data-ttu-id="e9512-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="e9512-110">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group
```

<span data-ttu-id="e9512-111">Hämtar alla operationalization-kluster i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="e9512-111">Gets all the operationalization clusters in a resource group.</span></span>

### <span data-ttu-id="e9512-112">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="e9512-112">Example 3</span></span>
```
PS C:\> Get-AzureRmMlOpCluster
```

<span data-ttu-id="e9512-113">Hämtar alla operationalization-kluster i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="e9512-113">Gets all the operationalization clusters in a subscription.</span></span>

## <span data-ttu-id="e9512-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e9512-114">PARAMETERS</span></span>

### <span data-ttu-id="e9512-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9512-115">-DefaultProfile</span></span>
<span data-ttu-id="e9512-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e9512-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9512-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="e9512-117">-Name</span></span>
<span data-ttu-id="e9512-118">Namnet på operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="e9512-118">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Get an operationalization cluster by its name.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9512-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9512-119">-ResourceGroupName</span></span>
<span data-ttu-id="e9512-120">Namnet på resurs gruppen för operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="e9512-120">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9512-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9512-121">CommonParameters</span></span>
<span data-ttu-id="e9512-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9512-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9512-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9512-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9512-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e9512-124">INPUTS</span></span>

### <span data-ttu-id="e9512-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="e9512-125">None</span></span>

## <span data-ttu-id="e9512-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e9512-126">OUTPUTS</span></span>

### <span data-ttu-id="e9512-127">Microsoft. Azure. commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="e9512-127">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="e9512-128">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. MachineLearningCompute. Models. PSOperationalizationCluster, Microsoft. Azure. commands. MachineLearningCompute, version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e9512-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster, Microsoft.Azure.Commands.MachineLearningCompute, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e9512-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e9512-129">NOTES</span></span>

## <span data-ttu-id="e9512-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e9512-130">RELATED LINKS</span></span>

