---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3107D061-7F25-45D0-8029-C99120A156DA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchAutoScale.md
ms.openlocfilehash: 1a85ac52622bb752b2e3437eb096f229c4d8e762
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585844"
---
# <span data-ttu-id="677b2-101">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="677b2-101">Enable-AzureBatchAutoScale</span></span>

## <span data-ttu-id="677b2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="677b2-102">SYNOPSIS</span></span>
<span data-ttu-id="677b2-103">Aktiverar automatisk skalning av en pool.</span><span class="sxs-lookup"><span data-stu-id="677b2-103">Enables automatic scaling of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="677b2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="677b2-104">SYNTAX</span></span>

```
Enable-AzureBatchAutoScale [-Id] <String> [[-AutoScaleFormula] <String>]
 [[-AutoScaleEvaluationInterval] <TimeSpan>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="677b2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="677b2-105">DESCRIPTION</span></span>
<span data-ttu-id="677b2-106">Cmdleten **Enable-AzureBatchAutoScale** aktiverar automatisk skalning av den angivna poolen.</span><span class="sxs-lookup"><span data-stu-id="677b2-106">The **Enable-AzureBatchAutoScale** cmdlet enables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="677b2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="677b2-107">EXAMPLES</span></span>

### <span data-ttu-id="677b2-108">Exempel 1: Aktivera automatisk skalning för en pool</span><span class="sxs-lookup"><span data-stu-id="677b2-108">Example 1: Enable automatic scaling for a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> Enable-AzureBatchAutoScale -Id "MyPool" -AutoScaleFormula $Formula -BatchContext $Context
```

<span data-ttu-id="677b2-109">Det första kommandot definierar en formel och sparar den sedan i $Formula variabel.</span><span class="sxs-lookup"><span data-stu-id="677b2-109">The first command defines a formula, and then saves it to the $Formula variable.</span></span>

<span data-ttu-id="677b2-110">Det andra kommandot aktiverar automatisk skalning på poolen med namnet min pool med formeln i $Formula.</span><span class="sxs-lookup"><span data-stu-id="677b2-110">The second command enables automatic scaling on the pool named MyPool using the formula in $Formula.</span></span>

## <span data-ttu-id="677b2-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="677b2-111">PARAMETERS</span></span>

### <span data-ttu-id="677b2-112">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="677b2-112">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="677b2-113">Anger hur länge (i minuter) som ska gå innan Poolens storlek justeras automatiskt enligt formeln för automatisk skalning.</span><span class="sxs-lookup"><span data-stu-id="677b2-113">Specifies the amount of time (in minutes) that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="677b2-114">Standardvärdet är 15 minuter och minimivärdet är 5 minuter.</span><span class="sxs-lookup"><span data-stu-id="677b2-114">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="677b2-115">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="677b2-115">-AutoScaleFormula</span></span>
<span data-ttu-id="677b2-116">Anger formeln för önskat antal beräknade noder i poolen.</span><span class="sxs-lookup"><span data-stu-id="677b2-116">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="677b2-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="677b2-117">-BatchContext</span></span>
<span data-ttu-id="677b2-118">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="677b2-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="677b2-119">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="677b2-119">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="677b2-120">-ID</span><span class="sxs-lookup"><span data-stu-id="677b2-120">-Id</span></span>
<span data-ttu-id="677b2-121">Anger objekt-ID: t för den pool där automatisk skalning ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="677b2-121">Specifies the object ID of the pool for which to enable automatic scaling.</span></span>

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

### <span data-ttu-id="677b2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="677b2-122">-DefaultProfile</span></span>
<span data-ttu-id="677b2-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="677b2-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="677b2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="677b2-124">CommonParameters</span></span>
<span data-ttu-id="677b2-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="677b2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="677b2-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="677b2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="677b2-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="677b2-127">INPUTS</span></span>

### <span data-ttu-id="677b2-128">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="677b2-128">BatchAccountContext</span></span>
<span data-ttu-id="677b2-129">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="677b2-129">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="677b2-130">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="677b2-130">String</span></span>
<span data-ttu-id="677b2-131">Parametern ' ID ' godkänner värdet för typen ' String ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="677b2-131">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="677b2-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="677b2-132">OUTPUTS</span></span>

## <span data-ttu-id="677b2-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="677b2-133">NOTES</span></span>

## <span data-ttu-id="677b2-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="677b2-134">RELATED LINKS</span></span>

[<span data-ttu-id="677b2-135">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="677b2-135">Disable-AzureBatchAutoScale</span></span>](./Disable-AzureBatchAutoScale.md)

[<span data-ttu-id="677b2-136">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="677b2-136">Test-AzureBatchAutoScale</span></span>](./Test-AzureBatchAutoScale.md)

[<span data-ttu-id="677b2-137">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="677b2-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


