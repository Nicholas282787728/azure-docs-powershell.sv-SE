---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJobSchedule.md
ms.openlocfilehash: 03decd5b1d32defb25692220c63ffe768445697e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417483"
---
# <span data-ttu-id="fc571-101">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="fc571-101">Enable-AzBatchJobSchedule</span></span>

## <span data-ttu-id="fc571-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fc571-102">SYNOPSIS</span></span>
<span data-ttu-id="fc571-103">Aktiverar ett batchjobb.</span><span class="sxs-lookup"><span data-stu-id="fc571-103">Enables a Batch job schedule.</span></span>

## <span data-ttu-id="fc571-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fc571-104">SYNTAX</span></span>

```
Enable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc571-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fc571-105">DESCRIPTION</span></span>
<span data-ttu-id="fc571-106">Cmdleten **Enable-AzBatchJobSchedule** aktiverar ett Azure batch-jobb.</span><span class="sxs-lookup"><span data-stu-id="fc571-106">The **Enable-AzBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="fc571-107">När du har aktiverat en jobb schema kan jobb skapas enligt det schemat.</span><span class="sxs-lookup"><span data-stu-id="fc571-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="fc571-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fc571-108">EXAMPLES</span></span>

### <span data-ttu-id="fc571-109">Exempel 1: aktivera ett jobb schema</span><span class="sxs-lookup"><span data-stu-id="fc571-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="fc571-110">Det här kommandot aktiverar det jobb schema som har ID-JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="fc571-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="fc571-111">Använd cmdleten **Get-AzBatchAccountKey** för att tilldela en kontext till variabeln $context.</span><span class="sxs-lookup"><span data-stu-id="fc571-111">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="fc571-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fc571-112">PARAMETERS</span></span>

### <span data-ttu-id="fc571-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="fc571-113">-BatchContext</span></span>
<span data-ttu-id="fc571-114">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="fc571-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="fc571-115">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="fc571-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="fc571-116">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="fc571-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="fc571-117">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="fc571-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="fc571-118">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="fc571-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="fc571-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc571-119">-DefaultProfile</span></span>
<span data-ttu-id="fc571-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fc571-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc571-121">-ID</span><span class="sxs-lookup"><span data-stu-id="fc571-121">-Id</span></span>
<span data-ttu-id="fc571-122">Anger ID för det projekt schema som denna cmdlet aktiverar.</span><span class="sxs-lookup"><span data-stu-id="fc571-122">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

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

### <span data-ttu-id="fc571-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc571-123">CommonParameters</span></span>
<span data-ttu-id="fc571-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc571-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc571-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc571-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc571-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fc571-126">INPUTS</span></span>

### <span data-ttu-id="fc571-127">System. String</span><span class="sxs-lookup"><span data-stu-id="fc571-127">System.String</span></span>

### <span data-ttu-id="fc571-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="fc571-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="fc571-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fc571-129">OUTPUTS</span></span>

### <span data-ttu-id="fc571-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="fc571-130">System.Void</span></span>

## <span data-ttu-id="fc571-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fc571-131">NOTES</span></span>

## <span data-ttu-id="fc571-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fc571-132">RELATED LINKS</span></span>

[<span data-ttu-id="fc571-133">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="fc571-133">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="fc571-134">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="fc571-134">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="fc571-135">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="fc571-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="fc571-136">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="fc571-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="fc571-137">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="fc571-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="fc571-138">Stopp-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="fc571-138">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="fc571-139">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="fc571-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
