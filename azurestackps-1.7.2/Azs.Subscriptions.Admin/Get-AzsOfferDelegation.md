---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6c58e8dedf4f55a9e1fb6451bf7f774b766b6d71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921231"
---
# <span data-ttu-id="569b9-101">Get-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="569b9-101">Get-AzsOfferDelegation</span></span>

## <span data-ttu-id="569b9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="569b9-102">SYNOPSIS</span></span>
<span data-ttu-id="569b9-103">Hämta listan med ombud.</span><span class="sxs-lookup"><span data-stu-id="569b9-103">Get the list of delegated offers.</span></span>

## <span data-ttu-id="569b9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="569b9-104">SYNTAX</span></span>

### <span data-ttu-id="569b9-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="569b9-105">List (Default)</span></span>
```
Get-AzsOfferDelegation -OfferName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="569b9-106">Lära</span><span class="sxs-lookup"><span data-stu-id="569b9-106">Get</span></span>
```
Get-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="569b9-107">ID</span><span class="sxs-lookup"><span data-stu-id="569b9-107">ResourceId</span></span>
```
Get-AzsOfferDelegation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="569b9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="569b9-108">DESCRIPTION</span></span>
<span data-ttu-id="569b9-109">Hämta listan med ombud.</span><span class="sxs-lookup"><span data-stu-id="569b9-109">Get the list of delegated offers.</span></span>

## <span data-ttu-id="569b9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="569b9-110">EXAMPLES</span></span>

### <span data-ttu-id="569b9-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="569b9-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1
```

<span data-ttu-id="569b9-112">Hämta listan med ombud.</span><span class="sxs-lookup"><span data-stu-id="569b9-112">Get the list of delegated offers.</span></span>

## <span data-ttu-id="569b9-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="569b9-113">PARAMETERS</span></span>

### <span data-ttu-id="569b9-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="569b9-114">-Name</span></span>
<span data-ttu-id="569b9-115">Namn på en ombuds delegering.</span><span class="sxs-lookup"><span data-stu-id="569b9-115">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="569b9-116">-OfferName</span><span class="sxs-lookup"><span data-stu-id="569b9-116">-OfferName</span></span>
<span data-ttu-id="569b9-117">Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="569b9-117">Name of an offer.</span></span>

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

### <span data-ttu-id="569b9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="569b9-118">-ResourceGroupName</span></span>
<span data-ttu-id="569b9-119">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="569b9-119">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="569b9-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="569b9-120">-ResourceId</span></span>
<span data-ttu-id="569b9-121">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="569b9-121">The resource id.</span></span>

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

### <span data-ttu-id="569b9-122">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="569b9-122">-Skip</span></span>
<span data-ttu-id="569b9-123">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="569b9-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="569b9-124">-Överst</span><span class="sxs-lookup"><span data-stu-id="569b9-124">-Top</span></span>
<span data-ttu-id="569b9-125">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="569b9-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="569b9-126">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="569b9-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="569b9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="569b9-127">CommonParameters</span></span>
<span data-ttu-id="569b9-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="569b9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="569b9-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="569b9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="569b9-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="569b9-130">INPUTS</span></span>

## <span data-ttu-id="569b9-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="569b9-131">OUTPUTS</span></span>

### <span data-ttu-id="569b9-132">Microsoft. AzureStack. Management. abonnemang. admin. Models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="569b9-132">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="569b9-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="569b9-133">NOTES</span></span>

## <span data-ttu-id="569b9-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="569b9-134">RELATED LINKS</span></span>

