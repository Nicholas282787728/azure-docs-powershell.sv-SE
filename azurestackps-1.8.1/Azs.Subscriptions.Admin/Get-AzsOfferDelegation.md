---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c1ab041d888a43f498e694be9bc2e103422177f7
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921673"
---
# <span data-ttu-id="45d6b-101">Get-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="45d6b-101">Get-AzsOfferDelegation</span></span>

## <span data-ttu-id="45d6b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="45d6b-102">SYNOPSIS</span></span>
<span data-ttu-id="45d6b-103">Hämta listan med ombud.</span><span class="sxs-lookup"><span data-stu-id="45d6b-103">Get the list of delegated offers.</span></span>

## <span data-ttu-id="45d6b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="45d6b-104">SYNTAX</span></span>

### <span data-ttu-id="45d6b-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="45d6b-105">List (Default)</span></span>
```
Get-AzsOfferDelegation -OfferName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="45d6b-106">Lära</span><span class="sxs-lookup"><span data-stu-id="45d6b-106">Get</span></span>
```
Get-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="45d6b-107">ID</span><span class="sxs-lookup"><span data-stu-id="45d6b-107">ResourceId</span></span>
```
Get-AzsOfferDelegation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="45d6b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="45d6b-108">DESCRIPTION</span></span>
<span data-ttu-id="45d6b-109">Hämta listan med ombud.</span><span class="sxs-lookup"><span data-stu-id="45d6b-109">Get the list of delegated offers.</span></span>

## <span data-ttu-id="45d6b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="45d6b-110">EXAMPLES</span></span>

### <span data-ttu-id="45d6b-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="45d6b-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1
```

<span data-ttu-id="45d6b-112">Hämta listan med ombud.</span><span class="sxs-lookup"><span data-stu-id="45d6b-112">Get the list of delegated offers.</span></span>

## <span data-ttu-id="45d6b-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="45d6b-113">PARAMETERS</span></span>

### <span data-ttu-id="45d6b-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="45d6b-114">-Name</span></span>
<span data-ttu-id="45d6b-115">Namn på en ombuds delegering.</span><span class="sxs-lookup"><span data-stu-id="45d6b-115">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="45d6b-116">-OfferName</span><span class="sxs-lookup"><span data-stu-id="45d6b-116">-OfferName</span></span>
<span data-ttu-id="45d6b-117">Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="45d6b-117">Name of an offer.</span></span>

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

### <span data-ttu-id="45d6b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45d6b-118">-ResourceGroupName</span></span>
<span data-ttu-id="45d6b-119">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="45d6b-119">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="45d6b-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45d6b-120">-ResourceId</span></span>
<span data-ttu-id="45d6b-121">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="45d6b-121">The resource id.</span></span>

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

### <span data-ttu-id="45d6b-122">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="45d6b-122">-Skip</span></span>
<span data-ttu-id="45d6b-123">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="45d6b-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="45d6b-124">-Överst</span><span class="sxs-lookup"><span data-stu-id="45d6b-124">-Top</span></span>
<span data-ttu-id="45d6b-125">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="45d6b-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="45d6b-126">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="45d6b-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="45d6b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45d6b-127">CommonParameters</span></span>
<span data-ttu-id="45d6b-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45d6b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45d6b-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45d6b-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45d6b-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="45d6b-130">INPUTS</span></span>

## <span data-ttu-id="45d6b-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="45d6b-131">OUTPUTS</span></span>

### <span data-ttu-id="45d6b-132">Microsoft. AzureStack. Management. abonnemang. admin. Models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="45d6b-132">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="45d6b-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="45d6b-133">NOTES</span></span>

## <span data-ttu-id="45d6b-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="45d6b-134">RELATED LINKS</span></span>

