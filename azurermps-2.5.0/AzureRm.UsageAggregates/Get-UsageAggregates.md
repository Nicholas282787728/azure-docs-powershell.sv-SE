---
external help file: Microsoft.Azure.Commands.UsageAggregates.dll-Help.xml
Module Name: AzureRM
ms.assetid: 52B3ECCB-80E5-4E16-954A-B83D0BDC7E22
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.usageaggregates/get-usageaggregates
schema: 2.0.0
ms.openlocfilehash: 70dda4d40f517d3d7bd7a3a8d64584e74f80310a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929217"
---
# <span data-ttu-id="811a3-101">Get-UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="811a3-101">Get-UsageAggregates</span></span>

## <span data-ttu-id="811a3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="811a3-102">SYNOPSIS</span></span>
<span data-ttu-id="811a3-103">Hämtar den rapporterade användnings informationen för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="811a3-103">Gets the reported Azure subscription usage details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="811a3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="811a3-104">SYNTAX</span></span>

```
Get-UsageAggregates -ReportedStartTime <DateTime> -ReportedEndTime <DateTime>
 [-AggregationGranularity <AggregationGranularity>] [-ShowDetails <Boolean>] [-ContinuationToken <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="811a3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="811a3-105">DESCRIPTION</span></span>
<span data-ttu-id="811a3-106">Cmdleten **Get-UsageAggregates** hämtar den aggregerade Azure-prenumerationens användnings data genom följande egenskaper:</span><span class="sxs-lookup"><span data-stu-id="811a3-106">The **Get-UsageAggregates** cmdlet gets aggregated Azure subscription usage data by the following properties:</span></span> 

- <span data-ttu-id="811a3-107">Start-och slut tider för när användning rapporterades.</span><span class="sxs-lookup"><span data-stu-id="811a3-107">Start and end times of when the usage was reported.</span></span>

- <span data-ttu-id="811a3-108">Mängd precision, antingen dagligen eller varje timme.</span><span class="sxs-lookup"><span data-stu-id="811a3-108">Aggregation precision, either daily or hourly.</span></span>

- <span data-ttu-id="811a3-109">Instans nivå information för flera instanser av samma resurs.</span><span class="sxs-lookup"><span data-stu-id="811a3-109">Instance level detail for multiple instances of the same resource.</span></span>

<span data-ttu-id="811a3-110">För enhetliga resultat baseras data som returneras när användnings uppgifterna rapporterades av Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="811a3-110">For consistent results, the returned data is based on when the usage details were reported by the Azure resource.</span></span>

<span data-ttu-id="811a3-111">Mer information finns i referens för Azure Bill REST API https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c ( https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) i Microsoft Developer Network Library.</span><span class="sxs-lookup"><span data-stu-id="811a3-111">For more information, see Azure Billing REST API Referencehttps://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c (https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) in the Microsoft Developer Network library.</span></span>

## <span data-ttu-id="811a3-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="811a3-112">EXAMPLES</span></span>

### <span data-ttu-id="811a3-113">Exempel 1: Hämta abonnemangs data</span><span class="sxs-lookup"><span data-stu-id="811a3-113">Example 1: Retrieve subscription data</span></span>
```
PS C:\>Get-UsageAggregates -ReportedStartTime "5/2/2015" -ReportedEndTime "5/5/2015"
```

<span data-ttu-id="811a3-114">Det här kommandot hämtar den rapporterade användnings informationen för prenumerationen mellan 5/2/2015 och 5/5/2015.</span><span class="sxs-lookup"><span data-stu-id="811a3-114">This command retrieves the reported usage data for the subscription between 5/2/2015 and 5/5/2015.</span></span>

## <span data-ttu-id="811a3-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="811a3-115">PARAMETERS</span></span>

### <span data-ttu-id="811a3-116">-AggregationGranularity</span><span class="sxs-lookup"><span data-stu-id="811a3-116">-AggregationGranularity</span></span>
<span data-ttu-id="811a3-117">Anger agg regerings precisionen för data.</span><span class="sxs-lookup"><span data-stu-id="811a3-117">Specifies the aggregation precision of the data.</span></span>
<span data-ttu-id="811a3-118">Giltiga värden är: per dag och timme.</span><span class="sxs-lookup"><span data-stu-id="811a3-118">Valid values are: Daily and Hourly.</span></span>

<span data-ttu-id="811a3-119">Standardvärdet är dagligen.</span><span class="sxs-lookup"><span data-stu-id="811a3-119">The default value is Daily.</span></span>

```yaml
Type: AggregationGranularity
Parameter Sets: (All)
Aliases: 
Accepted values: Daily, Hourly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="811a3-120">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="811a3-120">-ContinuationToken</span></span>
<span data-ttu-id="811a3-121">Anger det tilläggs token som hämtades från svars texten i det föregående samtalet.</span><span class="sxs-lookup"><span data-stu-id="811a3-121">Specifies the continuation token that was retrieved from the response body in the previous call.</span></span>
<span data-ttu-id="811a3-122">För en stor resultat mängd visas svaren med hjälp av fortsättnings-token.</span><span class="sxs-lookup"><span data-stu-id="811a3-122">For a large result set, responses are paged by using continuation tokens.</span></span>
<span data-ttu-id="811a3-123">Den fortsatta token fungerar som ett bok märke för status.</span><span class="sxs-lookup"><span data-stu-id="811a3-123">The continuation token serves as a bookmark for progress.</span></span>
<span data-ttu-id="811a3-124">Om du inte anger den här parametern hämtas data från början av den dag eller timme som anges i *ReportedStartTime*.</span><span class="sxs-lookup"><span data-stu-id="811a3-124">If you do not specify this parameter, the data is retrieved from the beginning of the day or hour specified in *ReportedStartTime*.</span></span>
<span data-ttu-id="811a3-125">Vi rekommenderar att du följer länken Nästa i svaret till sida med data.</span><span class="sxs-lookup"><span data-stu-id="811a3-125">We recommend that you follow the next link in the response to page though the data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="811a3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="811a3-126">-DefaultProfile</span></span>
<span data-ttu-id="811a3-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="811a3-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="811a3-128">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="811a3-128">-ReportedEndTime</span></span>
<span data-ttu-id="811a3-129">Anger den rapporterade slut tiden för när resursförbrukning registrerades i Azure-fakturerings systemet.</span><span class="sxs-lookup"><span data-stu-id="811a3-129">Specifies the reported end time for when resource usage was recorded in the Azure billing system.</span></span>

<span data-ttu-id="811a3-130">Azure är ett distribuerat system som sträcker sig över flera data Center över hela världen, så det finns en fördröjning mellan när resursen faktiskt förbrukades, vilket är resursanvändnings tiden och när användnings händelsen nådde fakturerings systemet, vilket är den tid som rapporter ATS för resursanvändningen.</span><span class="sxs-lookup"><span data-stu-id="811a3-130">Azure is a distributed system, spanning multiple datacenters around the world, so there is a delay between when the resource was actually consumed, which is the resource usage time, and when the usage event reached the billing system, which is the resource usage reported time.</span></span>
<span data-ttu-id="811a3-131">Om du vill få alla användar händelser för en prenumeration som rapporter ATS för en viss tids period frågar du efter rapporterings tid.</span><span class="sxs-lookup"><span data-stu-id="811a3-131">In order to get all usage events for a subscription that are reported for a time period, you query by reported time.</span></span>
<span data-ttu-id="811a3-132">Även om du frågar efter rapporterings tid aggregerar cmdleten svars informationen efter resursanvändnings tid.</span><span class="sxs-lookup"><span data-stu-id="811a3-132">Even though you query by reported time, the cmdlet aggregates the response data by the resource usage time.</span></span>
<span data-ttu-id="811a3-133">Resursanvändnings data är den användbara pivottabellen för analys av data.</span><span class="sxs-lookup"><span data-stu-id="811a3-133">The resource usage data is the useful pivot for analyzing the data.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="811a3-134">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="811a3-134">-ReportedStartTime</span></span>
<span data-ttu-id="811a3-135">Anger den rapporterade start tiden för när resursförbrukning registrerades i Azure-fakturerings systemet.</span><span class="sxs-lookup"><span data-stu-id="811a3-135">Specifies the reported start time for when resource usage was recorded in the Azure billing system.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="811a3-136">-ShowDetails</span><span class="sxs-lookup"><span data-stu-id="811a3-136">-ShowDetails</span></span>
<span data-ttu-id="811a3-137">Anger om den här cmdleten returnerar information om förekomst nivå med användnings data.</span><span class="sxs-lookup"><span data-stu-id="811a3-137">Indicates whether this cmdlet returns instance-level details with the usage data.</span></span>

<span data-ttu-id="811a3-138">Standardvärdet är $True.</span><span class="sxs-lookup"><span data-stu-id="811a3-138">The default value is $True.</span></span>

<span data-ttu-id="811a3-139">Om $False, aggregerar tjänsten resultaten på Server sidan och returnerar därför färre mängd grupper.</span><span class="sxs-lookup"><span data-stu-id="811a3-139">If $False, the service aggregates the results on the server side, and therefore returns fewer aggregate groups.</span></span>
<span data-ttu-id="811a3-140">Om du till exempel kör tre webbplatser får du tre linje objekt som standard för webbplats förbrukning.</span><span class="sxs-lookup"><span data-stu-id="811a3-140">For example, if you are running three websites, by default you will get three line items for website consumption.</span></span>
<span data-ttu-id="811a3-141">Men när värdet är $False döljs alla data för samma **subscriptionId** , **meterId** , **usageStartTime** och **usageEndTime** i ett enda objekt.</span><span class="sxs-lookup"><span data-stu-id="811a3-141">However, when the value is $False, all the data for the same **subscriptionId** , **meterId** , **usageStartTime** , and **usageEndTime** is collapsed into a single line item.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="811a3-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="811a3-142">CommonParameters</span></span>
<span data-ttu-id="811a3-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="811a3-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="811a3-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="811a3-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="811a3-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="811a3-145">INPUTS</span></span>

### <span data-ttu-id="811a3-146">Ingen</span><span class="sxs-lookup"><span data-stu-id="811a3-146">None</span></span>
<span data-ttu-id="811a3-147">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="811a3-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="811a3-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="811a3-148">OUTPUTS</span></span>

### <span data-ttu-id="811a3-149">Microsoft. Azure. Commerce. UsageAggregates. Models. UsageAggregationGetResponse</span><span class="sxs-lookup"><span data-stu-id="811a3-149">Microsoft.Azure.Commerce.UsageAggregates.Models.UsageAggregationGetResponse</span></span>

## <span data-ttu-id="811a3-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="811a3-150">NOTES</span></span>

## <span data-ttu-id="811a3-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="811a3-151">RELATED LINKS</span></span>

