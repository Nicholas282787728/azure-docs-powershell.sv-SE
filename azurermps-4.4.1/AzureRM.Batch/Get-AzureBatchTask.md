---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4B5FE41A-090B-4859-B021-05CF0A8B7882
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTask.md
ms.openlocfilehash: fb01af87d28323e3e25c46868f94e892b835afc7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583359"
---
# <span data-ttu-id="6e3ff-101">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="6e3ff-101">Get-AzureBatchTask</span></span>

## <span data-ttu-id="6e3ff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6e3ff-102">SYNOPSIS</span></span>
<span data-ttu-id="6e3ff-103">Hämtar batchjobben för ett jobb.</span><span class="sxs-lookup"><span data-stu-id="6e3ff-103">Gets the Batch tasks for a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e3ff-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6e3ff-104">SYNTAX</span></span>

### <span data-ttu-id="6e3ff-105">ODataFilter (standard)</span><span class="sxs-lookup"><span data-stu-id="6e3ff-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchTask [-JobId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6e3ff-106">Et</span><span class="sxs-lookup"><span data-stu-id="6e3ff-106">Id</span></span>
```
Get-AzureBatchTask [-JobId] <String> [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e3ff-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="6e3ff-107">ParentObject</span></span>
```
Get-AzureBatchTask [[-Job] <PSCloudJob>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6e3ff-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6e3ff-108">DESCRIPTION</span></span>
<span data-ttu-id="6e3ff-109">Cmdleten **Get-AzureBatchTask** får Azure Batch-uppgifter för ett batchjobb.</span><span class="sxs-lookup"><span data-stu-id="6e3ff-109">The **Get-AzureBatchTask** cmdlet gets Azure Batch tasks for a Batch job.</span></span>
<span data-ttu-id="6e3ff-110">Ange ett jobb genom parametern *jobId* eller *jobb* parameter.</span><span class="sxs-lookup"><span data-stu-id="6e3ff-110">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="6e3ff-111">Om du vill få en enda uppgift anger du *ID-* parametern.</span><span class="sxs-lookup"><span data-stu-id="6e3ff-111">To get a single task, specify the *Id* parameter.</span></span>
<span data-ttu-id="6e3ff-112">Du kan ange *filter* parametern för att få de uppgifter som matchar ett open data Protocol (OData)-filter.</span><span class="sxs-lookup"><span data-stu-id="6e3ff-112">You can specify the *Filter* parameter to get the tasks that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="6e3ff-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6e3ff-113">EXAMPLES</span></span>

### <span data-ttu-id="6e3ff-114">Exempel 1: Hämta en uppgift utifrån ID</span><span class="sxs-lookup"><span data-stu-id="6e3ff-114">Example 1: Get a task by ID</span></span>
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

<span data-ttu-id="6e3ff-115">Det här kommandot får uppgiften med ID-Task03 under jobb-Job01.</span><span class="sxs-lookup"><span data-stu-id="6e3ff-115">This command gets the task with ID Task03 under job Job01.</span></span>
<span data-ttu-id="6e3ff-116">Använd Get-AzureRmBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="6e3ff-116">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="6e3ff-117">Exempel 2: Hämta alla slutförda uppgifter från ett angivet jobb</span><span class="sxs-lookup"><span data-stu-id="6e3ff-117">Example 2: Get all completed tasks from a specified job</span></span>
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

<span data-ttu-id="6e3ff-118">Det här kommandot får de slutförda uppgifterna från jobbet som har ID-Job02.</span><span class="sxs-lookup"><span data-stu-id="6e3ff-118">This command gets the completed tasks from the job that has the ID Job02.</span></span>

## <span data-ttu-id="6e3ff-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6e3ff-119">PARAMETERS</span></span>

### <span data-ttu-id="6e3ff-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6e3ff-120">-BatchContext</span></span>
<span data-ttu-id="6e3ff-121">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="6e3ff-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6e3ff-122">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="6e3ff-122">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="6e3ff-123">-Expandera</span><span class="sxs-lookup"><span data-stu-id="6e3ff-123">-Expand</span></span>
<span data-ttu-id="6e3ff-124">Anger en OData Expand-sats.</span><span class="sxs-lookup"><span data-stu-id="6e3ff-124">Specifies an OData expand clause.</span></span>
<span data-ttu-id="6e3ff-125">Ange ett värde för den här parametern för att få associerade enheter i huvudentiteten att få.</span><span class="sxs-lookup"><span data-stu-id="6e3ff-125">Specify a value for this parameter to get associated entities of the main entity to get.</span></span>

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

### <span data-ttu-id="6e3ff-126">-Filter</span><span class="sxs-lookup"><span data-stu-id="6e3ff-126">-Filter</span></span>
<span data-ttu-id="6e3ff-127">Anger en OData filter-sats för aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="6e3ff-127">Specifies an OData filter clause for tasks.</span></span>
<span data-ttu-id="6e3ff-128">Om du inte anger något filter returnerar den här cmdleten alla aktiviteter för batch-kontot eller jobbet.</span><span class="sxs-lookup"><span data-stu-id="6e3ff-128">If you do not specify a filter, this cmdlet returns all tasks for the Batch account or job.</span></span>

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

### <span data-ttu-id="6e3ff-129">-ID</span><span class="sxs-lookup"><span data-stu-id="6e3ff-129">-Id</span></span>
<span data-ttu-id="6e3ff-130">Anger ID för den uppgift som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="6e3ff-130">Specifies the ID of the task that this cmdlet gets.</span></span>
<span data-ttu-id="6e3ff-131">Du kan inte ange jokertecken.</span><span class="sxs-lookup"><span data-stu-id="6e3ff-131">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e3ff-132">-Jobb</span><span class="sxs-lookup"><span data-stu-id="6e3ff-132">-Job</span></span>
<span data-ttu-id="6e3ff-133">Anger det jobb som innehåller uppgifter som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="6e3ff-133">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="6e3ff-134">För att hämta ett **PSCloudJob** -objekt, Använd cmdleten Get-AzureBatchJob.</span><span class="sxs-lookup"><span data-stu-id="6e3ff-134">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e3ff-135">-JobId</span><span class="sxs-lookup"><span data-stu-id="6e3ff-135">-JobId</span></span>
<span data-ttu-id="6e3ff-136">Anger ID för det jobb som innehåller de uppgifter som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="6e3ff-136">Specifies the ID of the job that contains the tasks that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6e3ff-137">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="6e3ff-137">-MaxCount</span></span>
<span data-ttu-id="6e3ff-138">Anger det maximala antalet uppgifter som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="6e3ff-138">Specifies the maximum number of tasks to return.</span></span>
<span data-ttu-id="6e3ff-139">Om du anger ett värde som är noll (0) eller mindre används ingen övre gräns av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6e3ff-139">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="6e3ff-140">Standardvärdet är 1000.</span><span class="sxs-lookup"><span data-stu-id="6e3ff-140">The default value is 1000.</span></span>

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

### <span data-ttu-id="6e3ff-141">-Välj</span><span class="sxs-lookup"><span data-stu-id="6e3ff-141">-Select</span></span>
<span data-ttu-id="6e3ff-142">Anger en OData SELECT-sats.</span><span class="sxs-lookup"><span data-stu-id="6e3ff-142">Specifies an OData select clause.</span></span>
<span data-ttu-id="6e3ff-143">Ange ett värde för den här parametern för att få specifika egenskaper i stället för alla objekt egenskaper.</span><span class="sxs-lookup"><span data-stu-id="6e3ff-143">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="6e3ff-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e3ff-144">-DefaultProfile</span></span>
<span data-ttu-id="6e3ff-145">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6e3ff-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e3ff-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e3ff-146">CommonParameters</span></span>
<span data-ttu-id="6e3ff-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e3ff-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e3ff-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e3ff-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e3ff-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6e3ff-149">INPUTS</span></span>

### <span data-ttu-id="6e3ff-150">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6e3ff-150">BatchAccountContext</span></span>
<span data-ttu-id="6e3ff-151">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="6e3ff-151">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="6e3ff-152">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="6e3ff-152">PSCloudJob</span></span>
<span data-ttu-id="6e3ff-153">Parametern ' Job ' godkänner värdet av typen ' PSCloudJob ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="6e3ff-153">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="6e3ff-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6e3ff-154">OUTPUTS</span></span>

### <span data-ttu-id="6e3ff-155">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="6e3ff-155">PSCloudTask</span></span>

## <span data-ttu-id="6e3ff-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6e3ff-156">NOTES</span></span>

## <span data-ttu-id="6e3ff-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6e3ff-157">RELATED LINKS</span></span>

[<span data-ttu-id="6e3ff-158">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="6e3ff-158">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="6e3ff-159">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="6e3ff-159">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="6e3ff-160">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="6e3ff-160">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="6e3ff-161">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="6e3ff-161">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="6e3ff-162">Stopp-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="6e3ff-162">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="6e3ff-163">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="6e3ff-163">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


