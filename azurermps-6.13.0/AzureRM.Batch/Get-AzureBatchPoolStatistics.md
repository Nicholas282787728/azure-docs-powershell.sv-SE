---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 8188C617-4895-4B43-8D3B-FA6FC5B868DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchpoolstatistics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolStatistics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolStatistics.md
ms.openlocfilehash: 0f6bee54c5abf795a49148e7c2d93707b45ba9a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580864"
---
# <span data-ttu-id="46ad0-101">Get-AzureBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="46ad0-101">Get-AzureBatchPoolStatistics</span></span>

## <span data-ttu-id="46ad0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="46ad0-102">SYNOPSIS</span></span>
<span data-ttu-id="46ad0-103">Sammanfattar statistik för pooler för ett batch-konto.</span><span class="sxs-lookup"><span data-stu-id="46ad0-103">Gets pool summary statistics for a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46ad0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="46ad0-104">SYNTAX</span></span>

```
Get-AzureBatchPoolStatistics -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="46ad0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="46ad0-105">DESCRIPTION</span></span>
<span data-ttu-id="46ad0-106">Cmdleten **Get-AzureBatchPoolStatistics** hämtar livs längds statistiken för alla pooler i angivet konto.</span><span class="sxs-lookup"><span data-stu-id="46ad0-106">The **Get-AzureBatchPoolStatistics** cmdlet gets the lifetime statistics for all of the pools in the specified account.</span></span>
<span data-ttu-id="46ad0-107">Statistik samlas in för alla pooler som någonsin funnits i kontot, från skapande till den senaste uppdaterings tiden för statistik.</span><span class="sxs-lookup"><span data-stu-id="46ad0-107">Statistics are aggregated across all pools that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="46ad0-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="46ad0-108">EXAMPLES</span></span>

### <span data-ttu-id="46ad0-109">Exempel 1: få resurs statistik för alla pooler på ett konto</span><span class="sxs-lookup"><span data-stu-id="46ad0-109">Example 1: Get resource statistics of all pools in an account</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $PoolStatistics = Get-AzureBatchPoolStatistics -BatchContext $Context
PS C:\> $PoolStatistics.ResourceStatistics 
AverageCpuPercentage : 0.351232518750755
AverageDiskGiB       : 55.2569014701165
AverageMemoryGiB     : 2.87273772318252
DiskReadGiB          : 45.1326256990433
DiskReadIOps         : 878278
DiskWriteGiB         : 1230.72120628133
DiskWriteIOps        : 176832212
LastUpdateTime       : 5/16/2016 4:30:00 PM
NetworkReadGiB       : 29.3502839952707
NetworkWriteGiB      : 25.5208827350289
PeakDiskGiB          : 21.9638671875
PeakMemoryGiB        : 1.11184692382813
StartTime            : 2/10/2016 7:07:24 PM
```

<span data-ttu-id="46ad0-110">Det första kommandot skapar en objekt referens till konto nycklarna för batch-kontot som heter ContosoBatchAccount genom att använda **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="46ad0-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="46ad0-111">Kommandot lagrar objekt referensen i $Context variabel.</span><span class="sxs-lookup"><span data-stu-id="46ad0-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="46ad0-112">Det andra kommandot får statistik för alla pooler på det angivna kontot och lagrar dem i $PoolStatistics.</span><span class="sxs-lookup"><span data-stu-id="46ad0-112">The second command gets the statistics of all of the pools in the specified account, and then stores them in the $PoolStatistics.</span></span>
<span data-ttu-id="46ad0-113">Det sista kommandot visar egenskapen **ResourceStatistics** för $PoolStatistics.</span><span class="sxs-lookup"><span data-stu-id="46ad0-113">The final command displays the **ResourceStatistics** property of $PoolStatistics.</span></span>

## <span data-ttu-id="46ad0-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="46ad0-114">PARAMETERS</span></span>

### <span data-ttu-id="46ad0-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="46ad0-115">-BatchContext</span></span>
<span data-ttu-id="46ad0-116">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="46ad0-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="46ad0-117">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="46ad0-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="46ad0-118">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="46ad0-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="46ad0-119">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="46ad0-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="46ad0-120">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="46ad0-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="46ad0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46ad0-121">-DefaultProfile</span></span>
<span data-ttu-id="46ad0-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="46ad0-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46ad0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46ad0-123">CommonParameters</span></span>
<span data-ttu-id="46ad0-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46ad0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46ad0-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46ad0-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46ad0-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="46ad0-126">INPUTS</span></span>

### <span data-ttu-id="46ad0-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="46ad0-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="46ad0-128">Parametrar: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="46ad0-128">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="46ad0-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="46ad0-129">OUTPUTS</span></span>

### <span data-ttu-id="46ad0-130">Microsoft.Azure.Commands.BatCH. Modeller. PSPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="46ad0-130">Microsoft.Azure.Commands.Batch.Models.PSPoolStatistics</span></span>

## <span data-ttu-id="46ad0-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="46ad0-131">NOTES</span></span>

## <span data-ttu-id="46ad0-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="46ad0-132">RELATED LINKS</span></span>

[<span data-ttu-id="46ad0-133">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="46ad0-133">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="46ad0-134">Get-AzureBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="46ad0-134">Get-AzureBatchPoolUsageMetrics</span></span>](./Get-AzureBatchPoolUsageMetrics.md)

[<span data-ttu-id="46ad0-135">Get-AzureBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="46ad0-135">Get-AzureBatchJobStatistics</span></span>](./Get-AzureBatchJobStatistics.md)


