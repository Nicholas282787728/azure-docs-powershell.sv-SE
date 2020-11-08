---
external help file: ''
Module Name: Azs.Commerce.Admin
online version: https://docs.microsoft.com/powershell/module/azs.commerce.admin/get-azssubscriberusage
schema: 2.0.0
ms.openlocfilehash: 9eed3f6f2a4d07bd48136c50ec173f801b30c928
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100188"
---
# <span data-ttu-id="03ad2-101">Get-AzsSubscriberUsage</span><span class="sxs-lookup"><span data-stu-id="03ad2-101">Get-AzsSubscriberUsage</span></span>

## <span data-ttu-id="03ad2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="03ad2-102">SYNOPSIS</span></span>
<span data-ttu-id="03ad2-103">Hämtar en samling SubscriberUsageAggregates, som är UsageAggregates för användare.</span><span class="sxs-lookup"><span data-stu-id="03ad2-103">Gets a collection of SubscriberUsageAggregates, which are UsageAggregates from users.</span></span>

## <span data-ttu-id="03ad2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="03ad2-104">SYNTAX</span></span>

```
Get-AzsSubscriberUsage -ReportedEndTime <DateTime> -ReportedStartTime <DateTime> [-SubscriptionId <String[]>]
 [-AggregationGranularity <String>] [-ContinuationToken <String>] [-SubscriberId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="03ad2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="03ad2-105">DESCRIPTION</span></span>
<span data-ttu-id="03ad2-106">Hämtar en samling SubscriberUsageAggregates, som är UsageAggregates för användare.</span><span class="sxs-lookup"><span data-stu-id="03ad2-106">Gets a collection of SubscriberUsageAggregates, which are UsageAggregates from users.</span></span>

## <span data-ttu-id="03ad2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="03ad2-107">EXAMPLES</span></span>

### <span data-ttu-id="03ad2-108">Exempel 1: Hämta användnings data samlade per dag</span><span class="sxs-lookup"><span data-stu-id="03ad2-108">Example 1: Get usage data aggregated by day</span></span>
```powershell
Get-AzsSubscriberUsage -ReportedStartTime "2019-12-30T00:00:00Z" -ReportedEndTime "2019-12-31T00:00:00Z" -AggregationGranularity Daily
```

<span data-ttu-id="03ad2-109">Hämta användnings data för hela dagen den 30: e december 2019 (i UTC) för alla innehavare under leverantör aggregerade av dagen.</span><span class="sxs-lookup"><span data-stu-id="03ad2-109">Get the usage data for the entire day of 30th Dec 2019 (in UTC) for all tenants under provider aggregated by the day.</span></span>
<span data-ttu-id="03ad2-110">ReportedStartTime och ReportedEndTime måste avrundas till dagar.</span><span class="sxs-lookup"><span data-stu-id="03ad2-110">ReportedStartTime and ReportedEndTime must be rounded to days.</span></span>
<span data-ttu-id="03ad2-111">Om den anropas som tjänst administratör visar detta effektivt All användnings information för varje klient organisation.</span><span class="sxs-lookup"><span data-stu-id="03ad2-111">If called as the service administrator, this effectively shows all usage data for every tenant.</span></span>

### <span data-ttu-id="03ad2-112">Exempel 2: Hämta användnings data samlade från timmen</span><span class="sxs-lookup"><span data-stu-id="03ad2-112">Example 2: Get usage data aggregated by the hour</span></span>
```powershell
Get-AzsSubscriberUsage -ReportedStartTime "2019-12-30T00:00:00Z" -ReportedEndTime "2019-12-30T02:00:00Z" -AggregationGranularity Hourly
```

<span data-ttu-id="03ad2-113">Hämta användnings data mellan 00.00-2am den 30 december dec 2019 (i UTC) samlade per timme.</span><span class="sxs-lookup"><span data-stu-id="03ad2-113">Get the usage data between  12am - 2am on 30th Dec 2019 (in UTC) aggregated by the hour.</span></span>
<span data-ttu-id="03ad2-114">ReportedStartTime och ReportedEndTime måste avrundas till timmar.</span><span class="sxs-lookup"><span data-stu-id="03ad2-114">ReportedStartTime and ReportedEndTime must be rounded to hours.</span></span>
<span data-ttu-id="03ad2-115">På samma sätt visar detta, om det kallas tjänst administratören, alla användar data för varje klient organisation.</span><span class="sxs-lookup"><span data-stu-id="03ad2-115">Likewise, if called as the service administrator, this effectively shows all usage data for every tenant.</span></span>

## <span data-ttu-id="03ad2-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="03ad2-116">PARAMETERS</span></span>

### <span data-ttu-id="03ad2-117">-AggregationGranularity</span><span class="sxs-lookup"><span data-stu-id="03ad2-117">-AggregationGranularity</span></span>
<span data-ttu-id="03ad2-118">Agg regerings precisionen.</span><span class="sxs-lookup"><span data-stu-id="03ad2-118">The aggregation granularity.</span></span>

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

### <span data-ttu-id="03ad2-119">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="03ad2-119">-ContinuationToken</span></span>
<span data-ttu-id="03ad2-120">Tilläggs-token.</span><span class="sxs-lookup"><span data-stu-id="03ad2-120">The continuation token.</span></span>

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

### <span data-ttu-id="03ad2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03ad2-121">-DefaultProfile</span></span>
<span data-ttu-id="03ad2-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="03ad2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="03ad2-123">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="03ad2-123">-ReportedEndTime</span></span>
<span data-ttu-id="03ad2-124">Den rapporterade slut tiden (exklusivt).</span><span class="sxs-lookup"><span data-stu-id="03ad2-124">The reported end time (exclusive).</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="03ad2-125">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="03ad2-125">-ReportedStartTime</span></span>
<span data-ttu-id="03ad2-126">Den rapporterade start tiden (inklusive detta).</span><span class="sxs-lookup"><span data-stu-id="03ad2-126">The reported start time (inclusive).</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="03ad2-127">-SubscriberId</span><span class="sxs-lookup"><span data-stu-id="03ad2-127">-SubscriberId</span></span>
<span data-ttu-id="03ad2-128">ID för klient organisationens prenumeration.</span><span class="sxs-lookup"><span data-stu-id="03ad2-128">The tenant subscription identifier.</span></span>

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

### <span data-ttu-id="03ad2-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="03ad2-129">-SubscriptionId</span></span>
<span data-ttu-id="03ad2-130">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="03ad2-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="03ad2-131">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="03ad2-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="03ad2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03ad2-132">CommonParameters</span></span>
<span data-ttu-id="03ad2-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03ad2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03ad2-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03ad2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03ad2-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="03ad2-135">INPUTS</span></span>

## <span data-ttu-id="03ad2-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="03ad2-136">OUTPUTS</span></span>

### <span data-ttu-id="03ad2-137">Microsoft. Azure. PowerShell. cmdletar. Commerce. Models. Api20150601Preview. IUsageAggregate</span><span class="sxs-lookup"><span data-stu-id="03ad2-137">Microsoft.Azure.PowerShell.Cmdlets.Commerce.Models.Api20150601Preview.IUsageAggregate</span></span>



## <span data-ttu-id="03ad2-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="03ad2-138">NOTES</span></span>

## <span data-ttu-id="03ad2-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="03ad2-139">RELATED LINKS</span></span>

