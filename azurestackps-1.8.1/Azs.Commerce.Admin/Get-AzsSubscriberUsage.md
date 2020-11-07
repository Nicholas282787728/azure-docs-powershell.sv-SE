---
external help file: Azs.Commerce.Admin-help.xml
Module Name: Azs.Commerce.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4f45a90d4f8e8c3072393c5dc959885636b64dce
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921864"
---
# <span data-ttu-id="dce6b-101">Get-AzsSubscriberUsage</span><span class="sxs-lookup"><span data-stu-id="dce6b-101">Get-AzsSubscriberUsage</span></span>

## <span data-ttu-id="dce6b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dce6b-102">SYNOPSIS</span></span>
<span data-ttu-id="dce6b-103">Hämta användnings data från under det angivna TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="dce6b-103">Get usage data from during the specified timespan.</span></span>

## <span data-ttu-id="dce6b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dce6b-104">SYNTAX</span></span>

```
Get-AzsSubscriberUsage [[-SubscriberId] <String>] [-ReportedStartTime] <DateTime>
 [[-AggregationGranularity] <String>] [[-Skip] <Int32>] [-ReportedEndTime] <DateTime>
 [[-ContinuationToken] <String>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="dce6b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dce6b-105">DESCRIPTION</span></span>
<span data-ttu-id="dce6b-106">Hämta användnings data från under det angivna TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="dce6b-106">Get usage data from during the specified timespan.</span></span>

## <span data-ttu-id="dce6b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dce6b-107">EXAMPLES</span></span>

### <span data-ttu-id="dce6b-108">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="dce6b-108">EXAMPLE 1</span></span>
```
Get-AzsSubscriberUsage -ReportedStartTime "2017-09-06T00:00:00Z" -ReportedEndTime "2017-09-07T00:00:00Z"
```

<span data-ttu-id="dce6b-109">Hämta användnings data från de senaste 24 timmarna.</span><span class="sxs-lookup"><span data-stu-id="dce6b-109">Get usage data from the last 24 hours.</span></span>

## <span data-ttu-id="dce6b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dce6b-110">PARAMETERS</span></span>

### <span data-ttu-id="dce6b-111">-SubscriberId</span><span class="sxs-lookup"><span data-stu-id="dce6b-111">-SubscriberId</span></span>
<span data-ttu-id="dce6b-112">ID för klient organisationens prenumeration.</span><span class="sxs-lookup"><span data-stu-id="dce6b-112">The tenant subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dce6b-113">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="dce6b-113">-ReportedStartTime</span></span>
<span data-ttu-id="dce6b-114">Den rapporterade start tiden (inklusive detta).</span><span class="sxs-lookup"><span data-stu-id="dce6b-114">The reported start time (inclusive).</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dce6b-115">-AggregationGranularity</span><span class="sxs-lookup"><span data-stu-id="dce6b-115">-AggregationGranularity</span></span>
<span data-ttu-id="dce6b-116">Agg regerings precisionen.</span><span class="sxs-lookup"><span data-stu-id="dce6b-116">The aggregation granularity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dce6b-117">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="dce6b-117">-Skip</span></span>
<span data-ttu-id="dce6b-118">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="dce6b-118">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dce6b-119">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="dce6b-119">-ReportedEndTime</span></span>
<span data-ttu-id="dce6b-120">Den rapporterade slut tiden (exklusivt).</span><span class="sxs-lookup"><span data-stu-id="dce6b-120">The reported end time (exclusive).</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dce6b-121">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="dce6b-121">-ContinuationToken</span></span>
<span data-ttu-id="dce6b-122">Tilläggs-token.</span><span class="sxs-lookup"><span data-stu-id="dce6b-122">The continuation token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dce6b-123">-Överst</span><span class="sxs-lookup"><span data-stu-id="dce6b-123">-Top</span></span>
<span data-ttu-id="dce6b-124">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="dce6b-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="dce6b-125">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="dce6b-125">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dce6b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dce6b-126">CommonParameters</span></span>
<span data-ttu-id="dce6b-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dce6b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dce6b-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dce6b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dce6b-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dce6b-129">INPUTS</span></span>

## <span data-ttu-id="dce6b-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dce6b-130">OUTPUTS</span></span>

### <span data-ttu-id="dce6b-131">Microsoft. AzureStack. Management. Commerce. admin. Models. UsageAggregate</span><span class="sxs-lookup"><span data-stu-id="dce6b-131">Microsoft.AzureStack.Management.Commerce.Admin.Models.UsageAggregate</span></span>

## <span data-ttu-id="dce6b-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dce6b-132">NOTES</span></span>

## <span data-ttu-id="dce6b-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dce6b-133">RELATED LINKS</span></span>
