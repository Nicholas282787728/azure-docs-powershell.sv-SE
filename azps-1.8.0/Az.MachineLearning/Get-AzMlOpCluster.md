---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlOpCluster.md
ms.openlocfilehash: 24400b7a2c882cef81d818c5f5b94fca4235ec83
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915897"
---
# <span data-ttu-id="52059-101">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="52059-101">Get-AzMlOpCluster</span></span>

## <span data-ttu-id="52059-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="52059-102">SYNOPSIS</span></span>
<span data-ttu-id="52059-103">Hämtar ett operationalization.</span><span class="sxs-lookup"><span data-stu-id="52059-103">Gets an operationalization cluster object.</span></span>

## <span data-ttu-id="52059-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="52059-104">SYNTAX</span></span>

### <span data-ttu-id="52059-105">GetByName</span><span class="sxs-lookup"><span data-stu-id="52059-105">GetByName</span></span>
```
Get-AzMlOpCluster -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="52059-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="52059-106">GetByResourceGroup</span></span>
```
Get-AzMlOpCluster [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52059-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="52059-107">DESCRIPTION</span></span>
<span data-ttu-id="52059-108">Hämtar ett operationalization-kluster objekt efter namn eller resurs grupp eller efter abonnemang.</span><span class="sxs-lookup"><span data-stu-id="52059-108">Gets an operationalization cluster object by name, or by resource group, or by subscription.</span></span>

## <span data-ttu-id="52059-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="52059-109">EXAMPLES</span></span>

### <span data-ttu-id="52059-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="52059-110">Example 1</span></span>
```
PS C:\> Get-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="52059-111">Hämtar ett specifikt operationalization-kluster efter namn.</span><span class="sxs-lookup"><span data-stu-id="52059-111">Gets a specific operationalization cluster by name.</span></span>

### <span data-ttu-id="52059-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="52059-112">Example 2</span></span>
```
PS C:\> Get-AzMlOpCluster -ResourceGroupName my-group
```

<span data-ttu-id="52059-113">Hämtar alla operationalization-kluster i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="52059-113">Gets all the operationalization clusters in a resource group.</span></span>

### <span data-ttu-id="52059-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="52059-114">Example 3</span></span>
```
PS C:\> Get-AzMlOpCluster
```

<span data-ttu-id="52059-115">Hämtar alla operationalization-kluster i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="52059-115">Gets all the operationalization clusters in a subscription.</span></span>

## <span data-ttu-id="52059-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="52059-116">PARAMETERS</span></span>

### <span data-ttu-id="52059-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52059-117">-DefaultProfile</span></span>
<span data-ttu-id="52059-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="52059-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52059-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="52059-119">-Name</span></span>
<span data-ttu-id="52059-120">Namnet på operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="52059-120">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="52059-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52059-121">-ResourceGroupName</span></span>
<span data-ttu-id="52059-122">Namnet på resurs gruppen för operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="52059-122">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="52059-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52059-123">CommonParameters</span></span>
<span data-ttu-id="52059-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52059-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52059-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52059-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52059-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="52059-126">INPUTS</span></span>

### <span data-ttu-id="52059-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="52059-127">None</span></span>

## <span data-ttu-id="52059-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="52059-128">OUTPUTS</span></span>

### <span data-ttu-id="52059-129">Microsoft. Azure. commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="52059-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="52059-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="52059-130">NOTES</span></span>

## <span data-ttu-id="52059-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="52059-131">RELATED LINKS</span></span>
