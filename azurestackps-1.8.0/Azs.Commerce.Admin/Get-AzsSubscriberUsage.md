---
external help file: Azs.Commerce.Admin-help.xml
Module Name: Azs.Commerce.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4f45a90d4f8e8c3072393c5dc959885636b64dce
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921290"
---
# <span data-ttu-id="3acac-101">Get-AzsSubscriberUsage</span><span class="sxs-lookup"><span data-stu-id="3acac-101">Get-AzsSubscriberUsage</span></span>

## <span data-ttu-id="3acac-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3acac-102">SYNOPSIS</span></span>
<span data-ttu-id="3acac-103">Hämta användnings data från under det angivna TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="3acac-103">Get usage data from during the specified timespan.</span></span>

## <span data-ttu-id="3acac-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3acac-104">SYNTAX</span></span>

```
Get-AzsSubscriberUsage [[-SubscriberId] <String>] [-ReportedStartTime] <DateTime>
 [[-AggregationGranularity] <String>] [[-Skip] <Int32>] [-ReportedEndTime] <DateTime>
 [[-ContinuationToken] <String>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="3acac-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3acac-105">DESCRIPTION</span></span>
<span data-ttu-id="3acac-106">Hämta användnings data från under det angivna TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="3acac-106">Get usage data from during the specified timespan.</span></span>

## <span data-ttu-id="3acac-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3acac-107">EXAMPLES</span></span>

### <span data-ttu-id="3acac-108">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="3acac-108">EXAMPLE 1</span></span>
```
Get-AzsSubscriberUsage -ReportedStartTime "2017-09-06T00:00:00Z" -ReportedEndTime "2017-09-07T00:00:00Z"
```

<span data-ttu-id="3acac-109">Hämta användnings data från de senaste 24 timmarna.</span><span class="sxs-lookup"><span data-stu-id="3acac-109">Get usage data from the last 24 hours.</span></span>

## <span data-ttu-id="3acac-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3acac-110">PARAMETERS</span></span>

### <span data-ttu-id="3acac-111">-SubscriberId</span><span class="sxs-lookup"><span data-stu-id="3acac-111">-SubscriberId</span></span>
<span data-ttu-id="3acac-112">ID för klient organisationens prenumeration.</span><span class="sxs-lookup"><span data-stu-id="3acac-112">The tenant subscription identifier.</span></span>

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

### <span data-ttu-id="3acac-113">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="3acac-113">-ReportedStartTime</span></span>
<span data-ttu-id="3acac-114">Den rapporterade start tiden (inklusive detta).</span><span class="sxs-lookup"><span data-stu-id="3acac-114">The reported start time (inclusive).</span></span>

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

### <span data-ttu-id="3acac-115">-AggregationGranularity</span><span class="sxs-lookup"><span data-stu-id="3acac-115">-AggregationGranularity</span></span>
<span data-ttu-id="3acac-116">Agg regerings precisionen.</span><span class="sxs-lookup"><span data-stu-id="3acac-116">The aggregation granularity.</span></span>

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

### <span data-ttu-id="3acac-117">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="3acac-117">-Skip</span></span>
<span data-ttu-id="3acac-118">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="3acac-118">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="3acac-119">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="3acac-119">-ReportedEndTime</span></span>
<span data-ttu-id="3acac-120">Den rapporterade slut tiden (exklusivt).</span><span class="sxs-lookup"><span data-stu-id="3acac-120">The reported end time (exclusive).</span></span>

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

### <span data-ttu-id="3acac-121">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="3acac-121">-ContinuationToken</span></span>
<span data-ttu-id="3acac-122">Tilläggs-token.</span><span class="sxs-lookup"><span data-stu-id="3acac-122">The continuation token.</span></span>

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

### <span data-ttu-id="3acac-123">-Överst</span><span class="sxs-lookup"><span data-stu-id="3acac-123">-Top</span></span>
<span data-ttu-id="3acac-124">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="3acac-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="3acac-125">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="3acac-125">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="3acac-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3acac-126">CommonParameters</span></span>
<span data-ttu-id="3acac-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3acac-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3acac-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3acac-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3acac-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3acac-129">INPUTS</span></span>

## <span data-ttu-id="3acac-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3acac-130">OUTPUTS</span></span>

### <span data-ttu-id="3acac-131">Microsoft. AzureStack. Management. Commerce. admin. Models. UsageAggregate</span><span class="sxs-lookup"><span data-stu-id="3acac-131">Microsoft.AzureStack.Management.Commerce.Admin.Models.UsageAggregate</span></span>

## <span data-ttu-id="3acac-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3acac-132">NOTES</span></span>

## <span data-ttu-id="3acac-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3acac-133">RELATED LINKS</span></span>
