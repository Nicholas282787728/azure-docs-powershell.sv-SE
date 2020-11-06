---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 975B707C-5001-43ED-81AB-9BB6665135BA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJob.md
ms.openlocfilehash: 8893ed4002e576e257cd9b885d5773c5851edde0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580684"
---
# <span data-ttu-id="d4739-101">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="d4739-101">Stop-AzureBatchJob</span></span>

## <span data-ttu-id="d4739-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d4739-102">SYNOPSIS</span></span>
<span data-ttu-id="d4739-103">Stoppar ett batchjobb.</span><span class="sxs-lookup"><span data-stu-id="d4739-103">Stops a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4739-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d4739-104">SYNTAX</span></span>

```
Stop-AzureBatchJob [-Id] <String> [[-TerminateReason] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4739-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d4739-105">DESCRIPTION</span></span>
<span data-ttu-id="d4739-106">Cmdleten **Stop-AzureBatchJob** stoppar ett Azure-batchjobb.</span><span class="sxs-lookup"><span data-stu-id="d4739-106">The **Stop-AzureBatchJob** cmdlet stops an Azure Batch job.</span></span>
<span data-ttu-id="d4739-107">Det här kommandot anger att jobbet är slutfört.</span><span class="sxs-lookup"><span data-stu-id="d4739-107">This command marks the job as completed.</span></span>

## <span data-ttu-id="d4739-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d4739-108">EXAMPLES</span></span>

### <span data-ttu-id="d4739-109">Exempel 1: stoppa ett batchjobb</span><span class="sxs-lookup"><span data-stu-id="d4739-109">Example 1: Stop a Batch job</span></span>
```
PS C:\>Stop-AzureBatchJob -Id "Job-000001" -TerminateReason "No more tasks to run" -BatchContext $Context
```

<span data-ttu-id="d4739-110">Det här kommandot stoppar jobbet som har ID-000001.</span><span class="sxs-lookup"><span data-stu-id="d4739-110">This command stops the job that has the ID Job-000001.</span></span>
<span data-ttu-id="d4739-111">Kommandot anger en orsak till att du har valt att stoppa jobbet.</span><span class="sxs-lookup"><span data-stu-id="d4739-111">The command specifies a reason that you chose to stop the job.</span></span>
<span data-ttu-id="d4739-112">Använd Get-AzureRmBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="d4739-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="d4739-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d4739-113">PARAMETERS</span></span>

### <span data-ttu-id="d4739-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d4739-114">-BatchContext</span></span>
<span data-ttu-id="d4739-115">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="d4739-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d4739-116">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="d4739-116">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="d4739-117">-ID</span><span class="sxs-lookup"><span data-stu-id="d4739-117">-Id</span></span>
<span data-ttu-id="d4739-118">Anger ID för det jobb som denna cmdlet stoppar.</span><span class="sxs-lookup"><span data-stu-id="d4739-118">Specifies the ID of the job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="d4739-119">-TerminateReason</span><span class="sxs-lookup"><span data-stu-id="d4739-119">-TerminateReason</span></span>
<span data-ttu-id="d4739-120">Anger skälet till att avbryta jobbet.</span><span class="sxs-lookup"><span data-stu-id="d4739-120">Specifies the reason that you decided to stop the job.</span></span>
<span data-ttu-id="d4739-121">Denna cmdlet lagrar den här texten som **TerminateReason** -egenskap för jobbet.</span><span class="sxs-lookup"><span data-stu-id="d4739-121">This cmdlet stores this text as the **TerminateReason** property of the job.</span></span>

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

### <span data-ttu-id="d4739-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4739-122">-DefaultProfile</span></span>
<span data-ttu-id="d4739-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d4739-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4739-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4739-124">CommonParameters</span></span>
<span data-ttu-id="d4739-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4739-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4739-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4739-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4739-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d4739-127">INPUTS</span></span>

### <span data-ttu-id="d4739-128">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d4739-128">BatchAccountContext</span></span>
<span data-ttu-id="d4739-129">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="d4739-129">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="d4739-130">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="d4739-130">String</span></span>
<span data-ttu-id="d4739-131">Parametern ' ID ' godkänner värdet för typen ' String ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="d4739-131">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="d4739-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d4739-132">OUTPUTS</span></span>

## <span data-ttu-id="d4739-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d4739-133">NOTES</span></span>

## <span data-ttu-id="d4739-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d4739-134">RELATED LINKS</span></span>

[<span data-ttu-id="d4739-135">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="d4739-135">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="d4739-136">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="d4739-136">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="d4739-137">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="d4739-137">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="d4739-138">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="d4739-138">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="d4739-139">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="d4739-139">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="d4739-140">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="d4739-140">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="d4739-141">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="d4739-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


