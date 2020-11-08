---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9b08aed00a4c16bd2031608ff795a4dde8491859
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100301"
---
# <span data-ttu-id="eac60-101">Set-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="eac60-101">Set-AzsOffer</span></span>

## <span data-ttu-id="eac60-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eac60-102">SYNOPSIS</span></span>
<span data-ttu-id="eac60-103">Uppdatera detta.</span><span class="sxs-lookup"><span data-stu-id="eac60-103">Update the offer.</span></span>

## <span data-ttu-id="eac60-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eac60-104">SYNTAX</span></span>

### <span data-ttu-id="eac60-105">Uppdatering (standard)</span><span class="sxs-lookup"><span data-stu-id="eac60-105">Update (Default)</span></span>
```
Set-AzsOffer -Name <String> -ResourceGroupName <String> [-DisplayName <String>] [-BasePlanIds <String[]>]
 [-Description <String>] [-ExternalReferenceId <String>] [-State <String>] [-Location <String>]
 [-SubscriptionCount <Int64>] [-MaxSubscriptionsPerAccount <Int64>]
 [-AddonPlanDefinition <AddonPlanDefinition[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eac60-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="eac60-106">InputObject</span></span>
```
Set-AzsOffer [-ResourceGroupName <String>] -InputObject <Offer> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eac60-107">ID</span><span class="sxs-lookup"><span data-stu-id="eac60-107">ResourceId</span></span>
```
Set-AzsOffer -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eac60-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eac60-108">DESCRIPTION</span></span>
<span data-ttu-id="eac60-109">Uppdatera detta.</span><span class="sxs-lookup"><span data-stu-id="eac60-109">Update the offer.</span></span>

## <span data-ttu-id="eac60-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eac60-110">EXAMPLES</span></span>

### <span data-ttu-id="eac60-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="eac60-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsOffer -Name offer1 -ResourceGroupName rg1 -State Private
```

<span data-ttu-id="eac60-112">Uppdatera detta.</span><span class="sxs-lookup"><span data-stu-id="eac60-112">Update the offer.</span></span>

## <span data-ttu-id="eac60-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eac60-113">PARAMETERS</span></span>

### <span data-ttu-id="eac60-114">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="eac60-114">-AddonPlanDefinition</span></span>
<span data-ttu-id="eac60-115">Referenser till tilläggs planer som en klient organisation kan erhålla för att bli en del av det.</span><span class="sxs-lookup"><span data-stu-id="eac60-115">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>

```yaml
Type: AddonPlanDefinition[]
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eac60-116">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="eac60-116">-BasePlanIds</span></span>
<span data-ttu-id="eac60-117">Identifierare för de grundläggande abonnemang som blir tillgängliga för klient organisationen omedelbart när en klient organisation abonnerar på ett bud.</span><span class="sxs-lookup"><span data-stu-id="eac60-117">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

```yaml
Type: String[]
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eac60-118">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="eac60-118">-Description</span></span>
<span data-ttu-id="eac60-119">Beskrivning av bud.</span><span class="sxs-lookup"><span data-stu-id="eac60-119">Description of offer.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eac60-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="eac60-120">-DisplayName</span></span>
<span data-ttu-id="eac60-121">Visnings namn för bud.</span><span class="sxs-lookup"><span data-stu-id="eac60-121">Display name of offer.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eac60-122">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="eac60-122">-ExternalReferenceId</span></span>
<span data-ttu-id="eac60-123">Extern referens-ID.</span><span class="sxs-lookup"><span data-stu-id="eac60-123">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eac60-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eac60-124">-InputObject</span></span>
<span data-ttu-id="eac60-125">Indatavärdet av typen Microsoft. AzureStack. Management. abonnemang. admin. Models. offer.</span><span class="sxs-lookup"><span data-stu-id="eac60-125">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer.</span></span>

```yaml
Type: Offer
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eac60-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="eac60-126">-Location</span></span>
<span data-ttu-id="eac60-127">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="eac60-127">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eac60-128">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="eac60-128">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="eac60-129">Maximalt antal prenumerationer per konto.</span><span class="sxs-lookup"><span data-stu-id="eac60-129">Maximum subscriptions per account.</span></span>

```yaml
Type: Int64
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eac60-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="eac60-130">-Name</span></span>
<span data-ttu-id="eac60-131">Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="eac60-131">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eac60-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eac60-132">-ResourceGroupName</span></span>
<span data-ttu-id="eac60-133">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="eac60-133">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: InputObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eac60-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eac60-134">-ResourceId</span></span>
<span data-ttu-id="eac60-135">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="eac60-135">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eac60-136">-State</span><span class="sxs-lookup"><span data-stu-id="eac60-136">-State</span></span>
<span data-ttu-id="eac60-137">Ge hjälpmedels status.</span><span class="sxs-lookup"><span data-stu-id="eac60-137">Offer accessibility state.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eac60-138">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="eac60-138">-SubscriptionCount</span></span>
<span data-ttu-id="eac60-139">Aktuellt antal prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="eac60-139">Current subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eac60-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="eac60-140">-Confirm</span></span>
<span data-ttu-id="eac60-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="eac60-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eac60-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eac60-142">-WhatIf</span></span>
<span data-ttu-id="eac60-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="eac60-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eac60-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="eac60-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eac60-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eac60-145">CommonParameters</span></span>
<span data-ttu-id="eac60-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eac60-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eac60-147">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eac60-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eac60-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eac60-148">INPUTS</span></span>

## <span data-ttu-id="eac60-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eac60-149">OUTPUTS</span></span>

### <span data-ttu-id="eac60-150">Microsoft. AzureStack. Management. abonnemang. admin. Models. erbjuda</span><span class="sxs-lookup"><span data-stu-id="eac60-150">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="eac60-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eac60-151">NOTES</span></span>

## <span data-ttu-id="eac60-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eac60-152">RELATED LINKS</span></span>

