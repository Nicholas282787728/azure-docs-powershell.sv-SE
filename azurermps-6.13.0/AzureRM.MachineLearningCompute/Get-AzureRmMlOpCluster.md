---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/get-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
ms.openlocfilehash: 746dde8dd3460add5eb6a20e4a9b771873dac0e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576935"
---
# <span data-ttu-id="6b9da-101">Get-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="6b9da-101">Get-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="6b9da-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6b9da-102">SYNOPSIS</span></span>
<span data-ttu-id="6b9da-103">Hämtar ett operationalization.</span><span class="sxs-lookup"><span data-stu-id="6b9da-103">Gets an operationalization cluster object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b9da-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6b9da-104">SYNTAX</span></span>

### <span data-ttu-id="6b9da-105">GetByName</span><span class="sxs-lookup"><span data-stu-id="6b9da-105">GetByName</span></span>
```
Get-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6b9da-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6b9da-106">GetByResourceGroup</span></span>
```
Get-AzureRmMlOpCluster [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6b9da-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6b9da-107">DESCRIPTION</span></span>
<span data-ttu-id="6b9da-108">Hämtar ett operationalization-kluster objekt efter namn eller resurs grupp eller efter abonnemang.</span><span class="sxs-lookup"><span data-stu-id="6b9da-108">Gets an operationalization cluster object by name, or by resource group, or by subscription.</span></span>

## <span data-ttu-id="6b9da-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6b9da-109">EXAMPLES</span></span>

### <span data-ttu-id="6b9da-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6b9da-110">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="6b9da-111">Hämtar ett specifikt operationalization-kluster efter namn.</span><span class="sxs-lookup"><span data-stu-id="6b9da-111">Gets a specific operationalization cluster by name.</span></span>

### <span data-ttu-id="6b9da-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="6b9da-112">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group
```

<span data-ttu-id="6b9da-113">Hämtar alla operationalization-kluster i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="6b9da-113">Gets all the operationalization clusters in a resource group.</span></span>

### <span data-ttu-id="6b9da-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="6b9da-114">Example 3</span></span>
```
PS C:\> Get-AzureRmMlOpCluster
```

<span data-ttu-id="6b9da-115">Hämtar alla operationalization-kluster i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="6b9da-115">Gets all the operationalization clusters in a subscription.</span></span>

## <span data-ttu-id="6b9da-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6b9da-116">PARAMETERS</span></span>

### <span data-ttu-id="6b9da-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b9da-117">-DefaultProfile</span></span>
<span data-ttu-id="6b9da-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6b9da-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b9da-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="6b9da-119">-Name</span></span>
<span data-ttu-id="6b9da-120">Namnet på operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="6b9da-120">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b9da-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b9da-121">-ResourceGroupName</span></span>
<span data-ttu-id="6b9da-122">Namnet på resurs gruppen för operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="6b9da-122">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b9da-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b9da-123">CommonParameters</span></span>
<span data-ttu-id="6b9da-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b9da-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b9da-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b9da-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b9da-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6b9da-126">INPUTS</span></span>

### <span data-ttu-id="6b9da-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="6b9da-127">None</span></span>

## <span data-ttu-id="6b9da-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6b9da-128">OUTPUTS</span></span>

### <span data-ttu-id="6b9da-129">Microsoft. Azure. commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="6b9da-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="6b9da-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6b9da-130">NOTES</span></span>

## <span data-ttu-id="6b9da-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6b9da-131">RELATED LINKS</span></span>
