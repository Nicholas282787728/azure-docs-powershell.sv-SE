---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 975B707C-5001-43ED-81AB-9BB6665135BA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJob.md
ms.openlocfilehash: f67660cdc64c814d04ec4a987b711c802ca222d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578976"
---
# <span data-ttu-id="88e5d-101">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="88e5d-101">Stop-AzureBatchJob</span></span>

## <span data-ttu-id="88e5d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="88e5d-102">SYNOPSIS</span></span>
<span data-ttu-id="88e5d-103">Stoppar ett batchjobb.</span><span class="sxs-lookup"><span data-stu-id="88e5d-103">Stops a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88e5d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="88e5d-104">SYNTAX</span></span>

```
Stop-AzureBatchJob [-Id] <String> [[-TerminateReason] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88e5d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="88e5d-105">DESCRIPTION</span></span>
<span data-ttu-id="88e5d-106">Cmdleten **Stop-AzureBatchJob** stoppar ett Azure-batchjobb.</span><span class="sxs-lookup"><span data-stu-id="88e5d-106">The **Stop-AzureBatchJob** cmdlet stops an Azure Batch job.</span></span>
<span data-ttu-id="88e5d-107">Det här kommandot anger att jobbet är slutfört.</span><span class="sxs-lookup"><span data-stu-id="88e5d-107">This command marks the job as completed.</span></span>

## <span data-ttu-id="88e5d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="88e5d-108">EXAMPLES</span></span>

### <span data-ttu-id="88e5d-109">Exempel 1: stoppa ett batchjobb</span><span class="sxs-lookup"><span data-stu-id="88e5d-109">Example 1: Stop a Batch job</span></span>
```
PS C:\>Stop-AzureBatchJob -Id "Job-000001" -TerminateReason "No more tasks to run" -BatchContext $Context
```

<span data-ttu-id="88e5d-110">Det här kommandot stoppar jobbet som har ID-000001.</span><span class="sxs-lookup"><span data-stu-id="88e5d-110">This command stops the job that has the ID Job-000001.</span></span>
<span data-ttu-id="88e5d-111">Kommandot anger en orsak till att du har valt att stoppa jobbet.</span><span class="sxs-lookup"><span data-stu-id="88e5d-111">The command specifies a reason that you chose to stop the job.</span></span>
<span data-ttu-id="88e5d-112">Använd Get-AzureRmBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="88e5d-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="88e5d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="88e5d-113">PARAMETERS</span></span>

### <span data-ttu-id="88e5d-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="88e5d-114">-BatchContext</span></span>
<span data-ttu-id="88e5d-115">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="88e5d-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="88e5d-116">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="88e5d-116">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="88e5d-117">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="88e5d-117">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="88e5d-118">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="88e5d-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="88e5d-119">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="88e5d-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="88e5d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88e5d-120">-DefaultProfile</span></span>
<span data-ttu-id="88e5d-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="88e5d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88e5d-122">-ID</span><span class="sxs-lookup"><span data-stu-id="88e5d-122">-Id</span></span>
<span data-ttu-id="88e5d-123">Anger ID för det jobb som denna cmdlet stoppar.</span><span class="sxs-lookup"><span data-stu-id="88e5d-123">Specifies the ID of the job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="88e5d-124">-TerminateReason</span><span class="sxs-lookup"><span data-stu-id="88e5d-124">-TerminateReason</span></span>
<span data-ttu-id="88e5d-125">Anger skälet till att avbryta jobbet.</span><span class="sxs-lookup"><span data-stu-id="88e5d-125">Specifies the reason that you decided to stop the job.</span></span>
<span data-ttu-id="88e5d-126">Denna cmdlet lagrar den här texten som **TerminateReason** -egenskap för jobbet.</span><span class="sxs-lookup"><span data-stu-id="88e5d-126">This cmdlet stores this text as the **TerminateReason** property of the job.</span></span>

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

### <span data-ttu-id="88e5d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88e5d-127">CommonParameters</span></span>
<span data-ttu-id="88e5d-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88e5d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88e5d-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88e5d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88e5d-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="88e5d-130">INPUTS</span></span>

### <span data-ttu-id="88e5d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="88e5d-131">System.String</span></span>

### <span data-ttu-id="88e5d-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="88e5d-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="88e5d-133">Parametrar: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="88e5d-133">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="88e5d-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="88e5d-134">OUTPUTS</span></span>

### <span data-ttu-id="88e5d-135">System. Void</span><span class="sxs-lookup"><span data-stu-id="88e5d-135">System.Void</span></span>

## <span data-ttu-id="88e5d-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="88e5d-136">NOTES</span></span>

## <span data-ttu-id="88e5d-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="88e5d-137">RELATED LINKS</span></span>

[<span data-ttu-id="88e5d-138">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="88e5d-138">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="88e5d-139">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="88e5d-139">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="88e5d-140">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="88e5d-140">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="88e5d-141">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="88e5d-141">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="88e5d-142">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="88e5d-142">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="88e5d-143">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="88e5d-143">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="88e5d-144">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="88e5d-144">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


