---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: E655684D-9601-4A0B-BB09-EFB787EB2B1B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchjobstatistics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobStatistics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobStatistics.md
ms.openlocfilehash: 80ee6f881731f61b045e448e8a231ae9c971552d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579644"
---
# <span data-ttu-id="c9eb3-101">Get-AzureBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="c9eb3-101">Get-AzureBatchJobStatistics</span></span>

## <span data-ttu-id="c9eb3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c9eb3-102">SYNOPSIS</span></span>
<span data-ttu-id="c9eb3-103">Hämtar statistik för jobb Sammanfattning för ett batch-konto.</span><span class="sxs-lookup"><span data-stu-id="c9eb3-103">Gets job summary statistics for a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9eb3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c9eb3-104">SYNTAX</span></span>

```
Get-AzureBatchJobStatistics -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c9eb3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c9eb3-105">DESCRIPTION</span></span>
<span data-ttu-id="c9eb3-106">Cmdleten **Get-AzureBatchJobStatistics** får livs längds statistik för alla jobb i ett Azure Batch-konto.</span><span class="sxs-lookup"><span data-stu-id="c9eb3-106">The **Get-AzureBatchJobStatistics** cmdlet gets lifetime summary statistics for all of the jobs in an Azure Batch account.</span></span>
<span data-ttu-id="c9eb3-107">Statistik samlas in på alla jobb som någonsin funnits i kontot, från skapande till den senaste uppdaterings tiden för statistiken.</span><span class="sxs-lookup"><span data-stu-id="c9eb3-107">Statistics are aggregated across all jobs that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="c9eb3-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c9eb3-108">EXAMPLES</span></span>

### <span data-ttu-id="c9eb3-109">Exempel 1: få sammanfattnings statistik för alla jobb</span><span class="sxs-lookup"><span data-stu-id="c9eb3-109">Example 1: Get summary statistics for all jobs</span></span>
```
PS C:\>Get-AzureBatchJobStatistics -BatchContext $Context
FailedTaskCount    : 330
KernelCpuTime      : 00:24:31.8440000
LastUpdateTime     : 5/16/2016 6:00:00 PM
ReadIOGiB          : 38.1271341182292
ReadIOps           : 26546054
StartTime          : 11/3/2015 9:47:14 PM
SucceededTaskCount : 766
TaskRetryCount     : 0
Url                : https://accountname.westus.batch.azure.com/lifetimejobstats
UserCpuTime        : 20:55:50.3200000
WaitTime           : 03:54:49.8530000
WallClockTime      : 20:55:50.3200000
WriteIOGiB         : 0.159623090177774
WriteIOps          : 146946
```

<span data-ttu-id="c9eb3-110">Det första kommandot skapar en objekt referens till konto nycklarna för batch-kontot som heter ContosoBatchAccount genom att använda **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="c9eb3-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="c9eb3-111">Kommandot lagrar objekt referensen i $Context variabel.</span><span class="sxs-lookup"><span data-stu-id="c9eb3-111">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="c9eb3-112">Det andra kommandot får sammanfattnings statistiken för alla jobb.</span><span class="sxs-lookup"><span data-stu-id="c9eb3-112">The second command gets the summary statistics for all of the jobs.</span></span>
<span data-ttu-id="c9eb3-113">Kommandot använder värdet $Context från det första kommandot.</span><span class="sxs-lookup"><span data-stu-id="c9eb3-113">The command uses the $Context value from the first command.</span></span>

## <span data-ttu-id="c9eb3-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c9eb3-114">PARAMETERS</span></span>

### <span data-ttu-id="c9eb3-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c9eb3-115">-BatchContext</span></span>
<span data-ttu-id="c9eb3-116">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c9eb3-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c9eb3-117">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c9eb3-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c9eb3-118">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="c9eb3-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c9eb3-119">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="c9eb3-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c9eb3-120">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="c9eb3-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c9eb3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9eb3-121">-DefaultProfile</span></span>
<span data-ttu-id="c9eb3-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c9eb3-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9eb3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9eb3-123">CommonParameters</span></span>
<span data-ttu-id="c9eb3-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9eb3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9eb3-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9eb3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9eb3-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c9eb3-126">INPUTS</span></span>

### <span data-ttu-id="c9eb3-127">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c9eb3-127">BatchAccountContext</span></span>
<span data-ttu-id="c9eb3-128">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="c9eb3-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="c9eb3-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c9eb3-129">OUTPUTS</span></span>

### <span data-ttu-id="c9eb3-130">PSJobStatistics</span><span class="sxs-lookup"><span data-stu-id="c9eb3-130">PSJobStatistics</span></span>

## <span data-ttu-id="c9eb3-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c9eb3-131">NOTES</span></span>

## <span data-ttu-id="c9eb3-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c9eb3-132">RELATED LINKS</span></span>

[<span data-ttu-id="c9eb3-133">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c9eb3-133">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="c9eb3-134">Get-AzureBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="c9eb3-134">Get-AzureBatchPoolStatistics</span></span>](./Get-AzureBatchPoolStatistics.md)

[<span data-ttu-id="c9eb3-135">Get-AzureBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="c9eb3-135">Get-AzureBatchPoolUsageMetrics</span></span>](./Get-AzureBatchPoolUsageMetrics.md)


