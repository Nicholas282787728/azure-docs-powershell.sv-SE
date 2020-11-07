---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cce59bbbef69f10f39478d784d688a4f1de312fb
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921664"
---
# <span data-ttu-id="0aab4-101">New-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="0aab4-101">New-AzsOffer</span></span>

## <span data-ttu-id="0aab4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0aab4-102">SYNOPSIS</span></span>
<span data-ttu-id="0aab4-103">Skapar ett nytt bud.</span><span class="sxs-lookup"><span data-stu-id="0aab4-103">Creates a new offer.</span></span>

## <span data-ttu-id="0aab4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0aab4-104">SYNTAX</span></span>

```
New-AzsOffer [-Name] <String> [-DisplayName] <String> [-ResourceGroupName] <String> [[-BasePlanIds] <String[]>]
 [[-Description] <String>] [[-ExternalReferenceId] <String>] [[-State] <String>] [[-Location] <String>]
 [[-MaxSubscriptionsPerAccount] <Int64>] [[-SubscriptionCount] <Int64>]
 [[-AddonPlanDefinition] <AddonPlanDefinition[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0aab4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0aab4-105">DESCRIPTION</span></span>
<span data-ttu-id="0aab4-106">Skapa eller uppdatera ett bud.</span><span class="sxs-lookup"><span data-stu-id="0aab4-106">Create or update the offer.</span></span>

## <span data-ttu-id="0aab4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0aab4-107">EXAMPLES</span></span>

### <span data-ttu-id="0aab4-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0aab4-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsOffer -Name offer1 -ResourceGroupName rg1 -State Public -DisplayName "offer1" -BasePlanIds "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/plans/plan1"
```

<span data-ttu-id="0aab4-109">Skapar ett nytt bud.</span><span class="sxs-lookup"><span data-stu-id="0aab4-109">Creates a new offer.</span></span>

## <span data-ttu-id="0aab4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0aab4-110">PARAMETERS</span></span>

### <span data-ttu-id="0aab4-111">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="0aab4-111">-AddonPlanDefinition</span></span>
<span data-ttu-id="0aab4-112">Referenser till tilläggs planer som en klient organisation kan erhålla för att bli en del av det.</span><span class="sxs-lookup"><span data-stu-id="0aab4-112">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>

```yaml
Type: AddonPlanDefinition[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aab4-113">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="0aab4-113">-BasePlanIds</span></span>
<span data-ttu-id="0aab4-114">Identifierare för de grundläggande abonnemang som blir tillgängliga för klient organisationen omedelbart när en klient organisation abonnerar på ett bud.</span><span class="sxs-lookup"><span data-stu-id="0aab4-114">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aab4-115">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="0aab4-115">-Description</span></span>
<span data-ttu-id="0aab4-116">Beskrivning av bud.</span><span class="sxs-lookup"><span data-stu-id="0aab4-116">Description of offer.</span></span>

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

### <span data-ttu-id="0aab4-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0aab4-117">-DisplayName</span></span>
<span data-ttu-id="0aab4-118">Visnings namn för bud.</span><span class="sxs-lookup"><span data-stu-id="0aab4-118">Display name of offer.</span></span>

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

### <span data-ttu-id="0aab4-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="0aab4-119">-ExternalReferenceId</span></span>
<span data-ttu-id="0aab4-120">Extern referens-ID.</span><span class="sxs-lookup"><span data-stu-id="0aab4-120">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aab4-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="0aab4-121">-Location</span></span>
<span data-ttu-id="0aab4-122">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="0aab4-122">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ArmLocation

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aab4-123">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="0aab4-123">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="0aab4-124">Maximalt antal prenumerationer per konto.</span><span class="sxs-lookup"><span data-stu-id="0aab4-124">Maximum subscriptions per account.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aab4-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="0aab4-125">-Name</span></span>
<span data-ttu-id="0aab4-126">Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="0aab4-126">Name of an offer.</span></span>

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

### <span data-ttu-id="0aab4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0aab4-127">-ResourceGroupName</span></span>
<span data-ttu-id="0aab4-128">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="0aab4-128">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="0aab4-129">-State</span><span class="sxs-lookup"><span data-stu-id="0aab4-129">-State</span></span>
<span data-ttu-id="0aab4-130">Ge hjälpmedels status.</span><span class="sxs-lookup"><span data-stu-id="0aab4-130">Offer accessibility state.</span></span>
<span data-ttu-id="0aab4-131">Standardvärdet är Private.</span><span class="sxs-lookup"><span data-stu-id="0aab4-131">Default value is Private.</span></span>
<span data-ttu-id="0aab4-132">Den här parametern blir föråldrad i framtida versioner</span><span class="sxs-lookup"><span data-stu-id="0aab4-132">This parameter will be deprecated in a future release</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: Private
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aab4-133">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="0aab4-133">-SubscriptionCount</span></span>
<span data-ttu-id="0aab4-134">Aktuellt antal prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="0aab4-134">Current subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aab4-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0aab4-135">-Confirm</span></span>
<span data-ttu-id="0aab4-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0aab4-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0aab4-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0aab4-137">-WhatIf</span></span>
<span data-ttu-id="0aab4-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0aab4-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0aab4-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0aab4-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0aab4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0aab4-140">CommonParameters</span></span>
<span data-ttu-id="0aab4-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0aab4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0aab4-142">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0aab4-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0aab4-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0aab4-143">INPUTS</span></span>

## <span data-ttu-id="0aab4-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0aab4-144">OUTPUTS</span></span>

### <span data-ttu-id="0aab4-145">Microsoft. AzureStack. Management. abonnemang. admin. Models. erbjuda</span><span class="sxs-lookup"><span data-stu-id="0aab4-145">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="0aab4-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0aab4-146">NOTES</span></span>

## <span data-ttu-id="0aab4-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0aab4-147">RELATED LINKS</span></span>

