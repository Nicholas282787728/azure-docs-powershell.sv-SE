---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchComputeNodeScheduling.md
ms.openlocfilehash: 778347394e9793b95434e1b308bbdb4e28fc0915
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583368"
---
# <span data-ttu-id="965aa-101">Disable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="965aa-101">Disable-AzureBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="965aa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="965aa-102">SYNOPSIS</span></span>
<span data-ttu-id="965aa-103">Inaktiverar schemaläggning av aktiviteter på angiven datornod.</span><span class="sxs-lookup"><span data-stu-id="965aa-103">Disables task scheduling on the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="965aa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="965aa-104">SYNTAX</span></span>

### <span data-ttu-id="965aa-105">ID (standard)</span><span class="sxs-lookup"><span data-stu-id="965aa-105">Id (Default)</span></span>
```
Disable-AzureBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="965aa-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="965aa-106">InputObject</span></span>
```
Disable-AzureBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="965aa-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="965aa-107">DESCRIPTION</span></span>
<span data-ttu-id="965aa-108">Cmdleten **disable-AzureBatchComputeNodeScheduling** inaktiverar schemaläggning av aktiviteter på angiven datornod.</span><span class="sxs-lookup"><span data-stu-id="965aa-108">The **Disable-AzureBatchComputeNodeScheduling** cmdlet disables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="965aa-109">En datornod är en virtuell Azure-dator avsedd för en viss program belastning.</span><span class="sxs-lookup"><span data-stu-id="965aa-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>
<span data-ttu-id="965aa-110">När du inaktiverar schemaläggning av aktiviteter på en datornod kan du välja att ta reda på vad som är möjligt för de jobb som finns i nodens uppgifts köer.</span><span class="sxs-lookup"><span data-stu-id="965aa-110">When you disable task scheduling on a compute node you will also have the option of determining what to do about jobs currently in the node's task queue.</span></span>
<span data-ttu-id="965aa-111">**Disable – AzureBatchComputeNodeScheduling** gör att du kan göra följande:</span><span class="sxs-lookup"><span data-stu-id="965aa-111">**Disable-AzureBatchComputeNodeScheduling** lets you do the following:</span></span> 

- <span data-ttu-id="965aa-112">Avsluta uppgifterna och placera dem i jobbkön igen.</span><span class="sxs-lookup"><span data-stu-id="965aa-112">Terminate the tasks and put them back in the job queue.</span></span>
<span data-ttu-id="965aa-113">Detta gör att aktiviteterna kan schemaläggas om på en annan datornod.</span><span class="sxs-lookup"><span data-stu-id="965aa-113">This enables those tasks to be rescheduled on another compute node.</span></span> 
- <span data-ttu-id="965aa-114">Avsluta aktiviteterna och ta bort dem från jobbkön.</span><span class="sxs-lookup"><span data-stu-id="965aa-114">Terminate the tasks and remove them from the job queue.</span></span>
<span data-ttu-id="965aa-115">Aktiviteter som stoppats på det här sättet ändras inte.</span><span class="sxs-lookup"><span data-stu-id="965aa-115">Tasks stopped in this manner will not be rescheduled.</span></span> 
- <span data-ttu-id="965aa-116">Vänta tills alla aktiviteter som körs för tillfället utförs och inaktivera schemaläggning på noden beräkning.</span><span class="sxs-lookup"><span data-stu-id="965aa-116">Wait for all the tasks currently being executed to complete and then disable task scheduling on the compute node.</span></span> 
- <span data-ttu-id="965aa-117">Vänta tills alla aktiviteter som körs ska slutföras och alla tids perioder för data upphör att gälla och inaktivera sedan schemaläggning på noden beräkning.</span><span class="sxs-lookup"><span data-stu-id="965aa-117">Wait for all the running tasks to complete and all the data retention periods to expire, and then disable task scheduling on the compute node.</span></span>

## <span data-ttu-id="965aa-118">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="965aa-118">EXAMPLES</span></span>

### <span data-ttu-id="965aa-119">Exempel 1: inaktivera schemaläggning av aktiviteter på en datornod</span><span class="sxs-lookup"><span data-stu-id="965aa-119">Example 1: Disable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Disable-AzureBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="965aa-120">Dessa kommandon inaktiverar aktivitets schema för noden Compute, TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="965aa-120">These commands disable task schedule on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="965aa-121">För att göra detta skapar det första kommandot i exemplet en objekt referens till konto nycklarna för batch-contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="965aa-121">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="965aa-122">Denna objekt referens lagras i en variabel som heter $context.</span><span class="sxs-lookup"><span data-stu-id="965aa-122">This object reference is stored in a variable named $context.</span></span>

<span data-ttu-id="965aa-123">Det andra kommandot använder då den här objekt referensen och cmdleten **disable-AzureBatchComputeNodeScheduling** för att ansluta till poolens icke-grupppool och inaktivera schemaläggning av aktivitet på noden TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="965aa-123">The second command then uses this object reference and the **Disable-AzureBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and disable task scheduling on node tvm-1783593343_34-20151117t222514z.</span></span>

<span data-ttu-id="965aa-124">Eftersom *DisableComputeNodeSchedulingOptions* -parametern inte inkluderade de uppgifter som för närvarande körs på noden beräkning, köas.</span><span class="sxs-lookup"><span data-stu-id="965aa-124">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute node will be requeued.</span></span>

### <span data-ttu-id="965aa-125">Exempel 2: inaktivera schemaläggning av aktiviteter på alla datornoder i en pool</span><span class="sxs-lookup"><span data-stu-id="965aa-125">Example 2: Disable task scheduling on all compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzureBatchComputeNodeScheduling -BatchContext $Context
```

<span data-ttu-id="965aa-126">De här kommandona inaktiverar schemaläggning av aktiviteter på alla noder i grupppoolens Pool06.</span><span class="sxs-lookup"><span data-stu-id="965aa-126">These commands disable task scheduling on all the computer nodes in the batch pool Pool06.</span></span>
<span data-ttu-id="965aa-127">För att utföra den här åtgärden skapar det första kommandot i exemplet en objekt referens till konto nycklarna för batch-contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="965aa-127">To perform this task, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="965aa-128">Denna objekt referens lagras i en variabel som heter $context.</span><span class="sxs-lookup"><span data-stu-id="965aa-128">This object reference is stored in a variable named $context.</span></span>

<span data-ttu-id="965aa-129">Med det andra kommandot i exemplet används den här objekt referensen och **Get-AzureBatchComputeNode** för att returnera en samling av alla datornoder som finns i Pool06.</span><span class="sxs-lookup"><span data-stu-id="965aa-129">The second command in the example then uses this object reference and **Get-AzureBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="965aa-130">Samlingen **avaktiverar sedan-AzureBatchComputeNodeScheduling-** cmdlet för att inaktivera schemaläggning av aktiviteter för varje datornod i samlingen.</span><span class="sxs-lookup"><span data-stu-id="965aa-130">That collection is then piped to then **Disable-AzureBatchComputeNodeScheduling** cmdlet to disable task scheduling on each compute node in the collection.</span></span>

<span data-ttu-id="965aa-131">Eftersom *DisableComputeNodeSchedulingOptions* -parametern inte inkluderade de uppgifter som för närvarande körs på datornoderna köas.</span><span class="sxs-lookup"><span data-stu-id="965aa-131">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute nodes will be requeued.</span></span>

## <span data-ttu-id="965aa-132">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="965aa-132">PARAMETERS</span></span>

### <span data-ttu-id="965aa-133">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="965aa-133">-BatchContext</span></span>
<span data-ttu-id="965aa-134">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="965aa-134">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="965aa-135">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="965aa-135">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="965aa-136">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="965aa-136">-ComputeNode</span></span>
<span data-ttu-id="965aa-137">Anger en objekt referens till noden Compute där aktivitets schemaläggningen är inaktive rad.</span><span class="sxs-lookup"><span data-stu-id="965aa-137">Specifies an object reference to the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="965aa-138">Den här objekt referensen skapas med Get-AzureBatchComputeNode cmdlet och det returnerade datornoder-objektet sparas i en variabel.</span><span class="sxs-lookup"><span data-stu-id="965aa-138">This object reference is created by using the Get-AzureBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="965aa-139">-DisableSchedulingOption</span><span class="sxs-lookup"><span data-stu-id="965aa-139">-DisableSchedulingOption</span></span>
<span data-ttu-id="965aa-140">Anger hur den här cmdleten hanterar aktiviteter som körs på den dator nod där schemaläggning inaktive ras.</span><span class="sxs-lookup"><span data-stu-id="965aa-140">Specifies how this cmdlet deals with any tasks currently running on the computer node where scheduling is being disabled.</span></span>
<span data-ttu-id="965aa-141">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="965aa-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="965aa-142">Köa om.</span><span class="sxs-lookup"><span data-stu-id="965aa-142">Requeue.</span></span>
<span data-ttu-id="965aa-143">Uppgifter stoppas direkt och återgår till jobbkön.</span><span class="sxs-lookup"><span data-stu-id="965aa-143">Tasks are stopped immediately and returned to the job queue.</span></span>
<span data-ttu-id="965aa-144">Detta gör att aktiviteter kan schemaläggas om på en annan datornod.</span><span class="sxs-lookup"><span data-stu-id="965aa-144">This enables the tasks to be rescheduled on another compute node.</span></span>
<span data-ttu-id="965aa-145">Det här är standardvärdet.</span><span class="sxs-lookup"><span data-stu-id="965aa-145">This is the default value.</span></span> 
- <span data-ttu-id="965aa-146">Säga upp.</span><span class="sxs-lookup"><span data-stu-id="965aa-146">Terminate.</span></span>
<span data-ttu-id="965aa-147">Uppgifter stoppas direkt och tas bort från jobbkön.</span><span class="sxs-lookup"><span data-stu-id="965aa-147">Tasks are stopped immediately and removed from the job queue.</span></span>
<span data-ttu-id="965aa-148">De här aktiviteterna kommer inte att schemaläggas om.</span><span class="sxs-lookup"><span data-stu-id="965aa-148">These tasks will not be rescheduled.</span></span> 
- <span data-ttu-id="965aa-149">TaskCompletion.</span><span class="sxs-lookup"><span data-stu-id="965aa-149">TaskCompletion.</span></span>
<span data-ttu-id="965aa-150">För tillfället pågående uppgifter kan slutföras innan aktivitets schemaläggningen är inaktive rad på noden Compute.</span><span class="sxs-lookup"><span data-stu-id="965aa-150">Currently running tasks will be able to complete before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="965aa-151">Inga nya aktiviteter schemaläggs på den här noden.</span><span class="sxs-lookup"><span data-stu-id="965aa-151">No new tasks will be scheduled on this node.</span></span> 
- <span data-ttu-id="965aa-152">RetainedData.</span><span class="sxs-lookup"><span data-stu-id="965aa-152">RetainedData.</span></span>
<span data-ttu-id="965aa-153">Aktiviteter som körs för tillfället kan slutföras och data lagrings perioderna kan upphöra innan aktivitets schemaläggningen är inaktive rad på noden Compute.</span><span class="sxs-lookup"><span data-stu-id="965aa-153">Currently running tasks will be able to complete and data retention periods will be able to expire before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="965aa-154">Inga nya aktiviteter schemaläggs på den här noden.</span><span class="sxs-lookup"><span data-stu-id="965aa-154">No new tasks will be scheduled on this node.</span></span>

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

### <span data-ttu-id="965aa-155">-ID</span><span class="sxs-lookup"><span data-stu-id="965aa-155">-Id</span></span>
<span data-ttu-id="965aa-156">Anger ID för den datornod där aktivitets schemaläggningen är inaktive rad.</span><span class="sxs-lookup"><span data-stu-id="965aa-156">Specifies the ID of the compute node where task scheduling is disabled.</span></span>

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

### <span data-ttu-id="965aa-157">-PoolId</span><span class="sxs-lookup"><span data-stu-id="965aa-157">-PoolId</span></span>
<span data-ttu-id="965aa-158">Anger ID för den gruppbearbetningssekvens som innehåller den datornod där aktivitets schemaläggningen är inaktive rad.</span><span class="sxs-lookup"><span data-stu-id="965aa-158">Specifies the ID of the batch pool that contains the compute node where task scheduling is disabled.</span></span>

<span data-ttu-id="965aa-159">Om du använder parametern *PoolId* ska du inte använda parametern *ComputeNode* i samma kommando.</span><span class="sxs-lookup"><span data-stu-id="965aa-159">If you use the *PoolId* parameter, do not use the *ComputeNode* parameter in that same command.</span></span>

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

### <span data-ttu-id="965aa-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="965aa-160">-DefaultProfile</span></span>
<span data-ttu-id="965aa-161">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="965aa-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="965aa-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="965aa-162">CommonParameters</span></span>
<span data-ttu-id="965aa-163">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="965aa-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="965aa-164">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="965aa-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="965aa-165">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="965aa-165">INPUTS</span></span>

### <span data-ttu-id="965aa-166">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="965aa-166">BatchAccountContext</span></span>
<span data-ttu-id="965aa-167">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="965aa-167">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="965aa-168">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="965aa-168">PSComputeNode</span></span>
<span data-ttu-id="965aa-169">Parametern ' ComputeNode ' godkänner värdet av typen ' PSComputeNode ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="965aa-169">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="965aa-170">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="965aa-170">OUTPUTS</span></span>

## <span data-ttu-id="965aa-171">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="965aa-171">NOTES</span></span>

## <span data-ttu-id="965aa-172">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="965aa-172">RELATED LINKS</span></span>

[<span data-ttu-id="965aa-173">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="965aa-173">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="965aa-174">Enable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="965aa-174">Enable-AzureBatchComputeNodeScheduling</span></span>](./Enable-AzureBatchComputeNodeScheduling.md)

