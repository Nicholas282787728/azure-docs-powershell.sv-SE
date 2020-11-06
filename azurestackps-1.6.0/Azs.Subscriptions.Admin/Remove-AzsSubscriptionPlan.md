---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b82dadf9a9e26b0023872378d41e4978e18436ab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571800"
---
# <span data-ttu-id="9fa0d-101">Remove-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="9fa0d-101">Remove-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="9fa0d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9fa0d-102">SYNOPSIS</span></span>
<span data-ttu-id="9fa0d-103">Tar bort en abonnemangs plan.</span><span class="sxs-lookup"><span data-stu-id="9fa0d-103">Deletes a subscription plan.</span></span>

## <span data-ttu-id="9fa0d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9fa0d-104">SYNTAX</span></span>

### <span data-ttu-id="9fa0d-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="9fa0d-105">Delete (Default)</span></span>
```
Remove-AzsSubscriptionPlan -AcquisitionId <Guid> -TargetSubscriptionId <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9fa0d-106">ID</span><span class="sxs-lookup"><span data-stu-id="9fa0d-106">ResourceId</span></span>
```
Remove-AzsSubscriptionPlan -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fa0d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9fa0d-107">DESCRIPTION</span></span>
<span data-ttu-id="9fa0d-108">Tar bort en abonnemangs plan.</span><span class="sxs-lookup"><span data-stu-id="9fa0d-108">Deletes a subscription plan.</span></span>

## <span data-ttu-id="9fa0d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9fa0d-109">EXAMPLES</span></span>

### <span data-ttu-id="9fa0d-110">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9fa0d-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsSubscriptionPlan -AcquisitionId $([Guid]::NewGuid()) -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="9fa0d-111">Ta bort en abonnemangs plan.</span><span class="sxs-lookup"><span data-stu-id="9fa0d-111">Delete a subscription plan.</span></span>

## <span data-ttu-id="9fa0d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9fa0d-112">PARAMETERS</span></span>

### <span data-ttu-id="9fa0d-113">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="9fa0d-113">-AcquisitionId</span></span>
<span data-ttu-id="9fa0d-114">Abonnemangets anskaffnings identifierare</span><span class="sxs-lookup"><span data-stu-id="9fa0d-114">The plan acquisition Identifier</span></span>

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

### <span data-ttu-id="9fa0d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9fa0d-115">-Force</span></span>
<span data-ttu-id="9fa0d-116">Flagga för att ta bort objektet utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="9fa0d-116">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="9fa0d-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9fa0d-117">-ResourceId</span></span>
<span data-ttu-id="9fa0d-118">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="9fa0d-118">The resource id.</span></span>

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

### <span data-ttu-id="9fa0d-119">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9fa0d-119">-TargetSubscriptionId</span></span>
<span data-ttu-id="9fa0d-120">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="9fa0d-120">The target subscription ID.</span></span>

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

### <span data-ttu-id="9fa0d-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9fa0d-121">-Confirm</span></span>
<span data-ttu-id="9fa0d-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9fa0d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fa0d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fa0d-123">-WhatIf</span></span>
<span data-ttu-id="9fa0d-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9fa0d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fa0d-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9fa0d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fa0d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fa0d-126">CommonParameters</span></span>
<span data-ttu-id="9fa0d-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fa0d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fa0d-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fa0d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fa0d-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9fa0d-129">INPUTS</span></span>

## <span data-ttu-id="9fa0d-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9fa0d-130">OUTPUTS</span></span>

## <span data-ttu-id="9fa0d-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9fa0d-131">NOTES</span></span>

## <span data-ttu-id="9fa0d-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9fa0d-132">RELATED LINKS</span></span>

