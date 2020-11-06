---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 8BF49C4D-E7CD-4FD0-AFAC-9856239D24EC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJob.md
ms.openlocfilehash: 1a5f971e52da27eb2abeca02c4362eee9b9755c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579012"
---
# <span data-ttu-id="1dcd9-101">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="1dcd9-101">Get-AzureBatchJob</span></span>

## <span data-ttu-id="1dcd9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1dcd9-102">SYNOPSIS</span></span>
<span data-ttu-id="1dcd9-103">Hämtar batchjobb för ett batch-konto eller jobb schema.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-103">Gets Batch jobs for a Batch account or job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1dcd9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1dcd9-104">SYNTAX</span></span>

### <span data-ttu-id="1dcd9-105">ODataFilter (standard)</span><span class="sxs-lookup"><span data-stu-id="1dcd9-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchJob [-JobScheduleId <String>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1dcd9-106">Et</span><span class="sxs-lookup"><span data-stu-id="1dcd9-106">Id</span></span>
```
Get-AzureBatchJob [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1dcd9-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="1dcd9-107">ParentObject</span></span>
```
Get-AzureBatchJob [[-JobSchedule] <PSCloudJobSchedule>] [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1dcd9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1dcd9-108">DESCRIPTION</span></span>
<span data-ttu-id="1dcd9-109">Cmdleten **Get-AzureBatchJob** hämtar Azure-kommandona för batch-kontot som anges av parametern *BatchAccountContext* .</span><span class="sxs-lookup"><span data-stu-id="1dcd9-109">The **Get-AzureBatchJob** cmdlet gets the Azure Batch jobs for the Batch account specified by the *BatchAccountContext* parameter.</span></span>
<span data-ttu-id="1dcd9-110">Du kan använda *ID-* parametern för att få ett enskilt jobb.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-110">You can use the *Id* parameter to get a single job.</span></span>
<span data-ttu-id="1dcd9-111">Du kan använda parametern *filter* för att hämta de jobb som matchar ett open data Protocol (OData)-filter.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-111">You can use the *Filter* parameter to get the jobs that match an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="1dcd9-112">Om du anger ett jobb schema-ID eller en **PSCloudJobSchedule** -instans returnerar denna cmdlet endast jobb för det jobb schema.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-112">If you supply a job schedule ID or **PSCloudJobSchedule** instance, this cmdlet returns only the jobs for that job schedule.</span></span>

## <span data-ttu-id="1dcd9-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1dcd9-113">EXAMPLES</span></span>

### <span data-ttu-id="1dcd9-114">Exempel 1: Hämta ett batchjobb utifrån ID</span><span class="sxs-lookup"><span data-stu-id="1dcd9-114">Example 1: Get a Batch job by ID</span></span>
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

<span data-ttu-id="1dcd9-115">Det här kommandot får jobbet med ID-Job01.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-115">This command gets the job that has the ID Job01.</span></span>
<span data-ttu-id="1dcd9-116">Använd Get-AzureRmBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-116">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="1dcd9-117">Exempel 2: Hämta alla aktiva jobb för ett schema</span><span class="sxs-lookup"><span data-stu-id="1dcd9-117">Example 2: Get all active jobs for a job schedule</span></span>
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

<span data-ttu-id="1dcd9-118">Det här kommandot får aktiva jobb för det jobb schema som har ID-JobSchedule27.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-118">This command gets the active jobs for the job schedule that has the ID JobSchedule27.</span></span>

### <span data-ttu-id="1dcd9-119">Exempel 3: hämtar alla jobb under ett schema med hjälp av försäljnings förloppet</span><span class="sxs-lookup"><span data-stu-id="1dcd9-119">Example 3: Gets all jobs under a job schedule by using the pipeline</span></span>
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

<span data-ttu-id="1dcd9-120">Det här kommandot får jobbet schema med ID-JobSchedule27 med hjälp av Get-AzureBatchJobSchedule cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-120">This command gets the job schedule that has the ID JobSchedule27 by using the Get-AzureBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="1dcd9-121">Kommandot skickar schemat till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-121">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1dcd9-122">Kommandot får alla jobb för detta jobb schema.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-122">The command gets all jobs for that job schedule.</span></span>

## <span data-ttu-id="1dcd9-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1dcd9-123">PARAMETERS</span></span>

### <span data-ttu-id="1dcd9-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="1dcd9-124">-BatchContext</span></span>
<span data-ttu-id="1dcd9-125">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="1dcd9-126">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-126">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="1dcd9-127">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-127">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="1dcd9-128">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="1dcd9-129">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="1dcd9-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dcd9-130">-DefaultProfile</span></span>
<span data-ttu-id="1dcd9-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1dcd9-132">-Expandera</span><span class="sxs-lookup"><span data-stu-id="1dcd9-132">-Expand</span></span>
<span data-ttu-id="1dcd9-133">Anger en Open data Protocol (OData) Expand-sats.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-133">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="1dcd9-134">Ange ett värde för den här parametern för att hämta associerade enheter för huvud enheten som du får.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-134">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="1dcd9-135">-Filter</span><span class="sxs-lookup"><span data-stu-id="1dcd9-135">-Filter</span></span>
<span data-ttu-id="1dcd9-136">Anger en OData filter-sats för jobb.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-136">Specifies an OData filter clause for jobs.</span></span>
<span data-ttu-id="1dcd9-137">Om du inte anger något filter returnerar denna cmdlet alla jobb för batch-kontot eller jobb schemat.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-137">If you do not specify a filter, this cmdlet returns all jobs for the Batch account or job schedule.</span></span>

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

### <span data-ttu-id="1dcd9-138">-ID</span><span class="sxs-lookup"><span data-stu-id="1dcd9-138">-Id</span></span>
<span data-ttu-id="1dcd9-139">Anger ID för det jobb som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-139">Specifies the ID of the job that this cmdlet gets.</span></span>
<span data-ttu-id="1dcd9-140">Du kan inte ange jokertecken.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-140">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="1dcd9-141">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="1dcd9-141">-JobSchedule</span></span>
<span data-ttu-id="1dcd9-142">Anger ett **PSCloudJobSchedule** -objekt som representerar den jobbmall som innehåller jobben.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-142">Specifies a **PSCloudJobSchedule** object that represents the job schedule which contains the jobs.</span></span>
<span data-ttu-id="1dcd9-143">För att hämta ett **PSCloudJobSchedule** -objekt, Använd cmdleten Get-AzureBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-143">To obtain a **PSCloudJobSchedule** object, use the Get-AzureBatchJobSchedule cmdlet.</span></span>

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

### <span data-ttu-id="1dcd9-144">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="1dcd9-144">-JobScheduleId</span></span>
<span data-ttu-id="1dcd9-145">Anger ID för den jobbmall som innehåller projekten.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-145">Specifies the ID of the job schedule which contains the jobs.</span></span>

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

### <span data-ttu-id="1dcd9-146">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="1dcd9-146">-MaxCount</span></span>
<span data-ttu-id="1dcd9-147">Anger maximalt antal jobb som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-147">Specifies the maximum number of jobs to return.</span></span>
<span data-ttu-id="1dcd9-148">Om du anger ett värde som är noll (0) eller mindre används ingen övre gräns av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-148">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="1dcd9-149">Standardvärdet är 1000.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-149">The default value is 1000.</span></span>

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

### <span data-ttu-id="1dcd9-150">-Välj</span><span class="sxs-lookup"><span data-stu-id="1dcd9-150">-Select</span></span>
<span data-ttu-id="1dcd9-151">Anger en OData SELECT-sats.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-151">Specifies an OData select clause.</span></span>
<span data-ttu-id="1dcd9-152">Ange ett värde för den här parametern för att få specifika egenskaper i stället för alla objekt egenskaper.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-152">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="1dcd9-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dcd9-153">CommonParameters</span></span>
<span data-ttu-id="1dcd9-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dcd9-155">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dcd9-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dcd9-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1dcd9-156">INPUTS</span></span>

### <span data-ttu-id="1dcd9-157">System. String</span><span class="sxs-lookup"><span data-stu-id="1dcd9-157">System.String</span></span>

### <span data-ttu-id="1dcd9-158">Microsoft.Azure.Commands.BatCH. Modeller. PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="1dcd9-158">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>
<span data-ttu-id="1dcd9-159">Parametrar: JobSchedule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1dcd9-159">Parameters: JobSchedule (ByValue)</span></span>

### <span data-ttu-id="1dcd9-160">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1dcd9-160">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="1dcd9-161">Parametrar: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1dcd9-161">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="1dcd9-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1dcd9-162">OUTPUTS</span></span>

### <span data-ttu-id="1dcd9-163">Microsoft.Azure.Commands.BatCH. Modeller. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="1dcd9-163">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

## <span data-ttu-id="1dcd9-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1dcd9-164">NOTES</span></span>

## <span data-ttu-id="1dcd9-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1dcd9-165">RELATED LINKS</span></span>

[<span data-ttu-id="1dcd9-166">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="1dcd9-166">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="1dcd9-167">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="1dcd9-167">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="1dcd9-168">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="1dcd9-168">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="1dcd9-169">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="1dcd9-169">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="1dcd9-170">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="1dcd9-170">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="1dcd9-171">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="1dcd9-171">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="1dcd9-172">Stopp-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="1dcd9-172">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="1dcd9-173">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="1dcd9-173">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


