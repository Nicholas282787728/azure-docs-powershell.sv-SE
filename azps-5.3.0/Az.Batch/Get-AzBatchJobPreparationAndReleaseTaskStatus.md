---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobpreparationandreleasetaskstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
ms.openlocfilehash: ffc89f298715f9e878bb3283c99e794f92662e84
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524799"
---
# <span data-ttu-id="48671-101">Get-AzBatchJobPreparationAndReleaseTaskStatus</span><span class="sxs-lookup"><span data-stu-id="48671-101">Get-AzBatchJobPreparationAndReleaseTaskStatus</span></span>

## <span data-ttu-id="48671-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="48671-102">SYNOPSIS</span></span>
<span data-ttu-id="48671-103">Hämtar och släpper aktivitets status.</span><span class="sxs-lookup"><span data-stu-id="48671-103">Gets Batch job preparation and release task status.</span></span>

## <span data-ttu-id="48671-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="48671-104">SYNTAX</span></span>

### <span data-ttu-id="48671-105">ID (standard)</span><span class="sxs-lookup"><span data-stu-id="48671-105">Id (Default)</span></span>
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-Id] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48671-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="48671-106">InputObject</span></span>
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-InputObject] <PSCloudJob> [-Filter <String>]
 [-MaxCount <Int32>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48671-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="48671-107">DESCRIPTION</span></span>
<span data-ttu-id="48671-108">Cmdleten **Get-AzBatchJobPreparationAndReleaseTaskStatus** får Azure Batch-jobbet förberedelse och utgivnings aktivitets status för ett batchjobb.</span><span class="sxs-lookup"><span data-stu-id="48671-108">The **Get-AzBatchJobPreparationAndReleaseTaskStatus** cmdlet gets the Azure Batch job preparation and release task status for a Batch job.</span></span>
<span data-ttu-id="48671-109">Du måste ange *ID-* parametern eller en **PSCloudJob** -instans till denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48671-109">You must supply the *Id* parameter or a **PSCloudJob** instance to this cmdlet.</span></span>

## <span data-ttu-id="48671-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="48671-110">EXAMPLES</span></span>

### <span data-ttu-id="48671-111">Exempel 1: få jobb förberedelsen och utgivnings status för ett jobb</span><span class="sxs-lookup"><span data-stu-id="48671-111">Example 1: Get the job preparation and release status of a job</span></span>
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $Context -Id Test

ComputeNodeId                          : tvm-2316545714_1-20170613t201733z
ComputeNodeUrl                         : https://account.westus.batch.azure.com/pools/test/nodes/tvm-2316545714_1-20170613t201733z
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 : test
```

<span data-ttu-id="48671-112">Det här kommandot får jobbet förberedelser och aktivitets status för jobbet "test".</span><span class="sxs-lookup"><span data-stu-id="48671-112">This command gets the job preparation and release task status for job "Test".</span></span>
<span data-ttu-id="48671-113">Använd Get-AzBatchAccountKey cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="48671-113">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="48671-114">Exempel 2: få jobbet Preparation och utgivnings status för ett jobb med filter och välj angiven</span><span class="sxs-lookup"><span data-stu-id="48671-114">Example 2: Get the job preparation and release status of a job with Filter and Select specified</span></span>
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $context -Id Test -Filter "nodeId eq 'tvm-2316545714_1-20170613t201733z'" -Select "jobPreparationTaskExecutionInfo"

ComputeNodeId                          :
ComputeNodeUrl                         :
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 :
```

<span data-ttu-id="48671-115">Det här kommandot får jobb förberedelsen och aktivitets status för jobbet "test" på noden "TVM-2316545714_1-20170613t201733z" och använder SELECT-satsen för att ange att endast JobPreparationTaskExecutionInformation-informationen ska returneras</span><span class="sxs-lookup"><span data-stu-id="48671-115">This command gets the job preparation and release task status for job "Test" on node "tvm-2316545714_1-20170613t201733z" and uses the Select clause to specify to only return the JobPreparationTaskExecutionInformation information</span></span>

## <span data-ttu-id="48671-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="48671-116">PARAMETERS</span></span>

### <span data-ttu-id="48671-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="48671-117">-BatchContext</span></span>
<span data-ttu-id="48671-118">Den BatchAccountContext-instans som ska användas vid interaktion med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="48671-118">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="48671-119">Använd Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="48671-119">Use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>

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

### <span data-ttu-id="48671-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48671-120">-DefaultProfile</span></span>
<span data-ttu-id="48671-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="48671-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48671-122">-Expandera</span><span class="sxs-lookup"><span data-stu-id="48671-122">-Expand</span></span>
<span data-ttu-id="48671-123">Anger en Open data Protocol (OData) Expand-sats.</span><span class="sxs-lookup"><span data-stu-id="48671-123">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="48671-124">Ange ett värde för den här parametern för att hämta associerade enheter för huvud enheten som du får.</span><span class="sxs-lookup"><span data-stu-id="48671-124">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="48671-125">-Filter</span><span class="sxs-lookup"><span data-stu-id="48671-125">-Filter</span></span>
<span data-ttu-id="48671-126">Anger en OData filter-sats.</span><span class="sxs-lookup"><span data-stu-id="48671-126">Specifies an OData filter clause.</span></span>
<span data-ttu-id="48671-127">Om du inte anger något filter returnerar denna cmdlet all jobb förberedelse och utgivnings status för jobbet.</span><span class="sxs-lookup"><span data-stu-id="48671-127">If you do not specify a filter, this cmdlet returns all job preparation and release task status' for the job.</span></span>

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

### <span data-ttu-id="48671-128">-ID</span><span class="sxs-lookup"><span data-stu-id="48671-128">-Id</span></span>
<span data-ttu-id="48671-129">Anger ID för det jobb vars förberedelse-och utgivnings aktiviteter ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="48671-129">Specifies the ID of the job whose preparation and release tasks should be retrieved.</span></span>
<span data-ttu-id="48671-130">Du kan inte ange jokertecken.</span><span class="sxs-lookup"><span data-stu-id="48671-130">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="48671-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48671-131">-InputObject</span></span>
<span data-ttu-id="48671-132">Anger ett **PSCloudJob** -objekt som representerar jobbet för att få statusen förberedelse-och utgivnings aktivitet från.</span><span class="sxs-lookup"><span data-stu-id="48671-132">Specifies a **PSCloudJob** object that represents the job to get the preparation and release task status from.</span></span>
<span data-ttu-id="48671-133">För att hämta ett **PSCloudJob** -objekt, Använd cmdleten Get-AzBatchJob.</span><span class="sxs-lookup"><span data-stu-id="48671-133">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48671-134">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="48671-134">-MaxCount</span></span>
<span data-ttu-id="48671-135">Anger det högsta antalet förberedelser och status för aktivitets statusen för att återgå.</span><span class="sxs-lookup"><span data-stu-id="48671-135">Specifies the maximum number of jobs preparation and release task status' to return.</span></span>
<span data-ttu-id="48671-136">Om du anger ett värde som är noll (0) eller mindre används ingen övre gräns av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="48671-136">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="48671-137">Standardvärdet är 1000.</span><span class="sxs-lookup"><span data-stu-id="48671-137">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48671-138">-Välj</span><span class="sxs-lookup"><span data-stu-id="48671-138">-Select</span></span>
<span data-ttu-id="48671-139">Anger en OData SELECT-sats.</span><span class="sxs-lookup"><span data-stu-id="48671-139">Specifies an OData select clause.</span></span>
<span data-ttu-id="48671-140">Ange ett värde för den här parametern för att få specifika egenskaper i stället för alla objekt egenskaper.</span><span class="sxs-lookup"><span data-stu-id="48671-140">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="48671-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48671-141">CommonParameters</span></span>
<span data-ttu-id="48671-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48671-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48671-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48671-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48671-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="48671-144">INPUTS</span></span>

### <span data-ttu-id="48671-145">Microsoft.Azure.Commands.BatCH. Modeller. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="48671-145">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="48671-146">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="48671-146">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="48671-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="48671-147">OUTPUTS</span></span>

### <span data-ttu-id="48671-148">Microsoft.Azure.Commands.BatCH. Modeller. PSJobPreparationAndReleaseTaskExecutionInformation</span><span class="sxs-lookup"><span data-stu-id="48671-148">Microsoft.Azure.Commands.Batch.Models.PSJobPreparationAndReleaseTaskExecutionInformation</span></span>

## <span data-ttu-id="48671-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="48671-149">NOTES</span></span>

## <span data-ttu-id="48671-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="48671-150">RELATED LINKS</span></span>

[<span data-ttu-id="48671-151">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="48671-151">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="48671-152">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="48671-152">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
