---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8BF49C4D-E7CD-4FD0-AFAC-9856239D24EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJob.md
ms.openlocfilehash: 332bdb8d32b42d391518d50aef82436675cf3f9e
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93755122"
---
# <span data-ttu-id="94ac4-101">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="94ac4-101">Get-AzBatchJob</span></span>

## <span data-ttu-id="94ac4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="94ac4-102">SYNOPSIS</span></span>
<span data-ttu-id="94ac4-103">Hämtar batchjobb för ett batch-konto eller jobb schema.</span><span class="sxs-lookup"><span data-stu-id="94ac4-103">Gets Batch jobs for a Batch account or job schedule.</span></span>

## <span data-ttu-id="94ac4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="94ac4-104">SYNTAX</span></span>

### <span data-ttu-id="94ac4-105">ODataFilter (standard)</span><span class="sxs-lookup"><span data-stu-id="94ac4-105">ODataFilter (Default)</span></span>
```
Get-AzBatchJob [-JobScheduleId <String>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="94ac4-106">Et</span><span class="sxs-lookup"><span data-stu-id="94ac4-106">Id</span></span>
```
Get-AzBatchJob [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94ac4-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="94ac4-107">ParentObject</span></span>
```
Get-AzBatchJob [[-JobSchedule] <PSCloudJobSchedule>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="94ac4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="94ac4-108">DESCRIPTION</span></span>
<span data-ttu-id="94ac4-109">Cmdleten **Get-AzBatchJob** hämtar Azure-kommandona för batch-kontot som anges av parametern *BatchAccountContext* .</span><span class="sxs-lookup"><span data-stu-id="94ac4-109">The **Get-AzBatchJob** cmdlet gets the Azure Batch jobs for the Batch account specified by the *BatchAccountContext* parameter.</span></span>
<span data-ttu-id="94ac4-110">Du kan använda *ID-* parametern för att få ett enskilt jobb.</span><span class="sxs-lookup"><span data-stu-id="94ac4-110">You can use the *Id* parameter to get a single job.</span></span>
<span data-ttu-id="94ac4-111">Du kan använda parametern *filter* för att hämta de jobb som matchar ett open data Protocol (OData)-filter.</span><span class="sxs-lookup"><span data-stu-id="94ac4-111">You can use the *Filter* parameter to get the jobs that match an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="94ac4-112">Om du anger ett jobb schema-ID eller en **PSCloudJobSchedule** -instans returnerar denna cmdlet endast jobb för det jobb schema.</span><span class="sxs-lookup"><span data-stu-id="94ac4-112">If you supply a job schedule ID or **PSCloudJobSchedule** instance, this cmdlet returns only the jobs for that job schedule.</span></span>

## <span data-ttu-id="94ac4-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="94ac4-113">EXAMPLES</span></span>

### <span data-ttu-id="94ac4-114">Exempel 1: Hämta ett batchjobb utifrån ID</span><span class="sxs-lookup"><span data-stu-id="94ac4-114">Example 1: Get a Batch job by ID</span></span>
```
PS C:\>Get-AzBatchJob -Id "Job01" -BatchContext $Context
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

<span data-ttu-id="94ac4-115">Det här kommandot får jobbet med ID-Job01.</span><span class="sxs-lookup"><span data-stu-id="94ac4-115">This command gets the job that has the ID Job01.</span></span>
<span data-ttu-id="94ac4-116">Använd Get-AzBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="94ac4-116">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="94ac4-117">Exempel 2: Hämta alla aktiva jobb för ett schema</span><span class="sxs-lookup"><span data-stu-id="94ac4-117">Example 2: Get all active jobs for a job schedule</span></span>
```
PS C:\>Get-AzBatchJob -JobScheduleId "JobSchedule27" -Filter "state eq 'active'" -BatchContext $Context
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

<span data-ttu-id="94ac4-118">Det här kommandot får aktiva jobb för det jobb schema som har ID-JobSchedule27.</span><span class="sxs-lookup"><span data-stu-id="94ac4-118">This command gets the active jobs for the job schedule that has the ID JobSchedule27.</span></span>

### <span data-ttu-id="94ac4-119">Exempel 3: hämtar alla jobb under ett schema med hjälp av försäljnings förloppet</span><span class="sxs-lookup"><span data-stu-id="94ac4-119">Example 3: Gets all jobs under a job schedule by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Id "JobSchedule27" -BatchContext $Context | Get-AzBatchJob -BatchContext $Context
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

<span data-ttu-id="94ac4-120">Det här kommandot får jobbet schema med ID-JobSchedule27 med hjälp av Get-AzBatchJobSchedule cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94ac4-120">This command gets the job schedule that has the ID JobSchedule27 by using the Get-AzBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="94ac4-121">Kommandot skickar schemat till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="94ac4-121">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="94ac4-122">Kommandot får alla jobb för detta jobb schema.</span><span class="sxs-lookup"><span data-stu-id="94ac4-122">The command gets all jobs for that job schedule.</span></span>

## <span data-ttu-id="94ac4-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="94ac4-123">PARAMETERS</span></span>

### <span data-ttu-id="94ac4-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="94ac4-124">-BatchContext</span></span>
<span data-ttu-id="94ac4-125">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="94ac4-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="94ac4-126">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="94ac4-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="94ac4-127">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="94ac4-127">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="94ac4-128">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="94ac4-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="94ac4-129">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="94ac4-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="94ac4-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94ac4-130">-DefaultProfile</span></span>
<span data-ttu-id="94ac4-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="94ac4-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94ac4-132">-Expandera</span><span class="sxs-lookup"><span data-stu-id="94ac4-132">-Expand</span></span>
<span data-ttu-id="94ac4-133">Anger en Open data Protocol (OData) Expand-sats.</span><span class="sxs-lookup"><span data-stu-id="94ac4-133">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="94ac4-134">Ange ett värde för den här parametern för att hämta associerade enheter för huvud enheten som du får.</span><span class="sxs-lookup"><span data-stu-id="94ac4-134">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="94ac4-135">-Filter</span><span class="sxs-lookup"><span data-stu-id="94ac4-135">-Filter</span></span>
<span data-ttu-id="94ac4-136">Anger en OData filter-sats för jobb.</span><span class="sxs-lookup"><span data-stu-id="94ac4-136">Specifies an OData filter clause for jobs.</span></span>
<span data-ttu-id="94ac4-137">Om du inte anger något filter returnerar denna cmdlet alla jobb för batch-kontot eller jobb schemat.</span><span class="sxs-lookup"><span data-stu-id="94ac4-137">If you do not specify a filter, this cmdlet returns all jobs for the Batch account or job schedule.</span></span>

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

### <span data-ttu-id="94ac4-138">-ID</span><span class="sxs-lookup"><span data-stu-id="94ac4-138">-Id</span></span>
<span data-ttu-id="94ac4-139">Anger ID för det jobb som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="94ac4-139">Specifies the ID of the job that this cmdlet gets.</span></span>
<span data-ttu-id="94ac4-140">Du kan inte ange jokertecken.</span><span class="sxs-lookup"><span data-stu-id="94ac4-140">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="94ac4-141">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="94ac4-141">-JobSchedule</span></span>
<span data-ttu-id="94ac4-142">Anger ett **PSCloudJobSchedule** -objekt som representerar den jobbmall som innehåller jobben.</span><span class="sxs-lookup"><span data-stu-id="94ac4-142">Specifies a **PSCloudJobSchedule** object that represents the job schedule which contains the jobs.</span></span>
<span data-ttu-id="94ac4-143">För att hämta ett **PSCloudJobSchedule** -objekt, Använd cmdleten Get-AzBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="94ac4-143">To obtain a **PSCloudJobSchedule** object, use the Get-AzBatchJobSchedule cmdlet.</span></span>

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

### <span data-ttu-id="94ac4-144">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="94ac4-144">-JobScheduleId</span></span>
<span data-ttu-id="94ac4-145">Anger ID för den jobbmall som innehåller projekten.</span><span class="sxs-lookup"><span data-stu-id="94ac4-145">Specifies the ID of the job schedule which contains the jobs.</span></span>

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

### <span data-ttu-id="94ac4-146">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="94ac4-146">-MaxCount</span></span>
<span data-ttu-id="94ac4-147">Anger maximalt antal jobb som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="94ac4-147">Specifies the maximum number of jobs to return.</span></span>
<span data-ttu-id="94ac4-148">Om du anger ett värde som är noll (0) eller mindre används ingen övre gräns av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="94ac4-148">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="94ac4-149">Standardvärdet är 1000.</span><span class="sxs-lookup"><span data-stu-id="94ac4-149">The default value is 1000.</span></span>

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

### <span data-ttu-id="94ac4-150">-Välj</span><span class="sxs-lookup"><span data-stu-id="94ac4-150">-Select</span></span>
<span data-ttu-id="94ac4-151">Anger en OData SELECT-sats.</span><span class="sxs-lookup"><span data-stu-id="94ac4-151">Specifies an OData select clause.</span></span>
<span data-ttu-id="94ac4-152">Ange ett värde för den här parametern för att få specifika egenskaper i stället för alla objekt egenskaper.</span><span class="sxs-lookup"><span data-stu-id="94ac4-152">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="94ac4-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94ac4-153">CommonParameters</span></span>
<span data-ttu-id="94ac4-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94ac4-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94ac4-155">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94ac4-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94ac4-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="94ac4-156">INPUTS</span></span>

### <span data-ttu-id="94ac4-157">System. String</span><span class="sxs-lookup"><span data-stu-id="94ac4-157">System.String</span></span>

### <span data-ttu-id="94ac4-158">Microsoft.Azure.Commands.BatCH. Modeller. PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="94ac4-158">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

### <span data-ttu-id="94ac4-159">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="94ac4-159">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="94ac4-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="94ac4-160">OUTPUTS</span></span>

### <span data-ttu-id="94ac4-161">Microsoft.Azure.Commands.BatCH. Modeller. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="94ac4-161">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

## <span data-ttu-id="94ac4-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="94ac4-162">NOTES</span></span>

## <span data-ttu-id="94ac4-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="94ac4-163">RELATED LINKS</span></span>

[<span data-ttu-id="94ac4-164">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="94ac4-164">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="94ac4-165">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="94ac4-165">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="94ac4-166">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="94ac4-166">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="94ac4-167">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="94ac4-167">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="94ac4-168">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="94ac4-168">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="94ac4-169">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="94ac4-169">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="94ac4-170">Stopp-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="94ac4-170">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="94ac4-171">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="94ac4-171">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)

