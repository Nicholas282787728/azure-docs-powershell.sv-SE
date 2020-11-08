---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d4b7abdeb085c7cfee6444c4afeeb6a3e79d99e9
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921645"
---
# <span data-ttu-id="2317c-101">New-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="2317c-101">New-AzsUserSubscription</span></span>

## <span data-ttu-id="2317c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2317c-102">SYNOPSIS</span></span>
<span data-ttu-id="2317c-103">Skapa en ny prenumeration.</span><span class="sxs-lookup"><span data-stu-id="2317c-103">Create a new subscription.</span></span>

## <span data-ttu-id="2317c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2317c-104">SYNTAX</span></span>

```
New-AzsUserSubscription [-Owner] <String> [-OfferId] <String> [[-TenantId] <String>] [[-DisplayName] <String>]
 [[-DelegatedProviderSubscriptionId] <String>] [[-RoutingResourceManagerType] <String>]
 [[-ExternalReferenceId] <String>] [[-State] <String>] [[-SubscriptionId] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2317c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2317c-105">DESCRIPTION</span></span>
<span data-ttu-id="2317c-106">Skapa en ny prenumeration.</span><span class="sxs-lookup"><span data-stu-id="2317c-106">Create a new subscription.</span></span>

## <span data-ttu-id="2317c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2317c-107">EXAMPLES</span></span>

### <span data-ttu-id="2317c-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2317c-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsUserSubscription -Owner user@contoso.com -OfferId "/subscriptions/302d0fcd-5263-4f4d-82ba-383ad95a3e53/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/offers/offer1"
```

<span data-ttu-id="2317c-109">Skapar en ny användar prenumeration</span><span class="sxs-lookup"><span data-stu-id="2317c-109">Creates a new user subscription</span></span>

## <span data-ttu-id="2317c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2317c-110">PARAMETERS</span></span>

### <span data-ttu-id="2317c-111">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2317c-111">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="2317c-112">Överordnat abonnemang för DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="2317c-112">Parent DelegatedProvider subscription identifier.</span></span>

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

### <span data-ttu-id="2317c-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2317c-113">-DisplayName</span></span>
<span data-ttu-id="2317c-114">Prenumerationens namn.</span><span class="sxs-lookup"><span data-stu-id="2317c-114">Subscription name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2317c-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="2317c-115">-ExternalReferenceId</span></span>
<span data-ttu-id="2317c-116">Extern referens-ID.</span><span class="sxs-lookup"><span data-stu-id="2317c-116">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2317c-117">-OfferId</span><span class="sxs-lookup"><span data-stu-id="2317c-117">-OfferId</span></span>
<span data-ttu-id="2317c-118">Identifierare för det som erbjuds under scopet för en delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="2317c-118">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="2317c-119">-Owner</span><span class="sxs-lookup"><span data-stu-id="2317c-119">-Owner</span></span>
<span data-ttu-id="2317c-120">Abonnemangs ägare.</span><span class="sxs-lookup"><span data-stu-id="2317c-120">Subscription owner.</span></span>

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

### <span data-ttu-id="2317c-121">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="2317c-121">-RoutingResourceManagerType</span></span>
<span data-ttu-id="2317c-122">Routning Resource Manager-typ.</span><span class="sxs-lookup"><span data-stu-id="2317c-122">Routing resource manager type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: Default
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2317c-123">-State</span><span class="sxs-lookup"><span data-stu-id="2317c-123">-State</span></span>
<span data-ttu-id="2317c-124">Abonnemangs status.</span><span class="sxs-lookup"><span data-stu-id="2317c-124">Subscription state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: Enabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2317c-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2317c-125">-SubscriptionId</span></span>
<span data-ttu-id="2317c-126">Prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="2317c-126">Subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2317c-127">-TenantId</span><span class="sxs-lookup"><span data-stu-id="2317c-127">-TenantId</span></span>
<span data-ttu-id="2317c-128">Identifierare för katalog klient organisation.</span><span class="sxs-lookup"><span data-stu-id="2317c-128">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="2317c-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2317c-129">-Confirm</span></span>
<span data-ttu-id="2317c-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2317c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2317c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2317c-131">-WhatIf</span></span>
<span data-ttu-id="2317c-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2317c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2317c-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2317c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2317c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2317c-134">CommonParameters</span></span>
<span data-ttu-id="2317c-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2317c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2317c-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2317c-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2317c-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2317c-137">INPUTS</span></span>

## <span data-ttu-id="2317c-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2317c-138">OUTPUTS</span></span>

### <span data-ttu-id="2317c-139">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Subscription</span><span class="sxs-lookup"><span data-stu-id="2317c-139">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="2317c-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2317c-140">NOTES</span></span>

## <span data-ttu-id="2317c-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2317c-141">RELATED LINKS</span></span>
