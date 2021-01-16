---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 029361F0-C4E9-4948-9EBA-BFBD1B029909
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/restart-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Restart-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Restart-AzBatchComputeNode.md
ms.openlocfilehash: 41c6ea8e069e03a759c04f39018e2fa3a4d16834
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401512"
---
# <span data-ttu-id="32faf-101">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="32faf-101">Restart-AzBatchComputeNode</span></span>

## <span data-ttu-id="32faf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="32faf-102">SYNOPSIS</span></span>
<span data-ttu-id="32faf-103">Startar om den angivna datornoderna.</span><span class="sxs-lookup"><span data-stu-id="32faf-103">Reboots the specified compute node.</span></span>

## <span data-ttu-id="32faf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="32faf-104">SYNTAX</span></span>

### <span data-ttu-id="32faf-105">ID (standard)</span><span class="sxs-lookup"><span data-stu-id="32faf-105">Id (Default)</span></span>
```
Restart-AzBatchComputeNode [-PoolId] <String> [-Id] <String> [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32faf-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="32faf-106">InputObject</span></span>
```
Restart-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>] [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32faf-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="32faf-107">DESCRIPTION</span></span>
<span data-ttu-id="32faf-108">Cmdleten **restart-AzBatchComputeNode** startar om den angivna datornoderna.</span><span class="sxs-lookup"><span data-stu-id="32faf-108">The **Restart-AzBatchComputeNode** cmdlet reboots the specified compute node.</span></span>

## <span data-ttu-id="32faf-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="32faf-109">EXAMPLES</span></span>

### <span data-ttu-id="32faf-110">Exempel 1: starta om en datornod</span><span class="sxs-lookup"><span data-stu-id="32faf-110">Example 1: Restart a compute node</span></span>
```
PS C:\>Restart-AzBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="32faf-111">Det här kommandot startar om den beräknade noden med ID: t "TVM-3257026573_2-20150813t200938z" i poolen för pool.</span><span class="sxs-lookup"><span data-stu-id="32faf-111">This command reboots the compute node with the ID "tvm-3257026573_2-20150813t200938z" in the pool MyPool.</span></span>

### <span data-ttu-id="32faf-112">Exempel 2: starta om varje datornod i en pool</span><span class="sxs-lookup"><span data-stu-id="32faf-112">Example 2: Restart every compute node in a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Restart-AzBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="32faf-113">Det här kommandot startar om varje datornod i poolen för pooler.</span><span class="sxs-lookup"><span data-stu-id="32faf-113">This command reboots every compute node in the pool MyPool.</span></span>

## <span data-ttu-id="32faf-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="32faf-114">PARAMETERS</span></span>

### <span data-ttu-id="32faf-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="32faf-115">-BatchContext</span></span>
<span data-ttu-id="32faf-116">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="32faf-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="32faf-117">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="32faf-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="32faf-118">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="32faf-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="32faf-119">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="32faf-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="32faf-120">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="32faf-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="32faf-121">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="32faf-121">-ComputeNode</span></span>
<span data-ttu-id="32faf-122">Anger det **PSComputeNode** -objekt som representerar noden Compute för omstart.</span><span class="sxs-lookup"><span data-stu-id="32faf-122">Specifies the **PSComputeNode** object that represents the compute node to reboot.</span></span>

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

### <span data-ttu-id="32faf-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32faf-123">-DefaultProfile</span></span>
<span data-ttu-id="32faf-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="32faf-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32faf-125">-ID</span><span class="sxs-lookup"><span data-stu-id="32faf-125">-Id</span></span>
<span data-ttu-id="32faf-126">Anger ID för den datornod som ska startas om.</span><span class="sxs-lookup"><span data-stu-id="32faf-126">Specifies the ID of the compute node to reboot.</span></span>

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

### <span data-ttu-id="32faf-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="32faf-127">-PoolId</span></span>
<span data-ttu-id="32faf-128">Anger ID för den pool som innehåller noden Compute.</span><span class="sxs-lookup"><span data-stu-id="32faf-128">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="32faf-129">-RebootOption</span><span class="sxs-lookup"><span data-stu-id="32faf-129">-RebootOption</span></span>
<span data-ttu-id="32faf-130">Anger när du vill starta om noden och vad du kan göra med aktiviteterna.</span><span class="sxs-lookup"><span data-stu-id="32faf-130">Specifies when to reboot the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="32faf-131">Standardvärdet är köa.</span><span class="sxs-lookup"><span data-stu-id="32faf-131">The default is Requeue.</span></span>

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

### <span data-ttu-id="32faf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32faf-132">CommonParameters</span></span>
<span data-ttu-id="32faf-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32faf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32faf-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32faf-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32faf-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="32faf-135">INPUTS</span></span>

### <span data-ttu-id="32faf-136">Microsoft.Azure.Commands.BatCH. Modeller. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="32faf-136">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="32faf-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="32faf-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="32faf-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="32faf-138">OUTPUTS</span></span>

### <span data-ttu-id="32faf-139">System. Void</span><span class="sxs-lookup"><span data-stu-id="32faf-139">System.Void</span></span>

## <span data-ttu-id="32faf-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="32faf-140">NOTES</span></span>

## <span data-ttu-id="32faf-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="32faf-141">RELATED LINKS</span></span>

[<span data-ttu-id="32faf-142">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="32faf-142">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="32faf-143">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="32faf-143">Reset-AzBatchComputeNode</span></span>](./Reset-AzBatchComputeNode.md)

[<span data-ttu-id="32faf-144">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="32faf-144">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
