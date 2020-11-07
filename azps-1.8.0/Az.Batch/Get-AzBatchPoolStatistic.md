---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8188C617-4895-4B43-8D3B-FA6FC5B868DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpoolstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolStatistic.md
ms.openlocfilehash: d75efbd2ef369444fb655d1a011d7a1dbfab9100
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93755106"
---
# <span data-ttu-id="6e027-101">Get-AzBatchPoolStatistic</span><span class="sxs-lookup"><span data-stu-id="6e027-101">Get-AzBatchPoolStatistic</span></span>

## <span data-ttu-id="6e027-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6e027-102">SYNOPSIS</span></span>
<span data-ttu-id="6e027-103">Sammanfattar statistik för pooler för ett batch-konto.</span><span class="sxs-lookup"><span data-stu-id="6e027-103">Gets pool summary statistics for a Batch account.</span></span>

## <span data-ttu-id="6e027-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6e027-104">SYNTAX</span></span>

```
Get-AzBatchPoolStatistic -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6e027-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6e027-105">DESCRIPTION</span></span>
<span data-ttu-id="6e027-106">Cmdleten **Get-AzBatchPoolStatistic** hämtar livs längds statistiken för alla pooler i angivet konto.</span><span class="sxs-lookup"><span data-stu-id="6e027-106">The **Get-AzBatchPoolStatistic** cmdlet gets the lifetime statistics for all of the pools in the specified account.</span></span>
<span data-ttu-id="6e027-107">Statistik samlas in för alla pooler som någonsin funnits i kontot, från skapande till den senaste uppdaterings tiden för statistik.</span><span class="sxs-lookup"><span data-stu-id="6e027-107">Statistics are aggregated across all pools that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="6e027-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6e027-108">EXAMPLES</span></span>

### <span data-ttu-id="6e027-109">Exempel 1: få resurs statistik för alla pooler på ett konto</span><span class="sxs-lookup"><span data-stu-id="6e027-109">Example 1: Get resource statistics of all pools in an account</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $PoolStatistics = Get-AzBatchPoolStatistic -BatchContext $Context
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

<span data-ttu-id="6e027-110">Det första kommandot skapar en objekt referens till konto nycklarna för batch-kontot som heter ContosoBatchAccount genom att använda **Get-AzBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="6e027-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKeys**.</span></span>
<span data-ttu-id="6e027-111">Kommandot lagrar objekt referensen i $Context variabel.</span><span class="sxs-lookup"><span data-stu-id="6e027-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="6e027-112">Det andra kommandot får statistik för alla pooler på det angivna kontot och lagrar dem i $PoolStatistics.</span><span class="sxs-lookup"><span data-stu-id="6e027-112">The second command gets the statistics of all of the pools in the specified account, and then stores them in the $PoolStatistics.</span></span>
<span data-ttu-id="6e027-113">Det sista kommandot visar egenskapen **ResourceStatistics** för $PoolStatistics.</span><span class="sxs-lookup"><span data-stu-id="6e027-113">The final command displays the **ResourceStatistics** property of $PoolStatistics.</span></span>

## <span data-ttu-id="6e027-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6e027-114">PARAMETERS</span></span>

### <span data-ttu-id="6e027-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6e027-115">-BatchContext</span></span>
<span data-ttu-id="6e027-116">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="6e027-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6e027-117">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="6e027-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6e027-118">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="6e027-118">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6e027-119">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="6e027-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6e027-120">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="6e027-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6e027-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e027-121">-DefaultProfile</span></span>
<span data-ttu-id="6e027-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6e027-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e027-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e027-123">CommonParameters</span></span>
<span data-ttu-id="6e027-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e027-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e027-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e027-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e027-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6e027-126">INPUTS</span></span>

### <span data-ttu-id="6e027-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6e027-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="6e027-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6e027-128">OUTPUTS</span></span>

### <span data-ttu-id="6e027-129">Microsoft.Azure.Commands.BatCH. Modeller. PSPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="6e027-129">Microsoft.Azure.Commands.Batch.Models.PSPoolStatistics</span></span>

## <span data-ttu-id="6e027-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6e027-130">NOTES</span></span>

## <span data-ttu-id="6e027-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6e027-131">RELATED LINKS</span></span>

[<span data-ttu-id="6e027-132">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="6e027-132">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="6e027-133">Get-AzBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="6e027-133">Get-AzBatchPoolUsageMetrics</span></span>](./Get-AzBatchPoolUsageMetric.md)

[<span data-ttu-id="6e027-134">Get-AzBatchJobStatistic</span><span class="sxs-lookup"><span data-stu-id="6e027-134">Get-AzBatchJobStatistic</span></span>](./Get-AzBatchJobStatistic.md)


