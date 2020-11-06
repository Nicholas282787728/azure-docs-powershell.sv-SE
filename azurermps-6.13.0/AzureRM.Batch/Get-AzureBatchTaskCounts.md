---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchtaskcounts
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTaskCounts.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTaskCounts.md
ms.openlocfilehash: 9010ec1d15958f5198c25fd0ef9e8a5ecfe6a39e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582812"
---
# <span data-ttu-id="285b9-101">Get-AzureBatchTaskCounts</span><span class="sxs-lookup"><span data-stu-id="285b9-101">Get-AzureBatchTaskCounts</span></span>

## <span data-ttu-id="285b9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="285b9-102">SYNOPSIS</span></span>
<span data-ttu-id="285b9-103">Hämtar antalet aktiviteter för det angivna jobbet.</span><span class="sxs-lookup"><span data-stu-id="285b9-103">Gets the task counts for the specified job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="285b9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="285b9-104">SYNTAX</span></span>

### <span data-ttu-id="285b9-105">Et</span><span class="sxs-lookup"><span data-stu-id="285b9-105">Id</span></span>
```
Get-AzureBatchTaskCounts [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="285b9-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="285b9-106">ParentObject</span></span>
```
Get-AzureBatchTaskCounts [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="285b9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="285b9-107">DESCRIPTION</span></span>
<span data-ttu-id="285b9-108">Cmdleten **Get-AzureBatchTaskCounts** hämtar antalet Azure Batch-uppgifter för ett batchjobb.</span><span class="sxs-lookup"><span data-stu-id="285b9-108">The **Get-AzureBatchTaskCounts** cmdlet gets the Azure Batch tasks count for a Batch job.</span></span>
<span data-ttu-id="285b9-109">Ange ett jobb genom parametern *jobId* eller *jobb* parameter.</span><span class="sxs-lookup"><span data-stu-id="285b9-109">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="285b9-110">Med aktivitets antal får du ett antal aktiviteter som är aktiva, kör eller slutförda aktivitets tillstånd och antalet uppgifter som lyckades eller misslyckades.</span><span class="sxs-lookup"><span data-stu-id="285b9-110">Task counts provide a count of the tasks by active, running or completed task state, and a count of tasks which succeeded or failed.</span></span> <span data-ttu-id="285b9-111">Uppgifter i tillståndet för att förbereda räknas som körs.</span><span class="sxs-lookup"><span data-stu-id="285b9-111">Tasks in the preparing state are counted as running.</span></span> <span data-ttu-id="285b9-112">Om validationStatus är avverifierat har batch-tjänsten inte kunnat kontrol lera status för de uppgifter som rapporter ATS i API för List aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="285b9-112">If the validationStatus is unvalidated, then the Batch service has not been able to check state counts against the task states as reported in the List Tasks API.</span></span> <span data-ttu-id="285b9-113">ValidationStatus kan vara avverifierad om jobbet innehåller fler än 200 000 uppgifter.</span><span class="sxs-lookup"><span data-stu-id="285b9-113">The validationStatus may be unvalidated if the job contains more than 200,000 tasks.</span></span>

## <span data-ttu-id="285b9-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="285b9-114">EXAMPLES</span></span>

### <span data-ttu-id="285b9-115">Exempel 1: Hämta antal aktiviteter efter ID</span><span class="sxs-lookup"><span data-stu-id="285b9-115">Example 1: Get task counts by ID</span></span>
```
PS C:\> Get-AzureBatchTaskCounts -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

<span data-ttu-id="285b9-116">Det här kommandot får antalet aktiviteter för jobbet Job01.</span><span class="sxs-lookup"><span data-stu-id="285b9-116">This command gets the task counts for job Job01.</span></span>
<span data-ttu-id="285b9-117">Använd Get-AzureRmBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="285b9-117">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="285b9-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="285b9-118">PARAMETERS</span></span>

### <span data-ttu-id="285b9-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="285b9-119">-BatchContext</span></span>
<span data-ttu-id="285b9-120">Den BatchAccountContext-instans som ska användas vid interaktion med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="285b9-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="285b9-121">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="285b9-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="285b9-122">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="285b9-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="285b9-123">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="285b9-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="285b9-124">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="285b9-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="285b9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="285b9-125">-DefaultProfile</span></span>
<span data-ttu-id="285b9-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="285b9-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="285b9-127">-Jobb</span><span class="sxs-lookup"><span data-stu-id="285b9-127">-Job</span></span>
<span data-ttu-id="285b9-128">Anger det jobb som innehåller uppgifter som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="285b9-128">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="285b9-129">För att hämta ett **PSCloudJob** -objekt, Använd cmdleten Get-AzureBatchJob.</span><span class="sxs-lookup"><span data-stu-id="285b9-129">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="285b9-130">-JobId</span><span class="sxs-lookup"><span data-stu-id="285b9-130">-JobId</span></span>
<span data-ttu-id="285b9-131">ID för det jobb som du vill hämta aktiviteter för.</span><span class="sxs-lookup"><span data-stu-id="285b9-131">The id of the job for which to get task counts.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="285b9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="285b9-132">CommonParameters</span></span>
<span data-ttu-id="285b9-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="285b9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="285b9-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="285b9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="285b9-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="285b9-135">INPUTS</span></span>

### <span data-ttu-id="285b9-136">System. String</span><span class="sxs-lookup"><span data-stu-id="285b9-136">System.String</span></span>

### <span data-ttu-id="285b9-137">Microsoft.Azure.Commands.BatCH. Modeller. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="285b9-137">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>
<span data-ttu-id="285b9-138">Parametrar: Job (ByValue)</span><span class="sxs-lookup"><span data-stu-id="285b9-138">Parameters: Job (ByValue)</span></span>

### <span data-ttu-id="285b9-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="285b9-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="285b9-140">Parametrar: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="285b9-140">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="285b9-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="285b9-141">OUTPUTS</span></span>

### <span data-ttu-id="285b9-142">Microsoft.Azure.Commands.BatCH. Modeller. PSTaskCounts</span><span class="sxs-lookup"><span data-stu-id="285b9-142">Microsoft.Azure.Commands.Batch.Models.PSTaskCounts</span></span>

## <span data-ttu-id="285b9-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="285b9-143">NOTES</span></span>

## <span data-ttu-id="285b9-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="285b9-144">RELATED LINKS</span></span>

[<span data-ttu-id="285b9-145">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="285b9-145">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="285b9-146">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="285b9-146">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="285b9-147">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="285b9-147">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
