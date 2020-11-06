---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 106293e9d959aefe25ae3e4b27519639a39193d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571788"
---
# <span data-ttu-id="6b403-101">Set-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="6b403-101">Set-AzsUserSubscription</span></span>

## <span data-ttu-id="6b403-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6b403-102">SYNOPSIS</span></span>
<span data-ttu-id="6b403-103">Uppdaterar angivet användar abonnemang</span><span class="sxs-lookup"><span data-stu-id="6b403-103">Updates the specified user subscription</span></span>

## <span data-ttu-id="6b403-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6b403-104">SYNTAX</span></span>

### <span data-ttu-id="6b403-105">Ange (standard)</span><span class="sxs-lookup"><span data-stu-id="6b403-105">Set (Default)</span></span>
```
Set-AzsUserSubscription -SubscriptionId <Guid> [-DisplayName <String>]
 [-DelegatedProviderSubscriptionId <String>] [-Owner <String>] [-TenantId <String>]
 [-RoutingResourceManagerType <String>] [-ExternalReferenceId <String>] [-State <String>] [-Location <String>]
 [-OfferId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b403-106">ID</span><span class="sxs-lookup"><span data-stu-id="6b403-106">ResourceId</span></span>
```
Set-AzsUserSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b403-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="6b403-107">InputObject</span></span>
```
Set-AzsUserSubscription -InputObject <Subscription> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b403-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6b403-108">DESCRIPTION</span></span>
<span data-ttu-id="6b403-109">Uppdaterar angivet användar abonnemang</span><span class="sxs-lookup"><span data-stu-id="6b403-109">Updates the specified user subscription</span></span>

## <span data-ttu-id="6b403-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6b403-110">EXAMPLES</span></span>

### <span data-ttu-id="6b403-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6b403-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsUserSubscription -SubscriptionId 8e425478-c7f0-49ca-bb92-b42889ec3642 -DisplayName "NewName"
```

<span data-ttu-id="6b403-112">Uppdaterar ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="6b403-112">Updates a subscription</span></span>

## <span data-ttu-id="6b403-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6b403-113">PARAMETERS</span></span>

### <span data-ttu-id="6b403-114">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6b403-114">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="6b403-115">Överordnat abonnemang för DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="6b403-115">Parent DelegatedProvider subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b403-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6b403-116">-DisplayName</span></span>
<span data-ttu-id="6b403-117">Prenumerationens namn.</span><span class="sxs-lookup"><span data-stu-id="6b403-117">Subscription name.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b403-118">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="6b403-118">-ExternalReferenceId</span></span>
<span data-ttu-id="6b403-119">Extern referens-ID.</span><span class="sxs-lookup"><span data-stu-id="6b403-119">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b403-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b403-120">-InputObject</span></span>
<span data-ttu-id="6b403-121">Indatavärdet av typen Microsoft. AzureStack. Management. Network. admin. Models. quota.</span><span class="sxs-lookup"><span data-stu-id="6b403-121">The input object of type Microsoft.AzureStack.Management.Network.Admin.Models.Quota.</span></span>

```yaml
Type: Subscription
Parameter Sets: InputObject
Aliases: Subscription

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b403-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="6b403-122">-Location</span></span>
<span data-ttu-id="6b403-123">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="6b403-123">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b403-124">-OfferId</span><span class="sxs-lookup"><span data-stu-id="6b403-124">-OfferId</span></span>
<span data-ttu-id="6b403-125">Identifierare för det som erbjuds under scopet för en delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="6b403-125">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b403-126">-Owner</span><span class="sxs-lookup"><span data-stu-id="6b403-126">-Owner</span></span>
<span data-ttu-id="6b403-127">Abonnemangs ägare.</span><span class="sxs-lookup"><span data-stu-id="6b403-127">Subscription owner.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b403-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b403-128">-ResourceId</span></span>
<span data-ttu-id="6b403-129">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="6b403-129">The resource ID.</span></span>

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

### <span data-ttu-id="6b403-130">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="6b403-130">-RoutingResourceManagerType</span></span>
<span data-ttu-id="6b403-131">Routning Resource Manager-typ.</span><span class="sxs-lookup"><span data-stu-id="6b403-131">Routing resource manager type.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b403-132">-State</span><span class="sxs-lookup"><span data-stu-id="6b403-132">-State</span></span>
<span data-ttu-id="6b403-133">Abonnemangs status.</span><span class="sxs-lookup"><span data-stu-id="6b403-133">Subscription state.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b403-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6b403-134">-SubscriptionId</span></span>
<span data-ttu-id="6b403-135">Prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="6b403-135">Subscription identifier.</span></span>

```yaml
Type: Guid
Parameter Sets: Set
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b403-136">-TenantId</span><span class="sxs-lookup"><span data-stu-id="6b403-136">-TenantId</span></span>
<span data-ttu-id="6b403-137">Identifierare för katalog klient organisation.</span><span class="sxs-lookup"><span data-stu-id="6b403-137">Directory tenant identifier.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b403-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6b403-138">-Confirm</span></span>
<span data-ttu-id="6b403-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6b403-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b403-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b403-140">-WhatIf</span></span>
<span data-ttu-id="6b403-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6b403-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b403-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6b403-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b403-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b403-143">CommonParameters</span></span>
<span data-ttu-id="6b403-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b403-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b403-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b403-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b403-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6b403-146">INPUTS</span></span>

## <span data-ttu-id="6b403-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6b403-147">OUTPUTS</span></span>

### <span data-ttu-id="6b403-148">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Subscription</span><span class="sxs-lookup"><span data-stu-id="6b403-148">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="6b403-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6b403-149">NOTES</span></span>

## <span data-ttu-id="6b403-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6b403-150">RELATED LINKS</span></span>

