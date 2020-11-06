---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchPoolResize.md
ms.openlocfilehash: 558f8c062e60f6e9f7c18c05be8f1ccb2eafa9fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579780"
---
# <span data-ttu-id="5245b-101">Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="5245b-101">Start-AzureBatchPoolResize</span></span>

## <span data-ttu-id="5245b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5245b-102">SYNOPSIS</span></span>
<span data-ttu-id="5245b-103">Ändrar storlek på en pool.</span><span class="sxs-lookup"><span data-stu-id="5245b-103">Starts to resize a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5245b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5245b-104">SYNTAX</span></span>

```
Start-AzureBatchPoolResize [-Id] <String> -TargetDedicated <Int32> [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5245b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5245b-105">DESCRIPTION</span></span>
<span data-ttu-id="5245b-106">Cmdleten **Start-AzureBatchPoolResize** startar en storleks ändring i Azure-satsen på en pool.</span><span class="sxs-lookup"><span data-stu-id="5245b-106">The **Start-AzureBatchPoolResize** cmdlet starts an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="5245b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5245b-107">EXAMPLES</span></span>

### <span data-ttu-id="5245b-108">Exempel 1: ändra storlek på en pool till 12 noder</span><span class="sxs-lookup"><span data-stu-id="5245b-108">Example 1: Resize a pool to 12 nodes</span></span>
```
PS C:\>Start-AzureBatchPoolResize -Id "ContosoPool06" -TargetDedicated 12 -BatchContext $Context
```

<span data-ttu-id="5245b-109">Det här kommandot startar en storleks ändring på poolen med ID-ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="5245b-109">This command starts a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="5245b-110">Målet för operationen är 12 dedikerade datornoder.</span><span class="sxs-lookup"><span data-stu-id="5245b-110">The target for the operation is 12 dedicated compute nodes.</span></span>
<span data-ttu-id="5245b-111">Använd Get-AzureRmBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="5245b-111">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="5245b-112">Exempel 2: ändra storlek på en pool med alternativet för avtilldelning</span><span class="sxs-lookup"><span data-stu-id="5245b-112">Example 2: Resize a pool using a deallocation option</span></span>
```
PS C:\>Get-AzureBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzureBatchPoolResize -TargetDedicated 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

<span data-ttu-id="5245b-113">Denna cmdlet ändrar storlek på en pool till fem dedikerade datornoder.</span><span class="sxs-lookup"><span data-stu-id="5245b-113">This cmdlet resizes a pool to five dedicated compute nodes.</span></span>
<span data-ttu-id="5245b-114">Kommandot hämtar den pool som har ID-ContosoPool06 med hjälp av Get-AzureBatchPool cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5245b-114">The command gets the pool that has the ID ContosoPool06 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="5245b-115">Kommandot skickar detta pool-objekt till den aktuella cmdleten med operatören.</span><span class="sxs-lookup"><span data-stu-id="5245b-115">The command passes that pool object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5245b-116">Kommandot startar en storleks ändring på poolen.</span><span class="sxs-lookup"><span data-stu-id="5245b-116">The command starts a resize operation on the pool.</span></span>
<span data-ttu-id="5245b-117">Målet är fem dedikerade datornoder.</span><span class="sxs-lookup"><span data-stu-id="5245b-117">The target is five dedicated compute nodes.</span></span>
<span data-ttu-id="5245b-118">Kommandot anger tids gräns för en timme.</span><span class="sxs-lookup"><span data-stu-id="5245b-118">The command specifies time-out period of one hour.</span></span>
<span data-ttu-id="5245b-119">Kommandot anger ett alternativ för avtilldelning av avslut.</span><span class="sxs-lookup"><span data-stu-id="5245b-119">The command specifies a deallocation option of Terminate.</span></span>

## <span data-ttu-id="5245b-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5245b-120">PARAMETERS</span></span>

### <span data-ttu-id="5245b-121">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="5245b-121">-BatchContext</span></span>
<span data-ttu-id="5245b-122">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="5245b-122">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5245b-123">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="5245b-123">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="5245b-124">-ComputeNodeDeallocationOption</span><span class="sxs-lookup"><span data-stu-id="5245b-124">-ComputeNodeDeallocationOption</span></span>
<span data-ttu-id="5245b-125">Anger ett alternativ för debeläggning för att ändra storlek på den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5245b-125">Specifies a deallocation option for the resizing operation that this cmdlet starts.</span></span>

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

### <span data-ttu-id="5245b-126">-ID</span><span class="sxs-lookup"><span data-stu-id="5245b-126">-Id</span></span>
<span data-ttu-id="5245b-127">Anger ID för den pool som denna cmdlet ändrar storlek på.</span><span class="sxs-lookup"><span data-stu-id="5245b-127">Specifies the ID of the pool that this cmdlet resizes.</span></span>

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

### <span data-ttu-id="5245b-128">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="5245b-128">-ResizeTimeout</span></span>
<span data-ttu-id="5245b-129">Anger en tids gräns för att ändra storlek på en operation.</span><span class="sxs-lookup"><span data-stu-id="5245b-129">Specifies a time-out period for the resizing operation.</span></span>
<span data-ttu-id="5245b-130">Om poolen inte når mål storleken just nu avbryts åtgärden.</span><span class="sxs-lookup"><span data-stu-id="5245b-130">If the pool does not reach the target size by this time, the resize operation stops.</span></span>

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

### <span data-ttu-id="5245b-131">-TargetDedicated</span><span class="sxs-lookup"><span data-stu-id="5245b-131">-TargetDedicated</span></span>
<span data-ttu-id="5245b-132">Anger mål numret för dedikerade datornoder.</span><span class="sxs-lookup"><span data-stu-id="5245b-132">Specifies the target number of dedicated compute nodes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5245b-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5245b-133">-DefaultProfile</span></span>
<span data-ttu-id="5245b-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5245b-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5245b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5245b-135">CommonParameters</span></span>
<span data-ttu-id="5245b-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5245b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5245b-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5245b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5245b-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5245b-138">INPUTS</span></span>

### <span data-ttu-id="5245b-139">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5245b-139">BatchAccountContext</span></span>
<span data-ttu-id="5245b-140">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="5245b-140">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="5245b-141">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="5245b-141">String</span></span>
<span data-ttu-id="5245b-142">Parametern ' ID ' godkänner värdet för typen ' String ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="5245b-142">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="5245b-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5245b-143">OUTPUTS</span></span>

## <span data-ttu-id="5245b-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5245b-144">NOTES</span></span>

## <span data-ttu-id="5245b-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5245b-145">RELATED LINKS</span></span>

[<span data-ttu-id="5245b-146">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="5245b-146">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="5245b-147">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="5245b-147">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="5245b-148">Stopp-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="5245b-148">Stop-AzureBatchPoolResize</span></span>](./Stop-AzureBatchPoolResize.md)

[<span data-ttu-id="5245b-149">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="5245b-149">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


