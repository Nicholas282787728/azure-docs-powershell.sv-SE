---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
ms.openlocfilehash: eb15991e0bf7aefd60b53dbb02785a1b2004cb22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585820"
---
# <span data-ttu-id="7213f-101">Set-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="7213f-101">Set-AzureBatchJob</span></span>

## <span data-ttu-id="7213f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7213f-102">SYNOPSIS</span></span>
<span data-ttu-id="7213f-103">Uppdaterar ett batchjobb.</span><span class="sxs-lookup"><span data-stu-id="7213f-103">Updates a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7213f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7213f-104">SYNTAX</span></span>

```
Set-AzureBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7213f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7213f-105">DESCRIPTION</span></span>
<span data-ttu-id="7213f-106">Cmdleten **set-AzureBatchJob** uppdaterar ett Azure-batchjobb.</span><span class="sxs-lookup"><span data-stu-id="7213f-106">The **Set-AzureBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="7213f-107">Använd Get-AzureBatchJob cmdlet för att hämta ett **PSCloudJob** -objekt.</span><span class="sxs-lookup"><span data-stu-id="7213f-107">Use the Get-AzureBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="7213f-108">Ändra egenskaperna för objektet och Använd sedan aktuell cmdlet för att bekräfta ändringarna i kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="7213f-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="7213f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7213f-109">EXAMPLES</span></span>

### <span data-ttu-id="7213f-110">Exempel 1: uppdatera ett jobb</span><span class="sxs-lookup"><span data-stu-id="7213f-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzureBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzureBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="7213f-111">Det första kommandot får en pool genom att använda **Get-AzureBatchJob** och lagrar den sedan i $Job variabel.</span><span class="sxs-lookup"><span data-stu-id="7213f-111">The first command gets a pool by using **Get-AzureBatchJob** , and then stores it in the $Job variable.</span></span>

<span data-ttu-id="7213f-112">Det andra kommandot ändrar prioritets specifikationen för $Job-objektet.</span><span class="sxs-lookup"><span data-stu-id="7213f-112">The second command modifies the priority specification on the $Job object.</span></span>

<span data-ttu-id="7213f-113">Det sista kommandot uppdaterar kommando tjänsten för att matcha det lokala objektet i $Job.</span><span class="sxs-lookup"><span data-stu-id="7213f-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="7213f-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7213f-114">PARAMETERS</span></span>

### <span data-ttu-id="7213f-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="7213f-115">-BatchContext</span></span>
<span data-ttu-id="7213f-116">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="7213f-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7213f-117">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="7213f-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="7213f-118">-Jobb</span><span class="sxs-lookup"><span data-stu-id="7213f-118">-Job</span></span>
<span data-ttu-id="7213f-119">Anger en **PSCloudJob** dit denna cmdlet uppdaterar kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="7213f-119">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7213f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7213f-120">-DefaultProfile</span></span>
<span data-ttu-id="7213f-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7213f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7213f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7213f-122">CommonParameters</span></span>
<span data-ttu-id="7213f-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7213f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7213f-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7213f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7213f-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7213f-125">INPUTS</span></span>

### <span data-ttu-id="7213f-126">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7213f-126">BatchAccountContext</span></span>
<span data-ttu-id="7213f-127">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="7213f-127">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="7213f-128">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="7213f-128">PSCloudJob</span></span>
<span data-ttu-id="7213f-129">Parametern ' Job ' godkänner värdet av typen ' PSCloudJob ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="7213f-129">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="7213f-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7213f-130">OUTPUTS</span></span>

## <span data-ttu-id="7213f-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7213f-131">NOTES</span></span>

## <span data-ttu-id="7213f-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7213f-132">RELATED LINKS</span></span>

[<span data-ttu-id="7213f-133">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="7213f-133">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="7213f-134">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="7213f-134">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="7213f-135">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="7213f-135">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="7213f-136">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="7213f-136">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="7213f-137">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="7213f-137">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="7213f-138">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="7213f-138">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="7213f-139">Stopp-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="7213f-139">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="7213f-140">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="7213f-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


