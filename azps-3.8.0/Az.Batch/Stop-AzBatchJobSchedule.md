---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
ms.openlocfilehash: 9536de21d205a051f0a0a2ea6f4a83c759b94c8c
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "94100463"
---
# <span data-ttu-id="13c86-101">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="13c86-101">Stop-AzBatchJobSchedule</span></span>

## <span data-ttu-id="13c86-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="13c86-102">SYNOPSIS</span></span>
<span data-ttu-id="13c86-103">Stoppar ett batchjobb.</span><span class="sxs-lookup"><span data-stu-id="13c86-103">Stops a Batch job schedule.</span></span>

## <span data-ttu-id="13c86-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="13c86-104">SYNTAX</span></span>

```
Stop-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13c86-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="13c86-105">DESCRIPTION</span></span>
<span data-ttu-id="13c86-106">Cmdleten **Stop-AzBatchJobSchedule** stoppar ett Azure Batch-schema.</span><span class="sxs-lookup"><span data-stu-id="13c86-106">The **Stop-AzBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="13c86-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="13c86-107">EXAMPLES</span></span>

### <span data-ttu-id="13c86-108">Exempel 1: stoppa ett schema</span><span class="sxs-lookup"><span data-stu-id="13c86-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="13c86-109">Det här kommandot stoppar projektschemat med ID-JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="13c86-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="13c86-110">Använd Get-AzBatchAccountKey cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="13c86-110">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="13c86-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="13c86-111">PARAMETERS</span></span>

### <span data-ttu-id="13c86-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="13c86-112">-BatchContext</span></span>
<span data-ttu-id="13c86-113">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="13c86-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="13c86-114">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="13c86-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="13c86-115">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="13c86-115">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="13c86-116">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="13c86-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="13c86-117">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="13c86-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="13c86-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13c86-118">-DefaultProfile</span></span>
<span data-ttu-id="13c86-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="13c86-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13c86-120">-ID</span><span class="sxs-lookup"><span data-stu-id="13c86-120">-Id</span></span>
<span data-ttu-id="13c86-121">Anger ID för det fin schema som denna cmdlet slutar.</span><span class="sxs-lookup"><span data-stu-id="13c86-121">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="13c86-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13c86-122">CommonParameters</span></span>
<span data-ttu-id="13c86-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13c86-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13c86-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13c86-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13c86-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="13c86-125">INPUTS</span></span>

### <span data-ttu-id="13c86-126">System. String</span><span class="sxs-lookup"><span data-stu-id="13c86-126">System.String</span></span>

### <span data-ttu-id="13c86-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="13c86-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="13c86-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="13c86-128">OUTPUTS</span></span>

### <span data-ttu-id="13c86-129">System. Void</span><span class="sxs-lookup"><span data-stu-id="13c86-129">System.Void</span></span>

## <span data-ttu-id="13c86-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="13c86-130">NOTES</span></span>

## <span data-ttu-id="13c86-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="13c86-131">RELATED LINKS</span></span>

[<span data-ttu-id="13c86-132">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="13c86-132">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="13c86-133">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="13c86-133">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="13c86-134">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="13c86-134">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="13c86-135">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="13c86-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="13c86-136">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="13c86-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="13c86-137">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="13c86-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="13c86-138">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="13c86-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


