---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4d0dad3650338d2bba4976ce66806b714bd9e0fe
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921666"
---
# <span data-ttu-id="50c71-101">Get-AzsOfferMetric</span><span class="sxs-lookup"><span data-stu-id="50c71-101">Get-AzsOfferMetric</span></span>

## <span data-ttu-id="50c71-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="50c71-102">SYNOPSIS</span></span>
<span data-ttu-id="50c71-103">Skaffa Mät värden.</span><span class="sxs-lookup"><span data-stu-id="50c71-103">Get the offer metrics.</span></span>

## <span data-ttu-id="50c71-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="50c71-104">SYNTAX</span></span>

```
Get-AzsOfferMetric [-OfferName] <String> [-ResourceGroupName] <String> [<CommonParameters>]
```

## <span data-ttu-id="50c71-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="50c71-105">DESCRIPTION</span></span>
<span data-ttu-id="50c71-106">Skaffa Mät värden.</span><span class="sxs-lookup"><span data-stu-id="50c71-106">Get the offer metrics.</span></span>

## <span data-ttu-id="50c71-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="50c71-107">EXAMPLES</span></span>

### <span data-ttu-id="50c71-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="50c71-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferMetric -ResourceGroupName rg1 -OfferName offername1
```

<span data-ttu-id="50c71-109">Skaffa Mät värden.</span><span class="sxs-lookup"><span data-stu-id="50c71-109">Get the offer metrics.</span></span>

## <span data-ttu-id="50c71-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="50c71-110">PARAMETERS</span></span>

### <span data-ttu-id="50c71-111">-OfferName</span><span class="sxs-lookup"><span data-stu-id="50c71-111">-OfferName</span></span>
<span data-ttu-id="50c71-112">Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="50c71-112">Name of an offer.</span></span>

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

### <span data-ttu-id="50c71-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50c71-113">-ResourceGroupName</span></span>
<span data-ttu-id="50c71-114">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="50c71-114">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="50c71-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50c71-115">CommonParameters</span></span>
<span data-ttu-id="50c71-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50c71-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50c71-117">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50c71-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50c71-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="50c71-118">INPUTS</span></span>

## <span data-ttu-id="50c71-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="50c71-119">OUTPUTS</span></span>

### <span data-ttu-id="50c71-120">Microsoft. AzureStack. Management. abonnemang. admin. Models. Metric</span><span class="sxs-lookup"><span data-stu-id="50c71-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Metric</span></span>

## <span data-ttu-id="50c71-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="50c71-121">NOTES</span></span>

## <span data-ttu-id="50c71-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="50c71-122">RELATED LINKS</span></span>

