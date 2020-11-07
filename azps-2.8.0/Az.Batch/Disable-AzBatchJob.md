---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C831F934-7513-4882-A155-816E56CD9807
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJob.md
ms.openlocfilehash: c560964308fe3bb2195f601f2e4138e022aa41e0
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93928461"
---
# <span data-ttu-id="a2c07-101">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a2c07-101">Disable-AzBatchJob</span></span>

## <span data-ttu-id="a2c07-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a2c07-102">SYNOPSIS</span></span>
<span data-ttu-id="a2c07-103">Inaktiverar ett batchjobb.</span><span class="sxs-lookup"><span data-stu-id="a2c07-103">Disables a Batch job.</span></span>

## <span data-ttu-id="a2c07-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a2c07-104">SYNTAX</span></span>

```
Disable-AzBatchJob [-Id] <String> [-DisableJobOption] <DisableJobOption> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2c07-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a2c07-105">DESCRIPTION</span></span>
<span data-ttu-id="a2c07-106">Cmdleten **disable-AzBatchJob** inaktiverar ett Azure-batchjobb.</span><span class="sxs-lookup"><span data-stu-id="a2c07-106">The **Disable-AzBatchJob** cmdlet disables an Azure Batch job.</span></span>
<span data-ttu-id="a2c07-107">När du har aktiverat ett jobb kan nya aktiviteter köras.</span><span class="sxs-lookup"><span data-stu-id="a2c07-107">After you enable a job, new tasks can run.</span></span>
<span data-ttu-id="a2c07-108">Inaktiva jobb kör inte nya aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="a2c07-108">Disabled jobs do not run new tasks.</span></span>
<span data-ttu-id="a2c07-109">Du kan aktivera ett inaktiverat jobb senare.</span><span class="sxs-lookup"><span data-stu-id="a2c07-109">You can enable a disabled job later.</span></span>

## <span data-ttu-id="a2c07-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a2c07-110">EXAMPLES</span></span>

### <span data-ttu-id="a2c07-111">Exempel 1: inaktivera ett batchjobb</span><span class="sxs-lookup"><span data-stu-id="a2c07-111">Example 1: Disable a Batch job</span></span>
```
PS C:\>Disable-AzBatchJob -Id "Job-000001" -DisableJobOption "Terminate" -BatchContext $Context
```

<span data-ttu-id="a2c07-112">Det här kommandot inaktiverar jobbet med ID-000001.</span><span class="sxs-lookup"><span data-stu-id="a2c07-112">This command disables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="a2c07-113">Kommandot avslutar aktiva uppgifter för jobbet.</span><span class="sxs-lookup"><span data-stu-id="a2c07-113">The command terminates active tasks for the job.</span></span>
<span data-ttu-id="a2c07-114">Använd cmdleten **Get-AzBatchAccountKeys** för att tilldela en kontext till variabeln $context.</span><span class="sxs-lookup"><span data-stu-id="a2c07-114">Use the **Get-AzBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="a2c07-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a2c07-115">PARAMETERS</span></span>

### <span data-ttu-id="a2c07-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a2c07-116">-BatchContext</span></span>
<span data-ttu-id="a2c07-117">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a2c07-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a2c07-118">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a2c07-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a2c07-119">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="a2c07-119">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a2c07-120">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="a2c07-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a2c07-121">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="a2c07-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a2c07-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2c07-122">-DefaultProfile</span></span>
<span data-ttu-id="a2c07-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a2c07-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2c07-124">-DisableJobOption</span><span class="sxs-lookup"><span data-stu-id="a2c07-124">-DisableJobOption</span></span>
<span data-ttu-id="a2c07-125">Ange vad du vill göra med aktiva uppgifter som är kopplade till det jobb som denna cmdlet inaktiverar.</span><span class="sxs-lookup"><span data-stu-id="a2c07-125">Specifies what to do with active tasks associated with the job that this cmdlet disables.</span></span>
<span data-ttu-id="a2c07-126">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="a2c07-126">Valid values are:</span></span> 
- <span data-ttu-id="a2c07-127">Köa om</span><span class="sxs-lookup"><span data-stu-id="a2c07-127">Requeue</span></span> 
- <span data-ttu-id="a2c07-128">Säga upp</span><span class="sxs-lookup"><span data-stu-id="a2c07-128">Terminate</span></span> 
- <span data-ttu-id="a2c07-129">Vänta</span><span class="sxs-lookup"><span data-stu-id="a2c07-129">Wait</span></span>

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

### <span data-ttu-id="a2c07-130">-ID</span><span class="sxs-lookup"><span data-stu-id="a2c07-130">-Id</span></span>
<span data-ttu-id="a2c07-131">Anger ID för det jobb som denna cmdlet inaktiverar.</span><span class="sxs-lookup"><span data-stu-id="a2c07-131">Specifies the ID of the job that this cmdlet disables.</span></span>

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

### <span data-ttu-id="a2c07-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2c07-132">CommonParameters</span></span>
<span data-ttu-id="a2c07-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2c07-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2c07-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2c07-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2c07-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a2c07-135">INPUTS</span></span>

### <span data-ttu-id="a2c07-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a2c07-136">System.String</span></span>

### <span data-ttu-id="a2c07-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a2c07-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a2c07-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a2c07-138">OUTPUTS</span></span>

### <span data-ttu-id="a2c07-139">System. Void</span><span class="sxs-lookup"><span data-stu-id="a2c07-139">System.Void</span></span>

## <span data-ttu-id="a2c07-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a2c07-140">NOTES</span></span>

## <span data-ttu-id="a2c07-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a2c07-141">RELATED LINKS</span></span>

[<span data-ttu-id="a2c07-142">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a2c07-142">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="a2c07-143">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a2c07-143">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="a2c07-144">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a2c07-144">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="a2c07-145">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a2c07-145">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="a2c07-146">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a2c07-146">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="a2c07-147">Stopp-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a2c07-147">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="a2c07-148">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="a2c07-148">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


