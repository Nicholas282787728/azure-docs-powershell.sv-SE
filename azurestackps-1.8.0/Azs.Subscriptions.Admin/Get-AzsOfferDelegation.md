---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c1ab041d888a43f498e694be9bc2e103422177f7
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921511"
---
# <span data-ttu-id="5a104-101">Get-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="5a104-101">Get-AzsOfferDelegation</span></span>

## <span data-ttu-id="5a104-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5a104-102">SYNOPSIS</span></span>
<span data-ttu-id="5a104-103">Hämta listan med ombud.</span><span class="sxs-lookup"><span data-stu-id="5a104-103">Get the list of delegated offers.</span></span>

## <span data-ttu-id="5a104-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5a104-104">SYNTAX</span></span>

### <span data-ttu-id="5a104-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="5a104-105">List (Default)</span></span>
```
Get-AzsOfferDelegation -OfferName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="5a104-106">Lära</span><span class="sxs-lookup"><span data-stu-id="5a104-106">Get</span></span>
```
Get-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="5a104-107">ID</span><span class="sxs-lookup"><span data-stu-id="5a104-107">ResourceId</span></span>
```
Get-AzsOfferDelegation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="5a104-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5a104-108">DESCRIPTION</span></span>
<span data-ttu-id="5a104-109">Hämta listan med ombud.</span><span class="sxs-lookup"><span data-stu-id="5a104-109">Get the list of delegated offers.</span></span>

## <span data-ttu-id="5a104-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5a104-110">EXAMPLES</span></span>

### <span data-ttu-id="5a104-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5a104-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1
```

<span data-ttu-id="5a104-112">Hämta listan med ombud.</span><span class="sxs-lookup"><span data-stu-id="5a104-112">Get the list of delegated offers.</span></span>

## <span data-ttu-id="5a104-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5a104-113">PARAMETERS</span></span>

### <span data-ttu-id="5a104-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="5a104-114">-Name</span></span>
<span data-ttu-id="5a104-115">Namn på en ombuds delegering.</span><span class="sxs-lookup"><span data-stu-id="5a104-115">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="5a104-116">-OfferName</span><span class="sxs-lookup"><span data-stu-id="5a104-116">-OfferName</span></span>
<span data-ttu-id="5a104-117">Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="5a104-117">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a104-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a104-118">-ResourceGroupName</span></span>
<span data-ttu-id="5a104-119">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="5a104-119">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a104-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a104-120">-ResourceId</span></span>
<span data-ttu-id="5a104-121">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="5a104-121">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a104-122">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="5a104-122">-Skip</span></span>
<span data-ttu-id="5a104-123">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="5a104-123">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a104-124">-Överst</span><span class="sxs-lookup"><span data-stu-id="5a104-124">-Top</span></span>
<span data-ttu-id="5a104-125">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="5a104-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="5a104-126">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="5a104-126">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a104-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a104-127">CommonParameters</span></span>
<span data-ttu-id="5a104-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a104-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a104-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a104-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a104-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5a104-130">INPUTS</span></span>

## <span data-ttu-id="5a104-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5a104-131">OUTPUTS</span></span>

### <span data-ttu-id="5a104-132">Microsoft. AzureStack. Management. abonnemang. admin. Models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="5a104-132">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="5a104-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5a104-133">NOTES</span></span>

## <span data-ttu-id="5a104-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5a104-134">RELATED LINKS</span></span>

