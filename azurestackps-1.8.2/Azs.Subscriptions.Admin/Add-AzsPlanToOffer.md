---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3e7d51bef12f0f7808aff3fda819ac614e0bb1c9
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94099843"
---
# <span data-ttu-id="08b29-101">Add-AzsPlanToOffer</span><span class="sxs-lookup"><span data-stu-id="08b29-101">Add-AzsPlanToOffer</span></span>

## <span data-ttu-id="08b29-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="08b29-102">SYNOPSIS</span></span>
<span data-ttu-id="08b29-103">Länkar ett abonnemang till ett bud.</span><span class="sxs-lookup"><span data-stu-id="08b29-103">Links a plan to an offer.</span></span>

## <span data-ttu-id="08b29-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="08b29-104">SYNTAX</span></span>

```
Add-AzsPlanToOffer [-PlanName] <String> [-OfferName] <String> [-ResourceGroupName] <String>
 [[-PlanLinkType] <String>] [[-MaxAcquisitionCount] <Int64>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08b29-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="08b29-105">DESCRIPTION</span></span>
<span data-ttu-id="08b29-106">Länkar ett abonnemang till ett bud.</span><span class="sxs-lookup"><span data-stu-id="08b29-106">Links a plan to an offer.</span></span>

## <span data-ttu-id="08b29-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="08b29-107">EXAMPLES</span></span>

### <span data-ttu-id="08b29-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="08b29-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsPlanToOffer -PlanLinkType Addon -Offer offer1 -PlanName plan1 -ResourceGroupName rg1 -MaxAcquisitionCount 2
```

## <span data-ttu-id="08b29-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="08b29-109">PARAMETERS</span></span>

### <span data-ttu-id="08b29-110">-Force</span><span class="sxs-lookup"><span data-stu-id="08b29-110">-Force</span></span>
<span data-ttu-id="08b29-111">Flagga för att ta bort objektet utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="08b29-111">Flag to remove the item without confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08b29-112">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="08b29-112">-MaxAcquisitionCount</span></span>
<span data-ttu-id="08b29-113">Maximalt antal köp via abonnenter</span><span class="sxs-lookup"><span data-stu-id="08b29-113">The maximum acquisition count by subscribers</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08b29-114">-OfferName</span><span class="sxs-lookup"><span data-stu-id="08b29-114">-OfferName</span></span>
<span data-ttu-id="08b29-115">Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="08b29-115">Name of an offer.</span></span>

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

### <span data-ttu-id="08b29-116">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="08b29-116">-PlanLinkType</span></span>
<span data-ttu-id="08b29-117">Typ av abonnemangs länk.</span><span class="sxs-lookup"><span data-stu-id="08b29-117">Type of the plan link.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08b29-118">-PlanName</span><span class="sxs-lookup"><span data-stu-id="08b29-118">-PlanName</span></span>
<span data-ttu-id="08b29-119">Namn på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="08b29-119">Name of the plan.</span></span>

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

### <span data-ttu-id="08b29-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08b29-120">-ResourceGroupName</span></span>
<span data-ttu-id="08b29-121">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="08b29-121">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08b29-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="08b29-122">-Confirm</span></span>
<span data-ttu-id="08b29-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="08b29-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08b29-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08b29-124">-WhatIf</span></span>
<span data-ttu-id="08b29-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="08b29-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08b29-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="08b29-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08b29-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08b29-127">CommonParameters</span></span>
<span data-ttu-id="08b29-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08b29-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08b29-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08b29-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08b29-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="08b29-130">INPUTS</span></span>

## <span data-ttu-id="08b29-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="08b29-131">OUTPUTS</span></span>

## <span data-ttu-id="08b29-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="08b29-132">NOTES</span></span>

## <span data-ttu-id="08b29-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="08b29-133">RELATED LINKS</span></span>

