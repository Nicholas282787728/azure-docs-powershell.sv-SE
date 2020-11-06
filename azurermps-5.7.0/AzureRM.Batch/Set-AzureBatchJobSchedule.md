---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
ms.openlocfilehash: 85e47b9f9bea7a19bb11817c414e5d3b9a35d6a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582056"
---
# <span data-ttu-id="6970c-101">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6970c-101">Set-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="6970c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6970c-102">SYNOPSIS</span></span>
<span data-ttu-id="6970c-103">Anger ett jobb schema.</span><span class="sxs-lookup"><span data-stu-id="6970c-103">Sets a job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6970c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6970c-104">SYNTAX</span></span>

```
Set-AzureBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6970c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6970c-105">DESCRIPTION</span></span>
<span data-ttu-id="6970c-106">Cmdleten **set-AzureBatchJobSchedule** anger ett schema i Azure Batch-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="6970c-106">The **Set-AzureBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="6970c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6970c-107">EXAMPLES</span></span>

## <span data-ttu-id="6970c-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6970c-108">PARAMETERS</span></span>

### <span data-ttu-id="6970c-109">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6970c-109">-BatchContext</span></span>
<span data-ttu-id="6970c-110">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="6970c-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6970c-111">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="6970c-111">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6970c-112">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="6970c-112">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6970c-113">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="6970c-113">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6970c-114">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="6970c-114">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6970c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6970c-115">-DefaultProfile</span></span>
<span data-ttu-id="6970c-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6970c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6970c-117">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="6970c-117">-JobSchedule</span></span>
<span data-ttu-id="6970c-118">Anger ett **PSCloudJobSchedule** -objekt som representerar ett jobb schema.</span><span class="sxs-lookup"><span data-stu-id="6970c-118">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="6970c-119">För att hämta ett **PSCloudJobSchedule** -objekt, Använd cmdleten Get-AzureBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="6970c-119">To obtain a **PSCloudJobSchedule** object, use the Get-AzureBatchJobSchedule cmdlet.</span></span>

```yaml
Type: PSCloudJobSchedule
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6970c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6970c-120">CommonParameters</span></span>
<span data-ttu-id="6970c-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6970c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6970c-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6970c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6970c-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6970c-123">INPUTS</span></span>

### <span data-ttu-id="6970c-124">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6970c-124">BatchAccountContext</span></span>
<span data-ttu-id="6970c-125">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="6970c-125">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="6970c-126">PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6970c-126">PSCloudJobSchedule</span></span>
<span data-ttu-id="6970c-127">Parametern ' JobSchedule ' godkänner värdet av typen ' PSCloudJobSchedule ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="6970c-127">Parameter 'JobSchedule' accepts value of type 'PSCloudJobSchedule' from the pipeline</span></span>

## <span data-ttu-id="6970c-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6970c-128">OUTPUTS</span></span>

## <span data-ttu-id="6970c-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6970c-129">NOTES</span></span>

## <span data-ttu-id="6970c-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6970c-130">RELATED LINKS</span></span>

[<span data-ttu-id="6970c-131">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6970c-131">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="6970c-132">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6970c-132">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="6970c-133">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6970c-133">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="6970c-134">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6970c-134">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="6970c-135">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6970c-135">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="6970c-136">Stopp-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6970c-136">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


