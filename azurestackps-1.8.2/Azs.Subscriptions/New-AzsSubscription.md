---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: d905159ca62f34584f045a699621f6672507ffe1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100177"
---
# <span data-ttu-id="02edc-101">New-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="02edc-101">New-AzsSubscription</span></span>

## <span data-ttu-id="02edc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="02edc-102">SYNOPSIS</span></span>
<span data-ttu-id="02edc-103">Skapa ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="02edc-103">Create a subscription.</span></span>

## <span data-ttu-id="02edc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="02edc-104">SYNTAX</span></span>

```
New-AzsSubscription [-OfferId] <String> [[-DisplayName] <String>] [[-TenantId] <String>]
 [[-SubscriptionId] <String>] [[-State] <String>] [[-Location] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="02edc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="02edc-105">DESCRIPTION</span></span>
<span data-ttu-id="02edc-106">Skapa ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="02edc-106">Create a subscription.</span></span>

## <span data-ttu-id="02edc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="02edc-107">EXAMPLES</span></span>

### <span data-ttu-id="02edc-108">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="02edc-108">EXAMPLE 1</span></span>
```
New-AzsSubscription -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="02edc-109">Skapa ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="02edc-109">Create a subscription.</span></span>

## <span data-ttu-id="02edc-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="02edc-110">PARAMETERS</span></span>

### <span data-ttu-id="02edc-111">-OfferId</span><span class="sxs-lookup"><span data-stu-id="02edc-111">-OfferId</span></span>
<span data-ttu-id="02edc-112">Identifierare för det som erbjuds under scopet för en delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="02edc-112">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="02edc-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="02edc-113">-DisplayName</span></span>
<span data-ttu-id="02edc-114">Prenumerationens namn.</span><span class="sxs-lookup"><span data-stu-id="02edc-114">Subscription name.</span></span>

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

### <span data-ttu-id="02edc-115">-TenantId</span><span class="sxs-lookup"><span data-stu-id="02edc-115">-TenantId</span></span>
<span data-ttu-id="02edc-116">Identifierare för katalog klient organisation.</span><span class="sxs-lookup"><span data-stu-id="02edc-116">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="02edc-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="02edc-117">-SubscriptionId</span></span>
<span data-ttu-id="02edc-118">Prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="02edc-118">Subscription identifier.</span></span>

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

### <span data-ttu-id="02edc-119">-State</span><span class="sxs-lookup"><span data-stu-id="02edc-119">-State</span></span>
<span data-ttu-id="02edc-120">Abonnemangs status.</span><span class="sxs-lookup"><span data-stu-id="02edc-120">Subscription state.</span></span>

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

### <span data-ttu-id="02edc-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="02edc-121">-Location</span></span>
<span data-ttu-id="02edc-122">Plats där resursen är plats.</span><span class="sxs-lookup"><span data-stu-id="02edc-122">Location where resource is location.</span></span>

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

### <span data-ttu-id="02edc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02edc-123">-WhatIf</span></span>
<span data-ttu-id="02edc-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="02edc-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02edc-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="02edc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02edc-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="02edc-126">-Confirm</span></span>
<span data-ttu-id="02edc-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="02edc-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02edc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02edc-128">CommonParameters</span></span>
<span data-ttu-id="02edc-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02edc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02edc-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02edc-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02edc-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="02edc-131">INPUTS</span></span>

## <span data-ttu-id="02edc-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="02edc-132">OUTPUTS</span></span>

### <span data-ttu-id="02edc-133">Microsoft. AzureStack. Management. Subscription. Models. SubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="02edc-133">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="02edc-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="02edc-134">NOTES</span></span>

## <span data-ttu-id="02edc-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="02edc-135">RELATED LINKS</span></span>
