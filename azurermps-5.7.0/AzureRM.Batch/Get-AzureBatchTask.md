---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4B5FE41A-090B-4859-B021-05CF0A8B7882
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTask.md
ms.openlocfilehash: 1a177f0987f27f81f0ab27d5e35db11df17ae005
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574426"
---
# <span data-ttu-id="986ea-101">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="986ea-101">Get-AzureBatchTask</span></span>

## <span data-ttu-id="986ea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="986ea-102">SYNOPSIS</span></span>
<span data-ttu-id="986ea-103">Hämtar batchjobben för ett jobb.</span><span class="sxs-lookup"><span data-stu-id="986ea-103">Gets the Batch tasks for a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="986ea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="986ea-104">SYNTAX</span></span>

### <span data-ttu-id="986ea-105">ODataFilter (standard)</span><span class="sxs-lookup"><span data-stu-id="986ea-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchTask [-JobId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="986ea-106">Et</span><span class="sxs-lookup"><span data-stu-id="986ea-106">Id</span></span>
```
Get-AzureBatchTask [-JobId] <String> [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="986ea-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="986ea-107">ParentObject</span></span>
```
Get-AzureBatchTask [[-Job] <PSCloudJob>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="986ea-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="986ea-108">DESCRIPTION</span></span>
<span data-ttu-id="986ea-109">Cmdleten **Get-AzureBatchTask** får Azure Batch-uppgifter för ett batchjobb.</span><span class="sxs-lookup"><span data-stu-id="986ea-109">The **Get-AzureBatchTask** cmdlet gets Azure Batch tasks for a Batch job.</span></span>
<span data-ttu-id="986ea-110">Ange ett jobb genom parametern *jobId* eller *jobb* parameter.</span><span class="sxs-lookup"><span data-stu-id="986ea-110">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="986ea-111">Om du vill få en enda uppgift anger du *ID-* parametern.</span><span class="sxs-lookup"><span data-stu-id="986ea-111">To get a single task, specify the *Id* parameter.</span></span>
<span data-ttu-id="986ea-112">Du kan ange *filter* parametern för att få de uppgifter som matchar ett open data Protocol (OData)-filter.</span><span class="sxs-lookup"><span data-stu-id="986ea-112">You can specify the *Filter* parameter to get the tasks that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="986ea-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="986ea-113">EXAMPLES</span></span>

### <span data-ttu-id="986ea-114">Exempel 1: Hämta en uppgift utifrån ID</span><span class="sxs-lookup"><span data-stu-id="986ea-114">Example 1: Get a task by ID</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job01" -Id "Task03" -BatchContext $Context
AffinityInformation         : 
CommandLine                 : cmd /c dir /s
ComputeNodeInformation      : Microsoft.Azure.Commands.Batch.Models.PSComputeNodeInformation
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
CreationTime                : 7/25/2015 11:24:52 PM
DisplayName                 : 
EnvironmentSettings         : 
ETag                        : 0x8D295483E08BD9D
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSTaskExecutionInformation
Id                          : Task03
LastModified                : 7/25/2015 11:24:52 PM
PreviousState               : Running
PreviousStateTransitionTime : 7/25/2015 11:24:59 PM
ResourceFiles               : 
RunElevated                 : False
State                       : Completed
StateTransitionTime         : 7/25/2015 11:24:59 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job01/tasks/Task03
```

<span data-ttu-id="986ea-115">Det här kommandot får uppgiften med ID-Task03 under jobb-Job01.</span><span class="sxs-lookup"><span data-stu-id="986ea-115">This command gets the task with ID Task03 under job Job01.</span></span>
<span data-ttu-id="986ea-116">Använd Get-AzureRmBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="986ea-116">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="986ea-117">Exempel 2: Hämta alla slutförda uppgifter från ett angivet jobb</span><span class="sxs-lookup"><span data-stu-id="986ea-117">Example 2: Get all completed tasks from a specified job</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job02" -Filter "state eq 'completed'" -BatchContext $Context
AffinityInformation         : 
CommandLine                 : cmd /c dir /s
ComputeNodeInformation      : Microsoft.Azure.Commands.Batch.Models.PSComputeNodeInformation
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
CreationTime                : 3/24/2015 10:21:51 PM
EnvironmentSettings         : 
ETag                        : 0x8D295483E08BD9D
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSTaskExecutionInformation
Id                          : Task17
LastModified                : 3/24/2015 10:21:51 PM
PreviousState               : Running
PreviousStateTransitionTime : 3/24/2015 10:22:00 PM
ResourceFiles               : 
RunElevated                 : False
State                       : Completed
StateTransitionTime         : 3/24/2015 10:22:00 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job02/tasks/Task17

AffinityInformation         : 
CommandLine                 : cmd /c echo hello > newFile.txt
ComputeNodeInformation      : Microsoft.Azure.Commands.Batch.Models.PSComputeNodeInformation
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
CreationTime                : 3/24/2015 10:21:51 PM
EnvironmentSettings         : 
ETag                        : 0x8D295483E08BD9D
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSTaskExecutionInformation
Id                          : Task27
LastModified                : 3/24/2015 10:23:35 PM
PreviousState               : Running
PreviousStateTransitionTime : 3/24/2015 10:23:37 PM
ResourceFiles               : 
RunElevated                 : True
State                       : Completed
StateTransitionTime         : 3/24/2015 10:23:37 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job02/tasks/Task27
```

<span data-ttu-id="986ea-118">Det här kommandot får de slutförda uppgifterna från jobbet som har ID-Job02.</span><span class="sxs-lookup"><span data-stu-id="986ea-118">This command gets the completed tasks from the job that has the ID Job02.</span></span>

## <span data-ttu-id="986ea-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="986ea-119">PARAMETERS</span></span>

### <span data-ttu-id="986ea-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="986ea-120">-BatchContext</span></span>
<span data-ttu-id="986ea-121">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="986ea-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="986ea-122">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="986ea-122">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="986ea-123">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="986ea-123">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="986ea-124">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="986ea-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="986ea-125">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="986ea-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="986ea-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="986ea-126">-DefaultProfile</span></span>
<span data-ttu-id="986ea-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="986ea-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="986ea-128">-Expandera</span><span class="sxs-lookup"><span data-stu-id="986ea-128">-Expand</span></span>
<span data-ttu-id="986ea-129">Anger en OData Expand-sats.</span><span class="sxs-lookup"><span data-stu-id="986ea-129">Specifies an OData expand clause.</span></span>
<span data-ttu-id="986ea-130">Ange ett värde för den här parametern för att få associerade enheter i huvudentiteten att få.</span><span class="sxs-lookup"><span data-stu-id="986ea-130">Specify a value for this parameter to get associated entities of the main entity to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="986ea-131">-Filter</span><span class="sxs-lookup"><span data-stu-id="986ea-131">-Filter</span></span>
<span data-ttu-id="986ea-132">Anger en OData filter-sats för aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="986ea-132">Specifies an OData filter clause for tasks.</span></span>
<span data-ttu-id="986ea-133">Om du inte anger något filter returnerar den här cmdleten alla aktiviteter för batch-kontot eller jobbet.</span><span class="sxs-lookup"><span data-stu-id="986ea-133">If you do not specify a filter, this cmdlet returns all tasks for the Batch account or job.</span></span>

```yaml
Type: String
Parameter Sets: ODataFilter, ParentObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="986ea-134">-ID</span><span class="sxs-lookup"><span data-stu-id="986ea-134">-Id</span></span>
<span data-ttu-id="986ea-135">Anger ID för den uppgift som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="986ea-135">Specifies the ID of the task that this cmdlet gets.</span></span>
<span data-ttu-id="986ea-136">Du kan inte ange jokertecken.</span><span class="sxs-lookup"><span data-stu-id="986ea-136">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="986ea-137">-Jobb</span><span class="sxs-lookup"><span data-stu-id="986ea-137">-Job</span></span>
<span data-ttu-id="986ea-138">Anger det jobb som innehåller uppgifter som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="986ea-138">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="986ea-139">För att hämta ett **PSCloudJob** -objekt, Använd cmdleten Get-AzureBatchJob.</span><span class="sxs-lookup"><span data-stu-id="986ea-139">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

```yaml
Type: PSCloudJob
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="986ea-140">-JobId</span><span class="sxs-lookup"><span data-stu-id="986ea-140">-JobId</span></span>
<span data-ttu-id="986ea-141">Anger ID för det jobb som innehåller de uppgifter som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="986ea-141">Specifies the ID of the job that contains the tasks that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ODataFilter, Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="986ea-142">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="986ea-142">-MaxCount</span></span>
<span data-ttu-id="986ea-143">Anger det maximala antalet uppgifter som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="986ea-143">Specifies the maximum number of tasks to return.</span></span>
<span data-ttu-id="986ea-144">Om du anger ett värde som är noll (0) eller mindre används ingen övre gräns av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="986ea-144">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="986ea-145">Standardvärdet är 1000.</span><span class="sxs-lookup"><span data-stu-id="986ea-145">The default value is 1000.</span></span>

```yaml
Type: Int32
Parameter Sets: ODataFilter, ParentObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="986ea-146">-Välj</span><span class="sxs-lookup"><span data-stu-id="986ea-146">-Select</span></span>
<span data-ttu-id="986ea-147">Anger en OData SELECT-sats.</span><span class="sxs-lookup"><span data-stu-id="986ea-147">Specifies an OData select clause.</span></span>
<span data-ttu-id="986ea-148">Ange ett värde för den här parametern för att få specifika egenskaper i stället för alla objekt egenskaper.</span><span class="sxs-lookup"><span data-stu-id="986ea-148">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="986ea-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="986ea-149">CommonParameters</span></span>
<span data-ttu-id="986ea-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="986ea-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="986ea-151">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="986ea-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="986ea-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="986ea-152">INPUTS</span></span>

### <span data-ttu-id="986ea-153">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="986ea-153">BatchAccountContext</span></span>
<span data-ttu-id="986ea-154">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="986ea-154">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="986ea-155">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="986ea-155">PSCloudJob</span></span>
<span data-ttu-id="986ea-156">Parametern ' Job ' godkänner värdet av typen ' PSCloudJob ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="986ea-156">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="986ea-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="986ea-157">OUTPUTS</span></span>

### <span data-ttu-id="986ea-158">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="986ea-158">PSCloudTask</span></span>

## <span data-ttu-id="986ea-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="986ea-159">NOTES</span></span>

## <span data-ttu-id="986ea-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="986ea-160">RELATED LINKS</span></span>

[<span data-ttu-id="986ea-161">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="986ea-161">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="986ea-162">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="986ea-162">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="986ea-163">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="986ea-163">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="986ea-164">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="986ea-164">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="986ea-165">Stopp-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="986ea-165">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="986ea-166">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="986ea-166">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


