---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsplanmetric
schema: 2.0.0
ms.openlocfilehash: 9a8ef074cf6e59d30217b55b956a4d5101708bcc
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100222"
---
# <span data-ttu-id="c7fa3-101">Get-AzsPlanMetric</span><span class="sxs-lookup"><span data-stu-id="c7fa3-101">Get-AzsPlanMetric</span></span>

## <span data-ttu-id="c7fa3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c7fa3-102">SYNOPSIS</span></span>
<span data-ttu-id="c7fa3-103">Hämta måtten för det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-103">Get the metrics of the specified plan.</span></span>

## <span data-ttu-id="c7fa3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c7fa3-104">SYNTAX</span></span>

```
Get-AzsPlanMetric -PlanName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c7fa3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c7fa3-105">DESCRIPTION</span></span>
<span data-ttu-id="c7fa3-106">Hämta måtten för det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-106">Get the metrics of the specified plan.</span></span>

## <span data-ttu-id="c7fa3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c7fa3-107">EXAMPLES</span></span>

### <span data-ttu-id="c7fa3-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c7fa3-108">Example 1</span></span>
```powershell
PS C:\> Get-AzsPlanMetric -PlanName "testplan" -ResourceGroupName "testrg"

EndTime               MetricUnit StartTime            TimeGrain
-------               ---------- ---------            ---------
3/13/2020 12:06:16 AM Count      3/6/2020 12:00:00 AM P1D      
3/13/2020 12:06:16 AM Count      3/6/2020 12:00:00 AM P1D
```

<span data-ttu-id="c7fa3-109">Få en plans mått.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-109">Get a plan's metrics.</span></span>

## <span data-ttu-id="c7fa3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c7fa3-110">PARAMETERS</span></span>

### <span data-ttu-id="c7fa3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7fa3-111">-DefaultProfile</span></span>
<span data-ttu-id="c7fa3-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7fa3-113">-PlanName</span><span class="sxs-lookup"><span data-stu-id="c7fa3-113">-PlanName</span></span>
<span data-ttu-id="c7fa3-114">Namn på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-114">Name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c7fa3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7fa3-115">-ResourceGroupName</span></span>
<span data-ttu-id="c7fa3-116">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-116">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c7fa3-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c7fa3-117">-SubscriptionId</span></span>
<span data-ttu-id="c7fa3-118">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-118">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c7fa3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7fa3-119">CommonParameters</span></span>
<span data-ttu-id="c7fa3-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7fa3-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7fa3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7fa3-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c7fa3-122">INPUTS</span></span>

## <span data-ttu-id="c7fa3-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c7fa3-123">OUTPUTS</span></span>

### <span data-ttu-id="c7fa3-124">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. Api20151101. IMetricList</span><span class="sxs-lookup"><span data-stu-id="c7fa3-124">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMetricList</span></span>

<span data-ttu-id="c7fa3-125">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c7fa3-125">ALIASES</span></span>

## <span data-ttu-id="c7fa3-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c7fa3-126">NOTES</span></span>

## <span data-ttu-id="c7fa3-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c7fa3-127">RELATED LINKS</span></span>

