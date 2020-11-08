---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 975B707C-5001-43ED-81AB-9BB6665135BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJob.md
ms.openlocfilehash: fa9945e80bfc3b94cf29e0751bc1ceedb36d12bd
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "94100467"
---
# <span data-ttu-id="72e55-101">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="72e55-101">Stop-AzBatchJob</span></span>

## <span data-ttu-id="72e55-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="72e55-102">SYNOPSIS</span></span>
<span data-ttu-id="72e55-103">Stoppar ett batchjobb.</span><span class="sxs-lookup"><span data-stu-id="72e55-103">Stops a Batch job.</span></span>

## <span data-ttu-id="72e55-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="72e55-104">SYNTAX</span></span>

```
Stop-AzBatchJob [-Id] <String> [[-TerminateReason] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72e55-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="72e55-105">DESCRIPTION</span></span>
<span data-ttu-id="72e55-106">Cmdleten **Stop-AzBatchJob** stoppar ett Azure-batchjobb.</span><span class="sxs-lookup"><span data-stu-id="72e55-106">The **Stop-AzBatchJob** cmdlet stops an Azure Batch job.</span></span>
<span data-ttu-id="72e55-107">Det här kommandot anger att jobbet är slutfört.</span><span class="sxs-lookup"><span data-stu-id="72e55-107">This command marks the job as completed.</span></span>

## <span data-ttu-id="72e55-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="72e55-108">EXAMPLES</span></span>

### <span data-ttu-id="72e55-109">Exempel 1: stoppa ett batchjobb</span><span class="sxs-lookup"><span data-stu-id="72e55-109">Example 1: Stop a Batch job</span></span>
```
PS C:\>Stop-AzBatchJob -Id "Job-000001" -TerminateReason "No more tasks to run" -BatchContext $Context
```

<span data-ttu-id="72e55-110">Det här kommandot stoppar jobbet som har ID-000001.</span><span class="sxs-lookup"><span data-stu-id="72e55-110">This command stops the job that has the ID Job-000001.</span></span>
<span data-ttu-id="72e55-111">Kommandot anger en orsak till att du har valt att stoppa jobbet.</span><span class="sxs-lookup"><span data-stu-id="72e55-111">The command specifies a reason that you chose to stop the job.</span></span>
<span data-ttu-id="72e55-112">Använd Get-AzBatchAccountKey cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="72e55-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="72e55-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="72e55-113">PARAMETERS</span></span>

### <span data-ttu-id="72e55-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="72e55-114">-BatchContext</span></span>
<span data-ttu-id="72e55-115">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="72e55-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="72e55-116">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="72e55-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="72e55-117">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="72e55-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="72e55-118">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="72e55-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="72e55-119">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="72e55-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="72e55-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72e55-120">-DefaultProfile</span></span>
<span data-ttu-id="72e55-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="72e55-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72e55-122">-ID</span><span class="sxs-lookup"><span data-stu-id="72e55-122">-Id</span></span>
<span data-ttu-id="72e55-123">Anger ID för det jobb som denna cmdlet stoppar.</span><span class="sxs-lookup"><span data-stu-id="72e55-123">Specifies the ID of the job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="72e55-124">-TerminateReason</span><span class="sxs-lookup"><span data-stu-id="72e55-124">-TerminateReason</span></span>
<span data-ttu-id="72e55-125">Anger skälet till att avbryta jobbet.</span><span class="sxs-lookup"><span data-stu-id="72e55-125">Specifies the reason that you decided to stop the job.</span></span>
<span data-ttu-id="72e55-126">Denna cmdlet lagrar den här texten som **TerminateReason** -egenskap för jobbet.</span><span class="sxs-lookup"><span data-stu-id="72e55-126">This cmdlet stores this text as the **TerminateReason** property of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e55-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72e55-127">CommonParameters</span></span>
<span data-ttu-id="72e55-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72e55-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72e55-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72e55-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72e55-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="72e55-130">INPUTS</span></span>

### <span data-ttu-id="72e55-131">System. String</span><span class="sxs-lookup"><span data-stu-id="72e55-131">System.String</span></span>

### <span data-ttu-id="72e55-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="72e55-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="72e55-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="72e55-133">OUTPUTS</span></span>

### <span data-ttu-id="72e55-134">System. Void</span><span class="sxs-lookup"><span data-stu-id="72e55-134">System.Void</span></span>

## <span data-ttu-id="72e55-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="72e55-135">NOTES</span></span>

## <span data-ttu-id="72e55-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="72e55-136">RELATED LINKS</span></span>

[<span data-ttu-id="72e55-137">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="72e55-137">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="72e55-138">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="72e55-138">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="72e55-139">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="72e55-139">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="72e55-140">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="72e55-140">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="72e55-141">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="72e55-141">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="72e55-142">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="72e55-142">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="72e55-143">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="72e55-143">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


