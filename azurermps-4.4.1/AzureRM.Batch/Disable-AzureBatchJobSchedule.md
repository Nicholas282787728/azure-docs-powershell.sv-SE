---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
ms.openlocfilehash: 73d80d3547ea895e5cbd35b2d514d9a757164bed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585847"
---
# <span data-ttu-id="8d27d-101">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8d27d-101">Disable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="8d27d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8d27d-102">SYNOPSIS</span></span>
<span data-ttu-id="8d27d-103">Inaktiverar schemaläggning av batchjobb.</span><span class="sxs-lookup"><span data-stu-id="8d27d-103">Disables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d27d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8d27d-104">SYNTAX</span></span>

```
Disable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d27d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8d27d-105">DESCRIPTION</span></span>
<span data-ttu-id="8d27d-106">Cmdleten **disable-AzureBatchJobSchedule** inaktiverar ett Azure Batch-schema.</span><span class="sxs-lookup"><span data-stu-id="8d27d-106">The **Disable-AzureBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="8d27d-107">Om du inaktiverar ett schema skapas inte jobb enligt det schemat.</span><span class="sxs-lookup"><span data-stu-id="8d27d-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="8d27d-108">Du kan aktivera ett inaktiverat schema senare.</span><span class="sxs-lookup"><span data-stu-id="8d27d-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="8d27d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8d27d-109">EXAMPLES</span></span>

### <span data-ttu-id="8d27d-110">Exempel 1: inaktivera en finplanera</span><span class="sxs-lookup"><span data-stu-id="8d27d-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="8d27d-111">Det här kommandot inaktiverar projektschemat med ID-JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="8d27d-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="8d27d-112">Använd cmdleten **Get-AzureRmBatchAccountKeys** för att tilldela en kontext till variabeln $context.</span><span class="sxs-lookup"><span data-stu-id="8d27d-112">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="8d27d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8d27d-113">PARAMETERS</span></span>

### <span data-ttu-id="8d27d-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8d27d-114">-BatchContext</span></span>
<span data-ttu-id="8d27d-115">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="8d27d-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8d27d-116">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="8d27d-116">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="8d27d-117">-ID</span><span class="sxs-lookup"><span data-stu-id="8d27d-117">-Id</span></span>
<span data-ttu-id="8d27d-118">Anger ID för det jobb schema som denna cmdlet inaktiverar.</span><span class="sxs-lookup"><span data-stu-id="8d27d-118">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

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

### <span data-ttu-id="8d27d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d27d-119">-DefaultProfile</span></span>
<span data-ttu-id="8d27d-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8d27d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d27d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d27d-121">CommonParameters</span></span>
<span data-ttu-id="8d27d-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d27d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d27d-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d27d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d27d-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8d27d-124">INPUTS</span></span>

### <span data-ttu-id="8d27d-125">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8d27d-125">BatchAccountContext</span></span>
<span data-ttu-id="8d27d-126">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="8d27d-126">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="8d27d-127">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="8d27d-127">String</span></span>
<span data-ttu-id="8d27d-128">Parametern ' ID ' godkänner värdet för typen ' String ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="8d27d-128">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="8d27d-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8d27d-129">OUTPUTS</span></span>

## <span data-ttu-id="8d27d-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8d27d-130">NOTES</span></span>

## <span data-ttu-id="8d27d-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8d27d-131">RELATED LINKS</span></span>

[<span data-ttu-id="8d27d-132">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8d27d-132">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="8d27d-133">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="8d27d-133">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="8d27d-134">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8d27d-134">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="8d27d-135">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8d27d-135">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="8d27d-136">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8d27d-136">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="8d27d-137">Stopp-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8d27d-137">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="8d27d-138">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="8d27d-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


