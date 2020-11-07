---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
ms.openlocfilehash: 665d7b64f3e8d83dd45ebc8de0cc36da960f8c35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758135"
---
# <span data-ttu-id="6c66d-101">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="6c66d-101">Enable-AzureBatchJob</span></span>

## <span data-ttu-id="6c66d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6c66d-102">SYNOPSIS</span></span>
<span data-ttu-id="6c66d-103">Aktiverar ett batchjobb.</span><span class="sxs-lookup"><span data-stu-id="6c66d-103">Enables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c66d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6c66d-104">SYNTAX</span></span>

```
Enable-AzureBatchJob [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c66d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6c66d-105">DESCRIPTION</span></span>
<span data-ttu-id="6c66d-106">Cmdleten **Enable-AzureBatchJob** aktiverar ett Azure-batchjobb.</span><span class="sxs-lookup"><span data-stu-id="6c66d-106">The **Enable-AzureBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="6c66d-107">När du har aktiverat ett jobb kan nya aktiviteter köras.</span><span class="sxs-lookup"><span data-stu-id="6c66d-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="6c66d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6c66d-108">EXAMPLES</span></span>

### <span data-ttu-id="6c66d-109">Exempel 1: aktivera ett batchjobb</span><span class="sxs-lookup"><span data-stu-id="6c66d-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzureBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="6c66d-110">Det här kommandot aktiverar jobbet med ID-000001.</span><span class="sxs-lookup"><span data-stu-id="6c66d-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="6c66d-111">Använd Get-AzureRmBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="6c66d-111">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="6c66d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6c66d-112">PARAMETERS</span></span>

### <span data-ttu-id="6c66d-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6c66d-113">-BatchContext</span></span>
<span data-ttu-id="6c66d-114">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="6c66d-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6c66d-115">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="6c66d-115">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="6c66d-116">-ID</span><span class="sxs-lookup"><span data-stu-id="6c66d-116">-Id</span></span>
<span data-ttu-id="6c66d-117">Anger ID för det jobb som denna cmdlet aktiverar.</span><span class="sxs-lookup"><span data-stu-id="6c66d-117">Specifies the ID of the job that this cmdlet enables.</span></span>

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

### <span data-ttu-id="6c66d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c66d-118">-DefaultProfile</span></span>
<span data-ttu-id="6c66d-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6c66d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c66d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c66d-120">CommonParameters</span></span>
<span data-ttu-id="6c66d-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c66d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c66d-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c66d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c66d-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6c66d-123">INPUTS</span></span>

### <span data-ttu-id="6c66d-124">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6c66d-124">BatchAccountContext</span></span>
<span data-ttu-id="6c66d-125">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="6c66d-125">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="6c66d-126">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="6c66d-126">String</span></span>
<span data-ttu-id="6c66d-127">Parametern ' ID ' godkänner värdet för typen ' String ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="6c66d-127">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="6c66d-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6c66d-128">OUTPUTS</span></span>

## <span data-ttu-id="6c66d-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6c66d-129">NOTES</span></span>

## <span data-ttu-id="6c66d-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6c66d-130">RELATED LINKS</span></span>

[<span data-ttu-id="6c66d-131">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="6c66d-131">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="6c66d-132">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="6c66d-132">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="6c66d-133">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="6c66d-133">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="6c66d-134">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="6c66d-134">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="6c66d-135">Stopp-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="6c66d-135">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="6c66d-136">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="6c66d-136">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


