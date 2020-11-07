---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C831F934-7513-4882-A155-816E56CD9807
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJob.md
ms.openlocfilehash: 2e19e6b1733ccc3dfe0a802756e2c0a517232803
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758136"
---
# <span data-ttu-id="36a2c-101">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="36a2c-101">Disable-AzureBatchJob</span></span>

## <span data-ttu-id="36a2c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="36a2c-102">SYNOPSIS</span></span>
<span data-ttu-id="36a2c-103">Inaktiverar ett batchjobb.</span><span class="sxs-lookup"><span data-stu-id="36a2c-103">Disables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36a2c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="36a2c-104">SYNTAX</span></span>

```
Disable-AzureBatchJob [-Id] <String> [-DisableJobOption] <DisableJobOption> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36a2c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="36a2c-105">DESCRIPTION</span></span>
<span data-ttu-id="36a2c-106">Cmdleten **disable-AzureBatchJob** inaktiverar ett Azure-batchjobb.</span><span class="sxs-lookup"><span data-stu-id="36a2c-106">The **Disable-AzureBatchJob** cmdlet disables an Azure Batch job.</span></span>
<span data-ttu-id="36a2c-107">När du har aktiverat ett jobb kan nya aktiviteter köras.</span><span class="sxs-lookup"><span data-stu-id="36a2c-107">After you enable a job, new tasks can run.</span></span>
<span data-ttu-id="36a2c-108">Inaktiva jobb kör inte nya aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="36a2c-108">Disabled jobs do not run new tasks.</span></span>
<span data-ttu-id="36a2c-109">Du kan aktivera ett inaktiverat jobb senare.</span><span class="sxs-lookup"><span data-stu-id="36a2c-109">You can enable a disabled job later.</span></span>

## <span data-ttu-id="36a2c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="36a2c-110">EXAMPLES</span></span>

### <span data-ttu-id="36a2c-111">Exempel 1: inaktivera ett batchjobb</span><span class="sxs-lookup"><span data-stu-id="36a2c-111">Example 1: Disable a Batch job</span></span>
```
PS C:\>Disable-AzureBatchJob -Id "Job-000001" -DisableJobOption "Terminate" -BatchContext $Context
```

<span data-ttu-id="36a2c-112">Det här kommandot inaktiverar jobbet med ID-000001.</span><span class="sxs-lookup"><span data-stu-id="36a2c-112">This command disables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="36a2c-113">Kommandot avslutar aktiva uppgifter för jobbet.</span><span class="sxs-lookup"><span data-stu-id="36a2c-113">The command terminates active tasks for the job.</span></span>
<span data-ttu-id="36a2c-114">Använd cmdleten **Get-AzureRmBatchAccountKeys** för att tilldela en kontext till variabeln $context.</span><span class="sxs-lookup"><span data-stu-id="36a2c-114">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="36a2c-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="36a2c-115">PARAMETERS</span></span>

### <span data-ttu-id="36a2c-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="36a2c-116">-BatchContext</span></span>
<span data-ttu-id="36a2c-117">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="36a2c-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="36a2c-118">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="36a2c-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="36a2c-119">-DisableJobOption</span><span class="sxs-lookup"><span data-stu-id="36a2c-119">-DisableJobOption</span></span>
<span data-ttu-id="36a2c-120">Ange vad du vill göra med aktiva uppgifter som är kopplade till det jobb som denna cmdlet inaktiverar.</span><span class="sxs-lookup"><span data-stu-id="36a2c-120">Specifies what to do with active tasks associated with the job that this cmdlet disables.</span></span>
<span data-ttu-id="36a2c-121">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="36a2c-121">Valid values are:</span></span> 

- <span data-ttu-id="36a2c-122">Köa om</span><span class="sxs-lookup"><span data-stu-id="36a2c-122">Requeue</span></span> 
- <span data-ttu-id="36a2c-123">Säga upp</span><span class="sxs-lookup"><span data-stu-id="36a2c-123">Terminate</span></span> 
- <span data-ttu-id="36a2c-124">Vänta</span><span class="sxs-lookup"><span data-stu-id="36a2c-124">Wait</span></span>

```yaml
Type: Microsoft.Azure.Batch.Common.DisableJobOption
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, Wait

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36a2c-125">-ID</span><span class="sxs-lookup"><span data-stu-id="36a2c-125">-Id</span></span>
<span data-ttu-id="36a2c-126">Anger ID för det jobb som denna cmdlet inaktiverar.</span><span class="sxs-lookup"><span data-stu-id="36a2c-126">Specifies the ID of the job that this cmdlet disables.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36a2c-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36a2c-127">-DefaultProfile</span></span>
<span data-ttu-id="36a2c-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="36a2c-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36a2c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36a2c-129">CommonParameters</span></span>
<span data-ttu-id="36a2c-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36a2c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36a2c-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36a2c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36a2c-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="36a2c-132">INPUTS</span></span>

### <span data-ttu-id="36a2c-133">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="36a2c-133">BatchAccountContext</span></span>
<span data-ttu-id="36a2c-134">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="36a2c-134">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="36a2c-135">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="36a2c-135">String</span></span>
<span data-ttu-id="36a2c-136">Parametern ' ID ' godkänner värdet för typen ' String ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="36a2c-136">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="36a2c-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="36a2c-137">OUTPUTS</span></span>

## <span data-ttu-id="36a2c-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="36a2c-138">NOTES</span></span>

## <span data-ttu-id="36a2c-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="36a2c-139">RELATED LINKS</span></span>

[<span data-ttu-id="36a2c-140">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="36a2c-140">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="36a2c-141">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="36a2c-141">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="36a2c-142">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="36a2c-142">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="36a2c-143">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="36a2c-143">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="36a2c-144">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="36a2c-144">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="36a2c-145">Stopp-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="36a2c-145">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="36a2c-146">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="36a2c-146">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


