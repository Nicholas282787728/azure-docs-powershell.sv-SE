---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
ms.openlocfilehash: e15dbe0f17f66f6bb8aaad0c4cfb1883ecfb2034
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "94100476"
---
# <span data-ttu-id="1e493-101">Set-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="1e493-101">Set-AzBatchJob</span></span>

## <span data-ttu-id="1e493-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1e493-102">SYNOPSIS</span></span>
<span data-ttu-id="1e493-103">Uppdaterar ett batchjobb.</span><span class="sxs-lookup"><span data-stu-id="1e493-103">Updates a Batch job.</span></span>

## <span data-ttu-id="1e493-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1e493-104">SYNTAX</span></span>

```
Set-AzBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e493-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1e493-105">DESCRIPTION</span></span>
<span data-ttu-id="1e493-106">Cmdleten **set-AzBatchJob** uppdaterar ett Azure-batchjobb.</span><span class="sxs-lookup"><span data-stu-id="1e493-106">The **Set-AzBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="1e493-107">Använd Get-AzBatchJob cmdlet för att hämta ett **PSCloudJob** -objekt.</span><span class="sxs-lookup"><span data-stu-id="1e493-107">Use the Get-AzBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="1e493-108">Ändra egenskaperna för objektet och Använd sedan aktuell cmdlet för att bekräfta ändringarna i kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="1e493-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="1e493-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1e493-109">EXAMPLES</span></span>

### <span data-ttu-id="1e493-110">Exempel 1: uppdatera ett jobb</span><span class="sxs-lookup"><span data-stu-id="1e493-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="1e493-111">Det första kommandot får jobbet genom att använda **Get-AzBatchJob** och lagrar det sedan i $Job variabel.</span><span class="sxs-lookup"><span data-stu-id="1e493-111">The first command gets a job by using **Get-AzBatchJob** , and then stores it in the $Job variable.</span></span>
<span data-ttu-id="1e493-112">Det andra kommandot ändrar prioritets specifikationen för $Job-objektet.</span><span class="sxs-lookup"><span data-stu-id="1e493-112">The second command modifies the priority specification on the $Job object.</span></span>
<span data-ttu-id="1e493-113">Det sista kommandot uppdaterar kommando tjänsten för att matcha det lokala objektet i $Job.</span><span class="sxs-lookup"><span data-stu-id="1e493-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="1e493-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1e493-114">PARAMETERS</span></span>

### <span data-ttu-id="1e493-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="1e493-115">-BatchContext</span></span>
<span data-ttu-id="1e493-116">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="1e493-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="1e493-117">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="1e493-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="1e493-118">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="1e493-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="1e493-119">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="1e493-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="1e493-120">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="1e493-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="1e493-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e493-121">-DefaultProfile</span></span>
<span data-ttu-id="1e493-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1e493-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e493-123">-Jobb</span><span class="sxs-lookup"><span data-stu-id="1e493-123">-Job</span></span>
<span data-ttu-id="1e493-124">Anger en **PSCloudJob** dit denna cmdlet uppdaterar kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="1e493-124">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="1e493-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e493-125">CommonParameters</span></span>
<span data-ttu-id="1e493-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e493-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e493-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e493-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e493-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1e493-128">INPUTS</span></span>

### <span data-ttu-id="1e493-129">Microsoft.Azure.Commands.BatCH. Modeller. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="1e493-129">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="1e493-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1e493-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="1e493-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1e493-131">OUTPUTS</span></span>

### <span data-ttu-id="1e493-132">System. Void</span><span class="sxs-lookup"><span data-stu-id="1e493-132">System.Void</span></span>

## <span data-ttu-id="1e493-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1e493-133">NOTES</span></span>

## <span data-ttu-id="1e493-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1e493-134">RELATED LINKS</span></span>

[<span data-ttu-id="1e493-135">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="1e493-135">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="1e493-136">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="1e493-136">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="1e493-137">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="1e493-137">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="1e493-138">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="1e493-138">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="1e493-139">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="1e493-139">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="1e493-140">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="1e493-140">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="1e493-141">Stopp-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="1e493-141">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="1e493-142">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="1e493-142">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)

