---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
ms.openlocfilehash: 3081721db5cb113d48417ddf28d8a96512d27f99
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583207"
---
# <span data-ttu-id="48407-101">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="48407-101">Enable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="48407-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="48407-102">SYNOPSIS</span></span>
<span data-ttu-id="48407-103">Aktiverar ett batchjobb.</span><span class="sxs-lookup"><span data-stu-id="48407-103">Enables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48407-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="48407-104">SYNTAX</span></span>

```
Enable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48407-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="48407-105">DESCRIPTION</span></span>
<span data-ttu-id="48407-106">Cmdleten **Enable-AzureBatchJobSchedule** aktiverar ett Azure batch-jobb.</span><span class="sxs-lookup"><span data-stu-id="48407-106">The **Enable-AzureBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="48407-107">När du har aktiverat en jobb schema kan jobb skapas enligt det schemat.</span><span class="sxs-lookup"><span data-stu-id="48407-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="48407-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="48407-108">EXAMPLES</span></span>

### <span data-ttu-id="48407-109">Exempel 1: aktivera ett jobb schema</span><span class="sxs-lookup"><span data-stu-id="48407-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="48407-110">Det här kommandot aktiverar det jobb schema som har ID-JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="48407-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="48407-111">Använd cmdleten **Get-AzureRmBatchAccountKeys** för att tilldela en kontext till variabeln $context.</span><span class="sxs-lookup"><span data-stu-id="48407-111">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="48407-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="48407-112">PARAMETERS</span></span>

### <span data-ttu-id="48407-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="48407-113">-BatchContext</span></span>
<span data-ttu-id="48407-114">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="48407-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="48407-115">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="48407-115">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="48407-116">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="48407-116">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="48407-117">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="48407-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="48407-118">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="48407-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="48407-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48407-119">-DefaultProfile</span></span>
<span data-ttu-id="48407-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="48407-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48407-121">-ID</span><span class="sxs-lookup"><span data-stu-id="48407-121">-Id</span></span>
<span data-ttu-id="48407-122">Anger ID för det projekt schema som denna cmdlet aktiverar.</span><span class="sxs-lookup"><span data-stu-id="48407-122">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

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

### <span data-ttu-id="48407-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48407-123">CommonParameters</span></span>
<span data-ttu-id="48407-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48407-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48407-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48407-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48407-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="48407-126">INPUTS</span></span>

### <span data-ttu-id="48407-127">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="48407-127">BatchAccountContext</span></span>
<span data-ttu-id="48407-128">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="48407-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="48407-129">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="48407-129">String</span></span>
<span data-ttu-id="48407-130">Parametern ' ID ' godkänner värdet för typen ' String ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="48407-130">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="48407-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="48407-131">OUTPUTS</span></span>

## <span data-ttu-id="48407-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="48407-132">NOTES</span></span>

## <span data-ttu-id="48407-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="48407-133">RELATED LINKS</span></span>

[<span data-ttu-id="48407-134">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="48407-134">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="48407-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="48407-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="48407-136">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="48407-136">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="48407-137">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="48407-137">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="48407-138">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="48407-138">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="48407-139">Stopp-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="48407-139">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="48407-140">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="48407-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


