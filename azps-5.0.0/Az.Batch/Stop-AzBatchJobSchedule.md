---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
ms.openlocfilehash: b236f163a6c5c849fcbfcea0a19dac955e15c798
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323958"
---
# <span data-ttu-id="c623e-101">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c623e-101">Stop-AzBatchJobSchedule</span></span>

## <span data-ttu-id="c623e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c623e-102">SYNOPSIS</span></span>
<span data-ttu-id="c623e-103">Stoppar ett batchjobb.</span><span class="sxs-lookup"><span data-stu-id="c623e-103">Stops a Batch job schedule.</span></span>

## <span data-ttu-id="c623e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c623e-104">SYNTAX</span></span>

```
Stop-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c623e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c623e-105">DESCRIPTION</span></span>
<span data-ttu-id="c623e-106">Cmdleten **Stop-AzBatchJobSchedule** stoppar ett Azure Batch-schema.</span><span class="sxs-lookup"><span data-stu-id="c623e-106">The **Stop-AzBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="c623e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c623e-107">EXAMPLES</span></span>

### <span data-ttu-id="c623e-108">Exempel 1: stoppa ett schema</span><span class="sxs-lookup"><span data-stu-id="c623e-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="c623e-109">Det här kommandot stoppar projektschemat med ID-JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="c623e-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="c623e-110">Använd Get-AzBatchAccountKey cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="c623e-110">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="c623e-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c623e-111">PARAMETERS</span></span>

### <span data-ttu-id="c623e-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c623e-112">-BatchContext</span></span>
<span data-ttu-id="c623e-113">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c623e-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c623e-114">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c623e-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c623e-115">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="c623e-115">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c623e-116">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="c623e-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c623e-117">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="c623e-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c623e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c623e-118">-DefaultProfile</span></span>
<span data-ttu-id="c623e-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c623e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c623e-120">-ID</span><span class="sxs-lookup"><span data-stu-id="c623e-120">-Id</span></span>
<span data-ttu-id="c623e-121">Anger ID för det fin schema som denna cmdlet slutar.</span><span class="sxs-lookup"><span data-stu-id="c623e-121">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="c623e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c623e-122">CommonParameters</span></span>
<span data-ttu-id="c623e-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c623e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c623e-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c623e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c623e-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c623e-125">INPUTS</span></span>

### <span data-ttu-id="c623e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c623e-126">System.String</span></span>

### <span data-ttu-id="c623e-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c623e-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="c623e-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c623e-128">OUTPUTS</span></span>

### <span data-ttu-id="c623e-129">System. Void</span><span class="sxs-lookup"><span data-stu-id="c623e-129">System.Void</span></span>

## <span data-ttu-id="c623e-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c623e-130">NOTES</span></span>

## <span data-ttu-id="c623e-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c623e-131">RELATED LINKS</span></span>

[<span data-ttu-id="c623e-132">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c623e-132">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="c623e-133">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c623e-133">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="c623e-134">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="c623e-134">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="c623e-135">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c623e-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="c623e-136">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c623e-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="c623e-137">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c623e-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="c623e-138">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="c623e-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
