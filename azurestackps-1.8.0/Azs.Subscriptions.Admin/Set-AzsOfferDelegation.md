---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1256fa41d7accc175e79bb531c62f76ace6482d8
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921309"
---
# <span data-ttu-id="b1a0a-101">Set-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="b1a0a-101">Set-AzsOfferDelegation</span></span>

## <span data-ttu-id="b1a0a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b1a0a-102">SYNOPSIS</span></span>
<span data-ttu-id="b1a0a-103">Uppdaterar alternativet för att tillhandahålla offerter.</span><span class="sxs-lookup"><span data-stu-id="b1a0a-103">Updates the offer delegation.</span></span>

## <span data-ttu-id="b1a0a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b1a0a-104">SYNTAX</span></span>

### <span data-ttu-id="b1a0a-105">Uppdatering (standard)</span><span class="sxs-lookup"><span data-stu-id="b1a0a-105">Update (Default)</span></span>
```
Set-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1a0a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b1a0a-106">InputObject</span></span>
```
Set-AzsOfferDelegation [-SubscriptionId <String>] [-Location <String>] -InputObject <OfferDelegation> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1a0a-107">ID</span><span class="sxs-lookup"><span data-stu-id="b1a0a-107">ResourceId</span></span>
```
Set-AzsOfferDelegation [-SubscriptionId <String>] -ResourceId <String> [-Location <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1a0a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b1a0a-108">DESCRIPTION</span></span>
<span data-ttu-id="b1a0a-109">Uppdaterar alternativet för att tillhandahålla offerter.</span><span class="sxs-lookup"><span data-stu-id="b1a0a-109">Updates the offer delegation.</span></span>

## <span data-ttu-id="b1a0a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b1a0a-110">EXAMPLES</span></span>

### <span data-ttu-id="b1a0a-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b1a0a-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsOfferDelegation -Offer offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946" -Location "local"
```

<span data-ttu-id="b1a0a-112">Uppdaterar alternativet för att tillhandahålla offerter.</span><span class="sxs-lookup"><span data-stu-id="b1a0a-112">Updates the offer delegation.</span></span>

## <span data-ttu-id="b1a0a-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b1a0a-113">PARAMETERS</span></span>

### <span data-ttu-id="b1a0a-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1a0a-114">-InputObject</span></span>
<span data-ttu-id="b1a0a-115">Indatavärdet av typen Microsoft. AzureStack. Management. abonnemang. admin. Models. OfferDelegation.</span><span class="sxs-lookup"><span data-stu-id="b1a0a-115">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation.</span></span>

```yaml
Type: OfferDelegation
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1a0a-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="b1a0a-116">-Location</span></span>
<span data-ttu-id="b1a0a-117">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="b1a0a-117">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1a0a-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="b1a0a-118">-Name</span></span>
<span data-ttu-id="b1a0a-119">Namn på en ombuds delegering.</span><span class="sxs-lookup"><span data-stu-id="b1a0a-119">Name of a offer delegation.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1a0a-120">-OfferName</span><span class="sxs-lookup"><span data-stu-id="b1a0a-120">-OfferName</span></span>
<span data-ttu-id="b1a0a-121">Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="b1a0a-121">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1a0a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1a0a-122">-ResourceGroupName</span></span>
<span data-ttu-id="b1a0a-123">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="b1a0a-123">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1a0a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1a0a-124">-ResourceId</span></span>
<span data-ttu-id="b1a0a-125">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="b1a0a-125">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1a0a-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b1a0a-126">-SubscriptionId</span></span>
<span data-ttu-id="b1a0a-127">ID för det abonnemang som tar emot det delegerade erbjudandet.</span><span class="sxs-lookup"><span data-stu-id="b1a0a-127">Identifier of the subscription receiving the delegated offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1a0a-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b1a0a-128">-Confirm</span></span>
<span data-ttu-id="b1a0a-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b1a0a-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1a0a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1a0a-130">-WhatIf</span></span>
<span data-ttu-id="b1a0a-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b1a0a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1a0a-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b1a0a-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1a0a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1a0a-133">CommonParameters</span></span>
<span data-ttu-id="b1a0a-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1a0a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1a0a-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1a0a-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1a0a-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b1a0a-136">INPUTS</span></span>

## <span data-ttu-id="b1a0a-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b1a0a-137">OUTPUTS</span></span>

### <span data-ttu-id="b1a0a-138">Microsoft. AzureStack. Management. abonnemang. admin. Models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="b1a0a-138">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="b1a0a-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b1a0a-139">NOTES</span></span>

## <span data-ttu-id="b1a0a-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b1a0a-140">RELATED LINKS</span></span>

