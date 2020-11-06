---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
ms.openlocfilehash: 33ae727ea31d533652943240cd9cd25014635533
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580852"
---
# <span data-ttu-id="11a14-101">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="11a14-101">Stop-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="11a14-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="11a14-102">SYNOPSIS</span></span>
<span data-ttu-id="11a14-103">Stoppar ett batchjobb.</span><span class="sxs-lookup"><span data-stu-id="11a14-103">Stops a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11a14-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="11a14-104">SYNTAX</span></span>

```
Stop-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11a14-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="11a14-105">DESCRIPTION</span></span>
<span data-ttu-id="11a14-106">Cmdleten **Stop-AzureBatchJobSchedule** stoppar ett Azure Batch-schema.</span><span class="sxs-lookup"><span data-stu-id="11a14-106">The **Stop-AzureBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="11a14-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="11a14-107">EXAMPLES</span></span>

### <span data-ttu-id="11a14-108">Exempel 1: stoppa ett schema</span><span class="sxs-lookup"><span data-stu-id="11a14-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="11a14-109">Det här kommandot stoppar projektschemat med ID-JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="11a14-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="11a14-110">Använd Get-AzureRmBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="11a14-110">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="11a14-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="11a14-111">PARAMETERS</span></span>

### <span data-ttu-id="11a14-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="11a14-112">-BatchContext</span></span>
<span data-ttu-id="11a14-113">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="11a14-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="11a14-114">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="11a14-114">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="11a14-115">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="11a14-115">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="11a14-116">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="11a14-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="11a14-117">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="11a14-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="11a14-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11a14-118">-DefaultProfile</span></span>
<span data-ttu-id="11a14-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="11a14-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11a14-120">-ID</span><span class="sxs-lookup"><span data-stu-id="11a14-120">-Id</span></span>
<span data-ttu-id="11a14-121">Anger ID för det fin schema som denna cmdlet slutar.</span><span class="sxs-lookup"><span data-stu-id="11a14-121">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="11a14-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11a14-122">CommonParameters</span></span>
<span data-ttu-id="11a14-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11a14-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11a14-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11a14-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11a14-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="11a14-125">INPUTS</span></span>

### <span data-ttu-id="11a14-126">System. String</span><span class="sxs-lookup"><span data-stu-id="11a14-126">System.String</span></span>

### <span data-ttu-id="11a14-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="11a14-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="11a14-128">Parametrar: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="11a14-128">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="11a14-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="11a14-129">OUTPUTS</span></span>

### <span data-ttu-id="11a14-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="11a14-130">System.Void</span></span>

## <span data-ttu-id="11a14-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="11a14-131">NOTES</span></span>

## <span data-ttu-id="11a14-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="11a14-132">RELATED LINKS</span></span>

[<span data-ttu-id="11a14-133">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="11a14-133">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="11a14-134">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="11a14-134">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="11a14-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="11a14-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="11a14-136">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="11a14-136">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="11a14-137">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="11a14-137">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="11a14-138">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="11a14-138">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="11a14-139">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="11a14-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


