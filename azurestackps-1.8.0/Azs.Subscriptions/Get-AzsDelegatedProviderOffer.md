---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66e8e58b84c0ea1ca0e71999dad56bcf464d6a0f
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921470"
---
# <span data-ttu-id="6e516-101">Get-AzsDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="6e516-101">Get-AzsDelegatedProviderOffer</span></span>

## <span data-ttu-id="6e516-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6e516-102">SYNOPSIS</span></span>
<span data-ttu-id="6e516-103">Hämta listan med erbjudanden för den angivna delegerade providern.</span><span class="sxs-lookup"><span data-stu-id="6e516-103">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="6e516-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6e516-104">SYNTAX</span></span>

### <span data-ttu-id="6e516-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="6e516-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="6e516-106">Lära</span><span class="sxs-lookup"><span data-stu-id="6e516-106">Get</span></span>
```
Get-AzsDelegatedProviderOffer -OfferName <String> -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="6e516-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6e516-107">DESCRIPTION</span></span>
<span data-ttu-id="6e516-108">Hämta listan med erbjudanden för den angivna delegerade providern.</span><span class="sxs-lookup"><span data-stu-id="6e516-108">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="6e516-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6e516-109">EXAMPLES</span></span>

### <span data-ttu-id="6e516-110">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="6e516-110">EXAMPLE 1</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId 4b763321-23f5-4a45-a44d-9ccfdd705a3d | fl
```

<span data-ttu-id="6e516-111">Hämta listan med erbjudanden för den angivna delegerade providern.</span><span class="sxs-lookup"><span data-stu-id="6e516-111">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="6e516-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6e516-112">PARAMETERS</span></span>

### <span data-ttu-id="6e516-113">-OfferName</span><span class="sxs-lookup"><span data-stu-id="6e516-113">-OfferName</span></span>
<span data-ttu-id="6e516-114">Namn på offerter.</span><span class="sxs-lookup"><span data-stu-id="6e516-114">Name of the offer.</span></span>

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

### <span data-ttu-id="6e516-115">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="6e516-115">-DelegatedProviderId</span></span>
<span data-ttu-id="6e516-116">ID för den delegerade providern.</span><span class="sxs-lookup"><span data-stu-id="6e516-116">Id of the delegated provider.</span></span>

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

### <span data-ttu-id="6e516-117">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="6e516-117">-Skip</span></span>
<span data-ttu-id="6e516-118">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="6e516-118">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="6e516-119">-Överst</span><span class="sxs-lookup"><span data-stu-id="6e516-119">-Top</span></span>
<span data-ttu-id="6e516-120">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="6e516-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="6e516-121">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="6e516-121">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="6e516-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e516-122">CommonParameters</span></span>
<span data-ttu-id="6e516-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e516-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e516-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e516-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e516-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6e516-125">INPUTS</span></span>

## <span data-ttu-id="6e516-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6e516-126">OUTPUTS</span></span>

### <span data-ttu-id="6e516-127">Microsoft. AzureStack. Management. Subscription. Models. erbjudande</span><span class="sxs-lookup"><span data-stu-id="6e516-127">Microsoft.AzureStack.Management.Subscription.Models.Offer</span></span>

## <span data-ttu-id="6e516-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6e516-128">NOTES</span></span>

## <span data-ttu-id="6e516-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6e516-129">RELATED LINKS</span></span>
