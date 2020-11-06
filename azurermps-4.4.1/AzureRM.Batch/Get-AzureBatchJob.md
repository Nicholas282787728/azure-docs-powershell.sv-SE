---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 8BF49C4D-E7CD-4FD0-AFAC-9856239D24EC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJob.md
ms.openlocfilehash: c2aa673b9cd0f8cccc3f1a8721313f5a3236270d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577720"
---
# <span data-ttu-id="bbd90-101">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="bbd90-101">Get-AzureBatchJob</span></span>

## <span data-ttu-id="bbd90-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bbd90-102">SYNOPSIS</span></span>
<span data-ttu-id="bbd90-103">Hämtar batchjobb för ett batch-konto eller jobb schema.</span><span class="sxs-lookup"><span data-stu-id="bbd90-103">Gets Batch jobs for a Batch account or job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbd90-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bbd90-104">SYNTAX</span></span>

### <span data-ttu-id="bbd90-105">ODataFilter (standard)</span><span class="sxs-lookup"><span data-stu-id="bbd90-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchJob [-JobScheduleId <String>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bbd90-106">Et</span><span class="sxs-lookup"><span data-stu-id="bbd90-106">Id</span></span>
```
Get-AzureBatchJob [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bbd90-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="bbd90-107">ParentObject</span></span>
```
Get-AzureBatchJob [[-JobSchedule] <PSCloudJobSchedule>] [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbd90-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bbd90-108">DESCRIPTION</span></span>
<span data-ttu-id="bbd90-109">Cmdleten **Get-AzureBatchJob** hämtar Azure-kommandona för batch-kontot som anges av parametern *BatchAccountContext* .</span><span class="sxs-lookup"><span data-stu-id="bbd90-109">The **Get-AzureBatchJob** cmdlet gets the Azure Batch jobs for the Batch account specified by the *BatchAccountContext* parameter.</span></span>
<span data-ttu-id="bbd90-110">Du kan använda *ID-* parametern för att få ett enskilt jobb.</span><span class="sxs-lookup"><span data-stu-id="bbd90-110">You can use the *Id* parameter to get a single job.</span></span>
<span data-ttu-id="bbd90-111">Du kan använda parametern *filter* för att hämta de jobb som matchar ett open data Protocol (OData)-filter.</span><span class="sxs-lookup"><span data-stu-id="bbd90-111">You can use the *Filter* parameter to get the jobs that match an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="bbd90-112">Om du anger ett jobb schema-ID eller en **PSCloudJobSchedule** -instans returnerar denna cmdlet endast jobb för det jobb schema.</span><span class="sxs-lookup"><span data-stu-id="bbd90-112">If you supply a job schedule ID or **PSCloudJobSchedule** instance, this cmdlet returns only the jobs for that job schedule.</span></span>

## <span data-ttu-id="bbd90-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bbd90-113">EXAMPLES</span></span>

### <span data-ttu-id="bbd90-114">Exempel 1: Hämta ett batchjobb utifrån ID</span><span class="sxs-lookup"><span data-stu-id="bbd90-114">Example 1: Get a Batch job by ID</span></span>
```
PS C:\>Get-AzureBatchJob -Id "Job01" -BatchContext $Context
CommonEnvironmentSettings   : 
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:12:07 PM
DisplayName                 : 
ETag                        : 0x8D29535B2941439
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : Job01
JobManagerTask              : 
JobPreparationTask          : 
JobReleaseTask              : 
LastModified                : 7/25/2015 9:12:07 PM
Metadata                    : 
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               : 
PreviousStateTransitionTime : 
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:12:07 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job01
```

<span data-ttu-id="bbd90-115">Det här kommandot får jobbet med ID-Job01.</span><span class="sxs-lookup"><span data-stu-id="bbd90-115">This command gets the job that has the ID Job01.</span></span>
<span data-ttu-id="bbd90-116">Använd Get-AzureRmBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="bbd90-116">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="bbd90-117">Exempel 2: Hämta alla aktiva jobb för ett schema</span><span class="sxs-lookup"><span data-stu-id="bbd90-117">Example 2: Get all active jobs for a job schedule</span></span>
```
PS C:\>Get-AzureBatchJob -JobScheduleId "JobSchedule27" -Filter "state eq 'active'" -BatchContext $Context
CommonEnvironmentSettings   : 
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:15:44 PM
DisplayName                 : 
ETag                        : 0x8D2953633DD13E1
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : JobSchedule27:job-1
JobManagerTask              : 
JobPreparationTask          : 
JobReleaseTask              : 
LastModified                : 7/25/2015 9:15:44 PM
Metadata                    : 
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               : 
PreviousStateTransitionTime : 
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:44 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/JobSchedule27:job-1
```

<span data-ttu-id="bbd90-118">Det här kommandot får aktiva jobb för det jobb schema som har ID-JobSchedule27.</span><span class="sxs-lookup"><span data-stu-id="bbd90-118">This command gets the active jobs for the job schedule that has the ID JobSchedule27.</span></span>

### <span data-ttu-id="bbd90-119">Exempel 3: hämtar alla jobb under ett schema med hjälp av försäljnings förloppet</span><span class="sxs-lookup"><span data-stu-id="bbd90-119">Example 3: Gets all jobs under a job schedule by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchJobSchedule -Id "JobSchedule27" -BatchContext $Context | Get-AzureBatchJob -BatchContext $Context
CommonEnvironmentSettings   : 
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:15:44 PM
DisplayName                 : 
ETag                        : 0x8D2953633DD13E1
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : JobSchedule27:job-1
JobManagerTask              : 
JobPreparationTask          : 
JobReleaseTask              : 
LastModified                : 7/25/2015 9:15:44 PM
Metadata                    : 
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               : 
PreviousStateTransitionTime : 
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:44 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/JobSchedule27:job-1
```

<span data-ttu-id="bbd90-120">Det här kommandot får jobbet schema med ID-JobSchedule27 med hjälp av Get-AzureBatchJobSchedule cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbd90-120">This command gets the job schedule that has the ID JobSchedule27 by using the Get-AzureBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="bbd90-121">Kommandot skickar schemat till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="bbd90-121">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bbd90-122">Kommandot får alla jobb för detta jobb schema.</span><span class="sxs-lookup"><span data-stu-id="bbd90-122">The command gets all jobs for that job schedule.</span></span>

## <span data-ttu-id="bbd90-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bbd90-123">PARAMETERS</span></span>

### <span data-ttu-id="bbd90-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="bbd90-124">-BatchContext</span></span>
<span data-ttu-id="bbd90-125">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="bbd90-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="bbd90-126">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="bbd90-126">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="bbd90-127">-Expandera</span><span class="sxs-lookup"><span data-stu-id="bbd90-127">-Expand</span></span>
<span data-ttu-id="bbd90-128">Anger en Open data Protocol (OData) Expand-sats.</span><span class="sxs-lookup"><span data-stu-id="bbd90-128">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="bbd90-129">Ange ett värde för den här parametern för att hämta associerade enheter för huvud enheten som du får.</span><span class="sxs-lookup"><span data-stu-id="bbd90-129">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="bbd90-130">-Filter</span><span class="sxs-lookup"><span data-stu-id="bbd90-130">-Filter</span></span>
<span data-ttu-id="bbd90-131">Anger en OData filter-sats för jobb.</span><span class="sxs-lookup"><span data-stu-id="bbd90-131">Specifies an OData filter clause for jobs.</span></span>
<span data-ttu-id="bbd90-132">Om du inte anger något filter returnerar denna cmdlet alla jobb för batch-kontot eller jobb schemat.</span><span class="sxs-lookup"><span data-stu-id="bbd90-132">If you do not specify a filter, this cmdlet returns all jobs for the Batch account or job schedule.</span></span>

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

### <span data-ttu-id="bbd90-133">-ID</span><span class="sxs-lookup"><span data-stu-id="bbd90-133">-Id</span></span>
<span data-ttu-id="bbd90-134">Anger ID för det jobb som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="bbd90-134">Specifies the ID of the job that this cmdlet gets.</span></span>
<span data-ttu-id="bbd90-135">Du kan inte ange jokertecken.</span><span class="sxs-lookup"><span data-stu-id="bbd90-135">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbd90-136">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="bbd90-136">-JobSchedule</span></span>
<span data-ttu-id="bbd90-137">Anger ett **PSCloudJobSchedule** -objekt som representerar den jobbmall som innehåller jobben.</span><span class="sxs-lookup"><span data-stu-id="bbd90-137">Specifies a **PSCloudJobSchedule** object that represents the job schedule which contains the jobs.</span></span>
<span data-ttu-id="bbd90-138">För att hämta ett **PSCloudJobSchedule** -objekt, Använd cmdleten Get-AzureBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="bbd90-138">To obtain a **PSCloudJobSchedule** object, use the Get-AzureBatchJobSchedule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bbd90-139">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="bbd90-139">-JobScheduleId</span></span>
<span data-ttu-id="bbd90-140">Anger ID för den jobbmall som innehåller projekten.</span><span class="sxs-lookup"><span data-stu-id="bbd90-140">Specifies the ID of the job schedule which contains the jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbd90-141">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="bbd90-141">-MaxCount</span></span>
<span data-ttu-id="bbd90-142">Anger maximalt antal jobb som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="bbd90-142">Specifies the maximum number of jobs to return.</span></span>
<span data-ttu-id="bbd90-143">Om du anger ett värde som är noll (0) eller mindre används ingen övre gräns av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bbd90-143">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="bbd90-144">Standardvärdet är 1000.</span><span class="sxs-lookup"><span data-stu-id="bbd90-144">The default value is 1000.</span></span>

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

### <span data-ttu-id="bbd90-145">-Välj</span><span class="sxs-lookup"><span data-stu-id="bbd90-145">-Select</span></span>
<span data-ttu-id="bbd90-146">Anger en OData SELECT-sats.</span><span class="sxs-lookup"><span data-stu-id="bbd90-146">Specifies an OData select clause.</span></span>
<span data-ttu-id="bbd90-147">Ange ett värde för den här parametern för att få specifika egenskaper i stället för alla objekt egenskaper.</span><span class="sxs-lookup"><span data-stu-id="bbd90-147">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="bbd90-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbd90-148">-DefaultProfile</span></span>
<span data-ttu-id="bbd90-149">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bbd90-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbd90-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbd90-150">CommonParameters</span></span>
<span data-ttu-id="bbd90-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbd90-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbd90-152">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbd90-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbd90-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bbd90-153">INPUTS</span></span>

### <span data-ttu-id="bbd90-154">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="bbd90-154">BatchAccountContext</span></span>
<span data-ttu-id="bbd90-155">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="bbd90-155">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="bbd90-156">PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="bbd90-156">PSCloudJobSchedule</span></span>
<span data-ttu-id="bbd90-157">Parametern ' JobSchedule ' godkänner värdet av typen ' PSCloudJobSchedule ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="bbd90-157">Parameter 'JobSchedule' accepts value of type 'PSCloudJobSchedule' from the pipeline</span></span>

## <span data-ttu-id="bbd90-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bbd90-158">OUTPUTS</span></span>

### <span data-ttu-id="bbd90-159">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="bbd90-159">PSCloudJob</span></span>

## <span data-ttu-id="bbd90-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bbd90-160">NOTES</span></span>

## <span data-ttu-id="bbd90-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bbd90-161">RELATED LINKS</span></span>

[<span data-ttu-id="bbd90-162">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="bbd90-162">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="bbd90-163">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="bbd90-163">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="bbd90-164">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="bbd90-164">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="bbd90-165">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="bbd90-165">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="bbd90-166">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="bbd90-166">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="bbd90-167">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="bbd90-167">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="bbd90-168">Stopp-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="bbd90-168">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="bbd90-169">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="bbd90-169">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


