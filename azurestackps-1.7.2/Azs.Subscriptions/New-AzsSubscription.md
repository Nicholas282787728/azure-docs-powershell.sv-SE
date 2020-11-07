---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 617a7ac7d949eb54ab08b0d0cb06c0fca3ba79bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921267"
---
# <span data-ttu-id="9e7f2-101">New-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="9e7f2-101">New-AzsSubscription</span></span>

## <span data-ttu-id="9e7f2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9e7f2-102">SYNOPSIS</span></span>
<span data-ttu-id="9e7f2-103">Skapa ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="9e7f2-103">Create a subscription.</span></span>

## <span data-ttu-id="9e7f2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9e7f2-104">SYNTAX</span></span>

```
New-AzsSubscription [-OfferId] <String> [[-DisplayName] <String>] [[-TenantId] <String>]
 [[-SubscriptionId] <String>] [[-State] <String>] [[-Location] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9e7f2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9e7f2-105">DESCRIPTION</span></span>
<span data-ttu-id="9e7f2-106">Skapa ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="9e7f2-106">Create a subscription.</span></span>

## <span data-ttu-id="9e7f2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9e7f2-107">EXAMPLES</span></span>

### <span data-ttu-id="9e7f2-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9e7f2-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsSubscription -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="9e7f2-109">Skapa ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="9e7f2-109">Create a subscription.</span></span>

## <span data-ttu-id="9e7f2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9e7f2-110">PARAMETERS</span></span>

### <span data-ttu-id="9e7f2-111">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9e7f2-111">-DisplayName</span></span>
<span data-ttu-id="9e7f2-112">Prenumerationens namn.</span><span class="sxs-lookup"><span data-stu-id="9e7f2-112">Subscription name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e7f2-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="9e7f2-113">-Location</span></span>
<span data-ttu-id="9e7f2-114">Plats där resursen är plats.</span><span class="sxs-lookup"><span data-stu-id="9e7f2-114">Location where resource is location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ArmLocation

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e7f2-115">-OfferId</span><span class="sxs-lookup"><span data-stu-id="9e7f2-115">-OfferId</span></span>
<span data-ttu-id="9e7f2-116">Identifierare för det som erbjuds under scopet för en delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="9e7f2-116">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="9e7f2-117">-State</span><span class="sxs-lookup"><span data-stu-id="9e7f2-117">-State</span></span>
<span data-ttu-id="9e7f2-118">Abonnemangs status.</span><span class="sxs-lookup"><span data-stu-id="9e7f2-118">Subscription state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: Enabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e7f2-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9e7f2-119">-SubscriptionId</span></span>
<span data-ttu-id="9e7f2-120">Prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="9e7f2-120">Subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e7f2-121">-TenantId</span><span class="sxs-lookup"><span data-stu-id="9e7f2-121">-TenantId</span></span>
<span data-ttu-id="9e7f2-122">Identifierare för katalog klient organisation.</span><span class="sxs-lookup"><span data-stu-id="9e7f2-122">Directory tenant identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e7f2-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9e7f2-123">-Confirm</span></span>
<span data-ttu-id="9e7f2-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9e7f2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e7f2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e7f2-125">-WhatIf</span></span>
<span data-ttu-id="9e7f2-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9e7f2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e7f2-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9e7f2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e7f2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e7f2-128">CommonParameters</span></span>
<span data-ttu-id="9e7f2-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e7f2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e7f2-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e7f2-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e7f2-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9e7f2-131">INPUTS</span></span>

## <span data-ttu-id="9e7f2-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9e7f2-132">OUTPUTS</span></span>

### <span data-ttu-id="9e7f2-133">Microsoft. AzureStack. Management. Subscription. Models. SubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="9e7f2-133">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="9e7f2-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9e7f2-134">NOTES</span></span>

## <span data-ttu-id="9e7f2-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9e7f2-135">RELATED LINKS</span></span>

