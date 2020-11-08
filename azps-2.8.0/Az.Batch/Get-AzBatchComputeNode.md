---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 93614655-A8F2-4A67-887D-43D41AB91F82
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchComputeNode.md
ms.openlocfilehash: 81f357f2394e266aa70c0d7e4a7720d8252f2edb
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93928297"
---
# <span data-ttu-id="78cf3-101">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="78cf3-101">Get-AzBatchComputeNode</span></span>

## <span data-ttu-id="78cf3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="78cf3-102">SYNOPSIS</span></span>
<span data-ttu-id="78cf3-103">Hämtar noder för batchattribut från en pool.</span><span class="sxs-lookup"><span data-stu-id="78cf3-103">Gets Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="78cf3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="78cf3-104">SYNTAX</span></span>

### <span data-ttu-id="78cf3-105">ODataFilter (standard)</span><span class="sxs-lookup"><span data-stu-id="78cf3-105">ODataFilter (Default)</span></span>
```
Get-AzBatchComputeNode [-PoolId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78cf3-106">Et</span><span class="sxs-lookup"><span data-stu-id="78cf3-106">Id</span></span>
```
Get-AzBatchComputeNode [-PoolId] <String> [[-Id] <String>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78cf3-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="78cf3-107">ParentObject</span></span>
```
Get-AzBatchComputeNode [[-Pool] <PSCloudPool>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78cf3-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="78cf3-108">DESCRIPTION</span></span>
<span data-ttu-id="78cf3-109">Cmdleten **Get-AzBatchComputeNode** tar emot Azure Batch-datornoder från en pool.</span><span class="sxs-lookup"><span data-stu-id="78cf3-109">The **Get-AzBatchComputeNode** cmdlet gets Azure Batch compute nodes from a pool.</span></span>
<span data-ttu-id="78cf3-110">Ange antingen parametern *PoolID* eller *pool* .</span><span class="sxs-lookup"><span data-stu-id="78cf3-110">Specify either the *PoolID* or *Pool* parameter.</span></span>
<span data-ttu-id="78cf3-111">Ange *ID-* parametern för att få en enda datornod.</span><span class="sxs-lookup"><span data-stu-id="78cf3-111">Specify the *Id* parameter to get a single compute node.</span></span>
<span data-ttu-id="78cf3-112">Ange parametern *filter* för att få datornoderna som matchar ett open data Protocol (OData)-filter.</span><span class="sxs-lookup"><span data-stu-id="78cf3-112">Specify the *Filter* parameter to get the compute nodes that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="78cf3-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="78cf3-113">EXAMPLES</span></span>

### <span data-ttu-id="78cf3-114">Exempel 1: Hämta en datornod med ID</span><span class="sxs-lookup"><span data-stu-id="78cf3-114">Example 1: Get a compute node by ID</span></span>
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
VirtualMachineSize    : small
TotalTasksRun         : 1
StartTaskInformation  : 
RecentTasks           : {}
StartTask             : 
CertificateReferences : 
Errors                :
```

<span data-ttu-id="78cf3-115">Det här kommandot får Compute-noden som har ID TVM-2316545714_1-20150725t213220z från poolen med ID Pool06.</span><span class="sxs-lookup"><span data-stu-id="78cf3-115">This command gets the compute node that has the ID tvm-2316545714_1-20150725t213220z from the pool that has the ID Pool06.</span></span>
<span data-ttu-id="78cf3-116">Använd Get-AzBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="78cf3-116">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="78cf3-117">Exempel 2: Hämta alla inaktiva datornoder från en pool</span><span class="sxs-lookup"><span data-stu-id="78cf3-117">Example 2: Get all idle compute nodes from a pool</span></span>
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
VirtualMachineSize    : small
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
VirtualMachineSize    : small
TotalTasksRun         : 0
StartTaskInformation  : 
RecentTasks           : 
StartTask             : 
CertificateReferences : 
Errors                :
```

<span data-ttu-id="78cf3-118">Det här kommandot får alla inaktiva datornoder som ingår i poolen med ID-Pool06.</span><span class="sxs-lookup"><span data-stu-id="78cf3-118">This command gets all idle compute nodes that are contained in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="78cf3-119">Kommandot anger Idle-tillståndet med *filter* parametern.</span><span class="sxs-lookup"><span data-stu-id="78cf3-119">The command specifies the idle state by using the *Filter* parameter.</span></span>

### <span data-ttu-id="78cf3-120">Exempel 3: Hämta alla datornoder i en angiven pool</span><span class="sxs-lookup"><span data-stu-id="78cf3-120">Example 3: Get all compute nodes in a specified pool</span></span>
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
VirtualMachineSize    : small
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
VirtualMachineSize    : small
TotalTasksRun         : 0
StartTaskInformation  : 
RecentTasks           : 
StartTask             : 
CertificateReferences : 
Errors                :
```

<span data-ttu-id="78cf3-121">Det här kommandot får poolen med ID-Pool07 med hjälp av Get-AzBatchPool cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78cf3-121">This command gets the pool that has the ID Pool07 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="78cf3-122">Kommandot skickar denna pool till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="78cf3-122">The command passes that pool to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="78cf3-123">Denna cmdlet får alla datornoder från den poolen.</span><span class="sxs-lookup"><span data-stu-id="78cf3-123">That cmdlet gets all compute nodes from that pool.</span></span>

## <span data-ttu-id="78cf3-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="78cf3-124">PARAMETERS</span></span>

### <span data-ttu-id="78cf3-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="78cf3-125">-BatchContext</span></span>
<span data-ttu-id="78cf3-126">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="78cf3-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="78cf3-127">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="78cf3-127">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="78cf3-128">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="78cf3-128">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="78cf3-129">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="78cf3-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="78cf3-130">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="78cf3-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="78cf3-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78cf3-131">-DefaultProfile</span></span>
<span data-ttu-id="78cf3-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="78cf3-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78cf3-133">-Filter</span><span class="sxs-lookup"><span data-stu-id="78cf3-133">-Filter</span></span>
<span data-ttu-id="78cf3-134">Anger en OData filter-sats.</span><span class="sxs-lookup"><span data-stu-id="78cf3-134">Specifies an OData filter clause.</span></span>
<span data-ttu-id="78cf3-135">Denna cmdlet returnerar beräknade noder som matchar det filter som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="78cf3-135">This cmdlet returns compute nodes that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="78cf3-136">Om du inte anger något filter returnerar den här cmdleten alla datornoder för poolen.</span><span class="sxs-lookup"><span data-stu-id="78cf3-136">If you do not specify a filter, this cmdlet returns all compute nodes for the pool.</span></span>

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

### <span data-ttu-id="78cf3-137">-ID</span><span class="sxs-lookup"><span data-stu-id="78cf3-137">-Id</span></span>
<span data-ttu-id="78cf3-138">Anger ID för den datornod som denna cmdlet hämtar från poolen.</span><span class="sxs-lookup"><span data-stu-id="78cf3-138">Specifies the ID of the compute node that this cmdlet gets from the pool.</span></span>
<span data-ttu-id="78cf3-139">Du kan inte ange jokertecken.</span><span class="sxs-lookup"><span data-stu-id="78cf3-139">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="78cf3-140">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="78cf3-140">-MaxCount</span></span>
<span data-ttu-id="78cf3-141">Anger det maximala antalet datornoder som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="78cf3-141">Specifies the maximum number of compute nodes to return.</span></span>
<span data-ttu-id="78cf3-142">Om du anger ett värde som är noll (0) eller mindre används ingen övre gräns av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="78cf3-142">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="78cf3-143">Standardvärdet är 1000.</span><span class="sxs-lookup"><span data-stu-id="78cf3-143">The default value is 1000.</span></span>

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

### <span data-ttu-id="78cf3-144">-Pool</span><span class="sxs-lookup"><span data-stu-id="78cf3-144">-Pool</span></span>
<span data-ttu-id="78cf3-145">Anger poolen, som ett **PSCloudPool** -objekt, som innehåller datornoderna.</span><span class="sxs-lookup"><span data-stu-id="78cf3-145">Specifies the pool, as a **PSCloudPool** object, that contains the compute nodes.</span></span>
<span data-ttu-id="78cf3-146">För att hämta ett **PSCloudPool** -objekt, Använd cmdleten Get-AzBatchPool.</span><span class="sxs-lookup"><span data-stu-id="78cf3-146">To obtain a **PSCloudPool** object, use the Get-AzBatchPool cmdlet.</span></span>

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

### <span data-ttu-id="78cf3-147">-PoolId</span><span class="sxs-lookup"><span data-stu-id="78cf3-147">-PoolId</span></span>
<span data-ttu-id="78cf3-148">Anger ID för den pool som innehåller datornoderna.</span><span class="sxs-lookup"><span data-stu-id="78cf3-148">Specifies the ID of the pool that contains the compute nodes.</span></span>

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

### <span data-ttu-id="78cf3-149">-Välj</span><span class="sxs-lookup"><span data-stu-id="78cf3-149">-Select</span></span>
<span data-ttu-id="78cf3-150">Anger en OData SELECT-sats.</span><span class="sxs-lookup"><span data-stu-id="78cf3-150">Specifies an OData select clause.</span></span>
<span data-ttu-id="78cf3-151">Ange ett värde för den här parametern för att få specifika egenskaper i stället för alla objekt egenskaper.</span><span class="sxs-lookup"><span data-stu-id="78cf3-151">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="78cf3-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78cf3-152">CommonParameters</span></span>
<span data-ttu-id="78cf3-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78cf3-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78cf3-154">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78cf3-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78cf3-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="78cf3-155">INPUTS</span></span>

### <span data-ttu-id="78cf3-156">System. String</span><span class="sxs-lookup"><span data-stu-id="78cf3-156">System.String</span></span>

### <span data-ttu-id="78cf3-157">Microsoft.Azure.Commands.BatCH. Modeller. PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="78cf3-157">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="78cf3-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="78cf3-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="78cf3-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="78cf3-159">OUTPUTS</span></span>

### <span data-ttu-id="78cf3-160">Microsoft.Azure.Commands.BatCH. Modeller. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="78cf3-160">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

## <span data-ttu-id="78cf3-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="78cf3-161">NOTES</span></span>

## <span data-ttu-id="78cf3-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="78cf3-162">RELATED LINKS</span></span>

[<span data-ttu-id="78cf3-163">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="78cf3-163">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="78cf3-164">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="78cf3-164">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="78cf3-165">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="78cf3-165">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)

[<span data-ttu-id="78cf3-166">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="78cf3-166">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="78cf3-167">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="78cf3-167">Reset-AzBatchComputeNode</span></span>](./Reset-AzBatchComputeNode.md)

[<span data-ttu-id="78cf3-168">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="78cf3-168">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)

[<span data-ttu-id="78cf3-169">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="78cf3-169">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)

