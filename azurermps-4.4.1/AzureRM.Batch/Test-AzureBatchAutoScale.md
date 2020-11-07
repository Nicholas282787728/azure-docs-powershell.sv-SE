---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: BF0C1A2F-2703-492F-A3A7-053416A5D1EB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Test-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Test-AzureBatchAutoScale.md
ms.openlocfilehash: 2ab8ca197c1d78980e1683f9572f6d3f6d4d55fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755304"
---
# <span data-ttu-id="996dc-101">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="996dc-101">Test-AzureBatchAutoScale</span></span>

## <span data-ttu-id="996dc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="996dc-102">SYNOPSIS</span></span>
<span data-ttu-id="996dc-103">Hämtar resultatet av en automatisk skalnings formel på en pool.</span><span class="sxs-lookup"><span data-stu-id="996dc-103">Gets the result of an automatic scaling formula on a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="996dc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="996dc-104">SYNTAX</span></span>

```
Test-AzureBatchAutoScale [-Id] <String> [-AutoScaleFormula] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="996dc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="996dc-105">DESCRIPTION</span></span>
<span data-ttu-id="996dc-106">**Test-AzureBatchAutoScale** cmdlet får resultatet av en automatisk skalnings formel på den angivna poolen.</span><span class="sxs-lookup"><span data-stu-id="996dc-106">The **Test-AzureBatchAutoScale** cmdlet gets the result of an automatic scaling formula on the specified pool.</span></span>

## <span data-ttu-id="996dc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="996dc-107">EXAMPLES</span></span>

### <span data-ttu-id="996dc-108">Exempel 1: utvärdera en Autoskala-formel i en pool</span><span class="sxs-lookup"><span data-stu-id="996dc-108">Example 1: Evaluate an autoscale formula on a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> $Evaluation = Test-AzureBatchAutoScale -Id "ContosoPool" -AutoScaleFormula $Formula -BatchContext $Context
PS C:\> $Evaluation.AutoScaleRun.Results
$TargetDedicated=5;$NodeDeallocationOption=requeue;totalNodes=5
```

<span data-ttu-id="996dc-109">I det första kommandot lagras en formel i $Formula variabel för användning i exemplet.</span><span class="sxs-lookup"><span data-stu-id="996dc-109">The first command stores a formula in the $Formula variable for use in the example.</span></span>

<span data-ttu-id="996dc-110">Det andra kommandot beräknar den automatiska skalnings formeln på poolen med ID-ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="996dc-110">The second command evaluates the autoscale formula on the pool that has the ID ContosoPool.</span></span>

<span data-ttu-id="996dc-111">Det sista kommandot visar **resultatet** med standardsyntaxen för dot.</span><span class="sxs-lookup"><span data-stu-id="996dc-111">The final command displays the **Results** by using standard dot syntax.</span></span>

## <span data-ttu-id="996dc-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="996dc-112">PARAMETERS</span></span>

### <span data-ttu-id="996dc-113">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="996dc-113">-AutoScaleFormula</span></span>
<span data-ttu-id="996dc-114">Anger formeln för önskat antal beräknade noder i poolen.</span><span class="sxs-lookup"><span data-stu-id="996dc-114">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

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

### <span data-ttu-id="996dc-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="996dc-115">-BatchContext</span></span>
<span data-ttu-id="996dc-116">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="996dc-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="996dc-117">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="996dc-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="996dc-118">-ID</span><span class="sxs-lookup"><span data-stu-id="996dc-118">-Id</span></span>
<span data-ttu-id="996dc-119">Anger objekt-ID: t för den pool som du vill testa automatisk skalning för.</span><span class="sxs-lookup"><span data-stu-id="996dc-119">Specifies the object ID of the pool for which to test automatic scaling.</span></span>

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

### <span data-ttu-id="996dc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="996dc-120">-DefaultProfile</span></span>
<span data-ttu-id="996dc-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="996dc-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="996dc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="996dc-122">CommonParameters</span></span>
<span data-ttu-id="996dc-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="996dc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="996dc-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="996dc-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="996dc-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="996dc-125">INPUTS</span></span>

### <span data-ttu-id="996dc-126">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="996dc-126">BatchAccountContext</span></span>
<span data-ttu-id="996dc-127">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="996dc-127">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="996dc-128">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="996dc-128">String</span></span>
<span data-ttu-id="996dc-129">Parametern ' ID ' godkänner värdet för typen ' String ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="996dc-129">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="996dc-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="996dc-130">OUTPUTS</span></span>

### <span data-ttu-id="996dc-131">PSAutoScaleEvaluation</span><span class="sxs-lookup"><span data-stu-id="996dc-131">PSAutoScaleEvaluation</span></span>

## <span data-ttu-id="996dc-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="996dc-132">NOTES</span></span>

## <span data-ttu-id="996dc-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="996dc-133">RELATED LINKS</span></span>

[<span data-ttu-id="996dc-134">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="996dc-134">Disable-AzureBatchAutoScale</span></span>](./Disable-AzureBatchAutoScale.md)

[<span data-ttu-id="996dc-135">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="996dc-135">Enable-AzureBatchAutoScale</span></span>](./Enable-AzureBatchAutoScale.md)

[<span data-ttu-id="996dc-136">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="996dc-136">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="996dc-137">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="996dc-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


