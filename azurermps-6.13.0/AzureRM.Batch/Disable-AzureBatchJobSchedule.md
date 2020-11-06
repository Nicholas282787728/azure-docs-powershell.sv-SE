---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/disable-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
ms.openlocfilehash: e1eb586ff23f5f56cd9fc117f5039d3ccc841367
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579044"
---
# <span data-ttu-id="62b62-101">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="62b62-101">Disable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="62b62-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="62b62-102">SYNOPSIS</span></span>
<span data-ttu-id="62b62-103">Inaktiverar schemaläggning av batchjobb.</span><span class="sxs-lookup"><span data-stu-id="62b62-103">Disables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62b62-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="62b62-104">SYNTAX</span></span>

```
Disable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62b62-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="62b62-105">DESCRIPTION</span></span>
<span data-ttu-id="62b62-106">Cmdleten **disable-AzureBatchJobSchedule** inaktiverar ett Azure Batch-schema.</span><span class="sxs-lookup"><span data-stu-id="62b62-106">The **Disable-AzureBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="62b62-107">Om du inaktiverar ett schema skapas inte jobb enligt det schemat.</span><span class="sxs-lookup"><span data-stu-id="62b62-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="62b62-108">Du kan aktivera ett inaktiverat schema senare.</span><span class="sxs-lookup"><span data-stu-id="62b62-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="62b62-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="62b62-109">EXAMPLES</span></span>

### <span data-ttu-id="62b62-110">Exempel 1: inaktivera en finplanera</span><span class="sxs-lookup"><span data-stu-id="62b62-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="62b62-111">Det här kommandot inaktiverar projektschemat med ID-JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="62b62-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="62b62-112">Använd cmdleten **Get-AzureRmBatchAccountKeys** för att tilldela en kontext till variabeln $context.</span><span class="sxs-lookup"><span data-stu-id="62b62-112">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="62b62-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="62b62-113">PARAMETERS</span></span>

### <span data-ttu-id="62b62-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="62b62-114">-BatchContext</span></span>
<span data-ttu-id="62b62-115">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="62b62-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="62b62-116">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="62b62-116">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="62b62-117">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="62b62-117">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="62b62-118">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="62b62-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="62b62-119">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="62b62-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="62b62-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62b62-120">-DefaultProfile</span></span>
<span data-ttu-id="62b62-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="62b62-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62b62-122">-ID</span><span class="sxs-lookup"><span data-stu-id="62b62-122">-Id</span></span>
<span data-ttu-id="62b62-123">Anger ID för det jobb schema som denna cmdlet inaktiverar.</span><span class="sxs-lookup"><span data-stu-id="62b62-123">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62b62-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62b62-124">CommonParameters</span></span>
<span data-ttu-id="62b62-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62b62-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62b62-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62b62-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62b62-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="62b62-127">INPUTS</span></span>

### <span data-ttu-id="62b62-128">System. String</span><span class="sxs-lookup"><span data-stu-id="62b62-128">System.String</span></span>

### <span data-ttu-id="62b62-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="62b62-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="62b62-130">Parametrar: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="62b62-130">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="62b62-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="62b62-131">OUTPUTS</span></span>

### <span data-ttu-id="62b62-132">System. Void</span><span class="sxs-lookup"><span data-stu-id="62b62-132">System.Void</span></span>

## <span data-ttu-id="62b62-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="62b62-133">NOTES</span></span>

## <span data-ttu-id="62b62-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="62b62-134">RELATED LINKS</span></span>

[<span data-ttu-id="62b62-135">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="62b62-135">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="62b62-136">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="62b62-136">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="62b62-137">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="62b62-137">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="62b62-138">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="62b62-138">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="62b62-139">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="62b62-139">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="62b62-140">Stopp-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="62b62-140">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="62b62-141">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="62b62-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


