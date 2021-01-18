---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4B373447-3078-4C1F-932E-8337AB170DEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpoolusagemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolUsageMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolUsageMetric.md
ms.openlocfilehash: 1700e20318a502f32386638f94a9c5c86c271d7d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524781"
---
# <span data-ttu-id="6b48d-101">Get-AzBatchPoolUsageMetric</span><span class="sxs-lookup"><span data-stu-id="6b48d-101">Get-AzBatchPoolUsageMetric</span></span>

## <span data-ttu-id="6b48d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6b48d-102">SYNOPSIS</span></span>
<span data-ttu-id="6b48d-103">Hämtar mått för användning av pooler för ett batch-konto.</span><span class="sxs-lookup"><span data-stu-id="6b48d-103">Gets pool usage metrics for a Batch account.</span></span>

## <span data-ttu-id="6b48d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6b48d-104">SYNTAX</span></span>

```
Get-AzBatchPoolUsageMetric [-StartTime <DateTime>] [-EndTime <DateTime>] [-Filter <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b48d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6b48d-105">DESCRIPTION</span></span>
<span data-ttu-id="6b48d-106">Cmdleten **Get-AzBatchPoolUsageMetric** hämtar användnings måtten som aggregeras per pool under enskilda tidsintervall för det angivna kontot.</span><span class="sxs-lookup"><span data-stu-id="6b48d-106">The **Get-AzBatchPoolUsageMetric** cmdlet gets the usage metrics, aggregated by pool across individual time intervals, for the specified account.</span></span>
<span data-ttu-id="6b48d-107">Du kan hämta statistik för en viss pool och för ett tidsintervall.</span><span class="sxs-lookup"><span data-stu-id="6b48d-107">You can get the statistics for a specific pool and for a time range.</span></span>

## <span data-ttu-id="6b48d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6b48d-108">EXAMPLES</span></span>

### <span data-ttu-id="6b48d-109">Exempel 1: Hämta mått för resursanvändning för ett tidsintervall</span><span class="sxs-lookup"><span data-stu-id="6b48d-109">Example 1: Get pool usage metrics for a time range</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $StartTime = Get-Date -Date "2016-05-16 00:00:00Z"
PS C:\> $EndTime = Get-Date -Date "2016-05-16 01:00:00Z"
PS C:\> Get-AzBatchPoolUsageMetric -StartTime $StartTime -EndTime $EndTime -BatchContext $context
DataEgressGiB      : 6.68875873088837E-06
DataIngressGiB     : 1.9485130906105E-05
EndTime            : 5/16/2016 12:30:00 AM
PoolId             : testpool1
StartTime          : 5/16/2016 12:00:00 AM
TotalCoreHours     : 8
VirtualMachineSize : standard_d4

DataEgressGiB      : 5.61587512493134E-06
DataIngressGiB     : 1.76150351762772E-05
EndTime            : 5/16/2016 12:30:00 AM
PoolId             : testpool2
StartTime          : 5/16/2016 12:00:00 AM
TotalCoreHours     : 12
VirtualMachineSize : standard_d4

DataEgressGiB      : 7.36676156520844E-06
DataIngressGiB     : 2.10804864764214E-05
EndTime            : 5/16/2016 1:00:00 AM
PoolId             : testpool1
StartTime          : 5/16/2016 12:30:00 AM
TotalCoreHours     : 7.99999999955555
VirtualMachineSize : standard_d4

DataEgressGiB      : 5.80586493015289E-06
DataIngressGiB     : 1.80602073669434E-05
EndTime            : 5/16/2016 1:00:00 AM
PoolId             : testpool2
StartTime          : 5/16/2016 12:30:00 AM
TotalCoreHours     : 11.9999999993333
VirtualMachineSize : standard_d4
```

<span data-ttu-id="6b48d-110">Det första kommandot skapar en objekt referens till konto nycklarna för batch-kontot som heter ContosoBatchAccount genom att använda **Get-AzBatchAccountKey**.</span><span class="sxs-lookup"><span data-stu-id="6b48d-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="6b48d-111">Kommandot lagrar objekt referensen i $Context variabel.</span><span class="sxs-lookup"><span data-stu-id="6b48d-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="6b48d-112">Med de två kommandona skapar du **datetime** -objekt med hjälp av Get-Date cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b48d-112">The next two commands create **DateTime** objects by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="6b48d-113">I kommandona lagras dessa värden i $StartTime och $EndTime variabler för att användas med kommandot slut.</span><span class="sxs-lookup"><span data-stu-id="6b48d-113">The commands store these values in the $StartTime and $EndTime variables for use with the final command.</span></span>
<span data-ttu-id="6b48d-114">Med det sista kommandot returneras alla användnings mått för poolen, aggregerade efter pool, över tidsintervall mellan angivna start-och slut tider.</span><span class="sxs-lookup"><span data-stu-id="6b48d-114">The final command returns all of the pool usage metrics, aggregated by pool, across time interval between the specified start and end times.</span></span>

### <span data-ttu-id="6b48d-115">Exempel 2: Hämta mått för användning av pool med hjälp av ett filter</span><span class="sxs-lookup"><span data-stu-id="6b48d-115">Example 2: Get pool usage metrics by using a filter</span></span>
```
PS C:\>Get-AzBatchPoolUsageMetric -Filter "poolId eq 'ContosoPool'" -BatchContext $Context
DataEgressGiB      : 9.0496614575386E-06
DataIngressGiB     : 2.60043889284134E-05
EndTime            : 5/16/2016 5:30:00 PM
PoolId             : MyPool
StartTime          : 5/16/2016 5:00:00 PM
TotalCoreHours     : 12
VirtualMachineSize : standard_d4
```

<span data-ttu-id="6b48d-116">Det här kommandot returnerar användnings måtten för poolen med namnet ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="6b48d-116">This command returns the usage metrics for pool named ContosoPool.</span></span>
<span data-ttu-id="6b48d-117">Kommandot anger en filter sträng för att ange poolen och använder samma $Context värde som föregående exempel.</span><span class="sxs-lookup"><span data-stu-id="6b48d-117">The command specifies a filter string to specify that pool, and uses the same $Context value as the previous example.</span></span>

## <span data-ttu-id="6b48d-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6b48d-118">PARAMETERS</span></span>

### <span data-ttu-id="6b48d-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6b48d-119">-BatchContext</span></span>
<span data-ttu-id="6b48d-120">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="6b48d-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6b48d-121">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="6b48d-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6b48d-122">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="6b48d-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6b48d-123">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="6b48d-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6b48d-124">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="6b48d-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6b48d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b48d-125">-DefaultProfile</span></span>
<span data-ttu-id="6b48d-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6b48d-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b48d-127">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="6b48d-127">-EndTime</span></span>
<span data-ttu-id="6b48d-128">Anger slutet av ett tidsintervall som denna cmdlet får användnings värden för.</span><span class="sxs-lookup"><span data-stu-id="6b48d-128">Specifies the end of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="6b48d-129">Ange en tid som är minst två timmar tidigare.</span><span class="sxs-lookup"><span data-stu-id="6b48d-129">Specify a time at least two hours earlier.</span></span>
<span data-ttu-id="6b48d-130">Om du inte anger en slut tid använder denna cmdlet det senaste mängd intervallet som är tillgängligt.</span><span class="sxs-lookup"><span data-stu-id="6b48d-130">If you do not specify an end time, this cmdlet uses the last aggregation interval currently available.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b48d-131">-Filter</span><span class="sxs-lookup"><span data-stu-id="6b48d-131">-Filter</span></span>
<span data-ttu-id="6b48d-132">Anger en OData filter-sats som ska användas för att filtrera de mät värden som returneras av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b48d-132">Specifies an OData filter clause to use to filter the metrics that this cmdlet returns.</span></span>
<span data-ttu-id="6b48d-133">Den enda giltiga egenskapen är **poolId** med ett sträng värde.</span><span class="sxs-lookup"><span data-stu-id="6b48d-133">The only valid property is **poolId** with a string value.</span></span>
<span data-ttu-id="6b48d-134">Möjlig åtgärd är följande: EQ, ge, gt, Le, lt, StartsWith.</span><span class="sxs-lookup"><span data-stu-id="6b48d-134">Possible operations are the following: eq, ge, gt, le, lt, startswith.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b48d-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="6b48d-135">-StartTime</span></span>
<span data-ttu-id="6b48d-136">Anger början av ett tidsintervall som denna cmdlet får användnings mått för.</span><span class="sxs-lookup"><span data-stu-id="6b48d-136">Specifies the start of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="6b48d-137">Ange en tid som är minst två och en halv timme tidigare.</span><span class="sxs-lookup"><span data-stu-id="6b48d-137">Specify a time at least two and a half hours earlier.</span></span>
<span data-ttu-id="6b48d-138">Om du inte anger en start tid använder denna cmdlet det senaste mängd intervallet som är tillgängligt.</span><span class="sxs-lookup"><span data-stu-id="6b48d-138">If you do not specify a start time, this cmdlet uses the last aggregation interval currently available.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b48d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b48d-139">CommonParameters</span></span>
<span data-ttu-id="6b48d-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b48d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b48d-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b48d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b48d-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6b48d-142">INPUTS</span></span>

### <span data-ttu-id="6b48d-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6b48d-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="6b48d-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6b48d-144">OUTPUTS</span></span>

### <span data-ttu-id="6b48d-145">Microsoft.Azure.Commands.BatCH. Modeller. PSPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="6b48d-145">Microsoft.Azure.Commands.Batch.Models.PSPoolUsageMetrics</span></span>

## <span data-ttu-id="6b48d-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6b48d-146">NOTES</span></span>

## <span data-ttu-id="6b48d-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6b48d-147">RELATED LINKS</span></span>

[<span data-ttu-id="6b48d-148">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="6b48d-148">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="6b48d-149">Get-AzBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="6b48d-149">Get-AzBatchPoolStatistics</span></span>](./Get-AzBatchPoolStatistic.md)

[<span data-ttu-id="6b48d-150">Get-AzBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="6b48d-150">Get-AzBatchJobStatistics</span></span>](./Get-AzBatchJobStatistic.md)
