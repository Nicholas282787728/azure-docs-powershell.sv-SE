---
external help file: Azs.Commerce.Admin-help.xml
Module Name: Azs.Commerce.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 12b98727cdb8e6d31fb1aaf1a2215b79a6b982e5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920475"
---
# <span data-ttu-id="de80f-101">Get-AzsSubscriberUsage</span><span class="sxs-lookup"><span data-stu-id="de80f-101">Get-AzsSubscriberUsage</span></span>

## <span data-ttu-id="de80f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="de80f-102">SYNOPSIS</span></span>
<span data-ttu-id="de80f-103">Hämta användnings data från under det angivna TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="de80f-103">Get usage data from during the specified timespan.</span></span>

## <span data-ttu-id="de80f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="de80f-104">SYNTAX</span></span>

```
Get-AzsSubscriberUsage [[-SubscriberId] <String>] [-ReportedStartTime] <DateTime>
 [[-AggregationGranularity] <String>] [[-Skip] <Int32>] [-ReportedEndTime] <DateTime>
 [[-ContinuationToken] <String>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="de80f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="de80f-105">DESCRIPTION</span></span>
<span data-ttu-id="de80f-106">Hämta användnings data från under det angivna TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="de80f-106">Get usage data from during the specified timespan.</span></span>

## <span data-ttu-id="de80f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="de80f-107">EXAMPLES</span></span>

### <span data-ttu-id="de80f-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="de80f-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSubscriberUsage -ReportedStartTime "2017-09-06T00:00:00Z" -ReportedEndTime "2017-09-07T00:00:00Z"
```

<span data-ttu-id="de80f-109">Hämta användnings data från de senaste 24 timmarna.</span><span class="sxs-lookup"><span data-stu-id="de80f-109">Get usage data from the last 24 hours.</span></span>

## <span data-ttu-id="de80f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="de80f-110">PARAMETERS</span></span>

### <span data-ttu-id="de80f-111">-AggregationGranularity</span><span class="sxs-lookup"><span data-stu-id="de80f-111">-AggregationGranularity</span></span>
<span data-ttu-id="de80f-112">Agg regerings precisionen.</span><span class="sxs-lookup"><span data-stu-id="de80f-112">The aggregation granularity.</span></span>

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

### <span data-ttu-id="de80f-113">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="de80f-113">-ContinuationToken</span></span>
<span data-ttu-id="de80f-114">Tilläggs-token.</span><span class="sxs-lookup"><span data-stu-id="de80f-114">The continuation token.</span></span>

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

### <span data-ttu-id="de80f-115">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="de80f-115">-ReportedEndTime</span></span>
<span data-ttu-id="de80f-116">Den rapporterade slut tiden (exklusivt).</span><span class="sxs-lookup"><span data-stu-id="de80f-116">The reported end time (exclusive).</span></span>

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

### <span data-ttu-id="de80f-117">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="de80f-117">-ReportedStartTime</span></span>
<span data-ttu-id="de80f-118">Den rapporterade start tiden (inklusive detta).</span><span class="sxs-lookup"><span data-stu-id="de80f-118">The reported start time (inclusive).</span></span>

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

### <span data-ttu-id="de80f-119">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="de80f-119">-Skip</span></span>
<span data-ttu-id="de80f-120">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="de80f-120">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="de80f-121">-SubscriberId</span><span class="sxs-lookup"><span data-stu-id="de80f-121">-SubscriberId</span></span>
<span data-ttu-id="de80f-122">ID för klient organisationens prenumeration.</span><span class="sxs-lookup"><span data-stu-id="de80f-122">The tenant subscription identifier.</span></span>

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

### <span data-ttu-id="de80f-123">-Överst</span><span class="sxs-lookup"><span data-stu-id="de80f-123">-Top</span></span>
<span data-ttu-id="de80f-124">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="de80f-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="de80f-125">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="de80f-125">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="de80f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de80f-126">CommonParameters</span></span>
<span data-ttu-id="de80f-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de80f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de80f-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de80f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de80f-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="de80f-129">INPUTS</span></span>

## <span data-ttu-id="de80f-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="de80f-130">OUTPUTS</span></span>

### <span data-ttu-id="de80f-131">Microsoft. AzureStack. Management. Commerce. admin. Models. UsageAggregate</span><span class="sxs-lookup"><span data-stu-id="de80f-131">Microsoft.AzureStack.Management.Commerce.Admin.Models.UsageAggregate</span></span>

## <span data-ttu-id="de80f-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="de80f-132">NOTES</span></span>

## <span data-ttu-id="de80f-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="de80f-133">RELATED LINKS</span></span>

