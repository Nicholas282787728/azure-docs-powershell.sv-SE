---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchtaskcount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
ms.openlocfilehash: d1f493556a1ff1007073611338b937ef0715c164
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412128"
---
# <span data-ttu-id="aea8d-101">Get-AzBatchTaskCount</span><span class="sxs-lookup"><span data-stu-id="aea8d-101">Get-AzBatchTaskCount</span></span>

## <span data-ttu-id="aea8d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aea8d-102">SYNOPSIS</span></span>
<span data-ttu-id="aea8d-103">Hämtar antalet aktiviteter för det angivna jobbet.</span><span class="sxs-lookup"><span data-stu-id="aea8d-103">Gets the task counts for the specified job.</span></span>

## <span data-ttu-id="aea8d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aea8d-104">SYNTAX</span></span>

### <span data-ttu-id="aea8d-105">Et</span><span class="sxs-lookup"><span data-stu-id="aea8d-105">Id</span></span>
```
Get-AzBatchTaskCount [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aea8d-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="aea8d-106">ParentObject</span></span>
```
Get-AzBatchTaskCount [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aea8d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aea8d-107">DESCRIPTION</span></span>
<span data-ttu-id="aea8d-108">Cmdleten **Get-AzBatchTaskCount** hämtar antalet Azure Batch-uppgifter för ett batchjobb.</span><span class="sxs-lookup"><span data-stu-id="aea8d-108">The **Get-AzBatchTaskCount** cmdlet gets the Azure Batch tasks count for a Batch job.</span></span>
<span data-ttu-id="aea8d-109">Ange ett jobb genom parametern *jobId* eller *jobb* parameter.</span><span class="sxs-lookup"><span data-stu-id="aea8d-109">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="aea8d-110">Med aktivitets antal får du ett antal aktiviteter som är aktiva, kör eller slutförda aktivitets tillstånd och antalet uppgifter som lyckades eller misslyckades.</span><span class="sxs-lookup"><span data-stu-id="aea8d-110">Task counts provide a count of the tasks by active, running or completed task state, and a count of tasks which succeeded or failed.</span></span> <span data-ttu-id="aea8d-111">Uppgifter i tillståndet för att förbereda räknas som körs.</span><span class="sxs-lookup"><span data-stu-id="aea8d-111">Tasks in the preparing state are counted as running.</span></span> <span data-ttu-id="aea8d-112">Om validationStatus är avverifierat har batch-tjänsten inte kunnat kontrol lera status för de uppgifter som rapporter ATS i API för List aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="aea8d-112">If the validationStatus is unvalidated, then the Batch service has not been able to check state counts against the task states as reported in the List Tasks API.</span></span> <span data-ttu-id="aea8d-113">ValidationStatus kan vara avverifierad om jobbet innehåller fler än 200 000 uppgifter.</span><span class="sxs-lookup"><span data-stu-id="aea8d-113">The validationStatus may be unvalidated if the job contains more than 200,000 tasks.</span></span>

## <span data-ttu-id="aea8d-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aea8d-114">EXAMPLES</span></span>

### <span data-ttu-id="aea8d-115">Exempel 1: Hämta antal aktiviteter efter ID</span><span class="sxs-lookup"><span data-stu-id="aea8d-115">Example 1: Get task counts by ID</span></span>
```
PS C:\> Get-AzBatchTaskCount -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

<span data-ttu-id="aea8d-116">Det här kommandot får antalet aktiviteter för jobbet Job01.</span><span class="sxs-lookup"><span data-stu-id="aea8d-116">This command gets the task counts for job Job01.</span></span>
<span data-ttu-id="aea8d-117">Använd Get-AzBatchAccountKey cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="aea8d-117">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="aea8d-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aea8d-118">PARAMETERS</span></span>

### <span data-ttu-id="aea8d-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="aea8d-119">-BatchContext</span></span>
<span data-ttu-id="aea8d-120">Den BatchAccountContext-instans som ska användas vid interaktion med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="aea8d-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="aea8d-121">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="aea8d-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="aea8d-122">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="aea8d-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="aea8d-123">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="aea8d-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="aea8d-124">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="aea8d-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="aea8d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aea8d-125">-DefaultProfile</span></span>
<span data-ttu-id="aea8d-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="aea8d-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aea8d-127">-Jobb</span><span class="sxs-lookup"><span data-stu-id="aea8d-127">-Job</span></span>
<span data-ttu-id="aea8d-128">Anger det jobb som innehåller uppgifter som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="aea8d-128">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="aea8d-129">För att hämta ett **PSCloudJob** -objekt, Använd cmdleten Get-AzBatchJob.</span><span class="sxs-lookup"><span data-stu-id="aea8d-129">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="aea8d-130">-JobId</span><span class="sxs-lookup"><span data-stu-id="aea8d-130">-JobId</span></span>
<span data-ttu-id="aea8d-131">ID för det jobb som du vill hämta aktiviteter för.</span><span class="sxs-lookup"><span data-stu-id="aea8d-131">The id of the job for which to get task counts.</span></span>

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

### <span data-ttu-id="aea8d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aea8d-132">CommonParameters</span></span>
<span data-ttu-id="aea8d-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aea8d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aea8d-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aea8d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aea8d-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aea8d-135">INPUTS</span></span>

### <span data-ttu-id="aea8d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="aea8d-136">System.String</span></span>

### <span data-ttu-id="aea8d-137">Microsoft.Azure.Commands.BatCH. Modeller. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="aea8d-137">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="aea8d-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="aea8d-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="aea8d-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aea8d-139">OUTPUTS</span></span>

### <span data-ttu-id="aea8d-140">Microsoft.Azure.Commands.BatCH. Modeller. PSTaskCounts</span><span class="sxs-lookup"><span data-stu-id="aea8d-140">Microsoft.Azure.Commands.Batch.Models.PSTaskCounts</span></span>

## <span data-ttu-id="aea8d-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aea8d-141">NOTES</span></span>

## <span data-ttu-id="aea8d-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aea8d-142">RELATED LINKS</span></span>

[<span data-ttu-id="aea8d-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="aea8d-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="aea8d-144">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="aea8d-144">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="aea8d-145">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="aea8d-145">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
