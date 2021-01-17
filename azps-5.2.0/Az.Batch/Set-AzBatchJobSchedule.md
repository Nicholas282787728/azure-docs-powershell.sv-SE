---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
ms.openlocfilehash: d6a17588b5718f9a6d735521a7a136cba472ead0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393616"
---
# <span data-ttu-id="bf63c-101">Set-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="bf63c-101">Set-AzBatchJobSchedule</span></span>

## <span data-ttu-id="bf63c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bf63c-102">SYNOPSIS</span></span>
<span data-ttu-id="bf63c-103">Anger ett jobb schema.</span><span class="sxs-lookup"><span data-stu-id="bf63c-103">Sets a job schedule.</span></span>

## <span data-ttu-id="bf63c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bf63c-104">SYNTAX</span></span>

```
Set-AzBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf63c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bf63c-105">DESCRIPTION</span></span>
<span data-ttu-id="bf63c-106">Cmdleten **set-AzBatchJobSchedule** anger ett schema i Azure Batch-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="bf63c-106">The **Set-AzBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="bf63c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bf63c-107">EXAMPLES</span></span>

### <span data-ttu-id="bf63c-108">Exempel 1: uppdatera ett jobb schema</span><span class="sxs-lookup"><span data-stu-id="bf63c-108">Example 1: Update a job schedule</span></span>
```
PS C:\> $JobSchedule = Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
PS C:\> $JobSchedule.Schedule.RecurrenceInterval = New-TimeSpan -Days 2
PS C:\> Set-AzBatchJobSchedule -JobSchedule $Job -BatchContext $Context
```

<span data-ttu-id="bf63c-109">Det första kommandot får jobbet genom att använda **Get-AzBatchJobSchedule** och lagrar det sedan i $JobSchedule variabel.</span><span class="sxs-lookup"><span data-stu-id="bf63c-109">The first command gets a job by using **Get-AzBatchJobSchedule**, and then stores it in the $JobSchedule variable.</span></span>
<span data-ttu-id="bf63c-110">Det andra kommandot ändrar upprepnings intervallet för `$JobSchedule.Schedule` objektet.</span><span class="sxs-lookup"><span data-stu-id="bf63c-110">The second command modifies the recurrence interval on the `$JobSchedule.Schedule` object.</span></span>
<span data-ttu-id="bf63c-111">Det sista kommandot uppdaterar kommando tjänsten för att matcha det lokala objektet i $JobSchedule.</span><span class="sxs-lookup"><span data-stu-id="bf63c-111">The final command updates the Batch service to match the local object in $JobSchedule.</span></span>

## <span data-ttu-id="bf63c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bf63c-112">PARAMETERS</span></span>

### <span data-ttu-id="bf63c-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="bf63c-113">-BatchContext</span></span>
<span data-ttu-id="bf63c-114">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="bf63c-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="bf63c-115">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="bf63c-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="bf63c-116">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="bf63c-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="bf63c-117">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="bf63c-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="bf63c-118">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="bf63c-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="bf63c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf63c-119">-DefaultProfile</span></span>
<span data-ttu-id="bf63c-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bf63c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf63c-121">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="bf63c-121">-JobSchedule</span></span>
<span data-ttu-id="bf63c-122">Anger ett **PSCloudJobSchedule** -objekt som representerar ett jobb schema.</span><span class="sxs-lookup"><span data-stu-id="bf63c-122">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="bf63c-123">För att hämta ett **PSCloudJobSchedule** -objekt, Använd cmdleten Get-AzBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="bf63c-123">To obtain a **PSCloudJobSchedule** object, use the Get-AzBatchJobSchedule cmdlet.</span></span>

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

### <span data-ttu-id="bf63c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf63c-124">CommonParameters</span></span>
<span data-ttu-id="bf63c-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf63c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf63c-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf63c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf63c-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bf63c-127">INPUTS</span></span>

### <span data-ttu-id="bf63c-128">Microsoft.Azure.Commands.BatCH. Modeller. PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="bf63c-128">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

### <span data-ttu-id="bf63c-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="bf63c-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="bf63c-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bf63c-130">OUTPUTS</span></span>

### <span data-ttu-id="bf63c-131">System. Void</span><span class="sxs-lookup"><span data-stu-id="bf63c-131">System.Void</span></span>

## <span data-ttu-id="bf63c-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bf63c-132">NOTES</span></span>

## <span data-ttu-id="bf63c-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bf63c-133">RELATED LINKS</span></span>

[<span data-ttu-id="bf63c-134">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="bf63c-134">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="bf63c-135">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="bf63c-135">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="bf63c-136">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="bf63c-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="bf63c-137">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="bf63c-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="bf63c-138">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="bf63c-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="bf63c-139">Stopp-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="bf63c-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)


