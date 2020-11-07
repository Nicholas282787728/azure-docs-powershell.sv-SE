---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3a4c99f48087dcbac17dc10da3c647525670fe90
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921649"
---
# <span data-ttu-id="9b096-101">New-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="9b096-101">New-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="9b096-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9b096-102">SYNOPSIS</span></span>
<span data-ttu-id="9b096-103">Skapar en abonnemangs plan.</span><span class="sxs-lookup"><span data-stu-id="9b096-103">Creates a subscription plan.</span></span>

## <span data-ttu-id="9b096-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9b096-104">SYNTAX</span></span>

```
New-AzsSubscriptionPlan [[-AcquisitionId] <Guid>] [-PlanId] <String> [-TargetSubscriptionId] <Guid> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b096-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9b096-105">DESCRIPTION</span></span>
<span data-ttu-id="9b096-106">Skapar en abonnemangs plan.</span><span class="sxs-lookup"><span data-stu-id="9b096-106">Creates a subscription plan.</span></span>

## <span data-ttu-id="9b096-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9b096-107">EXAMPLES</span></span>

### <span data-ttu-id="9b096-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9b096-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsSubscriptionPlan -PlanId "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/plans/plan1" -AcquisitionId $([Guid]::NewGuid()) -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="9b096-109">Skapa en abonnemangs plan.</span><span class="sxs-lookup"><span data-stu-id="9b096-109">Create an subscription plan.</span></span>

## <span data-ttu-id="9b096-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9b096-110">PARAMETERS</span></span>

### <span data-ttu-id="9b096-111">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="9b096-111">-AcquisitionId</span></span>
<span data-ttu-id="9b096-112">Anskaffnings-ID.</span><span class="sxs-lookup"><span data-stu-id="9b096-112">Acquisition identifier.</span></span>

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

### <span data-ttu-id="9b096-113">-PlanId</span><span class="sxs-lookup"><span data-stu-id="9b096-113">-PlanId</span></span>
<span data-ttu-id="9b096-114">Plan identifierare i kontexten för klient organisations prenumeration.</span><span class="sxs-lookup"><span data-stu-id="9b096-114">Plan identifier in the tenant subscription context.</span></span>

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

### <span data-ttu-id="9b096-115">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9b096-115">-TargetSubscriptionId</span></span>
<span data-ttu-id="9b096-116">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="9b096-116">The target subscription ID.</span></span>

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

### <span data-ttu-id="9b096-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9b096-117">-Confirm</span></span>
<span data-ttu-id="9b096-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9b096-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b096-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b096-119">-WhatIf</span></span>
<span data-ttu-id="9b096-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9b096-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b096-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9b096-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b096-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b096-122">CommonParameters</span></span>
<span data-ttu-id="9b096-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b096-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b096-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b096-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b096-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9b096-125">INPUTS</span></span>

## <span data-ttu-id="9b096-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9b096-126">OUTPUTS</span></span>

### <span data-ttu-id="9b096-127">Microsoft. AzureStack. Management. abonnemang. admin. Models. PlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="9b096-127">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.PlanAcquisition</span></span>

## <span data-ttu-id="9b096-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9b096-128">NOTES</span></span>

## <span data-ttu-id="9b096-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9b096-129">RELATED LINKS</span></span>

