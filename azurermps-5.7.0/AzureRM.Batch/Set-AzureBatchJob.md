---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJob.md
ms.openlocfilehash: a878002c509fd2a895f61a97af1bef2afebc3691
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583652"
---
# <span data-ttu-id="a5af0-101">Set-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a5af0-101">Set-AzureBatchJob</span></span>

## <span data-ttu-id="a5af0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a5af0-102">SYNOPSIS</span></span>
<span data-ttu-id="a5af0-103">Uppdaterar ett batchjobb.</span><span class="sxs-lookup"><span data-stu-id="a5af0-103">Updates a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5af0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a5af0-104">SYNTAX</span></span>

```
Set-AzureBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5af0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a5af0-105">DESCRIPTION</span></span>
<span data-ttu-id="a5af0-106">Cmdleten **set-AzureBatchJob** uppdaterar ett Azure-batchjobb.</span><span class="sxs-lookup"><span data-stu-id="a5af0-106">The **Set-AzureBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="a5af0-107">Använd Get-AzureBatchJob cmdlet för att hämta ett **PSCloudJob** -objekt.</span><span class="sxs-lookup"><span data-stu-id="a5af0-107">Use the Get-AzureBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="a5af0-108">Ändra egenskaperna för objektet och Använd sedan aktuell cmdlet för att bekräfta ändringarna i kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a5af0-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="a5af0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a5af0-109">EXAMPLES</span></span>

### <span data-ttu-id="a5af0-110">Exempel 1: uppdatera ett jobb</span><span class="sxs-lookup"><span data-stu-id="a5af0-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzureBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzureBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="a5af0-111">Det första kommandot får en pool genom att använda **Get-AzureBatchJob** och lagrar den sedan i $Job variabel.</span><span class="sxs-lookup"><span data-stu-id="a5af0-111">The first command gets a pool by using **Get-AzureBatchJob** , and then stores it in the $Job variable.</span></span>

<span data-ttu-id="a5af0-112">Det andra kommandot ändrar prioritets specifikationen för $Job-objektet.</span><span class="sxs-lookup"><span data-stu-id="a5af0-112">The second command modifies the priority specification on the $Job object.</span></span>

<span data-ttu-id="a5af0-113">Det sista kommandot uppdaterar kommando tjänsten för att matcha det lokala objektet i $Job.</span><span class="sxs-lookup"><span data-stu-id="a5af0-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="a5af0-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a5af0-114">PARAMETERS</span></span>

### <span data-ttu-id="a5af0-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a5af0-115">-BatchContext</span></span>
<span data-ttu-id="a5af0-116">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a5af0-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a5af0-117">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a5af0-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a5af0-118">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="a5af0-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a5af0-119">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="a5af0-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a5af0-120">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="a5af0-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a5af0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5af0-121">-DefaultProfile</span></span>
<span data-ttu-id="a5af0-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a5af0-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5af0-123">-Jobb</span><span class="sxs-lookup"><span data-stu-id="a5af0-123">-Job</span></span>
<span data-ttu-id="a5af0-124">Anger en **PSCloudJob** dit denna cmdlet uppdaterar kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a5af0-124">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: PSCloudJob
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5af0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5af0-125">CommonParameters</span></span>
<span data-ttu-id="a5af0-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5af0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5af0-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5af0-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5af0-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a5af0-128">INPUTS</span></span>

### <span data-ttu-id="a5af0-129">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a5af0-129">BatchAccountContext</span></span>
<span data-ttu-id="a5af0-130">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="a5af0-130">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="a5af0-131">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="a5af0-131">PSCloudJob</span></span>
<span data-ttu-id="a5af0-132">Parametern ' Job ' godkänner värdet av typen ' PSCloudJob ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="a5af0-132">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="a5af0-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a5af0-133">OUTPUTS</span></span>

## <span data-ttu-id="a5af0-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a5af0-134">NOTES</span></span>

## <span data-ttu-id="a5af0-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a5af0-135">RELATED LINKS</span></span>

[<span data-ttu-id="a5af0-136">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a5af0-136">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="a5af0-137">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a5af0-137">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="a5af0-138">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a5af0-138">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="a5af0-139">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a5af0-139">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="a5af0-140">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a5af0-140">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="a5af0-141">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a5af0-141">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="a5af0-142">Stopp-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a5af0-142">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="a5af0-143">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="a5af0-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


