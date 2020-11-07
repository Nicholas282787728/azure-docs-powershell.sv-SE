---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchjobpreparationandreleasetaskstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobPreparationAndReleaseTaskStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobPreparationAndReleaseTaskStatus.md
ms.openlocfilehash: 5f24e55042a8be7f36b1a9946c4bd5b87209a0f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583199"
---
# <span data-ttu-id="2aadb-101">Get-AzureBatchJobPreparationAndReleaseTaskStatus</span><span class="sxs-lookup"><span data-stu-id="2aadb-101">Get-AzureBatchJobPreparationAndReleaseTaskStatus</span></span>

## <span data-ttu-id="2aadb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2aadb-102">SYNOPSIS</span></span>
<span data-ttu-id="2aadb-103">Hämtar och släpper aktivitets status.</span><span class="sxs-lookup"><span data-stu-id="2aadb-103">Gets Batch job preparation and release task status.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2aadb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2aadb-104">SYNTAX</span></span>

### <span data-ttu-id="2aadb-105">ID (standard)</span><span class="sxs-lookup"><span data-stu-id="2aadb-105">Id (Default)</span></span>
```
Get-AzureBatchJobPreparationAndReleaseTaskStatus [-Id] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2aadb-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="2aadb-106">InputObject</span></span>
```
Get-AzureBatchJobPreparationAndReleaseTaskStatus [-InputObject] <PSCloudJob> [-Filter <String>]
 [-MaxCount <Int32>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2aadb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2aadb-107">DESCRIPTION</span></span>
<span data-ttu-id="2aadb-108">Cmdleten **Get-AzureBatchJobPreparationAndReleaseTaskStatus** får Azure Batch-jobbet förberedelse och utgivnings aktivitets status för ett batchjobb.</span><span class="sxs-lookup"><span data-stu-id="2aadb-108">The **Get-AzureBatchJobPreparationAndReleaseTaskStatus** cmdlet gets the Azure Batch job preparation and release task status for a Batch job.</span></span>
<span data-ttu-id="2aadb-109">Du måste ange *ID-* parametern eller en **PSCloudJob** -instans till denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2aadb-109">You must supply the *Id* parameter or a **PSCloudJob** instance to this cmdlet.</span></span>

## <span data-ttu-id="2aadb-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2aadb-110">EXAMPLES</span></span>

### <span data-ttu-id="2aadb-111">Exempel 1: få jobb förberedelsen och utgivnings status för ett jobb</span><span class="sxs-lookup"><span data-stu-id="2aadb-111">Example 1: Get the job preparation and release status of a job</span></span>
```
PS C:\> Get-AzureBatchJobPreparationAndReleaseTaskStatus -BatchContext $Context -Id Test

ComputeNodeId                          : tvm-2316545714_1-20170613t201733z
ComputeNodeUrl                         : https://account.westus.batch.azure.com/pools/test/nodes/tvm-2316545714_1-20170613t201733z
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 : test
```

<span data-ttu-id="2aadb-112">Det här kommandot får jobbet förberedelser och aktivitets status för jobbet "test".</span><span class="sxs-lookup"><span data-stu-id="2aadb-112">This command gets the job preparation and release task status for job "Test".</span></span>
<span data-ttu-id="2aadb-113">Använd Get-AzureRmBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="2aadb-113">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="2aadb-114">Exempel 2: få jobbet Preparation och utgivnings status för ett jobb med filter och välj angiven</span><span class="sxs-lookup"><span data-stu-id="2aadb-114">Example 2: Get the job preparation and release status of a job with Filter and Select specified</span></span>
```
PS C:\> Get-AzureBatchJobPreparationAndReleaseTaskStatus -BatchContext $context -Id Test -Filter "nodeId eq 'tvm-2316545714_1-20170613t201733z'" -Select "jobPreparationTaskExecutionInfo"

ComputeNodeId                          :
ComputeNodeUrl                         :
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 :
```

<span data-ttu-id="2aadb-115">Det här kommandot får jobb förberedelsen och aktivitets status för jobbet "test" på noden "TVM-2316545714_1-20170613t201733z" och använder SELECT-satsen för att ange att endast JobPreparationTaskExecutionInformation-informationen ska returneras</span><span class="sxs-lookup"><span data-stu-id="2aadb-115">This command gets the job preparation and release task status for job "Test" on node "tvm-2316545714_1-20170613t201733z" and uses the Select clause to specify to only return the JobPreparationTaskExecutionInformation information</span></span>

## <span data-ttu-id="2aadb-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2aadb-116">PARAMETERS</span></span>

### <span data-ttu-id="2aadb-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="2aadb-117">-BatchContext</span></span>
<span data-ttu-id="2aadb-118">Den BatchAccountContext-instans som ska användas vid interaktion med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="2aadb-118">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="2aadb-119">Använd Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="2aadb-119">Use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>

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

### <span data-ttu-id="2aadb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aadb-120">-DefaultProfile</span></span>
<span data-ttu-id="2aadb-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2aadb-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2aadb-122">-Expandera</span><span class="sxs-lookup"><span data-stu-id="2aadb-122">-Expand</span></span>
<span data-ttu-id="2aadb-123">Anger en Open data Protocol (OData) Expand-sats.</span><span class="sxs-lookup"><span data-stu-id="2aadb-123">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="2aadb-124">Ange ett värde för den här parametern för att hämta associerade enheter för huvud enheten som du får.</span><span class="sxs-lookup"><span data-stu-id="2aadb-124">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="2aadb-125">-Filter</span><span class="sxs-lookup"><span data-stu-id="2aadb-125">-Filter</span></span>
<span data-ttu-id="2aadb-126">Anger en OData filter-sats.</span><span class="sxs-lookup"><span data-stu-id="2aadb-126">Specifies an OData filter clause.</span></span>
<span data-ttu-id="2aadb-127">Om du inte anger något filter returnerar denna cmdlet all jobb förberedelse och utgivnings status för jobbet.</span><span class="sxs-lookup"><span data-stu-id="2aadb-127">If you do not specify a filter, this cmdlet returns all job preparation and release task status' for the job.</span></span>

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

### <span data-ttu-id="2aadb-128">-ID</span><span class="sxs-lookup"><span data-stu-id="2aadb-128">-Id</span></span>
<span data-ttu-id="2aadb-129">Anger ID för det jobb vars förberedelse-och utgivnings aktiviteter ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="2aadb-129">Specifies the ID of the job whose preparation and release tasks should be retrieved.</span></span>
<span data-ttu-id="2aadb-130">Du kan inte ange jokertecken.</span><span class="sxs-lookup"><span data-stu-id="2aadb-130">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aadb-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2aadb-131">-InputObject</span></span>
<span data-ttu-id="2aadb-132">Anger ett **PSCloudJob** -objekt som representerar jobbet för att få statusen förberedelse-och utgivnings aktivitet från.</span><span class="sxs-lookup"><span data-stu-id="2aadb-132">Specifies a **PSCloudJob** object that represents the job to get the preparation and release task status from.</span></span>
<span data-ttu-id="2aadb-133">För att hämta ett **PSCloudJob** -objekt, Använd cmdleten Get-AzureBatchJob.</span><span class="sxs-lookup"><span data-stu-id="2aadb-133">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

```yaml
Type: PSCloudJob
Parameter Sets: InputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2aadb-134">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="2aadb-134">-MaxCount</span></span>
<span data-ttu-id="2aadb-135">Anger det högsta antalet förberedelser och status för aktivitets statusen för att återgå.</span><span class="sxs-lookup"><span data-stu-id="2aadb-135">Specifies the maximum number of jobs preparation and release task status' to return.</span></span>
<span data-ttu-id="2aadb-136">Om du anger ett värde som är noll (0) eller mindre används ingen övre gräns av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2aadb-136">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="2aadb-137">Standardvärdet är 1000.</span><span class="sxs-lookup"><span data-stu-id="2aadb-137">The default value is 1000.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aadb-138">-Välj</span><span class="sxs-lookup"><span data-stu-id="2aadb-138">-Select</span></span>
<span data-ttu-id="2aadb-139">Anger en OData SELECT-sats.</span><span class="sxs-lookup"><span data-stu-id="2aadb-139">Specifies an OData select clause.</span></span>
<span data-ttu-id="2aadb-140">Ange ett värde för den här parametern för att få specifika egenskaper i stället för alla objekt egenskaper.</span><span class="sxs-lookup"><span data-stu-id="2aadb-140">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="2aadb-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aadb-141">CommonParameters</span></span>
<span data-ttu-id="2aadb-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2aadb-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aadb-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2aadb-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aadb-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2aadb-144">INPUTS</span></span>

### <span data-ttu-id="2aadb-145">System. String</span><span class="sxs-lookup"><span data-stu-id="2aadb-145">System.String</span></span>
<span data-ttu-id="2aadb-146">Microsoft.Azure.Commands.BatCH. Modeller. PSCloudJob Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2aadb-146">Microsoft.Azure.Commands.Batch.Models.PSCloudJob Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="2aadb-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2aadb-147">OUTPUTS</span></span>

### <span data-ttu-id="2aadb-148">Microsoft.Azure.Commands.BatCH. Modeller. PSJobPreparationAndReleaseTaskExecutionInformation</span><span class="sxs-lookup"><span data-stu-id="2aadb-148">Microsoft.Azure.Commands.Batch.Models.PSJobPreparationAndReleaseTaskExecutionInformation</span></span>

## <span data-ttu-id="2aadb-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2aadb-149">NOTES</span></span>

## <span data-ttu-id="2aadb-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2aadb-150">RELATED LINKS</span></span>

[<span data-ttu-id="2aadb-151">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="2aadb-151">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="2aadb-152">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="2aadb-152">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)