---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/start-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
ms.openlocfilehash: 51c1103b50ef236aeedfd2250d7b67c4f0662bcf
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "94100471"
---
# <span data-ttu-id="7cf45-101">Start-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="7cf45-101">Start-AzBatchPoolResize</span></span>

## <span data-ttu-id="7cf45-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7cf45-102">SYNOPSIS</span></span>
<span data-ttu-id="7cf45-103">Ändrar storlek på en pool.</span><span class="sxs-lookup"><span data-stu-id="7cf45-103">Starts to resize a pool.</span></span>

## <span data-ttu-id="7cf45-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7cf45-104">SYNTAX</span></span>

```
Start-AzBatchPoolResize [-Id] <String> [-TargetDedicatedComputeNodes <Int32>]
 [-TargetLowPriorityComputeNodes <Int32>] [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7cf45-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7cf45-105">DESCRIPTION</span></span>
<span data-ttu-id="7cf45-106">Cmdleten **Start-AzBatchPoolResize** startar en storleks ändring i Azure-satsen på en pool.</span><span class="sxs-lookup"><span data-stu-id="7cf45-106">The **Start-AzBatchPoolResize** cmdlet starts an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="7cf45-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7cf45-107">EXAMPLES</span></span>

### <span data-ttu-id="7cf45-108">Exempel 1: ändra storlek på en pool till 12 noder</span><span class="sxs-lookup"><span data-stu-id="7cf45-108">Example 1: Resize a pool to 12 nodes</span></span>
```
PS C:\>Start-AzBatchPoolResize -Id "ContosoPool06" -TargetDedicatedComputeNodes 12 -BatchContext $Context
```

<span data-ttu-id="7cf45-109">Det här kommandot startar en storleks ändring på poolen med ID-ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="7cf45-109">This command starts a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="7cf45-110">Målet för operationen är 12 dedikerade datornoder.</span><span class="sxs-lookup"><span data-stu-id="7cf45-110">The target for the operation is 12 dedicated compute nodes.</span></span>
<span data-ttu-id="7cf45-111">Använd Get-AzBatchAccountKey cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="7cf45-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="7cf45-112">Exempel 2: ändra storlek på en pool med alternativet för avtilldelning</span><span class="sxs-lookup"><span data-stu-id="7cf45-112">Example 2: Resize a pool using a deallocation option</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzBatchPoolResize -TargetDedicatedComputeNodes 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

<span data-ttu-id="7cf45-113">Denna cmdlet ändrar storlek på en pool till fem dedikerade datornoder.</span><span class="sxs-lookup"><span data-stu-id="7cf45-113">This cmdlet resizes a pool to five dedicated compute nodes.</span></span>
<span data-ttu-id="7cf45-114">Kommandot hämtar den pool som har ID-ContosoPool06 med hjälp av Get-AzBatchPool cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cf45-114">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="7cf45-115">Kommandot skickar detta pool-objekt till den aktuella cmdleten med operatören.</span><span class="sxs-lookup"><span data-stu-id="7cf45-115">The command passes that pool object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7cf45-116">Kommandot startar en storleks ändring på poolen.</span><span class="sxs-lookup"><span data-stu-id="7cf45-116">The command starts a resize operation on the pool.</span></span>
<span data-ttu-id="7cf45-117">Målet är fem dedikerade datornoder.</span><span class="sxs-lookup"><span data-stu-id="7cf45-117">The target is five dedicated compute nodes.</span></span>
<span data-ttu-id="7cf45-118">Kommandot anger tids gräns för en timme.</span><span class="sxs-lookup"><span data-stu-id="7cf45-118">The command specifies time-out period of one hour.</span></span>
<span data-ttu-id="7cf45-119">Kommandot anger ett alternativ för avtilldelning av avslut.</span><span class="sxs-lookup"><span data-stu-id="7cf45-119">The command specifies a deallocation option of Terminate.</span></span>

## <span data-ttu-id="7cf45-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7cf45-120">PARAMETERS</span></span>

### <span data-ttu-id="7cf45-121">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="7cf45-121">-BatchContext</span></span>
<span data-ttu-id="7cf45-122">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="7cf45-122">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7cf45-123">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="7cf45-123">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="7cf45-124">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="7cf45-124">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="7cf45-125">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="7cf45-125">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="7cf45-126">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="7cf45-126">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="7cf45-127">-ComputeNodeDeallocationOption</span><span class="sxs-lookup"><span data-stu-id="7cf45-127">-ComputeNodeDeallocationOption</span></span>
<span data-ttu-id="7cf45-128">Anger ett alternativ för debeläggning för att ändra storlek på den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7cf45-128">Specifies a deallocation option for the resizing operation that this cmdlet starts.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf45-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cf45-129">-DefaultProfile</span></span>
<span data-ttu-id="7cf45-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf45-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7cf45-131">-ID</span><span class="sxs-lookup"><span data-stu-id="7cf45-131">-Id</span></span>
<span data-ttu-id="7cf45-132">Anger ID för den pool som denna cmdlet ändrar storlek på.</span><span class="sxs-lookup"><span data-stu-id="7cf45-132">Specifies the ID of the pool that this cmdlet resizes.</span></span>

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

### <span data-ttu-id="7cf45-133">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="7cf45-133">-ResizeTimeout</span></span>
<span data-ttu-id="7cf45-134">Anger en tids gräns för att ändra storlek på en operation.</span><span class="sxs-lookup"><span data-stu-id="7cf45-134">Specifies a time-out period for the resizing operation.</span></span>
<span data-ttu-id="7cf45-135">Om poolen inte når mål storleken just nu avbryts åtgärden.</span><span class="sxs-lookup"><span data-stu-id="7cf45-135">If the pool does not reach the target size by this time, the resize operation stops.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf45-136">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="7cf45-136">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="7cf45-137">Antalet dedikerade datornoder för mål.</span><span class="sxs-lookup"><span data-stu-id="7cf45-137">The number of target dedicated compute nodes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: TargetDedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf45-138">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="7cf45-138">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="7cf45-139">Antalet mål noder med låg prioritets beräkning.</span><span class="sxs-lookup"><span data-stu-id="7cf45-139">The number of target low-priority compute nodes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf45-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cf45-140">CommonParameters</span></span>
<span data-ttu-id="7cf45-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cf45-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cf45-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7cf45-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cf45-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7cf45-143">INPUTS</span></span>

### <span data-ttu-id="7cf45-144">System. String</span><span class="sxs-lookup"><span data-stu-id="7cf45-144">System.String</span></span>

### <span data-ttu-id="7cf45-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7cf45-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="7cf45-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7cf45-146">OUTPUTS</span></span>

### <span data-ttu-id="7cf45-147">System. Void</span><span class="sxs-lookup"><span data-stu-id="7cf45-147">System.Void</span></span>

## <span data-ttu-id="7cf45-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7cf45-148">NOTES</span></span>

## <span data-ttu-id="7cf45-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7cf45-149">RELATED LINKS</span></span>

[<span data-ttu-id="7cf45-150">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="7cf45-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="7cf45-151">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="7cf45-151">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="7cf45-152">Stopp-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="7cf45-152">Stop-AzBatchPoolResize</span></span>](./Stop-AzBatchPoolResize.md)

[<span data-ttu-id="7cf45-153">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="7cf45-153">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


