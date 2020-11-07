---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: BF0C1A2F-2703-492F-A3A7-053416A5D1EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/test-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Test-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Test-AzBatchAutoScale.md
ms.openlocfilehash: dcac72f8ca362ea87d464e024d6e77b2b3b61425
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93755047"
---
# <span data-ttu-id="1cf43-101">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="1cf43-101">Test-AzBatchAutoScale</span></span>

## <span data-ttu-id="1cf43-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1cf43-102">SYNOPSIS</span></span>
<span data-ttu-id="1cf43-103">Hämtar resultatet av en automatisk skalnings formel på en pool.</span><span class="sxs-lookup"><span data-stu-id="1cf43-103">Gets the result of an automatic scaling formula on a pool.</span></span>

## <span data-ttu-id="1cf43-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1cf43-104">SYNTAX</span></span>

```
Test-AzBatchAutoScale [-Id] <String> [-AutoScaleFormula] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1cf43-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1cf43-105">DESCRIPTION</span></span>
<span data-ttu-id="1cf43-106">**Test-AzBatchAutoScale** cmdlet får resultatet av en automatisk skalnings formel på den angivna poolen.</span><span class="sxs-lookup"><span data-stu-id="1cf43-106">The **Test-AzBatchAutoScale** cmdlet gets the result of an automatic scaling formula on the specified pool.</span></span>

## <span data-ttu-id="1cf43-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1cf43-107">EXAMPLES</span></span>

### <span data-ttu-id="1cf43-108">Exempel 1: utvärdera en Autoskala-formel i en pool</span><span class="sxs-lookup"><span data-stu-id="1cf43-108">Example 1: Evaluate an autoscale formula on a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> $Evaluation = Test-AzBatchAutoScale -Id "ContosoPool" -AutoScaleFormula $Formula -BatchContext $Context
PS C:\> $Evaluation.AutoScaleRun.Results
$TargetDedicated=5;$NodeDeallocationOption=requeue;totalNodes=5
```

<span data-ttu-id="1cf43-109">I det första kommandot lagras en formel i $Formula variabel för användning i exemplet.</span><span class="sxs-lookup"><span data-stu-id="1cf43-109">The first command stores a formula in the $Formula variable for use in the example.</span></span>
<span data-ttu-id="1cf43-110">Det andra kommandot beräknar den automatiska skalnings formeln på poolen med ID-ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="1cf43-110">The second command evaluates the autoscale formula on the pool that has the ID ContosoPool.</span></span>
<span data-ttu-id="1cf43-111">Det sista kommandot visar **resultatet** med standardsyntaxen för dot.</span><span class="sxs-lookup"><span data-stu-id="1cf43-111">The final command displays the **Results** by using standard dot syntax.</span></span>

## <span data-ttu-id="1cf43-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1cf43-112">PARAMETERS</span></span>

### <span data-ttu-id="1cf43-113">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="1cf43-113">-AutoScaleFormula</span></span>
<span data-ttu-id="1cf43-114">Anger formeln för önskat antal beräknade noder i poolen.</span><span class="sxs-lookup"><span data-stu-id="1cf43-114">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cf43-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="1cf43-115">-BatchContext</span></span>
<span data-ttu-id="1cf43-116">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="1cf43-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="1cf43-117">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="1cf43-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="1cf43-118">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="1cf43-118">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="1cf43-119">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="1cf43-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="1cf43-120">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="1cf43-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="1cf43-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cf43-121">-DefaultProfile</span></span>
<span data-ttu-id="1cf43-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1cf43-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1cf43-123">-ID</span><span class="sxs-lookup"><span data-stu-id="1cf43-123">-Id</span></span>
<span data-ttu-id="1cf43-124">Anger objekt-ID: t för den pool som du vill testa automatisk skalning för.</span><span class="sxs-lookup"><span data-stu-id="1cf43-124">Specifies the object ID of the pool for which to test automatic scaling.</span></span>

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

### <span data-ttu-id="1cf43-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cf43-125">CommonParameters</span></span>
<span data-ttu-id="1cf43-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cf43-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cf43-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cf43-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cf43-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1cf43-128">INPUTS</span></span>

### <span data-ttu-id="1cf43-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1cf43-129">System.String</span></span>

### <span data-ttu-id="1cf43-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1cf43-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="1cf43-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1cf43-131">OUTPUTS</span></span>

### <span data-ttu-id="1cf43-132">Microsoft.Azure.Commands.BatCH. Modeller. PSAutoScaleRun</span><span class="sxs-lookup"><span data-stu-id="1cf43-132">Microsoft.Azure.Commands.Batch.Models.PSAutoScaleRun</span></span>

## <span data-ttu-id="1cf43-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1cf43-133">NOTES</span></span>

## <span data-ttu-id="1cf43-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1cf43-134">RELATED LINKS</span></span>

[<span data-ttu-id="1cf43-135">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="1cf43-135">Disable-AzBatchAutoScale</span></span>](./Disable-AzBatchAutoScale.md)

[<span data-ttu-id="1cf43-136">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="1cf43-136">Enable-AzBatchAutoScale</span></span>](./Enable-AzBatchAutoScale.md)

[<span data-ttu-id="1cf43-137">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="1cf43-137">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="1cf43-138">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="1cf43-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


