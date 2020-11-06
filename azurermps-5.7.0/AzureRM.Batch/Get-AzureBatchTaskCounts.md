---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchtaskcounts
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTaskCounts.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTaskCounts.md
ms.openlocfilehash: d0b98081675cd11d8d3eb60a6495ac87a1111034
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574423"
---
# <span data-ttu-id="971e6-101">Get-AzureBatchTaskCounts</span><span class="sxs-lookup"><span data-stu-id="971e6-101">Get-AzureBatchTaskCounts</span></span>

## <span data-ttu-id="971e6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="971e6-102">SYNOPSIS</span></span>
<span data-ttu-id="971e6-103">Hämtar antalet aktiviteter för det angivna jobbet.</span><span class="sxs-lookup"><span data-stu-id="971e6-103">Gets the task counts for the specified job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="971e6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="971e6-104">SYNTAX</span></span>

### <span data-ttu-id="971e6-105">Et</span><span class="sxs-lookup"><span data-stu-id="971e6-105">Id</span></span>
```
Get-AzureBatchTaskCounts [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="971e6-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="971e6-106">ParentObject</span></span>
```
Get-AzureBatchTaskCounts [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="971e6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="971e6-107">DESCRIPTION</span></span>
<span data-ttu-id="971e6-108">Cmdleten **Get-AzureBatchTaskCounts** hämtar antalet Azure Batch-uppgifter för ett batchjobb.</span><span class="sxs-lookup"><span data-stu-id="971e6-108">The **Get-AzureBatchTaskCounts** cmdlet gets the Azure Batch tasks count for a Batch job.</span></span>
<span data-ttu-id="971e6-109">Ange ett jobb genom parametern *jobId* eller *jobb* parameter.</span><span class="sxs-lookup"><span data-stu-id="971e6-109">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="971e6-110">Med aktivitets antal får du ett antal aktiviteter som är aktiva, kör eller slutförda aktivitets tillstånd och antalet uppgifter som lyckades eller misslyckades.</span><span class="sxs-lookup"><span data-stu-id="971e6-110">Task counts provide a count of the tasks by active, running or completed task state, and a count of tasks which succeeded or failed.</span></span> <span data-ttu-id="971e6-111">Uppgifter i tillståndet för att förbereda räknas som körs.</span><span class="sxs-lookup"><span data-stu-id="971e6-111">Tasks in the preparing state are counted as running.</span></span> <span data-ttu-id="971e6-112">Om validationStatus är avverifierat har batch-tjänsten inte kunnat kontrol lera status för de uppgifter som rapporter ATS i API för List aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="971e6-112">If the validationStatus is unvalidated, then the Batch service has not been able to check state counts against the task states as reported in the List Tasks API.</span></span> <span data-ttu-id="971e6-113">ValidationStatus kan vara avverifierad om jobbet innehåller fler än 200 000 uppgifter.</span><span class="sxs-lookup"><span data-stu-id="971e6-113">The validationStatus may be unvalidated if the job contains more than 200,000 tasks.</span></span>

## <span data-ttu-id="971e6-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="971e6-114">EXAMPLES</span></span>

### <span data-ttu-id="971e6-115">Exempel 1: Hämta antal aktiviteter efter ID</span><span class="sxs-lookup"><span data-stu-id="971e6-115">Example 1: Get task counts by ID</span></span>
```
PS C:\> Get-AzureBatchTaskCounts -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

<span data-ttu-id="971e6-116">Det här kommandot får antalet aktiviteter för jobbet Job01.</span><span class="sxs-lookup"><span data-stu-id="971e6-116">This command gets the task counts for job Job01.</span></span>
<span data-ttu-id="971e6-117">Använd Get-AzureRmBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="971e6-117">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="971e6-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="971e6-118">PARAMETERS</span></span>

### <span data-ttu-id="971e6-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="971e6-119">-BatchContext</span></span>
<span data-ttu-id="971e6-120">Den BatchAccountContext-instans som ska användas vid interaktion med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="971e6-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="971e6-121">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="971e6-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="971e6-122">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="971e6-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="971e6-123">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="971e6-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="971e6-124">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="971e6-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="971e6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="971e6-125">-DefaultProfile</span></span>
<span data-ttu-id="971e6-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="971e6-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="971e6-127">-Jobb</span><span class="sxs-lookup"><span data-stu-id="971e6-127">-Job</span></span>
<span data-ttu-id="971e6-128">Anger det jobb som innehåller uppgifter som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="971e6-128">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="971e6-129">För att hämta ett **PSCloudJob** -objekt, Använd cmdleten Get-AzureBatchJob.</span><span class="sxs-lookup"><span data-stu-id="971e6-129">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="971e6-130">-JobId</span><span class="sxs-lookup"><span data-stu-id="971e6-130">-JobId</span></span>
<span data-ttu-id="971e6-131">ID för det jobb som du vill hämta aktiviteter för.</span><span class="sxs-lookup"><span data-stu-id="971e6-131">The id of the job for which to get task counts.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="971e6-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="971e6-132">INPUTS</span></span>

### <span data-ttu-id="971e6-133">System. String</span><span class="sxs-lookup"><span data-stu-id="971e6-133">System.String</span></span>
<span data-ttu-id="971e6-134">Microsoft.Azure.Commands.BatCH. Modeller. PSCloudJob Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="971e6-134">Microsoft.Azure.Commands.Batch.Models.PSCloudJob Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>


## <span data-ttu-id="971e6-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="971e6-135">OUTPUTS</span></span>

### <span data-ttu-id="971e6-136">Microsoft.Azure.Commands.BatCH. Modeller. PSTaskCounts</span><span class="sxs-lookup"><span data-stu-id="971e6-136">Microsoft.Azure.Commands.Batch.Models.PSTaskCounts</span></span>


## <span data-ttu-id="971e6-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="971e6-137">NOTES</span></span>

## <span data-ttu-id="971e6-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="971e6-138">RELATED LINKS</span></span>

[<span data-ttu-id="971e6-139">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="971e6-139">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="971e6-140">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="971e6-140">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="971e6-141">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="971e6-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
