---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8034887f8b44bef5c3dd59f73186027af1a1e5eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571784"
---
# <span data-ttu-id="51cdf-101">Get-AzsDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="51cdf-101">Get-AzsDelegatedProviderOffer</span></span>

## <span data-ttu-id="51cdf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="51cdf-102">SYNOPSIS</span></span>
<span data-ttu-id="51cdf-103">Hämta listan med erbjudanden för den angivna delegerade providern.</span><span class="sxs-lookup"><span data-stu-id="51cdf-103">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="51cdf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="51cdf-104">SYNTAX</span></span>

### <span data-ttu-id="51cdf-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="51cdf-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="51cdf-106">Lära</span><span class="sxs-lookup"><span data-stu-id="51cdf-106">Get</span></span>
```
Get-AzsDelegatedProviderOffer -Name <String> -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="51cdf-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="51cdf-107">DESCRIPTION</span></span>
<span data-ttu-id="51cdf-108">Hämta listan med erbjudanden för den angivna delegerade providern.</span><span class="sxs-lookup"><span data-stu-id="51cdf-108">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="51cdf-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="51cdf-109">EXAMPLES</span></span>

### <span data-ttu-id="51cdf-110">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="51cdf-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId 4b763321-23f5-4a45-a44d-9ccfdd705a3d | fl
```

<span data-ttu-id="51cdf-111">Hämta listan med erbjudanden för den angivna delegerade providern.</span><span class="sxs-lookup"><span data-stu-id="51cdf-111">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="51cdf-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="51cdf-112">PARAMETERS</span></span>

### <span data-ttu-id="51cdf-113">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="51cdf-113">-DelegatedProviderId</span></span>
<span data-ttu-id="51cdf-114">ID för den delegerade providern.</span><span class="sxs-lookup"><span data-stu-id="51cdf-114">Id of the delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51cdf-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="51cdf-115">-Name</span></span>
<span data-ttu-id="51cdf-116">Namn på offerter.</span><span class="sxs-lookup"><span data-stu-id="51cdf-116">Name of the offer.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: OfferName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51cdf-117">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="51cdf-117">-Skip</span></span>
<span data-ttu-id="51cdf-118">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="51cdf-118">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51cdf-119">-Överst</span><span class="sxs-lookup"><span data-stu-id="51cdf-119">-Top</span></span>
<span data-ttu-id="51cdf-120">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="51cdf-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="51cdf-121">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="51cdf-121">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51cdf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51cdf-122">CommonParameters</span></span>
<span data-ttu-id="51cdf-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51cdf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51cdf-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51cdf-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51cdf-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="51cdf-125">INPUTS</span></span>

## <span data-ttu-id="51cdf-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="51cdf-126">OUTPUTS</span></span>

### <span data-ttu-id="51cdf-127">Microsoft. AzureStack. Management. Subscription. Models. erbjudande</span><span class="sxs-lookup"><span data-stu-id="51cdf-127">Microsoft.AzureStack.Management.Subscription.Models.Offer</span></span>

## <span data-ttu-id="51cdf-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="51cdf-128">NOTES</span></span>

## <span data-ttu-id="51cdf-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="51cdf-129">RELATED LINKS</span></span>

