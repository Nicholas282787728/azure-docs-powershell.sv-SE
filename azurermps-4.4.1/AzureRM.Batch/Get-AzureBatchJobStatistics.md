---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: E655684D-9601-4A0B-BB09-EFB787EB2B1B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobStatistics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobStatistics.md
ms.openlocfilehash: 03b7e3999fbc482223365b59867c02c75e9d5ba1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577712"
---
# <span data-ttu-id="4a366-101">Get-AzureBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="4a366-101">Get-AzureBatchJobStatistics</span></span>

## <span data-ttu-id="4a366-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4a366-102">SYNOPSIS</span></span>
<span data-ttu-id="4a366-103">Hämtar statistik för jobb Sammanfattning för ett batch-konto.</span><span class="sxs-lookup"><span data-stu-id="4a366-103">Gets job summary statistics for a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a366-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4a366-104">SYNTAX</span></span>

```
Get-AzureBatchJobStatistics -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a366-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4a366-105">DESCRIPTION</span></span>
<span data-ttu-id="4a366-106">Cmdleten **Get-AzureBatchJobStatistics** får livs längds statistik för alla jobb i ett Azure Batch-konto.</span><span class="sxs-lookup"><span data-stu-id="4a366-106">The **Get-AzureBatchJobStatistics** cmdlet gets lifetime summary statistics for all of the jobs in an Azure Batch account.</span></span>
<span data-ttu-id="4a366-107">Statistik samlas in på alla jobb som någonsin funnits i kontot, från skapande till den senaste uppdaterings tiden för statistiken.</span><span class="sxs-lookup"><span data-stu-id="4a366-107">Statistics are aggregated across all jobs that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="4a366-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4a366-108">EXAMPLES</span></span>

### <span data-ttu-id="4a366-109">Exempel 1: få sammanfattnings statistik för alla jobb</span><span class="sxs-lookup"><span data-stu-id="4a366-109">Example 1: Get summary statistics for all jobs</span></span>
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

<span data-ttu-id="4a366-110">Det första kommandot skapar en objekt referens till konto nycklarna för batch-kontot som heter ContosoBatchAccount genom att använda **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="4a366-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="4a366-111">Kommandot lagrar objekt referensen i $Context variabel.</span><span class="sxs-lookup"><span data-stu-id="4a366-111">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="4a366-112">Det andra kommandot får sammanfattnings statistiken för alla jobb.</span><span class="sxs-lookup"><span data-stu-id="4a366-112">The second command gets the summary statistics for all of the jobs.</span></span>
<span data-ttu-id="4a366-113">Kommandot använder värdet $Context från det första kommandot.</span><span class="sxs-lookup"><span data-stu-id="4a366-113">The command uses the $Context value from the first command.</span></span>

## <span data-ttu-id="4a366-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4a366-114">PARAMETERS</span></span>

### <span data-ttu-id="4a366-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4a366-115">-BatchContext</span></span>
<span data-ttu-id="4a366-116">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="4a366-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4a366-117">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="4a366-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="4a366-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a366-118">-DefaultProfile</span></span>
<span data-ttu-id="4a366-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4a366-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a366-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a366-120">CommonParameters</span></span>
<span data-ttu-id="4a366-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a366-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a366-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a366-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a366-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4a366-123">INPUTS</span></span>

### <span data-ttu-id="4a366-124">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4a366-124">BatchAccountContext</span></span>
<span data-ttu-id="4a366-125">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="4a366-125">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="4a366-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4a366-126">OUTPUTS</span></span>

### <span data-ttu-id="4a366-127">PSJobStatistics</span><span class="sxs-lookup"><span data-stu-id="4a366-127">PSJobStatistics</span></span>

## <span data-ttu-id="4a366-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4a366-128">NOTES</span></span>

## <span data-ttu-id="4a366-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4a366-129">RELATED LINKS</span></span>

[<span data-ttu-id="4a366-130">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="4a366-130">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="4a366-131">Get-AzureBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="4a366-131">Get-AzureBatchPoolStatistics</span></span>](./Get-AzureBatchPoolStatistics.md)

[<span data-ttu-id="4a366-132">Get-AzureBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="4a366-132">Get-AzureBatchPoolUsageMetrics</span></span>](./Get-AzureBatchPoolUsageMetrics.md)


