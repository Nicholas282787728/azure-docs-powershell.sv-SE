---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: E655684D-9601-4A0B-BB09-EFB787EB2B1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobStatistic.md
ms.openlocfilehash: 11532648242438983ae1bc9222dbc3ac12fa05e8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101721"
---
# <span data-ttu-id="44f29-101">Get-AzBatchJobStatistic</span><span class="sxs-lookup"><span data-stu-id="44f29-101">Get-AzBatchJobStatistic</span></span>

## <span data-ttu-id="44f29-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="44f29-102">SYNOPSIS</span></span>
<span data-ttu-id="44f29-103">Hämtar statistik för jobb Sammanfattning för ett batch-konto.</span><span class="sxs-lookup"><span data-stu-id="44f29-103">Gets job summary statistics for a Batch account.</span></span>

## <span data-ttu-id="44f29-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="44f29-104">SYNTAX</span></span>

```
Get-AzBatchJobStatistic -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="44f29-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="44f29-105">DESCRIPTION</span></span>
<span data-ttu-id="44f29-106">Cmdleten **Get-AzBatchJobStatistic** får livs längds statistik för alla jobb i ett Azure Batch-konto.</span><span class="sxs-lookup"><span data-stu-id="44f29-106">The **Get-AzBatchJobStatistic** cmdlet gets lifetime summary statistics for all of the jobs in an Azure Batch account.</span></span>
<span data-ttu-id="44f29-107">Statistik samlas in på alla jobb som någonsin funnits i kontot, från skapande till den senaste uppdaterings tiden för statistiken.</span><span class="sxs-lookup"><span data-stu-id="44f29-107">Statistics are aggregated across all jobs that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="44f29-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="44f29-108">EXAMPLES</span></span>

### <span data-ttu-id="44f29-109">Exempel 1: få sammanfattnings statistik för alla jobb</span><span class="sxs-lookup"><span data-stu-id="44f29-109">Example 1: Get summary statistics for all jobs</span></span>
```
PS C:\>Get-AzBatchJobStatistic -BatchContext $Context
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

<span data-ttu-id="44f29-110">Det första kommandot skapar en objekt referens till konto nycklarna för batch-kontot som heter ContosoBatchAccount genom att använda **Get-AzBatchAccountKey**.</span><span class="sxs-lookup"><span data-stu-id="44f29-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="44f29-111">Kommandot lagrar objekt referensen i $Context variabel.</span><span class="sxs-lookup"><span data-stu-id="44f29-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="44f29-112">Det andra kommandot får sammanfattnings statistiken för alla jobb.</span><span class="sxs-lookup"><span data-stu-id="44f29-112">The second command gets the summary statistics for all of the jobs.</span></span>
<span data-ttu-id="44f29-113">Kommandot använder värdet $Context från det första kommandot.</span><span class="sxs-lookup"><span data-stu-id="44f29-113">The command uses the $Context value from the first command.</span></span>

## <span data-ttu-id="44f29-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="44f29-114">PARAMETERS</span></span>

### <span data-ttu-id="44f29-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="44f29-115">-BatchContext</span></span>
<span data-ttu-id="44f29-116">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="44f29-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="44f29-117">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="44f29-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="44f29-118">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="44f29-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="44f29-119">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="44f29-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="44f29-120">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="44f29-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="44f29-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44f29-121">-DefaultProfile</span></span>
<span data-ttu-id="44f29-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="44f29-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44f29-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44f29-123">CommonParameters</span></span>
<span data-ttu-id="44f29-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44f29-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44f29-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44f29-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44f29-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="44f29-126">INPUTS</span></span>

### <span data-ttu-id="44f29-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="44f29-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="44f29-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="44f29-128">OUTPUTS</span></span>

### <span data-ttu-id="44f29-129">Microsoft.Azure.Commands.BatCH. Modeller. PSJobStatistics</span><span class="sxs-lookup"><span data-stu-id="44f29-129">Microsoft.Azure.Commands.Batch.Models.PSJobStatistics</span></span>

## <span data-ttu-id="44f29-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="44f29-130">NOTES</span></span>

## <span data-ttu-id="44f29-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="44f29-131">RELATED LINKS</span></span>

[<span data-ttu-id="44f29-132">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="44f29-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="44f29-133">Get-AzBatchPoolStatistic</span><span class="sxs-lookup"><span data-stu-id="44f29-133">Get-AzBatchPoolStatistic</span></span>](./Get-AzBatchPoolStatistic.md)

[<span data-ttu-id="44f29-134">Get-AzBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="44f29-134">Get-AzBatchPoolUsageMetrics</span></span>](./Get-AzBatchPoolUsageMetric.md)
