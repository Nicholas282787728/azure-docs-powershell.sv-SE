---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4B5FE41A-090B-4859-B021-05CF0A8B7882
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTask.md
ms.openlocfilehash: bf1a70dc697366099f1949878e81a25bd3adb0fa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269656"
---
# <span data-ttu-id="20a74-101">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="20a74-101">Get-AzBatchTask</span></span>

## <span data-ttu-id="20a74-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="20a74-102">SYNOPSIS</span></span>
<span data-ttu-id="20a74-103">Hämtar batchjobben för ett jobb.</span><span class="sxs-lookup"><span data-stu-id="20a74-103">Gets the Batch tasks for a job.</span></span>

## <span data-ttu-id="20a74-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="20a74-104">SYNTAX</span></span>

### <span data-ttu-id="20a74-105">ODataFilter (standard)</span><span class="sxs-lookup"><span data-stu-id="20a74-105">ODataFilter (Default)</span></span>
```
Get-AzBatchTask [-JobId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20a74-106">Et</span><span class="sxs-lookup"><span data-stu-id="20a74-106">Id</span></span>
```
Get-AzBatchTask [-JobId] <String> [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20a74-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="20a74-107">ParentObject</span></span>
```
Get-AzBatchTask [[-Job] <PSCloudJob>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="20a74-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="20a74-108">DESCRIPTION</span></span>
<span data-ttu-id="20a74-109">Cmdleten **Get-AzBatchTask** får Azure Batch-uppgifter för ett batchjobb.</span><span class="sxs-lookup"><span data-stu-id="20a74-109">The **Get-AzBatchTask** cmdlet gets Azure Batch tasks for a Batch job.</span></span>
<span data-ttu-id="20a74-110">Ange ett jobb genom parametern *jobId* eller *jobb* parameter.</span><span class="sxs-lookup"><span data-stu-id="20a74-110">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="20a74-111">Om du vill få en enda uppgift anger du *ID-* parametern.</span><span class="sxs-lookup"><span data-stu-id="20a74-111">To get a single task, specify the *Id* parameter.</span></span>
<span data-ttu-id="20a74-112">Du kan ange *filter* parametern för att få de uppgifter som matchar ett open data Protocol (OData)-filter.</span><span class="sxs-lookup"><span data-stu-id="20a74-112">You can specify the *Filter* parameter to get the tasks that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="20a74-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="20a74-113">EXAMPLES</span></span>

### <span data-ttu-id="20a74-114">Exempel 1: Hämta en uppgift utifrån ID</span><span class="sxs-lookup"><span data-stu-id="20a74-114">Example 1: Get a task by ID</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job01" -Id "Task03" -BatchContext $Context
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

<span data-ttu-id="20a74-115">Det här kommandot får uppgiften med ID-Task03 under jobb-Job01.</span><span class="sxs-lookup"><span data-stu-id="20a74-115">This command gets the task with ID Task03 under job Job01.</span></span>
<span data-ttu-id="20a74-116">Använd Get-AzBatchAccountKey cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="20a74-116">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="20a74-117">Exempel 2: Hämta alla slutförda uppgifter från ett angivet jobb</span><span class="sxs-lookup"><span data-stu-id="20a74-117">Example 2: Get all completed tasks from a specified job</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job02" -Filter "state eq 'completed'" -BatchContext $Context
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

<span data-ttu-id="20a74-118">Det här kommandot får de slutförda uppgifterna från jobbet som har ID-Job02.</span><span class="sxs-lookup"><span data-stu-id="20a74-118">This command gets the completed tasks from the job that has the ID Job02.</span></span>

## <span data-ttu-id="20a74-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="20a74-119">PARAMETERS</span></span>

### <span data-ttu-id="20a74-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="20a74-120">-BatchContext</span></span>
<span data-ttu-id="20a74-121">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="20a74-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="20a74-122">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="20a74-122">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="20a74-123">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="20a74-123">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="20a74-124">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="20a74-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="20a74-125">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="20a74-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="20a74-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20a74-126">-DefaultProfile</span></span>
<span data-ttu-id="20a74-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="20a74-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20a74-128">-Expandera</span><span class="sxs-lookup"><span data-stu-id="20a74-128">-Expand</span></span>
<span data-ttu-id="20a74-129">Anger en OData Expand-sats.</span><span class="sxs-lookup"><span data-stu-id="20a74-129">Specifies an OData expand clause.</span></span>
<span data-ttu-id="20a74-130">Ange ett värde för den här parametern för att få associerade enheter i huvudentiteten att få.</span><span class="sxs-lookup"><span data-stu-id="20a74-130">Specify a value for this parameter to get associated entities of the main entity to get.</span></span>

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

### <span data-ttu-id="20a74-131">-Filter</span><span class="sxs-lookup"><span data-stu-id="20a74-131">-Filter</span></span>
<span data-ttu-id="20a74-132">Anger en OData filter-sats för aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="20a74-132">Specifies an OData filter clause for tasks.</span></span>
<span data-ttu-id="20a74-133">Om du inte anger något filter returnerar den här cmdleten alla aktiviteter för batch-kontot eller jobbet.</span><span class="sxs-lookup"><span data-stu-id="20a74-133">If you do not specify a filter, this cmdlet returns all tasks for the Batch account or job.</span></span>

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

### <span data-ttu-id="20a74-134">-ID</span><span class="sxs-lookup"><span data-stu-id="20a74-134">-Id</span></span>
<span data-ttu-id="20a74-135">Anger ID för den uppgift som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="20a74-135">Specifies the ID of the task that this cmdlet gets.</span></span>
<span data-ttu-id="20a74-136">Du kan inte ange jokertecken.</span><span class="sxs-lookup"><span data-stu-id="20a74-136">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="20a74-137">-Jobb</span><span class="sxs-lookup"><span data-stu-id="20a74-137">-Job</span></span>
<span data-ttu-id="20a74-138">Anger det jobb som innehåller uppgifter som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="20a74-138">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="20a74-139">För att hämta ett **PSCloudJob** -objekt, Använd cmdleten Get-AzBatchJob.</span><span class="sxs-lookup"><span data-stu-id="20a74-139">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="20a74-140">-JobId</span><span class="sxs-lookup"><span data-stu-id="20a74-140">-JobId</span></span>
<span data-ttu-id="20a74-141">Anger ID för det jobb som innehåller de uppgifter som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="20a74-141">Specifies the ID of the job that contains the tasks that this cmdlet gets.</span></span>

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

### <span data-ttu-id="20a74-142">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="20a74-142">-MaxCount</span></span>
<span data-ttu-id="20a74-143">Anger det maximala antalet uppgifter som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="20a74-143">Specifies the maximum number of tasks to return.</span></span>
<span data-ttu-id="20a74-144">Om du anger ett värde som är noll (0) eller mindre används ingen övre gräns av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="20a74-144">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="20a74-145">Standardvärdet är 1000.</span><span class="sxs-lookup"><span data-stu-id="20a74-145">The default value is 1000.</span></span>

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

### <span data-ttu-id="20a74-146">-Välj</span><span class="sxs-lookup"><span data-stu-id="20a74-146">-Select</span></span>
<span data-ttu-id="20a74-147">Anger en OData SELECT-sats.</span><span class="sxs-lookup"><span data-stu-id="20a74-147">Specifies an OData select clause.</span></span>
<span data-ttu-id="20a74-148">Ange ett värde för den här parametern för att få specifika egenskaper i stället för alla objekt egenskaper.</span><span class="sxs-lookup"><span data-stu-id="20a74-148">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="20a74-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20a74-149">CommonParameters</span></span>
<span data-ttu-id="20a74-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20a74-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20a74-151">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20a74-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20a74-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="20a74-152">INPUTS</span></span>

### <span data-ttu-id="20a74-153">System. String</span><span class="sxs-lookup"><span data-stu-id="20a74-153">System.String</span></span>

### <span data-ttu-id="20a74-154">Microsoft.Azure.Commands.BatCH. Modeller. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="20a74-154">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="20a74-155">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="20a74-155">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="20a74-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="20a74-156">OUTPUTS</span></span>

### <span data-ttu-id="20a74-157">Microsoft.Azure.Commands.BatCH. Modeller. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="20a74-157">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

## <span data-ttu-id="20a74-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="20a74-158">NOTES</span></span>

## <span data-ttu-id="20a74-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="20a74-159">RELATED LINKS</span></span>

[<span data-ttu-id="20a74-160">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="20a74-160">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="20a74-161">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="20a74-161">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="20a74-162">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="20a74-162">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="20a74-163">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="20a74-163">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="20a74-164">Stopp-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="20a74-164">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="20a74-165">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="20a74-165">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
