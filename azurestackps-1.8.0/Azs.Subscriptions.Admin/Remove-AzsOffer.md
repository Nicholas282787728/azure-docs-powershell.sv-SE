---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 74772615551979a9ab0cdba3603305489698e212
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921314"
---
# <span data-ttu-id="855a4-101">Remove-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="855a4-101">Remove-AzsOffer</span></span>

## <span data-ttu-id="855a4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="855a4-102">SYNOPSIS</span></span>
<span data-ttu-id="855a4-103">Ta bort det angivna värdet.</span><span class="sxs-lookup"><span data-stu-id="855a4-103">Delete the specified offer.</span></span>

## <span data-ttu-id="855a4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="855a4-104">SYNTAX</span></span>

### <span data-ttu-id="855a4-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="855a4-105">Delete (Default)</span></span>
```
Remove-AzsOffer -Name <String> -ResourceGroupName <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="855a4-106">ID</span><span class="sxs-lookup"><span data-stu-id="855a4-106">ResourceId</span></span>
```
Remove-AzsOffer -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="855a4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="855a4-107">DESCRIPTION</span></span>
<span data-ttu-id="855a4-108">Ta bort det angivna värdet.</span><span class="sxs-lookup"><span data-stu-id="855a4-108">Delete the specified offer.</span></span>

## <span data-ttu-id="855a4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="855a4-109">EXAMPLES</span></span>

### <span data-ttu-id="855a4-110">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="855a4-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsOffer -Name offername1 -ResourceGroupName rg1
```

<span data-ttu-id="855a4-111">Ta bort det angivna värdet.</span><span class="sxs-lookup"><span data-stu-id="855a4-111">Delete the specified offer.</span></span>

## <span data-ttu-id="855a4-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="855a4-112">PARAMETERS</span></span>

### <span data-ttu-id="855a4-113">-Force</span><span class="sxs-lookup"><span data-stu-id="855a4-113">-Force</span></span>
<span data-ttu-id="855a4-114">Flagga för att ta bort objektet utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="855a4-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="855a4-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="855a4-115">-Name</span></span>
<span data-ttu-id="855a4-116">Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="855a4-116">Name of an offer.</span></span>

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

### <span data-ttu-id="855a4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="855a4-117">-ResourceGroupName</span></span>
<span data-ttu-id="855a4-118">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="855a4-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="855a4-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="855a4-119">-ResourceId</span></span>
<span data-ttu-id="855a4-120">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="855a4-120">The resource id.</span></span>

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

### <span data-ttu-id="855a4-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="855a4-121">-Confirm</span></span>
<span data-ttu-id="855a4-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="855a4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="855a4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="855a4-123">-WhatIf</span></span>
<span data-ttu-id="855a4-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="855a4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="855a4-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="855a4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="855a4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="855a4-126">CommonParameters</span></span>
<span data-ttu-id="855a4-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="855a4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="855a4-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="855a4-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="855a4-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="855a4-129">INPUTS</span></span>

## <span data-ttu-id="855a4-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="855a4-130">OUTPUTS</span></span>

## <span data-ttu-id="855a4-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="855a4-131">NOTES</span></span>

## <span data-ttu-id="855a4-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="855a4-132">RELATED LINKS</span></span>

