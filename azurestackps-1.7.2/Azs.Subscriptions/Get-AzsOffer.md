---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 885fef88b1042fb538c4e07b62410943063cb53d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743354"
---
# <span data-ttu-id="ac0d6-101">Get-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="ac0d6-101">Get-AzsOffer</span></span>

## <span data-ttu-id="ac0d6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ac0d6-102">SYNOPSIS</span></span>
<span data-ttu-id="ac0d6-103">Skaffa en lista över erbjudanden.</span><span class="sxs-lookup"><span data-stu-id="ac0d6-103">Get the list of public offers.</span></span>

## <span data-ttu-id="ac0d6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ac0d6-104">SYNTAX</span></span>

```
Get-AzsOffer [[-Skip] <Int32>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="ac0d6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ac0d6-105">DESCRIPTION</span></span>
<span data-ttu-id="ac0d6-106">Skaffa en lista över erbjudanden.</span><span class="sxs-lookup"><span data-stu-id="ac0d6-106">Get the list of public offers.</span></span>

## <span data-ttu-id="ac0d6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ac0d6-107">EXAMPLES</span></span>

### <span data-ttu-id="ac0d6-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ac0d6-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOffer | fl
```

<span data-ttu-id="ac0d6-109">Skaffa en lista över erbjudanden.</span><span class="sxs-lookup"><span data-stu-id="ac0d6-109">Get the list of public offers.</span></span>

## <span data-ttu-id="ac0d6-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ac0d6-110">PARAMETERS</span></span>

### <span data-ttu-id="ac0d6-111">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="ac0d6-111">-Skip</span></span>
<span data-ttu-id="ac0d6-112">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="ac0d6-112">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="ac0d6-113">-Överst</span><span class="sxs-lookup"><span data-stu-id="ac0d6-113">-Top</span></span>
<span data-ttu-id="ac0d6-114">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="ac0d6-114">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="ac0d6-115">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="ac0d6-115">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="ac0d6-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac0d6-116">CommonParameters</span></span>
<span data-ttu-id="ac0d6-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac0d6-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac0d6-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac0d6-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac0d6-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ac0d6-119">INPUTS</span></span>

## <span data-ttu-id="ac0d6-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ac0d6-120">OUTPUTS</span></span>

### <span data-ttu-id="ac0d6-121">Microsoft. AzureStack. Management. Subscription. Models. erbjudande</span><span class="sxs-lookup"><span data-stu-id="ac0d6-121">Microsoft.AzureStack.Management.Subscription.Models.Offer</span></span>

## <span data-ttu-id="ac0d6-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ac0d6-122">NOTES</span></span>

## <span data-ttu-id="ac0d6-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ac0d6-123">RELATED LINKS</span></span>
