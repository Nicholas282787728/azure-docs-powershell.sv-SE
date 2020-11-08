---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4d0dad3650338d2bba4976ce66806b714bd9e0fe
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100083"
---
# <span data-ttu-id="7272d-101">Get-AzsOfferMetric</span><span class="sxs-lookup"><span data-stu-id="7272d-101">Get-AzsOfferMetric</span></span>

## <span data-ttu-id="7272d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7272d-102">SYNOPSIS</span></span>
<span data-ttu-id="7272d-103">Skaffa Mät värden.</span><span class="sxs-lookup"><span data-stu-id="7272d-103">Get the offer metrics.</span></span>

## <span data-ttu-id="7272d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7272d-104">SYNTAX</span></span>

```
Get-AzsOfferMetric [-OfferName] <String> [-ResourceGroupName] <String> [<CommonParameters>]
```

## <span data-ttu-id="7272d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7272d-105">DESCRIPTION</span></span>
<span data-ttu-id="7272d-106">Skaffa Mät värden.</span><span class="sxs-lookup"><span data-stu-id="7272d-106">Get the offer metrics.</span></span>

## <span data-ttu-id="7272d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7272d-107">EXAMPLES</span></span>

### <span data-ttu-id="7272d-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7272d-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferMetric -ResourceGroupName rg1 -OfferName offername1
```

<span data-ttu-id="7272d-109">Skaffa Mät värden.</span><span class="sxs-lookup"><span data-stu-id="7272d-109">Get the offer metrics.</span></span>

## <span data-ttu-id="7272d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7272d-110">PARAMETERS</span></span>

### <span data-ttu-id="7272d-111">-OfferName</span><span class="sxs-lookup"><span data-stu-id="7272d-111">-OfferName</span></span>
<span data-ttu-id="7272d-112">Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="7272d-112">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7272d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7272d-113">-ResourceGroupName</span></span>
<span data-ttu-id="7272d-114">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="7272d-114">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7272d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7272d-115">CommonParameters</span></span>
<span data-ttu-id="7272d-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7272d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7272d-117">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7272d-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7272d-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7272d-118">INPUTS</span></span>

## <span data-ttu-id="7272d-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7272d-119">OUTPUTS</span></span>

### <span data-ttu-id="7272d-120">Microsoft. AzureStack. Management. abonnemang. admin. Models. Metric</span><span class="sxs-lookup"><span data-stu-id="7272d-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Metric</span></span>

## <span data-ttu-id="7272d-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7272d-121">NOTES</span></span>

## <span data-ttu-id="7272d-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7272d-122">RELATED LINKS</span></span>

