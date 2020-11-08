---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5f5c0050f6a1e226f5b5513e11d70fac1844ecda
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100002"
---
# <span data-ttu-id="836d3-101">Remove-AzsPlanFromOffer</span><span class="sxs-lookup"><span data-stu-id="836d3-101">Remove-AzsPlanFromOffer</span></span>

## <span data-ttu-id="836d3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="836d3-102">SYNOPSIS</span></span>
<span data-ttu-id="836d3-103">Koppla bort en plan från ett bud.</span><span class="sxs-lookup"><span data-stu-id="836d3-103">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="836d3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="836d3-104">SYNTAX</span></span>

```
Remove-AzsPlanFromOffer -PlanName <String> -OfferName <String> -ResourceGroupName <String>
 [-PlanLinkType <String>] [-MaxAcquisitionCount <Int64>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="836d3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="836d3-105">DESCRIPTION</span></span>
<span data-ttu-id="836d3-106">Koppla bort en plan från ett bud.</span><span class="sxs-lookup"><span data-stu-id="836d3-106">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="836d3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="836d3-107">EXAMPLES</span></span>

### <span data-ttu-id="836d3-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="836d3-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlanToOffer -Offer offer1 -PlanName plan1 -ResourceGroup rg1
```

## <span data-ttu-id="836d3-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="836d3-109">PARAMETERS</span></span>

### <span data-ttu-id="836d3-110">-Force</span><span class="sxs-lookup"><span data-stu-id="836d3-110">-Force</span></span>
<span data-ttu-id="836d3-111">Flagga för att ta bort objektet utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="836d3-111">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="836d3-112">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="836d3-112">-MaxAcquisitionCount</span></span>
<span data-ttu-id="836d3-113">Maximalt antal köp via abonnenter</span><span class="sxs-lookup"><span data-stu-id="836d3-113">The maximum acquisition count by subscribers</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="836d3-114">-OfferName</span><span class="sxs-lookup"><span data-stu-id="836d3-114">-OfferName</span></span>
<span data-ttu-id="836d3-115">Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="836d3-115">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="836d3-116">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="836d3-116">-PlanLinkType</span></span>
<span data-ttu-id="836d3-117">Typ av abonnemangs länk.</span><span class="sxs-lookup"><span data-stu-id="836d3-117">Type of the plan link.</span></span>

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

### <span data-ttu-id="836d3-118">-PlanName</span><span class="sxs-lookup"><span data-stu-id="836d3-118">-PlanName</span></span>
<span data-ttu-id="836d3-119">Namn på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="836d3-119">Name of the plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="836d3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="836d3-120">-ResourceGroupName</span></span>
<span data-ttu-id="836d3-121">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="836d3-121">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="836d3-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="836d3-122">-Confirm</span></span>
<span data-ttu-id="836d3-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="836d3-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="836d3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="836d3-124">-WhatIf</span></span>
<span data-ttu-id="836d3-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="836d3-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="836d3-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="836d3-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="836d3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="836d3-127">CommonParameters</span></span>
<span data-ttu-id="836d3-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="836d3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="836d3-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="836d3-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="836d3-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="836d3-130">INPUTS</span></span>

## <span data-ttu-id="836d3-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="836d3-131">OUTPUTS</span></span>

## <span data-ttu-id="836d3-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="836d3-132">NOTES</span></span>

## <span data-ttu-id="836d3-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="836d3-133">RELATED LINKS</span></span>

