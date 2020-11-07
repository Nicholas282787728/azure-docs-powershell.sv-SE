---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9212655ecb5f67dbf459548c48ff6d25420a8537
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754946"
---
# <span data-ttu-id="e2a42-101">Remove-AzsPlanFromOffer</span><span class="sxs-lookup"><span data-stu-id="e2a42-101">Remove-AzsPlanFromOffer</span></span>

## <span data-ttu-id="e2a42-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e2a42-102">SYNOPSIS</span></span>
<span data-ttu-id="e2a42-103">Koppla bort en plan från ett bud.</span><span class="sxs-lookup"><span data-stu-id="e2a42-103">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="e2a42-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e2a42-104">SYNTAX</span></span>

```
Remove-AzsPlanFromOffer -PlanName <String> -OfferName <String> -ResourceGroupName <String>
 [-PlanLinkType <String>] [-MaxAcquisitionCount <Int64>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2a42-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e2a42-105">DESCRIPTION</span></span>
<span data-ttu-id="e2a42-106">Koppla bort en plan från ett bud.</span><span class="sxs-lookup"><span data-stu-id="e2a42-106">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="e2a42-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e2a42-107">EXAMPLES</span></span>

### <span data-ttu-id="e2a42-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e2a42-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlanToOffer -Offer offer1 -PlanName plan1 -ResourceGroup rg1
```

## <span data-ttu-id="e2a42-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e2a42-109">PARAMETERS</span></span>

### <span data-ttu-id="e2a42-110">-Force</span><span class="sxs-lookup"><span data-stu-id="e2a42-110">-Force</span></span>
<span data-ttu-id="e2a42-111">Flagga för att ta bort objektet utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="e2a42-111">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="e2a42-112">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="e2a42-112">-MaxAcquisitionCount</span></span>
<span data-ttu-id="e2a42-113">Maximalt antal köp via abonnenter</span><span class="sxs-lookup"><span data-stu-id="e2a42-113">The maximum acquisition count by subscribers</span></span>

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

### <span data-ttu-id="e2a42-114">-OfferName</span><span class="sxs-lookup"><span data-stu-id="e2a42-114">-OfferName</span></span>
<span data-ttu-id="e2a42-115">Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="e2a42-115">Name of an offer.</span></span>

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

### <span data-ttu-id="e2a42-116">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="e2a42-116">-PlanLinkType</span></span>
<span data-ttu-id="e2a42-117">Typ av abonnemangs länk.</span><span class="sxs-lookup"><span data-stu-id="e2a42-117">Type of the plan link.</span></span>

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

### <span data-ttu-id="e2a42-118">-PlanName</span><span class="sxs-lookup"><span data-stu-id="e2a42-118">-PlanName</span></span>
<span data-ttu-id="e2a42-119">Namn på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="e2a42-119">Name of the plan.</span></span>

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

### <span data-ttu-id="e2a42-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2a42-120">-ResourceGroupName</span></span>
<span data-ttu-id="e2a42-121">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="e2a42-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="e2a42-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e2a42-122">-Confirm</span></span>
<span data-ttu-id="e2a42-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e2a42-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2a42-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2a42-124">-WhatIf</span></span>
<span data-ttu-id="e2a42-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e2a42-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2a42-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e2a42-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2a42-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2a42-127">CommonParameters</span></span>
<span data-ttu-id="e2a42-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2a42-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2a42-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2a42-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2a42-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e2a42-130">INPUTS</span></span>

## <span data-ttu-id="e2a42-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e2a42-131">OUTPUTS</span></span>

## <span data-ttu-id="e2a42-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e2a42-132">NOTES</span></span>

## <span data-ttu-id="e2a42-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e2a42-133">RELATED LINKS</span></span>

