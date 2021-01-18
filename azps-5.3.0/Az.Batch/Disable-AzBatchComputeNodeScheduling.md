---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 9e93d6fd17d4ba308e6d5752554fb03639fce769
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524832"
---
# <span data-ttu-id="3ddc6-101">Disable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="3ddc6-101">Disable-AzBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="3ddc6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3ddc6-102">SYNOPSIS</span></span>
<span data-ttu-id="3ddc6-103">Inaktiverar schemaläggning av aktiviteter på angiven datornod.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-103">Disables task scheduling on the specified compute node.</span></span>

## <span data-ttu-id="3ddc6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3ddc6-104">SYNTAX</span></span>

### <span data-ttu-id="3ddc6-105">ID (standard)</span><span class="sxs-lookup"><span data-stu-id="3ddc6-105">Id (Default)</span></span>
```
Disable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ddc6-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="3ddc6-106">InputObject</span></span>
```
Disable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ddc6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3ddc6-107">DESCRIPTION</span></span>
<span data-ttu-id="3ddc6-108">Cmdleten **disable-AzBatchComputeNodeScheduling** inaktiverar schemaläggning av aktiviteter på angiven datornod.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-108">The **Disable-AzBatchComputeNodeScheduling** cmdlet disables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="3ddc6-109">En datornod är en virtuell Azure-dator avsedd för en viss program belastning.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>
<span data-ttu-id="3ddc6-110">När du inaktiverar schemaläggning av aktiviteter på en datornod kan du välja att ta reda på vad som är möjligt för de jobb som finns i nodens uppgifts köer.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-110">When you disable task scheduling on a compute node you will also have the option of determining what to do about jobs currently in the node's task queue.</span></span>
<span data-ttu-id="3ddc6-111">**Disable – AzBatchComputeNodeScheduling** gör att du kan göra följande:</span><span class="sxs-lookup"><span data-stu-id="3ddc6-111">**Disable-AzBatchComputeNodeScheduling** lets you do the following:</span></span> 
- <span data-ttu-id="3ddc6-112">Avsluta uppgifterna och placera dem i jobbkön igen.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-112">Terminate the tasks and put them back in the job queue.</span></span>
<span data-ttu-id="3ddc6-113">Detta gör att aktiviteterna kan schemaläggas om på en annan datornod.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-113">This enables those tasks to be rescheduled on another compute node.</span></span> 
- <span data-ttu-id="3ddc6-114">Avsluta aktiviteterna och ta bort dem från jobbkön.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-114">Terminate the tasks and remove them from the job queue.</span></span>
<span data-ttu-id="3ddc6-115">Aktiviteter som stoppats på det här sättet ändras inte.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-115">Tasks stopped in this manner will not be rescheduled.</span></span> 
- <span data-ttu-id="3ddc6-116">Vänta tills alla aktiviteter som körs för tillfället utförs och inaktivera schemaläggning på noden beräkning.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-116">Wait for all the tasks currently being executed to complete and then disable task scheduling on the compute node.</span></span> 
- <span data-ttu-id="3ddc6-117">Vänta tills alla aktiviteter som körs ska slutföras och alla tids perioder för data upphör att gälla och inaktivera sedan schemaläggning på noden beräkning.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-117">Wait for all the running tasks to complete and all the data retention periods to expire, and then disable task scheduling on the compute node.</span></span>

## <span data-ttu-id="3ddc6-118">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3ddc6-118">EXAMPLES</span></span>

### <span data-ttu-id="3ddc6-119">Exempel 1: inaktivera schemaläggning av aktiviteter på en datornod</span><span class="sxs-lookup"><span data-stu-id="3ddc6-119">Example 1: Disable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Disable-AzBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="3ddc6-120">Dessa kommandon inaktiverar aktivitets schema för noden Compute, TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-120">These commands disable task schedule on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="3ddc6-121">För att göra detta skapar det första kommandot i exemplet en objekt referens till konto nycklarna för batch-contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-121">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="3ddc6-122">Denna objekt referens lagras i en variabel som heter $context.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-122">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="3ddc6-123">Det andra kommandot använder då den här objekt referensen och cmdleten **disable-AzBatchComputeNodeScheduling** för att ansluta till poolens icke-grupppool och inaktivera schemaläggning av aktivitet på noden TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-123">The second command then uses this object reference and the **Disable-AzBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and disable task scheduling on node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="3ddc6-124">Eftersom *DisableComputeNodeSchedulingOptions* -parametern inte inkluderade de uppgifter som för närvarande körs på noden beräkning, köas.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-124">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute node will be requeued.</span></span>

### <span data-ttu-id="3ddc6-125">Exempel 2: inaktivera schemaläggning av aktiviteter på alla datornoder i en pool</span><span class="sxs-lookup"><span data-stu-id="3ddc6-125">Example 2: Disable task scheduling on all compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzBatchComputeNodeScheduling -BatchContext $Context
```

<span data-ttu-id="3ddc6-126">De här kommandona inaktiverar schemaläggning av aktiviteter på alla noder i grupppoolens Pool06.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-126">These commands disable task scheduling on all the computer nodes in the batch pool Pool06.</span></span>
<span data-ttu-id="3ddc6-127">För att utföra den här åtgärden skapar det första kommandot i exemplet en objekt referens till konto nycklarna för batch-contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-127">To perform this task, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="3ddc6-128">Denna objekt referens lagras i en variabel som heter $context.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-128">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="3ddc6-129">Med det andra kommandot i exemplet används den här objekt referensen och **Get-AzBatchComputeNode** för att returnera en samling av alla datornoder som finns i Pool06.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-129">The second command in the example then uses this object reference and **Get-AzBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="3ddc6-130">Samlingen **avaktiverar sedan-AzBatchComputeNodeScheduling-** cmdlet för att inaktivera schemaläggning av aktiviteter för varje datornod i samlingen.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-130">That collection is then piped to then **Disable-AzBatchComputeNodeScheduling** cmdlet to disable task scheduling on each compute node in the collection.</span></span>
<span data-ttu-id="3ddc6-131">Eftersom *DisableComputeNodeSchedulingOptions* -parametern inte inkluderade de uppgifter som för närvarande körs på datornoderna köas.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-131">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute nodes will be requeued.</span></span>

## <span data-ttu-id="3ddc6-132">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3ddc6-132">PARAMETERS</span></span>

### <span data-ttu-id="3ddc6-133">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="3ddc6-133">-BatchContext</span></span>
<span data-ttu-id="3ddc6-134">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-134">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="3ddc6-135">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-135">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="3ddc6-136">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-136">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="3ddc6-137">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-137">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="3ddc6-138">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-138">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="3ddc6-139">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="3ddc6-139">-ComputeNode</span></span>
<span data-ttu-id="3ddc6-140">Anger en objekt referens till noden Compute där aktivitets schemaläggningen är inaktive rad.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-140">Specifies an object reference to the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="3ddc6-141">Den här objekt referensen skapas med Get-AzBatchComputeNode cmdlet och det returnerade datornoder-objektet sparas i en variabel.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-141">This object reference is created by using the Get-AzBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="3ddc6-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ddc6-142">-DefaultProfile</span></span>
<span data-ttu-id="3ddc6-143">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ddc6-144">-DisableSchedulingOption</span><span class="sxs-lookup"><span data-stu-id="3ddc6-144">-DisableSchedulingOption</span></span>
<span data-ttu-id="3ddc6-145">Anger hur den här cmdleten hanterar aktiviteter som körs på den dator nod där schemaläggning inaktive ras.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-145">Specifies how this cmdlet deals with any tasks currently running on the computer node where scheduling is being disabled.</span></span>
<span data-ttu-id="3ddc6-146">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3ddc6-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3ddc6-147">Köa om.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-147">Requeue.</span></span>
<span data-ttu-id="3ddc6-148">Uppgifter stoppas direkt och återgår till jobbkön.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-148">Tasks are stopped immediately and returned to the job queue.</span></span>
<span data-ttu-id="3ddc6-149">Detta gör att aktiviteter kan schemaläggas om på en annan datornod.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-149">This enables the tasks to be rescheduled on another compute node.</span></span>
<span data-ttu-id="3ddc6-150">Det här är standardvärdet.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-150">This is the default value.</span></span> 
- <span data-ttu-id="3ddc6-151">Säga upp.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-151">Terminate.</span></span>
<span data-ttu-id="3ddc6-152">Uppgifter stoppas direkt och tas bort från jobbkön.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-152">Tasks are stopped immediately and removed from the job queue.</span></span>
<span data-ttu-id="3ddc6-153">De här aktiviteterna kommer inte att schemaläggas om.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-153">These tasks will not be rescheduled.</span></span> 
- <span data-ttu-id="3ddc6-154">TaskCompletion.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-154">TaskCompletion.</span></span>
<span data-ttu-id="3ddc6-155">För tillfället pågående uppgifter kan slutföras innan aktivitets schemaläggningen är inaktive rad på noden Compute.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-155">Currently running tasks will be able to complete before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="3ddc6-156">Inga nya aktiviteter schemaläggs på den här noden.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-156">No new tasks will be scheduled on this node.</span></span> 
- <span data-ttu-id="3ddc6-157">RetainedData.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-157">RetainedData.</span></span>
<span data-ttu-id="3ddc6-158">Aktiviteter som körs för tillfället kan slutföras och data lagrings perioderna kan upphöra innan aktivitets schemaläggningen är inaktive rad på noden Compute.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-158">Currently running tasks will be able to complete and data retention periods will be able to expire before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="3ddc6-159">Inga nya aktiviteter schemaläggs på den här noden.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-159">No new tasks will be scheduled on this node.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.DisableComputeNodeSchedulingOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ddc6-160">-ID</span><span class="sxs-lookup"><span data-stu-id="3ddc6-160">-Id</span></span>
<span data-ttu-id="3ddc6-161">Anger ID för den datornod där aktivitets schemaläggningen är inaktive rad.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-161">Specifies the ID of the compute node where task scheduling is disabled.</span></span>

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

### <span data-ttu-id="3ddc6-162">-PoolId</span><span class="sxs-lookup"><span data-stu-id="3ddc6-162">-PoolId</span></span>
<span data-ttu-id="3ddc6-163">Anger ID för den gruppbearbetningssekvens som innehåller den datornod där aktivitets schemaläggningen är inaktive rad.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-163">Specifies the ID of the batch pool that contains the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="3ddc6-164">Om du använder parametern *PoolId* ska du inte använda parametern *ComputeNode* i samma kommando.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-164">If you use the *PoolId* parameter, do not use the *ComputeNode* parameter in that same command.</span></span>

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

### <span data-ttu-id="3ddc6-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ddc6-165">CommonParameters</span></span>
<span data-ttu-id="3ddc6-166">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ddc6-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ddc6-167">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ddc6-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ddc6-168">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3ddc6-168">INPUTS</span></span>

### <span data-ttu-id="3ddc6-169">Microsoft.Azure.Commands.BatCH. Modeller. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="3ddc6-169">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="3ddc6-170">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3ddc6-170">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="3ddc6-171">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3ddc6-171">OUTPUTS</span></span>

### <span data-ttu-id="3ddc6-172">System. Void</span><span class="sxs-lookup"><span data-stu-id="3ddc6-172">System.Void</span></span>

## <span data-ttu-id="3ddc6-173">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3ddc6-173">NOTES</span></span>

## <span data-ttu-id="3ddc6-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3ddc6-174">RELATED LINKS</span></span>

[<span data-ttu-id="3ddc6-175">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="3ddc6-175">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="3ddc6-176">Enable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="3ddc6-176">Enable-AzBatchComputeNodeScheduling</span></span>](./Enable-AzBatchComputeNodeScheduling.md)


