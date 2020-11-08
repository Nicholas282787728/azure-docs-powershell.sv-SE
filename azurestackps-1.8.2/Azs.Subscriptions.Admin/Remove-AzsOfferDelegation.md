---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e9fc37b5f99a9ad38e92ce1efc730718882b533d
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94099976"
---
# <span data-ttu-id="82c64-101">Remove-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="82c64-101">Remove-AzsOfferDelegation</span></span>

## <span data-ttu-id="82c64-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="82c64-102">SYNOPSIS</span></span>
<span data-ttu-id="82c64-103">Tar bort alternativet för att ge offerter</span><span class="sxs-lookup"><span data-stu-id="82c64-103">Removes the offer delegation</span></span>

## <span data-ttu-id="82c64-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="82c64-104">SYNTAX</span></span>

### <span data-ttu-id="82c64-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="82c64-105">Delete (Default)</span></span>
```
Remove-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82c64-106">ID</span><span class="sxs-lookup"><span data-stu-id="82c64-106">ResourceId</span></span>
```
Remove-AzsOfferDelegation -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82c64-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="82c64-107">DESCRIPTION</span></span>
<span data-ttu-id="82c64-108">Tar bort alternativet för att ge offerter</span><span class="sxs-lookup"><span data-stu-id="82c64-108">Removes the offer delegation</span></span>

## <span data-ttu-id="82c64-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="82c64-109">EXAMPLES</span></span>

### <span data-ttu-id="82c64-110">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="82c64-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegation1
```

<span data-ttu-id="82c64-111">Tar bort alternativet för att ge offerter</span><span class="sxs-lookup"><span data-stu-id="82c64-111">Removes the offer delegation</span></span>

## <span data-ttu-id="82c64-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="82c64-112">PARAMETERS</span></span>

### <span data-ttu-id="82c64-113">-Force</span><span class="sxs-lookup"><span data-stu-id="82c64-113">-Force</span></span>
<span data-ttu-id="82c64-114">Flagga för att ta bort objektet utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="82c64-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="82c64-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="82c64-115">-Name</span></span>
<span data-ttu-id="82c64-116">Namn på en ombuds delegering.</span><span class="sxs-lookup"><span data-stu-id="82c64-116">Name of a offer delegation.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82c64-117">-OfferName</span><span class="sxs-lookup"><span data-stu-id="82c64-117">-OfferName</span></span>
<span data-ttu-id="82c64-118">Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="82c64-118">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82c64-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82c64-119">-ResourceGroupName</span></span>
<span data-ttu-id="82c64-120">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="82c64-120">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82c64-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82c64-121">-ResourceId</span></span>
<span data-ttu-id="82c64-122">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="82c64-122">The resource id.</span></span>

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

### <span data-ttu-id="82c64-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="82c64-123">-Confirm</span></span>
<span data-ttu-id="82c64-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="82c64-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82c64-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82c64-125">-WhatIf</span></span>
<span data-ttu-id="82c64-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="82c64-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82c64-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="82c64-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82c64-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82c64-128">CommonParameters</span></span>
<span data-ttu-id="82c64-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82c64-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82c64-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82c64-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82c64-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="82c64-131">INPUTS</span></span>

## <span data-ttu-id="82c64-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="82c64-132">OUTPUTS</span></span>

## <span data-ttu-id="82c64-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="82c64-133">NOTES</span></span>

## <span data-ttu-id="82c64-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="82c64-134">RELATED LINKS</span></span>

