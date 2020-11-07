---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 78c0e9d2796cd6edf1a2d094cc6dd3b37614e3aa
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921492"
---
# <span data-ttu-id="66536-101">New-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="66536-101">New-AzsOfferDelegation</span></span>

## <span data-ttu-id="66536-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="66536-102">SYNOPSIS</span></span>
<span data-ttu-id="66536-103">Skapa en ny ombuds delegering.</span><span class="sxs-lookup"><span data-stu-id="66536-103">Create a new offer delegation.</span></span>

## <span data-ttu-id="66536-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="66536-104">SYNTAX</span></span>

```
New-AzsOfferDelegation [-Name] <String> [-OfferName] <String> [-SubscriptionId] <String>
 [-ResourceGroupName] <String> [[-Location] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66536-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="66536-105">DESCRIPTION</span></span>
<span data-ttu-id="66536-106">Skapa en ny ombuds delegering.</span><span class="sxs-lookup"><span data-stu-id="66536-106">Create a new offer delegation.</span></span>

## <span data-ttu-id="66536-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="66536-107">EXAMPLES</span></span>

### <span data-ttu-id="66536-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="66536-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="66536-109">Skapa en ny ombuds delegering.</span><span class="sxs-lookup"><span data-stu-id="66536-109">Create a new offer delegation.</span></span>

## <span data-ttu-id="66536-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="66536-110">PARAMETERS</span></span>

### <span data-ttu-id="66536-111">-Plats</span><span class="sxs-lookup"><span data-stu-id="66536-111">-Location</span></span>
<span data-ttu-id="66536-112">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="66536-112">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66536-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="66536-113">-Name</span></span>
<span data-ttu-id="66536-114">Namn på en ombuds delegering.</span><span class="sxs-lookup"><span data-stu-id="66536-114">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="66536-115">-OfferName</span><span class="sxs-lookup"><span data-stu-id="66536-115">-OfferName</span></span>
<span data-ttu-id="66536-116">Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="66536-116">Name of an offer.</span></span>

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

### <span data-ttu-id="66536-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66536-117">-ResourceGroupName</span></span>
<span data-ttu-id="66536-118">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="66536-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66536-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="66536-119">-SubscriptionId</span></span>
<span data-ttu-id="66536-120">ID för det abonnemang som tar emot det delegerade erbjudandet.</span><span class="sxs-lookup"><span data-stu-id="66536-120">Identifier of the subscription receiving the delegated offer.</span></span>

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

### <span data-ttu-id="66536-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="66536-121">-Confirm</span></span>
<span data-ttu-id="66536-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="66536-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66536-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66536-123">-WhatIf</span></span>
<span data-ttu-id="66536-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="66536-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66536-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="66536-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66536-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66536-126">CommonParameters</span></span>
<span data-ttu-id="66536-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66536-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66536-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66536-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66536-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="66536-129">INPUTS</span></span>

## <span data-ttu-id="66536-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="66536-130">OUTPUTS</span></span>

### <span data-ttu-id="66536-131">Microsoft. AzureStack. Management. abonnemang. admin. Models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="66536-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="66536-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="66536-132">NOTES</span></span>

## <span data-ttu-id="66536-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="66536-133">RELATED LINKS</span></span>

