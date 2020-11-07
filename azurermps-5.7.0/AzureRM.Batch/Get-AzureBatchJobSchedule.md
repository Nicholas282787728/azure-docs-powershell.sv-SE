---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 8BAA6D8C-1530-4CC4-8AE5-A2CE6B1192CA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobSchedule.md
ms.openlocfilehash: 3c53a81952b204f08911b11accf6feb6bd55a3e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756104"
---
# <span data-ttu-id="913ef-101">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="913ef-101">Get-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="913ef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="913ef-102">SYNOPSIS</span></span>
<span data-ttu-id="913ef-103">Hämtar scheman för batchjobb.</span><span class="sxs-lookup"><span data-stu-id="913ef-103">Gets Batch job schedules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="913ef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="913ef-104">SYNTAX</span></span>

### <span data-ttu-id="913ef-105">ODataFilter (standard)</span><span class="sxs-lookup"><span data-stu-id="913ef-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchJobSchedule [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="913ef-106">Et</span><span class="sxs-lookup"><span data-stu-id="913ef-106">Id</span></span>
```
Get-AzureBatchJobSchedule [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="913ef-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="913ef-107">DESCRIPTION</span></span>
<span data-ttu-id="913ef-108">Cmdleten **Get-AzureBatchJobSchedule** får Azure Batch-jobbet scheman för det batch-konto som anges i parametern *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="913ef-108">The **Get-AzureBatchJobSchedule** cmdlet gets Azure Batch job schedules for the Batch account specified by the *BatchContext* parameter.</span></span>
<span data-ttu-id="913ef-109">Ange ett ID för att få ett enskilt jobb schema.</span><span class="sxs-lookup"><span data-stu-id="913ef-109">Specify an ID to get a single job schedule.</span></span>
<span data-ttu-id="913ef-110">Ange parametern *filter* om du vill hämta de jobb scheman som matchar ett open data Protocol (OData)-filter.</span><span class="sxs-lookup"><span data-stu-id="913ef-110">Specify the *Filter* parameter to get the job schedules that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="913ef-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="913ef-111">EXAMPLES</span></span>

### <span data-ttu-id="913ef-112">Exempel 1: få ett jobb schema genom att ange ett ID</span><span class="sxs-lookup"><span data-stu-id="913ef-112">Example 1: Get a job schedule by specifying an ID</span></span>
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

<span data-ttu-id="913ef-113">Det här kommandot får jobbet schema med ID-JobSchedule23.</span><span class="sxs-lookup"><span data-stu-id="913ef-113">This command gets the job schedule that has the ID JobSchedule23.</span></span>
<span data-ttu-id="913ef-114">Använd Get-AzureRmBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="913ef-114">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="913ef-115">Exempel 2: Hämta jobb schema med hjälp av ett filter</span><span class="sxs-lookup"><span data-stu-id="913ef-115">Example 2: Get job schedules by using a filter</span></span>
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

<span data-ttu-id="913ef-116">Det här kommandot får alla jobb scheman som har ID: n som börjar med jobbet genom att ange *filter* parametern.</span><span class="sxs-lookup"><span data-stu-id="913ef-116">This command gets all job schedules that have IDs that start with Job by specifying the *Filter* parameter.</span></span>

## <span data-ttu-id="913ef-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="913ef-117">PARAMETERS</span></span>

### <span data-ttu-id="913ef-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="913ef-118">-BatchContext</span></span>
<span data-ttu-id="913ef-119">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="913ef-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="913ef-120">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="913ef-120">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="913ef-121">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="913ef-121">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="913ef-122">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="913ef-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="913ef-123">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="913ef-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="913ef-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="913ef-124">-DefaultProfile</span></span>
<span data-ttu-id="913ef-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="913ef-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="913ef-126">-Expandera</span><span class="sxs-lookup"><span data-stu-id="913ef-126">-Expand</span></span>
<span data-ttu-id="913ef-127">Anger en Open data Protocol (OData) Expand-sats.</span><span class="sxs-lookup"><span data-stu-id="913ef-127">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="913ef-128">Ange ett värde för den här parametern för att hämta associerade enheter för huvud enheten som du får.</span><span class="sxs-lookup"><span data-stu-id="913ef-128">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="913ef-129">-Filter</span><span class="sxs-lookup"><span data-stu-id="913ef-129">-Filter</span></span>
<span data-ttu-id="913ef-130">Anger en OData filter-sats.</span><span class="sxs-lookup"><span data-stu-id="913ef-130">Specifies an OData filter clause.</span></span>
<span data-ttu-id="913ef-131">Denna cmdlet returnerar jobb scheman som matchar det filter som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="913ef-131">This cmdlet returns job schedules that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="913ef-132">Om du inte anger något filter returnerar denna cmdlet alla jobb uppställningar för grupp kontexten.</span><span class="sxs-lookup"><span data-stu-id="913ef-132">If you do not specify a filter, this cmdlet returns all job schedules for the Batch context.</span></span>

```yaml
Type: String
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913ef-133">-ID</span><span class="sxs-lookup"><span data-stu-id="913ef-133">-Id</span></span>
<span data-ttu-id="913ef-134">Anger ID för det fin schema som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="913ef-134">Specifies the ID of the job schedule that this cmdlet gets.</span></span>
<span data-ttu-id="913ef-135">Du kan inte ange jokertecken.</span><span class="sxs-lookup"><span data-stu-id="913ef-135">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="913ef-136">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="913ef-136">-MaxCount</span></span>
<span data-ttu-id="913ef-137">Anger maximalt antal jobb scheman att returnera.</span><span class="sxs-lookup"><span data-stu-id="913ef-137">Specifies the maximum number of job schedules to return.</span></span>
<span data-ttu-id="913ef-138">Om du anger ett värde som är noll (0) eller mindre används ingen övre gräns av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="913ef-138">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="913ef-139">Standardvärdet är 1000.</span><span class="sxs-lookup"><span data-stu-id="913ef-139">The default value is 1000.</span></span>

```yaml
Type: Int32
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913ef-140">-Välj</span><span class="sxs-lookup"><span data-stu-id="913ef-140">-Select</span></span>
<span data-ttu-id="913ef-141">Anger en OData SELECT-sats.</span><span class="sxs-lookup"><span data-stu-id="913ef-141">Specifies an OData select clause.</span></span>
<span data-ttu-id="913ef-142">Ange ett värde för den här parametern för att få specifika egenskaper i stället för alla objekt egenskaper.</span><span class="sxs-lookup"><span data-stu-id="913ef-142">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="913ef-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="913ef-143">CommonParameters</span></span>
<span data-ttu-id="913ef-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="913ef-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="913ef-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="913ef-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="913ef-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="913ef-146">INPUTS</span></span>

### <span data-ttu-id="913ef-147">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="913ef-147">BatchAccountContext</span></span>
<span data-ttu-id="913ef-148">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="913ef-148">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="913ef-149">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="913ef-149">String</span></span>
<span data-ttu-id="913ef-150">Parametern ' ID ' godkänner värdet för typen ' String ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="913ef-150">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="913ef-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="913ef-151">OUTPUTS</span></span>

### <span data-ttu-id="913ef-152">PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="913ef-152">PSCloudJobSchedule</span></span>

## <span data-ttu-id="913ef-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="913ef-153">NOTES</span></span>

## <span data-ttu-id="913ef-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="913ef-154">RELATED LINKS</span></span>

[<span data-ttu-id="913ef-155">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="913ef-155">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="913ef-156">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="913ef-156">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="913ef-157">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="913ef-157">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="913ef-158">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="913ef-158">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="913ef-159">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="913ef-159">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="913ef-160">Stopp-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="913ef-160">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="913ef-161">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="913ef-161">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


