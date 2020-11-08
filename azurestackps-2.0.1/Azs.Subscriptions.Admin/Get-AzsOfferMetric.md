---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsoffermetric
schema: 2.0.0
ms.openlocfilehash: 515cf3d9c26c9ca4ed59178e49854e23edfea84c
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94093051"
---
# <span data-ttu-id="10e4f-101">Get-AzsOfferMetric</span><span class="sxs-lookup"><span data-stu-id="10e4f-101">Get-AzsOfferMetric</span></span>

## <span data-ttu-id="10e4f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="10e4f-102">SYNOPSIS</span></span>
<span data-ttu-id="10e4f-103">Skaffa Mät värden.</span><span class="sxs-lookup"><span data-stu-id="10e4f-103">Get the offer metrics.</span></span>

## <span data-ttu-id="10e4f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="10e4f-104">SYNTAX</span></span>

```
Get-AzsOfferMetric -OfferName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="10e4f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="10e4f-105">DESCRIPTION</span></span>
<span data-ttu-id="10e4f-106">Skaffa Mät värden.</span><span class="sxs-lookup"><span data-stu-id="10e4f-106">Get the offer metrics.</span></span>

## <span data-ttu-id="10e4f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="10e4f-107">EXAMPLES</span></span>

### <span data-ttu-id="10e4f-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="10e4f-108">Example 1</span></span>
```powershell
PS C:\> Get-AzsOfferMetric -OfferName "testoffer" -ResourceGroupName "testrg"

EndTime               MetricUnit StartTime            TimeGrain
-------               ---------- ---------            ---------
3/13/2020 12:04:33 AM Count      3/6/2020 12:00:00 AM P1D      
3/13/2020 12:04:33 AM Count      3/6/2020 12:00:00 AM P1D
```

<span data-ttu-id="10e4f-109">Skaffa Mät värden.</span><span class="sxs-lookup"><span data-stu-id="10e4f-109">Get the offer metrics.</span></span>

## <span data-ttu-id="10e4f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="10e4f-110">PARAMETERS</span></span>

### <span data-ttu-id="10e4f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10e4f-111">-DefaultProfile</span></span>
<span data-ttu-id="10e4f-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="10e4f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10e4f-113">-OfferName</span><span class="sxs-lookup"><span data-stu-id="10e4f-113">-OfferName</span></span>
<span data-ttu-id="10e4f-114">Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="10e4f-114">Name of an offer.</span></span>

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

### <span data-ttu-id="10e4f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10e4f-115">-ResourceGroupName</span></span>
<span data-ttu-id="10e4f-116">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="10e4f-116">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="10e4f-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="10e4f-117">-SubscriptionId</span></span>
<span data-ttu-id="10e4f-118">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="10e4f-118">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="10e4f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10e4f-119">CommonParameters</span></span>
<span data-ttu-id="10e4f-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10e4f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10e4f-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="10e4f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10e4f-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="10e4f-122">INPUTS</span></span>

## <span data-ttu-id="10e4f-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="10e4f-123">OUTPUTS</span></span>

### <span data-ttu-id="10e4f-124">Microsoft. Azure. PowerShell. cmdletar. SubscriptionsAdmin. Models. Api20151101. IMetricList</span><span class="sxs-lookup"><span data-stu-id="10e4f-124">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMetricList</span></span>

<span data-ttu-id="10e4f-125">ALIAS</span><span class="sxs-lookup"><span data-stu-id="10e4f-125">ALIASES</span></span>

## <span data-ttu-id="10e4f-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="10e4f-126">NOTES</span></span>

## <span data-ttu-id="10e4f-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="10e4f-127">RELATED LINKS</span></span>
