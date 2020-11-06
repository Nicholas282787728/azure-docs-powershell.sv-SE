---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 029361F0-C4E9-4948-9EBA-BFBD1B029909
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Restart-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Restart-AzureBatchComputeNode.md
ms.openlocfilehash: eff141494c2b34622f35b687dd1803c449e8b727
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581523"
---
# <span data-ttu-id="56e4b-101">Restart-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="56e4b-101">Restart-AzureBatchComputeNode</span></span>

## <span data-ttu-id="56e4b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="56e4b-102">SYNOPSIS</span></span>
<span data-ttu-id="56e4b-103">Startar om den angivna datornoderna.</span><span class="sxs-lookup"><span data-stu-id="56e4b-103">Reboots the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56e4b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="56e4b-104">SYNTAX</span></span>

### <span data-ttu-id="56e4b-105">ID (standard)</span><span class="sxs-lookup"><span data-stu-id="56e4b-105">Id (Default)</span></span>
```
Restart-AzureBatchComputeNode [-PoolId] <String> [-Id] <String> [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56e4b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="56e4b-106">InputObject</span></span>
```
Restart-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>] [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56e4b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="56e4b-107">DESCRIPTION</span></span>
<span data-ttu-id="56e4b-108">Cmdleten **restart-AzureBatchComputeNode** startar om den angivna datornoderna.</span><span class="sxs-lookup"><span data-stu-id="56e4b-108">The **Restart-AzureBatchComputeNode** cmdlet reboots the specified compute node.</span></span>

## <span data-ttu-id="56e4b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="56e4b-109">EXAMPLES</span></span>

### <span data-ttu-id="56e4b-110">Exempel 1: starta om en datornod</span><span class="sxs-lookup"><span data-stu-id="56e4b-110">Example 1: Restart a compute node</span></span>
```
PS C:\>Restart-AzureBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="56e4b-111">Det här kommandot startar om den beräknade noden med ID: t "TVM-3257026573_2-20150813t200938z" i poolen för pool.</span><span class="sxs-lookup"><span data-stu-id="56e4b-111">This command reboots the compute node with the ID "tvm-3257026573_2-20150813t200938z" in the pool MyPool.</span></span>

### <span data-ttu-id="56e4b-112">Exempel 2: starta om varje datornod i en pool</span><span class="sxs-lookup"><span data-stu-id="56e4b-112">Example 2: Restart every compute node in a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Restart-AzureBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="56e4b-113">Det här kommandot startar om varje datornod i poolen för pooler.</span><span class="sxs-lookup"><span data-stu-id="56e4b-113">This command reboots every compute node in the pool MyPool.</span></span>

## <span data-ttu-id="56e4b-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="56e4b-114">PARAMETERS</span></span>

### <span data-ttu-id="56e4b-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="56e4b-115">-BatchContext</span></span>
<span data-ttu-id="56e4b-116">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="56e4b-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="56e4b-117">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="56e4b-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="56e4b-118">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="56e4b-118">-ComputeNode</span></span>
<span data-ttu-id="56e4b-119">Anger det **PSComputeNode** -objekt som representerar noden Compute för omstart.</span><span class="sxs-lookup"><span data-stu-id="56e4b-119">Specifies the **PSComputeNode** object that represents the compute node to reboot.</span></span>

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

### <span data-ttu-id="56e4b-120">-ID</span><span class="sxs-lookup"><span data-stu-id="56e4b-120">-Id</span></span>
<span data-ttu-id="56e4b-121">Anger ID för den datornod som ska startas om.</span><span class="sxs-lookup"><span data-stu-id="56e4b-121">Specifies the ID of the compute node to reboot.</span></span>

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

### <span data-ttu-id="56e4b-122">-PoolId</span><span class="sxs-lookup"><span data-stu-id="56e4b-122">-PoolId</span></span>
<span data-ttu-id="56e4b-123">Anger ID för den pool som innehåller noden Compute.</span><span class="sxs-lookup"><span data-stu-id="56e4b-123">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="56e4b-124">-RebootOption</span><span class="sxs-lookup"><span data-stu-id="56e4b-124">-RebootOption</span></span>
<span data-ttu-id="56e4b-125">Anger när du vill starta om noden och vad du kan göra med aktiviteterna.</span><span class="sxs-lookup"><span data-stu-id="56e4b-125">Specifies when to reboot the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="56e4b-126">Standardvärdet är köa.</span><span class="sxs-lookup"><span data-stu-id="56e4b-126">The default is Requeue.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeRebootOption]
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56e4b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56e4b-127">-DefaultProfile</span></span>
<span data-ttu-id="56e4b-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="56e4b-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56e4b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56e4b-129">CommonParameters</span></span>
<span data-ttu-id="56e4b-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56e4b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56e4b-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56e4b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56e4b-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="56e4b-132">INPUTS</span></span>

### <span data-ttu-id="56e4b-133">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="56e4b-133">BatchAccountContext</span></span>
<span data-ttu-id="56e4b-134">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="56e4b-134">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="56e4b-135">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="56e4b-135">PSComputeNode</span></span>
<span data-ttu-id="56e4b-136">Parametern ' ComputeNode ' godkänner värdet av typen ' PSComputeNode ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="56e4b-136">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="56e4b-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="56e4b-137">OUTPUTS</span></span>

## <span data-ttu-id="56e4b-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="56e4b-138">NOTES</span></span>

## <span data-ttu-id="56e4b-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="56e4b-139">RELATED LINKS</span></span>

[<span data-ttu-id="56e4b-140">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="56e4b-140">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="56e4b-141">Reset-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="56e4b-141">Reset-AzureBatchComputeNode</span></span>](./Reset-AzureBatchComputeNode.md)

[<span data-ttu-id="56e4b-142">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="56e4b-142">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


