---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3107D061-7F25-45D0-8029-C99120A156DA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchAutoScale.md
ms.openlocfilehash: 920a3bbc02360a0ed771e7120b7d0b9455e08e45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579035"
---
# <span data-ttu-id="24ffe-101">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="24ffe-101">Enable-AzureBatchAutoScale</span></span>

## <span data-ttu-id="24ffe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="24ffe-102">SYNOPSIS</span></span>
<span data-ttu-id="24ffe-103">Aktiverar automatisk skalning av en pool.</span><span class="sxs-lookup"><span data-stu-id="24ffe-103">Enables automatic scaling of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24ffe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="24ffe-104">SYNTAX</span></span>

```
Enable-AzureBatchAutoScale [-Id] <String> [[-AutoScaleFormula] <String>]
 [[-AutoScaleEvaluationInterval] <TimeSpan>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24ffe-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="24ffe-105">DESCRIPTION</span></span>
<span data-ttu-id="24ffe-106">Cmdleten **Enable-AzureBatchAutoScale** aktiverar automatisk skalning av den angivna poolen.</span><span class="sxs-lookup"><span data-stu-id="24ffe-106">The **Enable-AzureBatchAutoScale** cmdlet enables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="24ffe-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="24ffe-107">EXAMPLES</span></span>

### <span data-ttu-id="24ffe-108">Exempel 1: Aktivera automatisk skalning för en pool</span><span class="sxs-lookup"><span data-stu-id="24ffe-108">Example 1: Enable automatic scaling for a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> Enable-AzureBatchAutoScale -Id "MyPool" -AutoScaleFormula $Formula -BatchContext $Context
```

<span data-ttu-id="24ffe-109">Det första kommandot definierar en formel och sparar den sedan i $Formula variabel.</span><span class="sxs-lookup"><span data-stu-id="24ffe-109">The first command defines a formula, and then saves it to the $Formula variable.</span></span>
<span data-ttu-id="24ffe-110">Det andra kommandot aktiverar automatisk skalning på poolen med namnet min pool med formeln i $Formula.</span><span class="sxs-lookup"><span data-stu-id="24ffe-110">The second command enables automatic scaling on the pool named MyPool using the formula in $Formula.</span></span>

## <span data-ttu-id="24ffe-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="24ffe-111">PARAMETERS</span></span>

### <span data-ttu-id="24ffe-112">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="24ffe-112">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="24ffe-113">Anger hur länge (i minuter) som ska gå innan Poolens storlek justeras automatiskt enligt formeln för automatisk skalning.</span><span class="sxs-lookup"><span data-stu-id="24ffe-113">Specifies the amount of time (in minutes) that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="24ffe-114">Standardvärdet är 15 minuter och minimivärdet är 5 minuter.</span><span class="sxs-lookup"><span data-stu-id="24ffe-114">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="24ffe-115">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="24ffe-115">-AutoScaleFormula</span></span>
<span data-ttu-id="24ffe-116">Anger formeln för önskat antal beräknade noder i poolen.</span><span class="sxs-lookup"><span data-stu-id="24ffe-116">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

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

### <span data-ttu-id="24ffe-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="24ffe-117">-BatchContext</span></span>
<span data-ttu-id="24ffe-118">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="24ffe-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="24ffe-119">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="24ffe-119">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="24ffe-120">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="24ffe-120">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="24ffe-121">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="24ffe-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="24ffe-122">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="24ffe-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="24ffe-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24ffe-123">-DefaultProfile</span></span>
<span data-ttu-id="24ffe-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="24ffe-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24ffe-125">-ID</span><span class="sxs-lookup"><span data-stu-id="24ffe-125">-Id</span></span>
<span data-ttu-id="24ffe-126">Anger objekt-ID: t för den pool där automatisk skalning ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="24ffe-126">Specifies the object ID of the pool for which to enable automatic scaling.</span></span>

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

### <span data-ttu-id="24ffe-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24ffe-127">CommonParameters</span></span>
<span data-ttu-id="24ffe-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24ffe-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24ffe-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24ffe-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24ffe-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="24ffe-130">INPUTS</span></span>

### <span data-ttu-id="24ffe-131">System. String</span><span class="sxs-lookup"><span data-stu-id="24ffe-131">System.String</span></span>

### <span data-ttu-id="24ffe-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="24ffe-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="24ffe-133">Parametrar: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="24ffe-133">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="24ffe-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="24ffe-134">OUTPUTS</span></span>

### <span data-ttu-id="24ffe-135">System. Void</span><span class="sxs-lookup"><span data-stu-id="24ffe-135">System.Void</span></span>

## <span data-ttu-id="24ffe-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="24ffe-136">NOTES</span></span>

## <span data-ttu-id="24ffe-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="24ffe-137">RELATED LINKS</span></span>

[<span data-ttu-id="24ffe-138">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="24ffe-138">Disable-AzureBatchAutoScale</span></span>](./Disable-AzureBatchAutoScale.md)

[<span data-ttu-id="24ffe-139">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="24ffe-139">Test-AzureBatchAutoScale</span></span>](./Test-AzureBatchAutoScale.md)

[<span data-ttu-id="24ffe-140">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="24ffe-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


