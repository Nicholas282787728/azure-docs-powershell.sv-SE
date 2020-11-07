---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A202537B-D292-4822-A0B9-27A6A20621D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/reset-azurebatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Reset-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Reset-AzureBatchComputeNode.md
ms.openlocfilehash: 8e1fd78c51a6a41f1f455fc3672a0c340309f76c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757952"
---
# <span data-ttu-id="4cb79-101">Reset-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="4cb79-101">Reset-AzureBatchComputeNode</span></span>

## <span data-ttu-id="4cb79-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4cb79-102">SYNOPSIS</span></span>
<span data-ttu-id="4cb79-103">Operativ systemet installeras om på angiven datornod.</span><span class="sxs-lookup"><span data-stu-id="4cb79-103">Reinstalls the operating system on the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cb79-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4cb79-104">SYNTAX</span></span>

### <span data-ttu-id="4cb79-105">ID (standard)</span><span class="sxs-lookup"><span data-stu-id="4cb79-105">Id (Default)</span></span>
```
Reset-AzureBatchComputeNode [-PoolId] <String> [-Id] <String> [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4cb79-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="4cb79-106">InputObject</span></span>
```
Reset-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>] [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4cb79-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4cb79-107">DESCRIPTION</span></span>
<span data-ttu-id="4cb79-108">Cmdleten **Reset-AzureBatchComputeNode** installerar om operativ systemet på angiven datornod.</span><span class="sxs-lookup"><span data-stu-id="4cb79-108">The **Reset-AzureBatchComputeNode** cmdlet reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="4cb79-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4cb79-109">EXAMPLES</span></span>

### <span data-ttu-id="4cb79-110">Exempel 1: återbilden av en nod</span><span class="sxs-lookup"><span data-stu-id="4cb79-110">Example 1: Reimage a node</span></span>
```
PS C:\>Reset-AzureBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="4cb79-111">Det här kommandot återgör om Compute-noden med ID: t "TVM-3257026573_2-20150813t200938z" i poolen med namnet nonpool.</span><span class="sxs-lookup"><span data-stu-id="4cb79-111">This command reimages the compute node with ID "tvm-3257026573_2-20150813t200938z" in the pool named MyPool.</span></span>
<span data-ttu-id="4cb79-112">Använd Get-AzureRmBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="4cb79-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="4cb79-113">Exempel 2: återpå alla noder i en pool</span><span class="sxs-lookup"><span data-stu-id="4cb79-113">Example 2: Reimage all nodes in a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Reset-AzureBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="4cb79-114">Det här kommandot återgör varje datornod i poolen med namnet min pool.</span><span class="sxs-lookup"><span data-stu-id="4cb79-114">This command reimages every compute node in the pool named MyPool.</span></span>

## <span data-ttu-id="4cb79-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4cb79-115">PARAMETERS</span></span>

### <span data-ttu-id="4cb79-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4cb79-116">-BatchContext</span></span>
<span data-ttu-id="4cb79-117">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="4cb79-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4cb79-118">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="4cb79-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="4cb79-119">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="4cb79-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="4cb79-120">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="4cb79-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="4cb79-121">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="4cb79-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="4cb79-122">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="4cb79-122">-ComputeNode</span></span>
<span data-ttu-id="4cb79-123">Anger det **PSComputeNode** -objekt som representerar Compute-noden som ska återbildas.</span><span class="sxs-lookup"><span data-stu-id="4cb79-123">Specifies the **PSComputeNode** object that represents the compute node to reimage.</span></span>

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

### <span data-ttu-id="4cb79-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cb79-124">-DefaultProfile</span></span>
<span data-ttu-id="4cb79-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4cb79-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cb79-126">-ID</span><span class="sxs-lookup"><span data-stu-id="4cb79-126">-Id</span></span>
<span data-ttu-id="4cb79-127">Anger ID för den datornod som ska återskrivas.</span><span class="sxs-lookup"><span data-stu-id="4cb79-127">Specifies the ID of the compute node to reimage.</span></span>

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

### <span data-ttu-id="4cb79-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="4cb79-128">-PoolId</span></span>
<span data-ttu-id="4cb79-129">Anger ID för den pool som innehåller noden Compute.</span><span class="sxs-lookup"><span data-stu-id="4cb79-129">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="4cb79-130">-ReimageOption</span><span class="sxs-lookup"><span data-stu-id="4cb79-130">-ReimageOption</span></span>
<span data-ttu-id="4cb79-131">Anger när du vill att noden ska visas igen och vad du kan göra med aktiviteterna.</span><span class="sxs-lookup"><span data-stu-id="4cb79-131">Specifies when to reimage the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="4cb79-132">Standardvärdet är köa.</span><span class="sxs-lookup"><span data-stu-id="4cb79-132">The default is Requeue.</span></span>

```yaml
Type: ComputeNodeReimageOption
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cb79-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cb79-133">CommonParameters</span></span>
<span data-ttu-id="4cb79-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cb79-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cb79-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cb79-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cb79-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4cb79-136">INPUTS</span></span>

### <span data-ttu-id="4cb79-137">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4cb79-137">BatchAccountContext</span></span>
<span data-ttu-id="4cb79-138">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="4cb79-138">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="4cb79-139">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="4cb79-139">PSComputeNode</span></span>
<span data-ttu-id="4cb79-140">Parametern ' ComputeNode ' godkänner värdet av typen ' PSComputeNode ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="4cb79-140">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="4cb79-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4cb79-141">OUTPUTS</span></span>

## <span data-ttu-id="4cb79-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4cb79-142">NOTES</span></span>

## <span data-ttu-id="4cb79-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4cb79-143">RELATED LINKS</span></span>

[<span data-ttu-id="4cb79-144">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="4cb79-144">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="4cb79-145">Restart-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="4cb79-145">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)

[<span data-ttu-id="4cb79-146">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="4cb79-146">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


