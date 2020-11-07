---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3e7d51bef12f0f7808aff3fda819ac614e0bb1c9
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921526"
---
# <span data-ttu-id="db1f0-101">Add-AzsPlanToOffer</span><span class="sxs-lookup"><span data-stu-id="db1f0-101">Add-AzsPlanToOffer</span></span>

## <span data-ttu-id="db1f0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="db1f0-102">SYNOPSIS</span></span>
<span data-ttu-id="db1f0-103">Länkar ett abonnemang till ett bud.</span><span class="sxs-lookup"><span data-stu-id="db1f0-103">Links a plan to an offer.</span></span>

## <span data-ttu-id="db1f0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="db1f0-104">SYNTAX</span></span>

```
Add-AzsPlanToOffer [-PlanName] <String> [-OfferName] <String> [-ResourceGroupName] <String>
 [[-PlanLinkType] <String>] [[-MaxAcquisitionCount] <Int64>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db1f0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="db1f0-105">DESCRIPTION</span></span>
<span data-ttu-id="db1f0-106">Länkar ett abonnemang till ett bud.</span><span class="sxs-lookup"><span data-stu-id="db1f0-106">Links a plan to an offer.</span></span>

## <span data-ttu-id="db1f0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="db1f0-107">EXAMPLES</span></span>

### <span data-ttu-id="db1f0-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="db1f0-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsPlanToOffer -PlanLinkType Addon -Offer offer1 -PlanName plan1 -ResourceGroupName rg1 -MaxAcquisitionCount 2
```

## <span data-ttu-id="db1f0-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="db1f0-109">PARAMETERS</span></span>

### <span data-ttu-id="db1f0-110">-Force</span><span class="sxs-lookup"><span data-stu-id="db1f0-110">-Force</span></span>
<span data-ttu-id="db1f0-111">Flagga för att ta bort objektet utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="db1f0-111">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="db1f0-112">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="db1f0-112">-MaxAcquisitionCount</span></span>
<span data-ttu-id="db1f0-113">Maximalt antal köp via abonnenter</span><span class="sxs-lookup"><span data-stu-id="db1f0-113">The maximum acquisition count by subscribers</span></span>

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

### <span data-ttu-id="db1f0-114">-OfferName</span><span class="sxs-lookup"><span data-stu-id="db1f0-114">-OfferName</span></span>
<span data-ttu-id="db1f0-115">Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="db1f0-115">Name of an offer.</span></span>

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

### <span data-ttu-id="db1f0-116">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="db1f0-116">-PlanLinkType</span></span>
<span data-ttu-id="db1f0-117">Typ av abonnemangs länk.</span><span class="sxs-lookup"><span data-stu-id="db1f0-117">Type of the plan link.</span></span>

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

### <span data-ttu-id="db1f0-118">-PlanName</span><span class="sxs-lookup"><span data-stu-id="db1f0-118">-PlanName</span></span>
<span data-ttu-id="db1f0-119">Namn på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="db1f0-119">Name of the plan.</span></span>

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

### <span data-ttu-id="db1f0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db1f0-120">-ResourceGroupName</span></span>
<span data-ttu-id="db1f0-121">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="db1f0-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="db1f0-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="db1f0-122">-Confirm</span></span>
<span data-ttu-id="db1f0-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="db1f0-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db1f0-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db1f0-124">-WhatIf</span></span>
<span data-ttu-id="db1f0-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="db1f0-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db1f0-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="db1f0-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db1f0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db1f0-127">CommonParameters</span></span>
<span data-ttu-id="db1f0-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db1f0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db1f0-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db1f0-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db1f0-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="db1f0-130">INPUTS</span></span>

## <span data-ttu-id="db1f0-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="db1f0-131">OUTPUTS</span></span>

## <span data-ttu-id="db1f0-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="db1f0-132">NOTES</span></span>

## <span data-ttu-id="db1f0-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="db1f0-133">RELATED LINKS</span></span>

