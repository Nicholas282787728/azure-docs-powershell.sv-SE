---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66e8e58b84c0ea1ca0e71999dad56bcf464d6a0f
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100240"
---
# <span data-ttu-id="5ec7e-101">Get-AzsDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="5ec7e-101">Get-AzsDelegatedProviderOffer</span></span>

## <span data-ttu-id="5ec7e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5ec7e-102">SYNOPSIS</span></span>
<span data-ttu-id="5ec7e-103">Hämta listan med erbjudanden för den angivna delegerade providern.</span><span class="sxs-lookup"><span data-stu-id="5ec7e-103">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="5ec7e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5ec7e-104">SYNTAX</span></span>

### <span data-ttu-id="5ec7e-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="5ec7e-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="5ec7e-106">Lära</span><span class="sxs-lookup"><span data-stu-id="5ec7e-106">Get</span></span>
```
Get-AzsDelegatedProviderOffer -OfferName <String> -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="5ec7e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5ec7e-107">DESCRIPTION</span></span>
<span data-ttu-id="5ec7e-108">Hämta listan med erbjudanden för den angivna delegerade providern.</span><span class="sxs-lookup"><span data-stu-id="5ec7e-108">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="5ec7e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5ec7e-109">EXAMPLES</span></span>

### <span data-ttu-id="5ec7e-110">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="5ec7e-110">EXAMPLE 1</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId 4b763321-23f5-4a45-a44d-9ccfdd705a3d | fl
```

<span data-ttu-id="5ec7e-111">Hämta listan med erbjudanden för den angivna delegerade providern.</span><span class="sxs-lookup"><span data-stu-id="5ec7e-111">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="5ec7e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5ec7e-112">PARAMETERS</span></span>

### <span data-ttu-id="5ec7e-113">-OfferName</span><span class="sxs-lookup"><span data-stu-id="5ec7e-113">-OfferName</span></span>
<span data-ttu-id="5ec7e-114">Namn på offerter.</span><span class="sxs-lookup"><span data-stu-id="5ec7e-114">Name of the offer.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ec7e-115">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="5ec7e-115">-DelegatedProviderId</span></span>
<span data-ttu-id="5ec7e-116">ID för den delegerade providern.</span><span class="sxs-lookup"><span data-stu-id="5ec7e-116">Id of the delegated provider.</span></span>

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

### <span data-ttu-id="5ec7e-117">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="5ec7e-117">-Skip</span></span>
<span data-ttu-id="5ec7e-118">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="5ec7e-118">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="5ec7e-119">-Överst</span><span class="sxs-lookup"><span data-stu-id="5ec7e-119">-Top</span></span>
<span data-ttu-id="5ec7e-120">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="5ec7e-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="5ec7e-121">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="5ec7e-121">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="5ec7e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ec7e-122">CommonParameters</span></span>
<span data-ttu-id="5ec7e-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ec7e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ec7e-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ec7e-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ec7e-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5ec7e-125">INPUTS</span></span>

## <span data-ttu-id="5ec7e-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5ec7e-126">OUTPUTS</span></span>

### <span data-ttu-id="5ec7e-127">Microsoft. AzureStack. Management. Subscription. Models. erbjudande</span><span class="sxs-lookup"><span data-stu-id="5ec7e-127">Microsoft.AzureStack.Management.Subscription.Models.Offer</span></span>

## <span data-ttu-id="5ec7e-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5ec7e-128">NOTES</span></span>

## <span data-ttu-id="5ec7e-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5ec7e-129">RELATED LINKS</span></span>
