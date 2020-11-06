---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C831F934-7513-4882-A155-816E56CD9807
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/disable-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJob.md
ms.openlocfilehash: fcb3586d1c27fd95c6bf386943830b92635162e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586372"
---
# <span data-ttu-id="bd49a-101">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="bd49a-101">Disable-AzureBatchJob</span></span>

## <span data-ttu-id="bd49a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bd49a-102">SYNOPSIS</span></span>
<span data-ttu-id="bd49a-103">Inaktiverar ett batchjobb.</span><span class="sxs-lookup"><span data-stu-id="bd49a-103">Disables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd49a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bd49a-104">SYNTAX</span></span>

```
Disable-AzureBatchJob [-Id] <String> [-DisableJobOption] <DisableJobOption> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd49a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bd49a-105">DESCRIPTION</span></span>
<span data-ttu-id="bd49a-106">Cmdleten **disable-AzureBatchJob** inaktiverar ett Azure-batchjobb.</span><span class="sxs-lookup"><span data-stu-id="bd49a-106">The **Disable-AzureBatchJob** cmdlet disables an Azure Batch job.</span></span>
<span data-ttu-id="bd49a-107">När du har aktiverat ett jobb kan nya aktiviteter köras.</span><span class="sxs-lookup"><span data-stu-id="bd49a-107">After you enable a job, new tasks can run.</span></span>
<span data-ttu-id="bd49a-108">Inaktiva jobb kör inte nya aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="bd49a-108">Disabled jobs do not run new tasks.</span></span>
<span data-ttu-id="bd49a-109">Du kan aktivera ett inaktiverat jobb senare.</span><span class="sxs-lookup"><span data-stu-id="bd49a-109">You can enable a disabled job later.</span></span>

## <span data-ttu-id="bd49a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bd49a-110">EXAMPLES</span></span>

### <span data-ttu-id="bd49a-111">Exempel 1: inaktivera ett batchjobb</span><span class="sxs-lookup"><span data-stu-id="bd49a-111">Example 1: Disable a Batch job</span></span>
```
PS C:\>Disable-AzureBatchJob -Id "Job-000001" -DisableJobOption "Terminate" -BatchContext $Context
```

<span data-ttu-id="bd49a-112">Det här kommandot inaktiverar jobbet med ID-000001.</span><span class="sxs-lookup"><span data-stu-id="bd49a-112">This command disables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="bd49a-113">Kommandot avslutar aktiva uppgifter för jobbet.</span><span class="sxs-lookup"><span data-stu-id="bd49a-113">The command terminates active tasks for the job.</span></span>
<span data-ttu-id="bd49a-114">Använd cmdleten **Get-AzureRmBatchAccountKeys** för att tilldela en kontext till variabeln $context.</span><span class="sxs-lookup"><span data-stu-id="bd49a-114">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="bd49a-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bd49a-115">PARAMETERS</span></span>

### <span data-ttu-id="bd49a-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="bd49a-116">-BatchContext</span></span>
<span data-ttu-id="bd49a-117">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="bd49a-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="bd49a-118">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="bd49a-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="bd49a-119">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="bd49a-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="bd49a-120">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="bd49a-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="bd49a-121">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="bd49a-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="bd49a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd49a-122">-DefaultProfile</span></span>
<span data-ttu-id="bd49a-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bd49a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd49a-124">-DisableJobOption</span><span class="sxs-lookup"><span data-stu-id="bd49a-124">-DisableJobOption</span></span>
<span data-ttu-id="bd49a-125">Ange vad du vill göra med aktiva uppgifter som är kopplade till det jobb som denna cmdlet inaktiverar.</span><span class="sxs-lookup"><span data-stu-id="bd49a-125">Specifies what to do with active tasks associated with the job that this cmdlet disables.</span></span>
<span data-ttu-id="bd49a-126">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="bd49a-126">Valid values are:</span></span> 

- <span data-ttu-id="bd49a-127">Köa om</span><span class="sxs-lookup"><span data-stu-id="bd49a-127">Requeue</span></span> 
- <span data-ttu-id="bd49a-128">Säga upp</span><span class="sxs-lookup"><span data-stu-id="bd49a-128">Terminate</span></span> 
- <span data-ttu-id="bd49a-129">Vänta</span><span class="sxs-lookup"><span data-stu-id="bd49a-129">Wait</span></span>

```yaml
Type: DisableJobOption
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, Wait

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd49a-130">-ID</span><span class="sxs-lookup"><span data-stu-id="bd49a-130">-Id</span></span>
<span data-ttu-id="bd49a-131">Anger ID för det jobb som denna cmdlet inaktiverar.</span><span class="sxs-lookup"><span data-stu-id="bd49a-131">Specifies the ID of the job that this cmdlet disables.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd49a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd49a-132">CommonParameters</span></span>
<span data-ttu-id="bd49a-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd49a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd49a-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd49a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd49a-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bd49a-135">INPUTS</span></span>

### <span data-ttu-id="bd49a-136">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="bd49a-136">BatchAccountContext</span></span>
<span data-ttu-id="bd49a-137">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="bd49a-137">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="bd49a-138">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="bd49a-138">String</span></span>
<span data-ttu-id="bd49a-139">Parametern ' ID ' godkänner värdet för typen ' String ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="bd49a-139">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="bd49a-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bd49a-140">OUTPUTS</span></span>

## <span data-ttu-id="bd49a-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bd49a-141">NOTES</span></span>

## <span data-ttu-id="bd49a-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bd49a-142">RELATED LINKS</span></span>

[<span data-ttu-id="bd49a-143">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="bd49a-143">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="bd49a-144">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="bd49a-144">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="bd49a-145">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="bd49a-145">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="bd49a-146">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="bd49a-146">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="bd49a-147">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="bd49a-147">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="bd49a-148">Stopp-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="bd49a-148">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="bd49a-149">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="bd49a-149">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


