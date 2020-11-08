---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77d6a4861dbdb93dff2d5511faeceac30e3f9cf8
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94099991"
---
# <span data-ttu-id="eb138-101">Get-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="eb138-101">Get-AzsOffer</span></span>

## <span data-ttu-id="eb138-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eb138-102">SYNOPSIS</span></span>
<span data-ttu-id="eb138-103">Skaffa en lista över erbjudanden.</span><span class="sxs-lookup"><span data-stu-id="eb138-103">Get the list of public offers.</span></span>

## <span data-ttu-id="eb138-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eb138-104">SYNTAX</span></span>

```
Get-AzsOffer [[-Skip] <Int32>] [[-Top] <Int32>] [[-Provider] <String>] [<CommonParameters>]
```

## <span data-ttu-id="eb138-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eb138-105">DESCRIPTION</span></span>
<span data-ttu-id="eb138-106">Skaffa en lista över erbjudanden.</span><span class="sxs-lookup"><span data-stu-id="eb138-106">Get the list of public offers.</span></span>

## <span data-ttu-id="eb138-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eb138-107">EXAMPLES</span></span>

### <span data-ttu-id="eb138-108">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="eb138-108">EXAMPLE 1</span></span>
```
Get-AzsOffer | fl
```

<span data-ttu-id="eb138-109">Skaffa en lista över erbjudanden.</span><span class="sxs-lookup"><span data-stu-id="eb138-109">Get the list of public offers.</span></span>

## <span data-ttu-id="eb138-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eb138-110">PARAMETERS</span></span>

### <span data-ttu-id="eb138-111">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="eb138-111">-Skip</span></span>
<span data-ttu-id="eb138-112">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="eb138-112">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb138-113">-Överst</span><span class="sxs-lookup"><span data-stu-id="eb138-113">-Top</span></span>
<span data-ttu-id="eb138-114">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="eb138-114">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="eb138-115">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="eb138-115">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb138-116">-Leverantör</span><span class="sxs-lookup"><span data-stu-id="eb138-116">-Provider</span></span>
<span data-ttu-id="eb138-117">Valfri parameter för att ange den delegerade leverantörens namn.</span><span class="sxs-lookup"><span data-stu-id="eb138-117">Optional parameter to specify the delegated provider name.</span></span> <span data-ttu-id="eb138-118">Denna parameter används inte och kommer att föråldras i framtiden.</span><span class="sxs-lookup"><span data-stu-id="eb138-118">This parameter is not being used and will be deprecated in future.</span></span>

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

### <span data-ttu-id="eb138-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb138-119">CommonParameters</span></span>
<span data-ttu-id="eb138-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb138-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb138-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb138-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb138-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eb138-122">INPUTS</span></span>

## <span data-ttu-id="eb138-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eb138-123">OUTPUTS</span></span>

### <span data-ttu-id="eb138-124">Microsoft. AzureStack. Management. Subscription. Models. erbjudande</span><span class="sxs-lookup"><span data-stu-id="eb138-124">Microsoft.AzureStack.Management.Subscription.Models.Offer</span></span>

## <span data-ttu-id="eb138-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eb138-125">NOTES</span></span>

## <span data-ttu-id="eb138-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eb138-126">RELATED LINKS</span></span>
