---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
ms.openlocfilehash: c012fe266bc25752729b14192c4d9c0a42cd8961
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585839"
---
# <span data-ttu-id="c6794-101">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c6794-101">Enable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="c6794-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c6794-102">SYNOPSIS</span></span>
<span data-ttu-id="c6794-103">Aktiverar ett batchjobb.</span><span class="sxs-lookup"><span data-stu-id="c6794-103">Enables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6794-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c6794-104">SYNTAX</span></span>

```
Enable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6794-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c6794-105">DESCRIPTION</span></span>
<span data-ttu-id="c6794-106">Cmdleten **Enable-AzureBatchJobSchedule** aktiverar ett Azure batch-jobb.</span><span class="sxs-lookup"><span data-stu-id="c6794-106">The **Enable-AzureBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="c6794-107">När du har aktiverat en jobb schema kan jobb skapas enligt det schemat.</span><span class="sxs-lookup"><span data-stu-id="c6794-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="c6794-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c6794-108">EXAMPLES</span></span>

### <span data-ttu-id="c6794-109">Exempel 1: aktivera ett jobb schema</span><span class="sxs-lookup"><span data-stu-id="c6794-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="c6794-110">Det här kommandot aktiverar det jobb schema som har ID-JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="c6794-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="c6794-111">Använd cmdleten **Get-AzureRmBatchAccountKeys** för att tilldela en kontext till variabeln $context.</span><span class="sxs-lookup"><span data-stu-id="c6794-111">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="c6794-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c6794-112">PARAMETERS</span></span>

### <span data-ttu-id="c6794-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c6794-113">-BatchContext</span></span>
<span data-ttu-id="c6794-114">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c6794-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c6794-115">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="c6794-115">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="c6794-116">-ID</span><span class="sxs-lookup"><span data-stu-id="c6794-116">-Id</span></span>
<span data-ttu-id="c6794-117">Anger ID för det projekt schema som denna cmdlet aktiverar.</span><span class="sxs-lookup"><span data-stu-id="c6794-117">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

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

### <span data-ttu-id="c6794-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6794-118">-DefaultProfile</span></span>
<span data-ttu-id="c6794-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c6794-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6794-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6794-120">CommonParameters</span></span>
<span data-ttu-id="c6794-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6794-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6794-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6794-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6794-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c6794-123">INPUTS</span></span>

### <span data-ttu-id="c6794-124">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c6794-124">BatchAccountContext</span></span>
<span data-ttu-id="c6794-125">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="c6794-125">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="c6794-126">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="c6794-126">String</span></span>
<span data-ttu-id="c6794-127">Parametern ' ID ' godkänner värdet för typen ' String ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="c6794-127">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="c6794-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c6794-128">OUTPUTS</span></span>

## <span data-ttu-id="c6794-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c6794-129">NOTES</span></span>

## <span data-ttu-id="c6794-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c6794-130">RELATED LINKS</span></span>

[<span data-ttu-id="c6794-131">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c6794-131">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="c6794-132">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c6794-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="c6794-133">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c6794-133">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="c6794-134">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c6794-134">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="c6794-135">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c6794-135">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="c6794-136">Stopp-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c6794-136">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="c6794-137">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="c6794-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


