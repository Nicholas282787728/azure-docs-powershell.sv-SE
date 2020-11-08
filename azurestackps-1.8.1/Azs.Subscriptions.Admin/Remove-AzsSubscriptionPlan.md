---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b2f5117224318eae53b8b11f4af58c736ac800b
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921613"
---
# <span data-ttu-id="868d4-101">Remove-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="868d4-101">Remove-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="868d4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="868d4-102">SYNOPSIS</span></span>
<span data-ttu-id="868d4-103">Tar bort en abonnemangs plan.</span><span class="sxs-lookup"><span data-stu-id="868d4-103">Deletes a subscription plan.</span></span>

## <span data-ttu-id="868d4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="868d4-104">SYNTAX</span></span>

### <span data-ttu-id="868d4-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="868d4-105">Delete (Default)</span></span>
```
Remove-AzsSubscriptionPlan -AcquisitionId <Guid> -TargetSubscriptionId <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="868d4-106">ID</span><span class="sxs-lookup"><span data-stu-id="868d4-106">ResourceId</span></span>
```
Remove-AzsSubscriptionPlan -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="868d4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="868d4-107">DESCRIPTION</span></span>
<span data-ttu-id="868d4-108">Tar bort en abonnemangs plan.</span><span class="sxs-lookup"><span data-stu-id="868d4-108">Deletes a subscription plan.</span></span>

## <span data-ttu-id="868d4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="868d4-109">EXAMPLES</span></span>

### <span data-ttu-id="868d4-110">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="868d4-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsSubscriptionPlan -AcquisitionId $([Guid]::NewGuid()) -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="868d4-111">Ta bort en abonnemangs plan.</span><span class="sxs-lookup"><span data-stu-id="868d4-111">Delete a subscription plan.</span></span>

## <span data-ttu-id="868d4-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="868d4-112">PARAMETERS</span></span>

### <span data-ttu-id="868d4-113">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="868d4-113">-AcquisitionId</span></span>
<span data-ttu-id="868d4-114">Abonnemangets anskaffnings identifierare</span><span class="sxs-lookup"><span data-stu-id="868d4-114">The plan acquisition Identifier</span></span>

```yaml
Type: Guid
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="868d4-115">-Force</span><span class="sxs-lookup"><span data-stu-id="868d4-115">-Force</span></span>
<span data-ttu-id="868d4-116">Flagga för att ta bort objektet utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="868d4-116">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="868d4-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="868d4-117">-ResourceId</span></span>
<span data-ttu-id="868d4-118">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="868d4-118">The resource id.</span></span>

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

### <span data-ttu-id="868d4-119">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="868d4-119">-TargetSubscriptionId</span></span>
<span data-ttu-id="868d4-120">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="868d4-120">The target subscription ID.</span></span>

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

### <span data-ttu-id="868d4-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="868d4-121">-Confirm</span></span>
<span data-ttu-id="868d4-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="868d4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="868d4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="868d4-123">-WhatIf</span></span>
<span data-ttu-id="868d4-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="868d4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="868d4-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="868d4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="868d4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="868d4-126">CommonParameters</span></span>
<span data-ttu-id="868d4-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="868d4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="868d4-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="868d4-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="868d4-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="868d4-129">INPUTS</span></span>

## <span data-ttu-id="868d4-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="868d4-130">OUTPUTS</span></span>

## <span data-ttu-id="868d4-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="868d4-131">NOTES</span></span>

## <span data-ttu-id="868d4-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="868d4-132">RELATED LINKS</span></span>
