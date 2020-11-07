---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A202537B-D292-4822-A0B9-27A6A20621D4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Reset-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Reset-AzureBatchComputeNode.md
ms.openlocfilehash: b90a70bb6b4a8104597056715c75f5699db5a24e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756112"
---
# <span data-ttu-id="690f9-101">Reset-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="690f9-101">Reset-AzureBatchComputeNode</span></span>

## <span data-ttu-id="690f9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="690f9-102">SYNOPSIS</span></span>
<span data-ttu-id="690f9-103">Operativ systemet installeras om på angiven datornod.</span><span class="sxs-lookup"><span data-stu-id="690f9-103">Reinstalls the operating system on the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="690f9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="690f9-104">SYNTAX</span></span>

### <span data-ttu-id="690f9-105">ID (standard)</span><span class="sxs-lookup"><span data-stu-id="690f9-105">Id (Default)</span></span>
```
Reset-AzureBatchComputeNode [-PoolId] <String> [-Id] <String> [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="690f9-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="690f9-106">InputObject</span></span>
```
Reset-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>] [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="690f9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="690f9-107">DESCRIPTION</span></span>
<span data-ttu-id="690f9-108">Cmdleten **Reset-AzureBatchComputeNode** installerar om operativ systemet på angiven datornod.</span><span class="sxs-lookup"><span data-stu-id="690f9-108">The **Reset-AzureBatchComputeNode** cmdlet reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="690f9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="690f9-109">EXAMPLES</span></span>

### <span data-ttu-id="690f9-110">Exempel 1: återbilden av en nod</span><span class="sxs-lookup"><span data-stu-id="690f9-110">Example 1: Reimage a node</span></span>
```
PS C:\>Reset-AzureBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="690f9-111">Det här kommandot återgör om Compute-noden med ID: t "TVM-3257026573_2-20150813t200938z" i poolen med namnet nonpool.</span><span class="sxs-lookup"><span data-stu-id="690f9-111">This command reimages the compute node with ID "tvm-3257026573_2-20150813t200938z" in the pool named MyPool.</span></span>
<span data-ttu-id="690f9-112">Använd Get-AzureRmBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="690f9-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="690f9-113">Exempel 2: återpå alla noder i en pool</span><span class="sxs-lookup"><span data-stu-id="690f9-113">Example 2: Reimage all nodes in a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Reset-AzureBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="690f9-114">Det här kommandot återgör varje datornod i poolen med namnet min pool.</span><span class="sxs-lookup"><span data-stu-id="690f9-114">This command reimages every compute node in the pool named MyPool.</span></span>

## <span data-ttu-id="690f9-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="690f9-115">PARAMETERS</span></span>

### <span data-ttu-id="690f9-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="690f9-116">-BatchContext</span></span>
<span data-ttu-id="690f9-117">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="690f9-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="690f9-118">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="690f9-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="690f9-119">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="690f9-119">-ComputeNode</span></span>
<span data-ttu-id="690f9-120">Anger det **PSComputeNode** -objekt som representerar Compute-noden som ska återbildas.</span><span class="sxs-lookup"><span data-stu-id="690f9-120">Specifies the **PSComputeNode** object that represents the compute node to reimage.</span></span>

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

### <span data-ttu-id="690f9-121">-ID</span><span class="sxs-lookup"><span data-stu-id="690f9-121">-Id</span></span>
<span data-ttu-id="690f9-122">Anger ID för den datornod som ska återskrivas.</span><span class="sxs-lookup"><span data-stu-id="690f9-122">Specifies the ID of the compute node to reimage.</span></span>

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

### <span data-ttu-id="690f9-123">-PoolId</span><span class="sxs-lookup"><span data-stu-id="690f9-123">-PoolId</span></span>
<span data-ttu-id="690f9-124">Anger ID för den pool som innehåller noden Compute.</span><span class="sxs-lookup"><span data-stu-id="690f9-124">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="690f9-125">-ReimageOption</span><span class="sxs-lookup"><span data-stu-id="690f9-125">-ReimageOption</span></span>
<span data-ttu-id="690f9-126">Anger när du vill att noden ska visas igen och vad du kan göra med aktiviteterna.</span><span class="sxs-lookup"><span data-stu-id="690f9-126">Specifies when to reimage the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="690f9-127">Standardvärdet är köa.</span><span class="sxs-lookup"><span data-stu-id="690f9-127">The default is Requeue.</span></span>

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

### <span data-ttu-id="690f9-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="690f9-128">-DefaultProfile</span></span>
<span data-ttu-id="690f9-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="690f9-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="690f9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="690f9-130">CommonParameters</span></span>
<span data-ttu-id="690f9-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="690f9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="690f9-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="690f9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="690f9-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="690f9-133">INPUTS</span></span>

### <span data-ttu-id="690f9-134">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="690f9-134">BatchAccountContext</span></span>
<span data-ttu-id="690f9-135">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="690f9-135">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="690f9-136">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="690f9-136">PSComputeNode</span></span>
<span data-ttu-id="690f9-137">Parametern ' ComputeNode ' godkänner värdet av typen ' PSComputeNode ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="690f9-137">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="690f9-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="690f9-138">OUTPUTS</span></span>

## <span data-ttu-id="690f9-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="690f9-139">NOTES</span></span>

## <span data-ttu-id="690f9-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="690f9-140">RELATED LINKS</span></span>

[<span data-ttu-id="690f9-141">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="690f9-141">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="690f9-142">Restart-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="690f9-142">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)

[<span data-ttu-id="690f9-143">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="690f9-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


