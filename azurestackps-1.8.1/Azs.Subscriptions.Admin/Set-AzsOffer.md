---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9b08aed00a4c16bd2031608ff795a4dde8491859
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921609"
---
# <span data-ttu-id="77d00-101">Set-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="77d00-101">Set-AzsOffer</span></span>

## <span data-ttu-id="77d00-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="77d00-102">SYNOPSIS</span></span>
<span data-ttu-id="77d00-103">Uppdatera detta.</span><span class="sxs-lookup"><span data-stu-id="77d00-103">Update the offer.</span></span>

## <span data-ttu-id="77d00-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="77d00-104">SYNTAX</span></span>

### <span data-ttu-id="77d00-105">Uppdatering (standard)</span><span class="sxs-lookup"><span data-stu-id="77d00-105">Update (Default)</span></span>
```
Set-AzsOffer -Name <String> -ResourceGroupName <String> [-DisplayName <String>] [-BasePlanIds <String[]>]
 [-Description <String>] [-ExternalReferenceId <String>] [-State <String>] [-Location <String>]
 [-SubscriptionCount <Int64>] [-MaxSubscriptionsPerAccount <Int64>]
 [-AddonPlanDefinition <AddonPlanDefinition[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77d00-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="77d00-106">InputObject</span></span>
```
Set-AzsOffer [-ResourceGroupName <String>] -InputObject <Offer> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77d00-107">ID</span><span class="sxs-lookup"><span data-stu-id="77d00-107">ResourceId</span></span>
```
Set-AzsOffer -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77d00-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="77d00-108">DESCRIPTION</span></span>
<span data-ttu-id="77d00-109">Uppdatera detta.</span><span class="sxs-lookup"><span data-stu-id="77d00-109">Update the offer.</span></span>

## <span data-ttu-id="77d00-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="77d00-110">EXAMPLES</span></span>

### <span data-ttu-id="77d00-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="77d00-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsOffer -Name offer1 -ResourceGroupName rg1 -State Private
```

<span data-ttu-id="77d00-112">Uppdatera detta.</span><span class="sxs-lookup"><span data-stu-id="77d00-112">Update the offer.</span></span>

## <span data-ttu-id="77d00-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="77d00-113">PARAMETERS</span></span>

### <span data-ttu-id="77d00-114">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="77d00-114">-AddonPlanDefinition</span></span>
<span data-ttu-id="77d00-115">Referenser till tilläggs planer som en klient organisation kan erhålla för att bli en del av det.</span><span class="sxs-lookup"><span data-stu-id="77d00-115">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>

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

### <span data-ttu-id="77d00-116">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="77d00-116">-BasePlanIds</span></span>
<span data-ttu-id="77d00-117">Identifierare för de grundläggande abonnemang som blir tillgängliga för klient organisationen omedelbart när en klient organisation abonnerar på ett bud.</span><span class="sxs-lookup"><span data-stu-id="77d00-117">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

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

### <span data-ttu-id="77d00-118">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="77d00-118">-Description</span></span>
<span data-ttu-id="77d00-119">Beskrivning av bud.</span><span class="sxs-lookup"><span data-stu-id="77d00-119">Description of offer.</span></span>

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

### <span data-ttu-id="77d00-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="77d00-120">-DisplayName</span></span>
<span data-ttu-id="77d00-121">Visnings namn för bud.</span><span class="sxs-lookup"><span data-stu-id="77d00-121">Display name of offer.</span></span>

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

### <span data-ttu-id="77d00-122">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="77d00-122">-ExternalReferenceId</span></span>
<span data-ttu-id="77d00-123">Extern referens-ID.</span><span class="sxs-lookup"><span data-stu-id="77d00-123">External reference identifier.</span></span>

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

### <span data-ttu-id="77d00-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77d00-124">-InputObject</span></span>
<span data-ttu-id="77d00-125">Indatavärdet av typen Microsoft. AzureStack. Management. abonnemang. admin. Models. offer.</span><span class="sxs-lookup"><span data-stu-id="77d00-125">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer.</span></span>

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

### <span data-ttu-id="77d00-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="77d00-126">-Location</span></span>
<span data-ttu-id="77d00-127">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="77d00-127">Location of the resource.</span></span>

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

### <span data-ttu-id="77d00-128">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="77d00-128">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="77d00-129">Maximalt antal prenumerationer per konto.</span><span class="sxs-lookup"><span data-stu-id="77d00-129">Maximum subscriptions per account.</span></span>

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

### <span data-ttu-id="77d00-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="77d00-130">-Name</span></span>
<span data-ttu-id="77d00-131">Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="77d00-131">Name of an offer.</span></span>

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

### <span data-ttu-id="77d00-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77d00-132">-ResourceGroupName</span></span>
<span data-ttu-id="77d00-133">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="77d00-133">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="77d00-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77d00-134">-ResourceId</span></span>
<span data-ttu-id="77d00-135">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="77d00-135">The resource id.</span></span>

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

### <span data-ttu-id="77d00-136">-State</span><span class="sxs-lookup"><span data-stu-id="77d00-136">-State</span></span>
<span data-ttu-id="77d00-137">Ge hjälpmedels status.</span><span class="sxs-lookup"><span data-stu-id="77d00-137">Offer accessibility state.</span></span>

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

### <span data-ttu-id="77d00-138">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="77d00-138">-SubscriptionCount</span></span>
<span data-ttu-id="77d00-139">Aktuellt antal prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="77d00-139">Current subscription count.</span></span>

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

### <span data-ttu-id="77d00-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="77d00-140">-Confirm</span></span>
<span data-ttu-id="77d00-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="77d00-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77d00-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77d00-142">-WhatIf</span></span>
<span data-ttu-id="77d00-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="77d00-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77d00-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="77d00-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77d00-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77d00-145">CommonParameters</span></span>
<span data-ttu-id="77d00-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77d00-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77d00-147">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77d00-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77d00-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="77d00-148">INPUTS</span></span>

## <span data-ttu-id="77d00-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="77d00-149">OUTPUTS</span></span>

### <span data-ttu-id="77d00-150">Microsoft. AzureStack. Management. abonnemang. admin. Models. erbjuda</span><span class="sxs-lookup"><span data-stu-id="77d00-150">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="77d00-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="77d00-151">NOTES</span></span>

## <span data-ttu-id="77d00-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="77d00-152">RELATED LINKS</span></span>

