---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 8BAA6D8C-1530-4CC4-8AE5-A2CE6B1192CA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobSchedule.md
ms.openlocfilehash: 139282332fb1c5d0ace02ddd7b998c1875af931a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577715"
---
# <span data-ttu-id="2016e-101">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="2016e-101">Get-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="2016e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2016e-102">SYNOPSIS</span></span>
<span data-ttu-id="2016e-103">Hämtar scheman för batchjobb.</span><span class="sxs-lookup"><span data-stu-id="2016e-103">Gets Batch job schedules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2016e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2016e-104">SYNTAX</span></span>

### <span data-ttu-id="2016e-105">ODataFilter (standard)</span><span class="sxs-lookup"><span data-stu-id="2016e-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchJobSchedule [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2016e-106">Et</span><span class="sxs-lookup"><span data-stu-id="2016e-106">Id</span></span>
```
Get-AzureBatchJobSchedule [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2016e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2016e-107">DESCRIPTION</span></span>
<span data-ttu-id="2016e-108">Cmdleten **Get-AzureBatchJobSchedule** får Azure Batch-jobbet scheman för det batch-konto som anges i parametern *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="2016e-108">The **Get-AzureBatchJobSchedule** cmdlet gets Azure Batch job schedules for the Batch account specified by the *BatchContext* parameter.</span></span>
<span data-ttu-id="2016e-109">Ange ett ID för att få ett enskilt jobb schema.</span><span class="sxs-lookup"><span data-stu-id="2016e-109">Specify an ID to get a single job schedule.</span></span>
<span data-ttu-id="2016e-110">Ange parametern *filter* om du vill hämta de jobb scheman som matchar ett open data Protocol (OData)-filter.</span><span class="sxs-lookup"><span data-stu-id="2016e-110">Specify the *Filter* parameter to get the job schedules that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="2016e-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2016e-111">EXAMPLES</span></span>

### <span data-ttu-id="2016e-112">Exempel 1: få ett jobb schema genom att ange ett ID</span><span class="sxs-lookup"><span data-stu-id="2016e-112">Example 1: Get a job schedule by specifying an ID</span></span>
```
PS C:\>Get-AzureBatchJobSchedule -Id "JobSchedule23" -BatchContext $Context
CreationTime                : 7/25/2015 9:15:43 PM
DisplayName                 : 
ETag                        : 0x8D2953633427FCA
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobScheduleExecutionInformation
Id                          : JobSchedule23
JobSpecification            : Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
LastModified                : 7/25/2015 9:15:43 PM
Metadata                    : 
PreviousState               : Invalid
PreviousStateTransitionTime : 
Schedule                    : 
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:43 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobschedules/JobSchedule23
```

<span data-ttu-id="2016e-113">Det här kommandot får jobbet schema med ID-JobSchedule23.</span><span class="sxs-lookup"><span data-stu-id="2016e-113">This command gets the job schedule that has the ID JobSchedule23.</span></span>
<span data-ttu-id="2016e-114">Använd Get-AzureRmBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="2016e-114">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="2016e-115">Exempel 2: Hämta jobb schema med hjälp av ett filter</span><span class="sxs-lookup"><span data-stu-id="2016e-115">Example 2: Get job schedules by using a filter</span></span>
```
PS C:\>Get-AzureBatchJobSchedule -Filter "startswith(id,'Job')" -BatchContext $Context
CreationTime                : 7/25/2015 9:15:43 PM
DisplayName                 : 
ETag                        : 0x8D2953633427FCA
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobScheduleExecutionInformation
Id                          : JobSchedule23
JobSpecification            : Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
LastModified                : 7/25/2015 9:15:43 PM
Metadata                    : 
PreviousState               : Invalid
PreviousStateTransitionTime : 
Schedule                    : 
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:43 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobschedules/JobSchedule23

CreationTime                : 7/26/2015 5:39:33 PM
DisplayName                 : 
ETag                        : 0x8D295E12B1084B4
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobScheduleExecutionInformation
Id                          : JobSchedule26
JobSpecification            : Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
LastModified                : 7/26/2015 5:39:33 PM
Metadata                    : 
PreviousState               : Invalid
PreviousStateTransitionTime : 
Schedule                    : 
State                       : Active
StateTransitionTime         : 7/26/2015 5:39:33 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobschedules/JobSchedule26
```

<span data-ttu-id="2016e-116">Det här kommandot får alla jobb scheman som har ID: n som börjar med jobbet genom att ange *filter* parametern.</span><span class="sxs-lookup"><span data-stu-id="2016e-116">This command gets all job schedules that have IDs that start with Job by specifying the *Filter* parameter.</span></span>

## <span data-ttu-id="2016e-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2016e-117">PARAMETERS</span></span>

### <span data-ttu-id="2016e-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="2016e-118">-BatchContext</span></span>
<span data-ttu-id="2016e-119">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="2016e-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2016e-120">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="2016e-120">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="2016e-121">-Expandera</span><span class="sxs-lookup"><span data-stu-id="2016e-121">-Expand</span></span>
<span data-ttu-id="2016e-122">Anger en Open data Protocol (OData) Expand-sats.</span><span class="sxs-lookup"><span data-stu-id="2016e-122">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="2016e-123">Ange ett värde för den här parametern för att hämta associerade enheter för huvud enheten som du får.</span><span class="sxs-lookup"><span data-stu-id="2016e-123">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="2016e-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="2016e-124">-Filter</span></span>
<span data-ttu-id="2016e-125">Anger en OData filter-sats.</span><span class="sxs-lookup"><span data-stu-id="2016e-125">Specifies an OData filter clause.</span></span>
<span data-ttu-id="2016e-126">Denna cmdlet returnerar jobb scheman som matchar det filter som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="2016e-126">This cmdlet returns job schedules that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="2016e-127">Om du inte anger något filter returnerar denna cmdlet alla jobb uppställningar för grupp kontexten.</span><span class="sxs-lookup"><span data-stu-id="2016e-127">If you do not specify a filter, this cmdlet returns all job schedules for the Batch context.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2016e-128">-ID</span><span class="sxs-lookup"><span data-stu-id="2016e-128">-Id</span></span>
<span data-ttu-id="2016e-129">Anger ID för det fin schema som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="2016e-129">Specifies the ID of the job schedule that this cmdlet gets.</span></span>
<span data-ttu-id="2016e-130">Du kan inte ange jokertecken.</span><span class="sxs-lookup"><span data-stu-id="2016e-130">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2016e-131">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="2016e-131">-MaxCount</span></span>
<span data-ttu-id="2016e-132">Anger maximalt antal jobb scheman att returnera.</span><span class="sxs-lookup"><span data-stu-id="2016e-132">Specifies the maximum number of job schedules to return.</span></span>
<span data-ttu-id="2016e-133">Om du anger ett värde som är noll (0) eller mindre används ingen övre gräns av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2016e-133">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="2016e-134">Standardvärdet är 1000.</span><span class="sxs-lookup"><span data-stu-id="2016e-134">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2016e-135">-Välj</span><span class="sxs-lookup"><span data-stu-id="2016e-135">-Select</span></span>
<span data-ttu-id="2016e-136">Anger en OData SELECT-sats.</span><span class="sxs-lookup"><span data-stu-id="2016e-136">Specifies an OData select clause.</span></span>
<span data-ttu-id="2016e-137">Ange ett värde för den här parametern för att få specifika egenskaper i stället för alla objekt egenskaper.</span><span class="sxs-lookup"><span data-stu-id="2016e-137">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="2016e-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2016e-138">-DefaultProfile</span></span>
<span data-ttu-id="2016e-139">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2016e-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2016e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2016e-140">CommonParameters</span></span>
<span data-ttu-id="2016e-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2016e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2016e-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2016e-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2016e-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2016e-143">INPUTS</span></span>

### <span data-ttu-id="2016e-144">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2016e-144">BatchAccountContext</span></span>
<span data-ttu-id="2016e-145">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="2016e-145">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="2016e-146">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="2016e-146">String</span></span>
<span data-ttu-id="2016e-147">Parametern ' ID ' godkänner värdet för typen ' String ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="2016e-147">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="2016e-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2016e-148">OUTPUTS</span></span>

### <span data-ttu-id="2016e-149">PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="2016e-149">PSCloudJobSchedule</span></span>

## <span data-ttu-id="2016e-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2016e-150">NOTES</span></span>

## <span data-ttu-id="2016e-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2016e-151">RELATED LINKS</span></span>

[<span data-ttu-id="2016e-152">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="2016e-152">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="2016e-153">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="2016e-153">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="2016e-154">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="2016e-154">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="2016e-155">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="2016e-155">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="2016e-156">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="2016e-156">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="2016e-157">Stopp-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="2016e-157">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="2016e-158">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="2016e-158">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


