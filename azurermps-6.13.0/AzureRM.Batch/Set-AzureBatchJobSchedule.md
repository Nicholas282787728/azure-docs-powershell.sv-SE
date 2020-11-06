---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
ms.openlocfilehash: 5e26bd47c9c53b88442505aeb66d81a96c137b1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572927"
---
# <span data-ttu-id="cc448-101">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cc448-101">Set-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="cc448-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cc448-102">SYNOPSIS</span></span>
<span data-ttu-id="cc448-103">Anger ett jobb schema.</span><span class="sxs-lookup"><span data-stu-id="cc448-103">Sets a job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc448-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cc448-104">SYNTAX</span></span>

```
Set-AzureBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc448-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cc448-105">DESCRIPTION</span></span>
<span data-ttu-id="cc448-106">Cmdleten **set-AzureBatchJobSchedule** anger ett schema i Azure Batch-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="cc448-106">The **Set-AzureBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="cc448-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cc448-107">EXAMPLES</span></span>

## <span data-ttu-id="cc448-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cc448-108">PARAMETERS</span></span>

### <span data-ttu-id="cc448-109">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="cc448-109">-BatchContext</span></span>
<span data-ttu-id="cc448-110">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="cc448-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cc448-111">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="cc448-111">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="cc448-112">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="cc448-112">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="cc448-113">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="cc448-113">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="cc448-114">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="cc448-114">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="cc448-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc448-115">-DefaultProfile</span></span>
<span data-ttu-id="cc448-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cc448-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc448-117">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="cc448-117">-JobSchedule</span></span>
<span data-ttu-id="cc448-118">Anger ett **PSCloudJobSchedule** -objekt som representerar ett jobb schema.</span><span class="sxs-lookup"><span data-stu-id="cc448-118">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="cc448-119">För att hämta ett **PSCloudJobSchedule** -objekt, Använd cmdleten Get-AzureBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="cc448-119">To obtain a **PSCloudJobSchedule** object, use the Get-AzureBatchJobSchedule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc448-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc448-120">CommonParameters</span></span>
<span data-ttu-id="cc448-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc448-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc448-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc448-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc448-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cc448-123">INPUTS</span></span>

### <span data-ttu-id="cc448-124">Microsoft.Azure.Commands.BatCH. Modeller. PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cc448-124">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>
<span data-ttu-id="cc448-125">Parametrar: JobSchedule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cc448-125">Parameters: JobSchedule (ByValue)</span></span>

### <span data-ttu-id="cc448-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cc448-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="cc448-127">Parametrar: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cc448-127">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="cc448-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cc448-128">OUTPUTS</span></span>

### <span data-ttu-id="cc448-129">System. Void</span><span class="sxs-lookup"><span data-stu-id="cc448-129">System.Void</span></span>

## <span data-ttu-id="cc448-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cc448-130">NOTES</span></span>

## <span data-ttu-id="cc448-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cc448-131">RELATED LINKS</span></span>

[<span data-ttu-id="cc448-132">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cc448-132">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="cc448-133">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cc448-133">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="cc448-134">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cc448-134">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="cc448-135">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cc448-135">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="cc448-136">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cc448-136">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="cc448-137">Stopp-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cc448-137">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


