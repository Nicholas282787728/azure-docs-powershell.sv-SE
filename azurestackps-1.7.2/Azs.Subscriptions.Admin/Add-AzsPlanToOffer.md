---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e501feeea3509725b53c85007934c8e682de48a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920894"
---
# <span data-ttu-id="6b7f1-101">Add-AzsPlanToOffer</span><span class="sxs-lookup"><span data-stu-id="6b7f1-101">Add-AzsPlanToOffer</span></span>

## <span data-ttu-id="6b7f1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6b7f1-102">SYNOPSIS</span></span>
<span data-ttu-id="6b7f1-103">Länkar ett abonnemang till ett bud.</span><span class="sxs-lookup"><span data-stu-id="6b7f1-103">Links a plan to an offer.</span></span>

## <span data-ttu-id="6b7f1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6b7f1-104">SYNTAX</span></span>

```
Add-AzsPlanToOffer [-PlanName] <String> [-OfferName] <String> [-ResourceGroupName] <String>
 [[-PlanLinkType] <String>] [[-MaxAcquisitionCount] <Int64>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b7f1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6b7f1-105">DESCRIPTION</span></span>
<span data-ttu-id="6b7f1-106">Länkar ett abonnemang till ett bud.</span><span class="sxs-lookup"><span data-stu-id="6b7f1-106">Links a plan to an offer.</span></span>

## <span data-ttu-id="6b7f1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6b7f1-107">EXAMPLES</span></span>

### <span data-ttu-id="6b7f1-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6b7f1-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsPlanToOffer -PlanLinkType Addon -Offer offer1 -PlanName plan1 -ResourceGroupName rg1 -MaxAcquisitionCount 2
```

## <span data-ttu-id="6b7f1-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6b7f1-109">PARAMETERS</span></span>

### <span data-ttu-id="6b7f1-110">-Force</span><span class="sxs-lookup"><span data-stu-id="6b7f1-110">-Force</span></span>
<span data-ttu-id="6b7f1-111">Flagga för att ta bort objektet utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="6b7f1-111">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="6b7f1-112">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="6b7f1-112">-MaxAcquisitionCount</span></span>
<span data-ttu-id="6b7f1-113">Maximalt antal köp via abonnenter</span><span class="sxs-lookup"><span data-stu-id="6b7f1-113">The maximum acquisition count by subscribers</span></span>

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

### <span data-ttu-id="6b7f1-114">-OfferName</span><span class="sxs-lookup"><span data-stu-id="6b7f1-114">-OfferName</span></span>
<span data-ttu-id="6b7f1-115">Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="6b7f1-115">Name of an offer.</span></span>

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

### <span data-ttu-id="6b7f1-116">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="6b7f1-116">-PlanLinkType</span></span>
<span data-ttu-id="6b7f1-117">Typ av abonnemangs länk.</span><span class="sxs-lookup"><span data-stu-id="6b7f1-117">Type of the plan link.</span></span>

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

### <span data-ttu-id="6b7f1-118">-PlanName</span><span class="sxs-lookup"><span data-stu-id="6b7f1-118">-PlanName</span></span>
<span data-ttu-id="6b7f1-119">Namn på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="6b7f1-119">Name of the plan.</span></span>

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

### <span data-ttu-id="6b7f1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b7f1-120">-ResourceGroupName</span></span>
<span data-ttu-id="6b7f1-121">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="6b7f1-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="6b7f1-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6b7f1-122">-Confirm</span></span>
<span data-ttu-id="6b7f1-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6b7f1-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b7f1-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b7f1-124">-WhatIf</span></span>
<span data-ttu-id="6b7f1-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6b7f1-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b7f1-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6b7f1-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b7f1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b7f1-127">CommonParameters</span></span>
<span data-ttu-id="6b7f1-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b7f1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b7f1-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b7f1-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b7f1-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6b7f1-130">INPUTS</span></span>

## <span data-ttu-id="6b7f1-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6b7f1-131">OUTPUTS</span></span>

## <span data-ttu-id="6b7f1-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6b7f1-132">NOTES</span></span>

## <span data-ttu-id="6b7f1-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6b7f1-133">RELATED LINKS</span></span>
