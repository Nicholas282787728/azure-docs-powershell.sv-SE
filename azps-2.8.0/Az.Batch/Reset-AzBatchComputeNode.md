---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A202537B-D292-4822-A0B9-27A6A20621D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/reset-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Reset-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Reset-AzBatchComputeNode.md
ms.openlocfilehash: 530db3d911d0300e1bd587cd953fb357ca810c9c
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93928565"
---
# <span data-ttu-id="f98dc-101">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="f98dc-101">Reset-AzBatchComputeNode</span></span>

## <span data-ttu-id="f98dc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f98dc-102">SYNOPSIS</span></span>
<span data-ttu-id="f98dc-103">Operativ systemet installeras om på angiven datornod.</span><span class="sxs-lookup"><span data-stu-id="f98dc-103">Reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="f98dc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f98dc-104">SYNTAX</span></span>

### <span data-ttu-id="f98dc-105">ID (standard)</span><span class="sxs-lookup"><span data-stu-id="f98dc-105">Id (Default)</span></span>
```
Reset-AzBatchComputeNode [-PoolId] <String> [-Id] <String> [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f98dc-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f98dc-106">InputObject</span></span>
```
Reset-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>] [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f98dc-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f98dc-107">DESCRIPTION</span></span>
<span data-ttu-id="f98dc-108">Cmdleten **Reset-AzBatchComputeNode** installerar om operativ systemet på angiven datornod.</span><span class="sxs-lookup"><span data-stu-id="f98dc-108">The **Reset-AzBatchComputeNode** cmdlet reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="f98dc-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f98dc-109">EXAMPLES</span></span>

### <span data-ttu-id="f98dc-110">Exempel 1: återbilden av en nod</span><span class="sxs-lookup"><span data-stu-id="f98dc-110">Example 1: Reimage a node</span></span>
```
PS C:\>Reset-AzBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="f98dc-111">Det här kommandot återgör om Compute-noden med ID: t "TVM-3257026573_2-20150813t200938z" i poolen med namnet nonpool.</span><span class="sxs-lookup"><span data-stu-id="f98dc-111">This command reimages the compute node with ID "tvm-3257026573_2-20150813t200938z" in the pool named MyPool.</span></span>
<span data-ttu-id="f98dc-112">Använd Get-AzBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="f98dc-112">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="f98dc-113">Exempel 2: återpå alla noder i en pool</span><span class="sxs-lookup"><span data-stu-id="f98dc-113">Example 2: Reimage all nodes in a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Reset-AzBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="f98dc-114">Det här kommandot återgör varje datornod i poolen med namnet min pool.</span><span class="sxs-lookup"><span data-stu-id="f98dc-114">This command reimages every compute node in the pool named MyPool.</span></span>

## <span data-ttu-id="f98dc-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f98dc-115">PARAMETERS</span></span>

### <span data-ttu-id="f98dc-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f98dc-116">-BatchContext</span></span>
<span data-ttu-id="f98dc-117">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f98dc-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f98dc-118">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f98dc-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f98dc-119">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="f98dc-119">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f98dc-120">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="f98dc-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f98dc-121">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="f98dc-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f98dc-122">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="f98dc-122">-ComputeNode</span></span>
<span data-ttu-id="f98dc-123">Anger det **PSComputeNode** -objekt som representerar Compute-noden som ska återbildas.</span><span class="sxs-lookup"><span data-stu-id="f98dc-123">Specifies the **PSComputeNode** object that represents the compute node to reimage.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f98dc-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f98dc-124">-DefaultProfile</span></span>
<span data-ttu-id="f98dc-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f98dc-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f98dc-126">-ID</span><span class="sxs-lookup"><span data-stu-id="f98dc-126">-Id</span></span>
<span data-ttu-id="f98dc-127">Anger ID för den datornod som ska återskrivas.</span><span class="sxs-lookup"><span data-stu-id="f98dc-127">Specifies the ID of the compute node to reimage.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f98dc-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="f98dc-128">-PoolId</span></span>
<span data-ttu-id="f98dc-129">Anger ID för den pool som innehåller noden Compute.</span><span class="sxs-lookup"><span data-stu-id="f98dc-129">Specifies the ID of the pool that contains the compute node.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f98dc-130">-ReimageOption</span><span class="sxs-lookup"><span data-stu-id="f98dc-130">-ReimageOption</span></span>
<span data-ttu-id="f98dc-131">Anger när du vill att noden ska visas igen och vad du kan göra med aktiviteterna.</span><span class="sxs-lookup"><span data-stu-id="f98dc-131">Specifies when to reimage the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="f98dc-132">Standardvärdet är köa.</span><span class="sxs-lookup"><span data-stu-id="f98dc-132">The default is Requeue.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeReimageOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f98dc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f98dc-133">CommonParameters</span></span>
<span data-ttu-id="f98dc-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f98dc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f98dc-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f98dc-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f98dc-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f98dc-136">INPUTS</span></span>

### <span data-ttu-id="f98dc-137">Microsoft.Azure.Commands.BatCH. Modeller. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="f98dc-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="f98dc-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f98dc-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f98dc-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f98dc-139">OUTPUTS</span></span>

### <span data-ttu-id="f98dc-140">System. Void</span><span class="sxs-lookup"><span data-stu-id="f98dc-140">System.Void</span></span>

## <span data-ttu-id="f98dc-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f98dc-141">NOTES</span></span>

## <span data-ttu-id="f98dc-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f98dc-142">RELATED LINKS</span></span>

[<span data-ttu-id="f98dc-143">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="f98dc-143">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="f98dc-144">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="f98dc-144">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)

[<span data-ttu-id="f98dc-145">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="f98dc-145">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


