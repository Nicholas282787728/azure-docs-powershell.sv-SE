---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 36a4ddec5825be1e1f897cb3a12e7bc26a2c6817
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571608"
---
# <span data-ttu-id="1cd28-101">New-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="1cd28-101">New-AzsOfferDelegation</span></span>

## <span data-ttu-id="1cd28-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1cd28-102">SYNOPSIS</span></span>
<span data-ttu-id="1cd28-103">Skapa en ny ombuds delegering.</span><span class="sxs-lookup"><span data-stu-id="1cd28-103">Create a new offer delegation.</span></span>

## <span data-ttu-id="1cd28-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1cd28-104">SYNTAX</span></span>

```
New-AzsOfferDelegation [-Name] <String> [-OfferName] <String> [-SubscriptionId] <String>
 [-ResourceGroupName] <String> [[-Location] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cd28-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1cd28-105">DESCRIPTION</span></span>
<span data-ttu-id="1cd28-106">Skapa en ny ombuds delegering.</span><span class="sxs-lookup"><span data-stu-id="1cd28-106">Create a new offer delegation.</span></span>

## <span data-ttu-id="1cd28-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1cd28-107">EXAMPLES</span></span>

### <span data-ttu-id="1cd28-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1cd28-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="1cd28-109">Skapa en ny ombuds delegering.</span><span class="sxs-lookup"><span data-stu-id="1cd28-109">Create a new offer delegation.</span></span>

## <span data-ttu-id="1cd28-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1cd28-110">PARAMETERS</span></span>

### <span data-ttu-id="1cd28-111">-Plats</span><span class="sxs-lookup"><span data-stu-id="1cd28-111">-Location</span></span>
<span data-ttu-id="1cd28-112">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="1cd28-112">Location of the resource.</span></span>

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

### <span data-ttu-id="1cd28-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="1cd28-113">-Name</span></span>
<span data-ttu-id="1cd28-114">Namn på en ombuds delegering.</span><span class="sxs-lookup"><span data-stu-id="1cd28-114">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="1cd28-115">-OfferName</span><span class="sxs-lookup"><span data-stu-id="1cd28-115">-OfferName</span></span>
<span data-ttu-id="1cd28-116">Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="1cd28-116">Name of an offer.</span></span>

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

### <span data-ttu-id="1cd28-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cd28-117">-ResourceGroupName</span></span>
<span data-ttu-id="1cd28-118">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="1cd28-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="1cd28-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1cd28-119">-SubscriptionId</span></span>
<span data-ttu-id="1cd28-120">ID för det abonnemang som tar emot det delegerade erbjudandet.</span><span class="sxs-lookup"><span data-stu-id="1cd28-120">Identifier of the subscription receiving the delegated offer.</span></span>

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

### <span data-ttu-id="1cd28-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1cd28-121">-Confirm</span></span>
<span data-ttu-id="1cd28-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1cd28-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cd28-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cd28-123">-WhatIf</span></span>
<span data-ttu-id="1cd28-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1cd28-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cd28-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1cd28-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cd28-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cd28-126">CommonParameters</span></span>
<span data-ttu-id="1cd28-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cd28-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cd28-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cd28-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cd28-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1cd28-129">INPUTS</span></span>

## <span data-ttu-id="1cd28-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1cd28-130">OUTPUTS</span></span>

### <span data-ttu-id="1cd28-131">Microsoft. AzureStack. Management. abonnemang. admin. Models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="1cd28-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="1cd28-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1cd28-132">NOTES</span></span>

## <span data-ttu-id="1cd28-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1cd28-133">RELATED LINKS</span></span>

