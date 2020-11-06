---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
ms.openlocfilehash: 58ac726d722959e3ee32bce84c0abe3c771fcbcc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580683"
---
# <span data-ttu-id="15aa4-101">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="15aa4-101">Stop-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="15aa4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="15aa4-102">SYNOPSIS</span></span>
<span data-ttu-id="15aa4-103">Stoppar ett batchjobb.</span><span class="sxs-lookup"><span data-stu-id="15aa4-103">Stops a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15aa4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="15aa4-104">SYNTAX</span></span>

```
Stop-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15aa4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="15aa4-105">DESCRIPTION</span></span>
<span data-ttu-id="15aa4-106">Cmdleten **Stop-AzureBatchJobSchedule** stoppar ett Azure Batch-schema.</span><span class="sxs-lookup"><span data-stu-id="15aa4-106">The **Stop-AzureBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="15aa4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="15aa4-107">EXAMPLES</span></span>

### <span data-ttu-id="15aa4-108">Exempel 1: stoppa ett schema</span><span class="sxs-lookup"><span data-stu-id="15aa4-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="15aa4-109">Det här kommandot stoppar projektschemat med ID-JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="15aa4-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="15aa4-110">Använd Get-AzureRmBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="15aa4-110">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="15aa4-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="15aa4-111">PARAMETERS</span></span>

### <span data-ttu-id="15aa4-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="15aa4-112">-BatchContext</span></span>
<span data-ttu-id="15aa4-113">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="15aa4-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="15aa4-114">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="15aa4-114">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="15aa4-115">-ID</span><span class="sxs-lookup"><span data-stu-id="15aa4-115">-Id</span></span>
<span data-ttu-id="15aa4-116">Anger ID för det fin schema som denna cmdlet slutar.</span><span class="sxs-lookup"><span data-stu-id="15aa4-116">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="15aa4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15aa4-117">-DefaultProfile</span></span>
<span data-ttu-id="15aa4-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="15aa4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15aa4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15aa4-119">CommonParameters</span></span>
<span data-ttu-id="15aa4-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15aa4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15aa4-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15aa4-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15aa4-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="15aa4-122">INPUTS</span></span>

### <span data-ttu-id="15aa4-123">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="15aa4-123">BatchAccountContext</span></span>
<span data-ttu-id="15aa4-124">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="15aa4-124">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="15aa4-125">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="15aa4-125">String</span></span>
<span data-ttu-id="15aa4-126">Parametern ' ID ' godkänner värdet för typen ' String ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="15aa4-126">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="15aa4-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="15aa4-127">OUTPUTS</span></span>

## <span data-ttu-id="15aa4-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="15aa4-128">NOTES</span></span>

## <span data-ttu-id="15aa4-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="15aa4-129">RELATED LINKS</span></span>

[<span data-ttu-id="15aa4-130">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="15aa4-130">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="15aa4-131">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="15aa4-131">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="15aa4-132">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="15aa4-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="15aa4-133">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="15aa4-133">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="15aa4-134">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="15aa4-134">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="15aa4-135">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="15aa4-135">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="15aa4-136">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="15aa4-136">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


