---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 93614655-A8F2-4A67-887D-43D41AB91F82
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchComputeNode.md
ms.openlocfilehash: a50329620944aa18458c3bb667e3a95ff45bc21f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325943"
---
# <span data-ttu-id="79290-101">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="79290-101">Get-AzBatchComputeNode</span></span>

## <span data-ttu-id="79290-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="79290-102">SYNOPSIS</span></span>
<span data-ttu-id="79290-103">Hämtar noder för batchattribut från en pool.</span><span class="sxs-lookup"><span data-stu-id="79290-103">Gets Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="79290-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="79290-104">SYNTAX</span></span>

### <span data-ttu-id="79290-105">ODataFilter (standard)</span><span class="sxs-lookup"><span data-stu-id="79290-105">ODataFilter (Default)</span></span>
```
Get-AzBatchComputeNode [-PoolId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79290-106">Et</span><span class="sxs-lookup"><span data-stu-id="79290-106">Id</span></span>
```
Get-AzBatchComputeNode [-PoolId] <String> [[-Id] <String>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79290-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="79290-107">ParentObject</span></span>
```
Get-AzBatchComputeNode [[-Pool] <PSCloudPool>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79290-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="79290-108">DESCRIPTION</span></span>
<span data-ttu-id="79290-109">Cmdleten **Get-AzBatchComputeNode** tar emot Azure Batch-datornoder från en pool.</span><span class="sxs-lookup"><span data-stu-id="79290-109">The **Get-AzBatchComputeNode** cmdlet gets Azure Batch compute nodes from a pool.</span></span>
<span data-ttu-id="79290-110">Ange antingen parametern *PoolID* eller *pool* .</span><span class="sxs-lookup"><span data-stu-id="79290-110">Specify either the *PoolID* or *Pool* parameter.</span></span>
<span data-ttu-id="79290-111">Ange *ID-* parametern för att få en enda datornod.</span><span class="sxs-lookup"><span data-stu-id="79290-111">Specify the *Id* parameter to get a single compute node.</span></span>
<span data-ttu-id="79290-112">Ange parametern *filter* för att få datornoderna som matchar ett open data Protocol (OData)-filter.</span><span class="sxs-lookup"><span data-stu-id="79290-112">Specify the *Filter* parameter to get the compute nodes that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="79290-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="79290-113">EXAMPLES</span></span>

### <span data-ttu-id="79290-114">Exempel 1: Hämta en datornod med ID</span><span class="sxs-lookup"><span data-stu-id="79290-114">Example 1: Get a compute node by ID</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool06" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 1
StartTaskInformation  :
RecentTasks           : {}
StartTask             :
CertificateReferences :
Errors                :
```

<span data-ttu-id="79290-115">Det här kommandot får Compute-noden som har ID TVM-2316545714_1-20150725t213220z från poolen med ID Pool06.</span><span class="sxs-lookup"><span data-stu-id="79290-115">This command gets the compute node that has the ID tvm-2316545714_1-20150725t213220z from the pool that has the ID Pool06.</span></span>
<span data-ttu-id="79290-116">Använd Get-AzBatchAccountKey cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="79290-116">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="79290-117">Exempel 2: Hämta alla inaktiva datornoder från en pool</span><span class="sxs-lookup"><span data-stu-id="79290-117">Example 2: Get all idle compute nodes from a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool06" -Filter "state eq 'idle'" -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 1
StartTaskInformation  :
RecentTasks           : {}
StartTask             :
CertificateReferences :
Errors                :

Id                    : tvm-2316545714_2-20150726t172920z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_2-20150726t172920z
State                 : Idle
StateTransitionTime   : 7/26/2015 5:33:58 PM
LastBootTime          : 7/26/2015 5:33:58 PM
AllocationTime        : 7/26/2015 5:29:20 PM
IPAddress             : 10.14.121.38
AffinityId            : TVM:tvm-2316545714_2-20150726t172920z
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 0
StartTaskInformation  :
RecentTasks           :
StartTask             :
CertificateReferences :
Errors                :
```

<span data-ttu-id="79290-118">Det här kommandot får alla inaktiva datornoder som ingår i poolen med ID-Pool06.</span><span class="sxs-lookup"><span data-stu-id="79290-118">This command gets all idle compute nodes that are contained in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="79290-119">Kommandot anger Idle-tillståndet med *filter* parametern.</span><span class="sxs-lookup"><span data-stu-id="79290-119">The command specifies the idle state by using the *Filter* parameter.</span></span>

### <span data-ttu-id="79290-120">Exempel 3: Hämta alla datornoder i en angiven pool</span><span class="sxs-lookup"><span data-stu-id="79290-120">Example 3: Get all compute nodes in a specified pool</span></span>
```
PS C:\>Get-AzBatchPool -Id "Pool07" -BatchContext $Context | Get-AzBatchComputeNode -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 1
StartTaskInformation  :
RecentTasks           : {}
StartTask             :
CertificateReferences :
Errors                :


Id                    : tvm-2316545714_2-20150726t172920z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_2-20150726t172920z
State                 : Idle
StateTransitionTime   : 7/26/2015 5:33:58 PM
LastBootTime          : 7/26/2015 5:33:58 PM
AllocationTime        : 7/26/2015 5:29:20 PM

IPAddress             : 10.14.121.38
AffinityId            : TVM:tvm-2316545714_2-20150726t172920z
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 0
StartTaskInformation  :
RecentTasks           :
StartTask             :
CertificateReferences :
Errors                :
```

<span data-ttu-id="79290-121">Det här kommandot får poolen med ID-Pool07 med hjälp av Get-AzBatchPool cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79290-121">This command gets the pool that has the ID Pool07 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="79290-122">Kommandot skickar denna pool till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="79290-122">The command passes that pool to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="79290-123">Denna cmdlet får alla datornoder från den poolen.</span><span class="sxs-lookup"><span data-stu-id="79290-123">That cmdlet gets all compute nodes from that pool.</span></span>

## <span data-ttu-id="79290-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="79290-124">PARAMETERS</span></span>

### <span data-ttu-id="79290-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="79290-125">-BatchContext</span></span>
<span data-ttu-id="79290-126">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="79290-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="79290-127">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="79290-127">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="79290-128">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="79290-128">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="79290-129">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="79290-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="79290-130">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="79290-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="79290-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79290-131">-DefaultProfile</span></span>
<span data-ttu-id="79290-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="79290-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79290-133">-Filter</span><span class="sxs-lookup"><span data-stu-id="79290-133">-Filter</span></span>
<span data-ttu-id="79290-134">Anger en OData filter-sats.</span><span class="sxs-lookup"><span data-stu-id="79290-134">Specifies an OData filter clause.</span></span>
<span data-ttu-id="79290-135">Denna cmdlet returnerar beräknade noder som matchar det filter som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="79290-135">This cmdlet returns compute nodes that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="79290-136">Om du inte anger något filter returnerar den här cmdleten alla datornoder för poolen.</span><span class="sxs-lookup"><span data-stu-id="79290-136">If you do not specify a filter, this cmdlet returns all compute nodes for the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79290-137">-ID</span><span class="sxs-lookup"><span data-stu-id="79290-137">-Id</span></span>
<span data-ttu-id="79290-138">Anger ID för den datornod som denna cmdlet hämtar från poolen.</span><span class="sxs-lookup"><span data-stu-id="79290-138">Specifies the ID of the compute node that this cmdlet gets from the pool.</span></span>
<span data-ttu-id="79290-139">Du kan inte ange jokertecken.</span><span class="sxs-lookup"><span data-stu-id="79290-139">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79290-140">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="79290-140">-MaxCount</span></span>
<span data-ttu-id="79290-141">Anger det maximala antalet datornoder som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="79290-141">Specifies the maximum number of compute nodes to return.</span></span>
<span data-ttu-id="79290-142">Om du anger ett värde som är noll (0) eller mindre används ingen övre gräns av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="79290-142">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="79290-143">Standardvärdet är 1000.</span><span class="sxs-lookup"><span data-stu-id="79290-143">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter, ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79290-144">-Pool</span><span class="sxs-lookup"><span data-stu-id="79290-144">-Pool</span></span>
<span data-ttu-id="79290-145">Anger poolen, som ett **PSCloudPool** -objekt, som innehåller datornoderna.</span><span class="sxs-lookup"><span data-stu-id="79290-145">Specifies the pool, as a **PSCloudPool** object, that contains the compute nodes.</span></span>
<span data-ttu-id="79290-146">För att hämta ett **PSCloudPool** -objekt, Använd cmdleten Get-AzBatchPool.</span><span class="sxs-lookup"><span data-stu-id="79290-146">To obtain a **PSCloudPool** object, use the Get-AzBatchPool cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudPool
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79290-147">-PoolId</span><span class="sxs-lookup"><span data-stu-id="79290-147">-PoolId</span></span>
<span data-ttu-id="79290-148">Anger ID för den pool som innehåller datornoderna.</span><span class="sxs-lookup"><span data-stu-id="79290-148">Specifies the ID of the pool that contains the compute nodes.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79290-149">-Välj</span><span class="sxs-lookup"><span data-stu-id="79290-149">-Select</span></span>
<span data-ttu-id="79290-150">Anger en OData SELECT-sats.</span><span class="sxs-lookup"><span data-stu-id="79290-150">Specifies an OData select clause.</span></span>
<span data-ttu-id="79290-151">Ange ett värde för den här parametern för att få specifika egenskaper i stället för alla objekt egenskaper.</span><span class="sxs-lookup"><span data-stu-id="79290-151">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79290-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79290-152">CommonParameters</span></span>
<span data-ttu-id="79290-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79290-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79290-154">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79290-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79290-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="79290-155">INPUTS</span></span>

### <span data-ttu-id="79290-156">System. String</span><span class="sxs-lookup"><span data-stu-id="79290-156">System.String</span></span>

### <span data-ttu-id="79290-157">Microsoft.Azure.Commands.BatCH. Modeller. PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="79290-157">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="79290-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="79290-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="79290-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="79290-159">OUTPUTS</span></span>

### <span data-ttu-id="79290-160">Microsoft.Azure.Commands.BatCH. Modeller. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="79290-160">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

## <span data-ttu-id="79290-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="79290-161">NOTES</span></span>

## <span data-ttu-id="79290-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="79290-162">RELATED LINKS</span></span>

[<span data-ttu-id="79290-163">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="79290-163">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="79290-164">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="79290-164">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="79290-165">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="79290-165">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)

[<span data-ttu-id="79290-166">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="79290-166">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="79290-167">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="79290-167">Reset-AzBatchComputeNode</span></span>](./Reset-AzBatchComputeNode.md)

[<span data-ttu-id="79290-168">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="79290-168">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)

[<span data-ttu-id="79290-169">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="79290-169">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
