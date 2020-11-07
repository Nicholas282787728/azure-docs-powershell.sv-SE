---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 285b9509241e9035c007f871ac6395008a1f9cde
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921065"
---
# <span data-ttu-id="90aa7-101">Set-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="90aa7-101">Set-AzsOffer</span></span>

## <span data-ttu-id="90aa7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="90aa7-102">SYNOPSIS</span></span>
<span data-ttu-id="90aa7-103">Uppdatera detta.</span><span class="sxs-lookup"><span data-stu-id="90aa7-103">Update the offer.</span></span>

## <span data-ttu-id="90aa7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="90aa7-104">SYNTAX</span></span>

### <span data-ttu-id="90aa7-105">Uppdatering (standard)</span><span class="sxs-lookup"><span data-stu-id="90aa7-105">Update (Default)</span></span>
```
Set-AzsOffer -Name <String> -ResourceGroupName <String> [-DisplayName <String>] [-BasePlanIds <String[]>]
 [-Description <String>] [-ExternalReferenceId <String>] [-State <String>] [-Location <String>]
 [-SubscriptionCount <Int64>] [-MaxSubscriptionsPerAccount <Int64>]
 [-AddonPlanDefinition <AddonPlanDefinition[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90aa7-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="90aa7-106">InputObject</span></span>
```
Set-AzsOffer [-ResourceGroupName <String>] -InputObject <Offer> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90aa7-107">ID</span><span class="sxs-lookup"><span data-stu-id="90aa7-107">ResourceId</span></span>
```
Set-AzsOffer -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90aa7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="90aa7-108">DESCRIPTION</span></span>
<span data-ttu-id="90aa7-109">Uppdatera detta.</span><span class="sxs-lookup"><span data-stu-id="90aa7-109">Update the offer.</span></span>

## <span data-ttu-id="90aa7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="90aa7-110">EXAMPLES</span></span>

### <span data-ttu-id="90aa7-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="90aa7-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsOffer -Name offer1 -ResourceGroupName rg1 -State Private
```

<span data-ttu-id="90aa7-112">Uppdatera detta.</span><span class="sxs-lookup"><span data-stu-id="90aa7-112">Update the offer.</span></span>

## <span data-ttu-id="90aa7-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="90aa7-113">PARAMETERS</span></span>

### <span data-ttu-id="90aa7-114">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="90aa7-114">-AddonPlanDefinition</span></span>
<span data-ttu-id="90aa7-115">Referenser till tilläggs planer som en klient organisation kan erhålla för att bli en del av det.</span><span class="sxs-lookup"><span data-stu-id="90aa7-115">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>

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

### <span data-ttu-id="90aa7-116">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="90aa7-116">-BasePlanIds</span></span>
<span data-ttu-id="90aa7-117">Identifierare för de grundläggande abonnemang som blir tillgängliga för klient organisationen omedelbart när en klient organisation abonnerar på ett bud.</span><span class="sxs-lookup"><span data-stu-id="90aa7-117">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

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

### <span data-ttu-id="90aa7-118">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="90aa7-118">-Description</span></span>
<span data-ttu-id="90aa7-119">Beskrivning av bud.</span><span class="sxs-lookup"><span data-stu-id="90aa7-119">Description of offer.</span></span>

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

### <span data-ttu-id="90aa7-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="90aa7-120">-DisplayName</span></span>
<span data-ttu-id="90aa7-121">Visnings namn för bud.</span><span class="sxs-lookup"><span data-stu-id="90aa7-121">Display name of offer.</span></span>

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

### <span data-ttu-id="90aa7-122">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="90aa7-122">-ExternalReferenceId</span></span>
<span data-ttu-id="90aa7-123">Extern referens-ID.</span><span class="sxs-lookup"><span data-stu-id="90aa7-123">External reference identifier.</span></span>

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

### <span data-ttu-id="90aa7-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90aa7-124">-InputObject</span></span>
<span data-ttu-id="90aa7-125">Indatavärdet av typen Microsoft. AzureStack. Management. abonnemang. admin. Models. offer.</span><span class="sxs-lookup"><span data-stu-id="90aa7-125">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer.</span></span>

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

### <span data-ttu-id="90aa7-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="90aa7-126">-Location</span></span>
<span data-ttu-id="90aa7-127">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="90aa7-127">Location of the resource.</span></span>

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

### <span data-ttu-id="90aa7-128">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="90aa7-128">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="90aa7-129">Maximalt antal prenumerationer per konto.</span><span class="sxs-lookup"><span data-stu-id="90aa7-129">Maximum subscriptions per account.</span></span>

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

### <span data-ttu-id="90aa7-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="90aa7-130">-Name</span></span>
<span data-ttu-id="90aa7-131">Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="90aa7-131">Name of an offer.</span></span>

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

### <span data-ttu-id="90aa7-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90aa7-132">-ResourceGroupName</span></span>
<span data-ttu-id="90aa7-133">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="90aa7-133">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="90aa7-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="90aa7-134">-ResourceId</span></span>
<span data-ttu-id="90aa7-135">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="90aa7-135">The resource id.</span></span>

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

### <span data-ttu-id="90aa7-136">-State</span><span class="sxs-lookup"><span data-stu-id="90aa7-136">-State</span></span>
<span data-ttu-id="90aa7-137">Ge hjälpmedels status.</span><span class="sxs-lookup"><span data-stu-id="90aa7-137">Offer accessibility state.</span></span>

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

### <span data-ttu-id="90aa7-138">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="90aa7-138">-SubscriptionCount</span></span>
<span data-ttu-id="90aa7-139">Aktuellt antal prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="90aa7-139">Current subscription count.</span></span>

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

### <span data-ttu-id="90aa7-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="90aa7-140">-Confirm</span></span>
<span data-ttu-id="90aa7-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="90aa7-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90aa7-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90aa7-142">-WhatIf</span></span>
<span data-ttu-id="90aa7-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="90aa7-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90aa7-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="90aa7-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90aa7-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90aa7-145">CommonParameters</span></span>
<span data-ttu-id="90aa7-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90aa7-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90aa7-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90aa7-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90aa7-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="90aa7-148">INPUTS</span></span>

## <span data-ttu-id="90aa7-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="90aa7-149">OUTPUTS</span></span>

### <span data-ttu-id="90aa7-150">Microsoft. AzureStack. Management. abonnemang. admin. Models. erbjuda</span><span class="sxs-lookup"><span data-stu-id="90aa7-150">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="90aa7-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="90aa7-151">NOTES</span></span>

## <span data-ttu-id="90aa7-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="90aa7-152">RELATED LINKS</span></span>

