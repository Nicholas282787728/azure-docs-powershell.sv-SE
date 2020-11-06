---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
ms.openlocfilehash: be73b757bf20a2f688d7f7293ac4022e7bc8f4aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579027"
---
# <span data-ttu-id="e9e1a-101">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="e9e1a-101">Enable-AzureBatchJob</span></span>

## <span data-ttu-id="e9e1a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e9e1a-102">SYNOPSIS</span></span>
<span data-ttu-id="e9e1a-103">Aktiverar ett batchjobb.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-103">Enables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9e1a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e9e1a-104">SYNTAX</span></span>

```
Enable-AzureBatchJob [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9e1a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e9e1a-105">DESCRIPTION</span></span>
<span data-ttu-id="e9e1a-106">Cmdleten **Enable-AzureBatchJob** aktiverar ett Azure-batchjobb.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-106">The **Enable-AzureBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="e9e1a-107">När du har aktiverat ett jobb kan nya aktiviteter köras.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="e9e1a-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e9e1a-108">EXAMPLES</span></span>

### <span data-ttu-id="e9e1a-109">Exempel 1: aktivera ett batchjobb</span><span class="sxs-lookup"><span data-stu-id="e9e1a-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzureBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="e9e1a-110">Det här kommandot aktiverar jobbet med ID-000001.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="e9e1a-111">Använd Get-AzureRmBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-111">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="e9e1a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e9e1a-112">PARAMETERS</span></span>

### <span data-ttu-id="e9e1a-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e9e1a-113">-BatchContext</span></span>
<span data-ttu-id="e9e1a-114">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e9e1a-115">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-115">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e9e1a-116">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-116">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e9e1a-117">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e9e1a-118">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e9e1a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9e1a-119">-DefaultProfile</span></span>
<span data-ttu-id="e9e1a-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9e1a-121">-ID</span><span class="sxs-lookup"><span data-stu-id="e9e1a-121">-Id</span></span>
<span data-ttu-id="e9e1a-122">Anger ID för det jobb som denna cmdlet aktiverar.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-122">Specifies the ID of the job that this cmdlet enables.</span></span>

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

### <span data-ttu-id="e9e1a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9e1a-123">CommonParameters</span></span>
<span data-ttu-id="e9e1a-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9e1a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9e1a-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9e1a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9e1a-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e9e1a-126">INPUTS</span></span>

### <span data-ttu-id="e9e1a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="e9e1a-127">System.String</span></span>

### <span data-ttu-id="e9e1a-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e9e1a-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="e9e1a-129">Parametrar: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e9e1a-129">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="e9e1a-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e9e1a-130">OUTPUTS</span></span>

### <span data-ttu-id="e9e1a-131">System. Void</span><span class="sxs-lookup"><span data-stu-id="e9e1a-131">System.Void</span></span>

## <span data-ttu-id="e9e1a-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e9e1a-132">NOTES</span></span>

## <span data-ttu-id="e9e1a-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e9e1a-133">RELATED LINKS</span></span>

[<span data-ttu-id="e9e1a-134">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="e9e1a-134">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="e9e1a-135">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="e9e1a-135">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="e9e1a-136">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="e9e1a-136">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="e9e1a-137">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="e9e1a-137">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="e9e1a-138">Stopp-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="e9e1a-138">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="e9e1a-139">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="e9e1a-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


