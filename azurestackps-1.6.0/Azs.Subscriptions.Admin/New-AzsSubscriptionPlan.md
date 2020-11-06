---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: aee9eab2ce04c1b9454fcf133edc290e887caf50
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571448"
---
# <span data-ttu-id="8a356-101">New-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="8a356-101">New-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="8a356-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8a356-102">SYNOPSIS</span></span>
<span data-ttu-id="8a356-103">Skapar en abonnemangs plan.</span><span class="sxs-lookup"><span data-stu-id="8a356-103">Creates a subscription plan.</span></span>

## <span data-ttu-id="8a356-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8a356-104">SYNTAX</span></span>

```
New-AzsSubscriptionPlan [[-AcquisitionId] <Guid>] [-PlanId] <String> [-TargetSubscriptionId] <Guid> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a356-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8a356-105">DESCRIPTION</span></span>
<span data-ttu-id="8a356-106">Skapar en abonnemangs plan.</span><span class="sxs-lookup"><span data-stu-id="8a356-106">Creates a subscription plan.</span></span>

## <span data-ttu-id="8a356-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8a356-107">EXAMPLES</span></span>

### <span data-ttu-id="8a356-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8a356-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsSubscriptionPlan -PlanId "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/plans/plan1" -AcquisitionId $([Guid]::NewGuid()) -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="8a356-109">Skapa en abonnemangs plan.</span><span class="sxs-lookup"><span data-stu-id="8a356-109">Create an subscription plan.</span></span>

## <span data-ttu-id="8a356-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8a356-110">PARAMETERS</span></span>

### <span data-ttu-id="8a356-111">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="8a356-111">-AcquisitionId</span></span>
<span data-ttu-id="8a356-112">Anskaffnings-ID.</span><span class="sxs-lookup"><span data-stu-id="8a356-112">Acquisition identifier.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: $([Guid]::NewGuid())
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a356-113">-PlanId</span><span class="sxs-lookup"><span data-stu-id="8a356-113">-PlanId</span></span>
<span data-ttu-id="8a356-114">Plan identifierare i kontexten för klient organisations prenumeration.</span><span class="sxs-lookup"><span data-stu-id="8a356-114">Plan identifier in the tenant subscription context.</span></span>

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

### <span data-ttu-id="8a356-115">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8a356-115">-TargetSubscriptionId</span></span>
<span data-ttu-id="8a356-116">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="8a356-116">The target subscription ID.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a356-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8a356-117">-Confirm</span></span>
<span data-ttu-id="8a356-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8a356-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a356-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a356-119">-WhatIf</span></span>
<span data-ttu-id="8a356-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8a356-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a356-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8a356-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a356-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a356-122">CommonParameters</span></span>
<span data-ttu-id="8a356-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a356-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a356-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a356-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a356-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8a356-125">INPUTS</span></span>

## <span data-ttu-id="8a356-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8a356-126">OUTPUTS</span></span>

### <span data-ttu-id="8a356-127">Microsoft. AzureStack. Management. abonnemang. admin. Models. PlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="8a356-127">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.PlanAcquisition</span></span>

## <span data-ttu-id="8a356-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8a356-128">NOTES</span></span>

## <span data-ttu-id="8a356-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8a356-129">RELATED LINKS</span></span>

