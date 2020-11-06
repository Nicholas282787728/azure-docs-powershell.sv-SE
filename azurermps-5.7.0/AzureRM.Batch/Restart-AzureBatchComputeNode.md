---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 029361F0-C4E9-4948-9EBA-BFBD1B029909
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/restart-azurebatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Restart-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Restart-AzureBatchComputeNode.md
ms.openlocfilehash: 5f32963630769dc25ed62f47d93fe47e56abda91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576630"
---
# <span data-ttu-id="34eef-101">Restart-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="34eef-101">Restart-AzureBatchComputeNode</span></span>

## <span data-ttu-id="34eef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="34eef-102">SYNOPSIS</span></span>
<span data-ttu-id="34eef-103">Startar om den angivna datornoderna.</span><span class="sxs-lookup"><span data-stu-id="34eef-103">Reboots the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34eef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="34eef-104">SYNTAX</span></span>

### <span data-ttu-id="34eef-105">ID (standard)</span><span class="sxs-lookup"><span data-stu-id="34eef-105">Id (Default)</span></span>
```
Restart-AzureBatchComputeNode [-PoolId] <String> [-Id] <String> [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34eef-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="34eef-106">InputObject</span></span>
```
Restart-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>] [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34eef-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="34eef-107">DESCRIPTION</span></span>
<span data-ttu-id="34eef-108">Cmdleten **restart-AzureBatchComputeNode** startar om den angivna datornoderna.</span><span class="sxs-lookup"><span data-stu-id="34eef-108">The **Restart-AzureBatchComputeNode** cmdlet reboots the specified compute node.</span></span>

## <span data-ttu-id="34eef-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="34eef-109">EXAMPLES</span></span>

### <span data-ttu-id="34eef-110">Exempel 1: starta om en datornod</span><span class="sxs-lookup"><span data-stu-id="34eef-110">Example 1: Restart a compute node</span></span>
```
PS C:\>Restart-AzureBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="34eef-111">Det här kommandot startar om den beräknade noden med ID: t "TVM-3257026573_2-20150813t200938z" i poolen för pool.</span><span class="sxs-lookup"><span data-stu-id="34eef-111">This command reboots the compute node with the ID "tvm-3257026573_2-20150813t200938z" in the pool MyPool.</span></span>

### <span data-ttu-id="34eef-112">Exempel 2: starta om varje datornod i en pool</span><span class="sxs-lookup"><span data-stu-id="34eef-112">Example 2: Restart every compute node in a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Restart-AzureBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="34eef-113">Det här kommandot startar om varje datornod i poolen för pooler.</span><span class="sxs-lookup"><span data-stu-id="34eef-113">This command reboots every compute node in the pool MyPool.</span></span>

## <span data-ttu-id="34eef-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="34eef-114">PARAMETERS</span></span>

### <span data-ttu-id="34eef-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="34eef-115">-BatchContext</span></span>
<span data-ttu-id="34eef-116">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="34eef-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="34eef-117">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="34eef-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="34eef-118">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="34eef-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="34eef-119">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="34eef-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="34eef-120">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="34eef-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34eef-121">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="34eef-121">-ComputeNode</span></span>
<span data-ttu-id="34eef-122">Anger det **PSComputeNode** -objekt som representerar noden Compute för omstart.</span><span class="sxs-lookup"><span data-stu-id="34eef-122">Specifies the **PSComputeNode** object that represents the compute node to reboot.</span></span>

```yaml
Type: PSComputeNode
Parameter Sets: InputObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34eef-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34eef-123">-DefaultProfile</span></span>
<span data-ttu-id="34eef-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="34eef-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34eef-125">-ID</span><span class="sxs-lookup"><span data-stu-id="34eef-125">-Id</span></span>
<span data-ttu-id="34eef-126">Anger ID för den datornod som ska startas om.</span><span class="sxs-lookup"><span data-stu-id="34eef-126">Specifies the ID of the compute node to reboot.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34eef-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="34eef-127">-PoolId</span></span>
<span data-ttu-id="34eef-128">Anger ID för den pool som innehåller noden Compute.</span><span class="sxs-lookup"><span data-stu-id="34eef-128">Specifies the ID of the pool that contains the compute node.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34eef-129">-RebootOption</span><span class="sxs-lookup"><span data-stu-id="34eef-129">-RebootOption</span></span>
<span data-ttu-id="34eef-130">Anger när du vill starta om noden och vad du kan göra med aktiviteterna.</span><span class="sxs-lookup"><span data-stu-id="34eef-130">Specifies when to reboot the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="34eef-131">Standardvärdet är köa.</span><span class="sxs-lookup"><span data-stu-id="34eef-131">The default is Requeue.</span></span>

```yaml
Type: ComputeNodeRebootOption
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34eef-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34eef-132">CommonParameters</span></span>
<span data-ttu-id="34eef-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34eef-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34eef-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34eef-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34eef-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="34eef-135">INPUTS</span></span>

### <span data-ttu-id="34eef-136">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="34eef-136">BatchAccountContext</span></span>
<span data-ttu-id="34eef-137">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="34eef-137">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="34eef-138">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="34eef-138">PSComputeNode</span></span>
<span data-ttu-id="34eef-139">Parametern ' ComputeNode ' godkänner värdet av typen ' PSComputeNode ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="34eef-139">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="34eef-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="34eef-140">OUTPUTS</span></span>

## <span data-ttu-id="34eef-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="34eef-141">NOTES</span></span>

## <span data-ttu-id="34eef-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="34eef-142">RELATED LINKS</span></span>

[<span data-ttu-id="34eef-143">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="34eef-143">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="34eef-144">Reset-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="34eef-144">Reset-AzureBatchComputeNode</span></span>](./Reset-AzureBatchComputeNode.md)

[<span data-ttu-id="34eef-145">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="34eef-145">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


