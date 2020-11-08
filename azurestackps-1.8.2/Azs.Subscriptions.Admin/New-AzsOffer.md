---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cce59bbbef69f10f39478d784d688a4f1de312fb
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100096"
---
# <span data-ttu-id="59d4d-101">New-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="59d4d-101">New-AzsOffer</span></span>

## <span data-ttu-id="59d4d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="59d4d-102">SYNOPSIS</span></span>
<span data-ttu-id="59d4d-103">Skapar ett nytt bud.</span><span class="sxs-lookup"><span data-stu-id="59d4d-103">Creates a new offer.</span></span>

## <span data-ttu-id="59d4d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="59d4d-104">SYNTAX</span></span>

```
New-AzsOffer [-Name] <String> [-DisplayName] <String> [-ResourceGroupName] <String> [[-BasePlanIds] <String[]>]
 [[-Description] <String>] [[-ExternalReferenceId] <String>] [[-State] <String>] [[-Location] <String>]
 [[-MaxSubscriptionsPerAccount] <Int64>] [[-SubscriptionCount] <Int64>]
 [[-AddonPlanDefinition] <AddonPlanDefinition[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59d4d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="59d4d-105">DESCRIPTION</span></span>
<span data-ttu-id="59d4d-106">Skapa eller uppdatera ett bud.</span><span class="sxs-lookup"><span data-stu-id="59d4d-106">Create or update the offer.</span></span>

## <span data-ttu-id="59d4d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="59d4d-107">EXAMPLES</span></span>

### <span data-ttu-id="59d4d-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="59d4d-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsOffer -Name offer1 -ResourceGroupName rg1 -State Public -DisplayName "offer1" -BasePlanIds "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/plans/plan1"
```

<span data-ttu-id="59d4d-109">Skapar ett nytt bud.</span><span class="sxs-lookup"><span data-stu-id="59d4d-109">Creates a new offer.</span></span>

## <span data-ttu-id="59d4d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="59d4d-110">PARAMETERS</span></span>

### <span data-ttu-id="59d4d-111">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="59d4d-111">-AddonPlanDefinition</span></span>
<span data-ttu-id="59d4d-112">Referenser till tilläggs planer som en klient organisation kan erhålla för att bli en del av det.</span><span class="sxs-lookup"><span data-stu-id="59d4d-112">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>

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

### <span data-ttu-id="59d4d-113">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="59d4d-113">-BasePlanIds</span></span>
<span data-ttu-id="59d4d-114">Identifierare för de grundläggande abonnemang som blir tillgängliga för klient organisationen omedelbart när en klient organisation abonnerar på ett bud.</span><span class="sxs-lookup"><span data-stu-id="59d4d-114">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

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

### <span data-ttu-id="59d4d-115">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="59d4d-115">-Description</span></span>
<span data-ttu-id="59d4d-116">Beskrivning av bud.</span><span class="sxs-lookup"><span data-stu-id="59d4d-116">Description of offer.</span></span>

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

### <span data-ttu-id="59d4d-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="59d4d-117">-DisplayName</span></span>
<span data-ttu-id="59d4d-118">Visnings namn för bud.</span><span class="sxs-lookup"><span data-stu-id="59d4d-118">Display name of offer.</span></span>

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

### <span data-ttu-id="59d4d-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="59d4d-119">-ExternalReferenceId</span></span>
<span data-ttu-id="59d4d-120">Extern referens-ID.</span><span class="sxs-lookup"><span data-stu-id="59d4d-120">External reference identifier.</span></span>

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

### <span data-ttu-id="59d4d-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="59d4d-121">-Location</span></span>
<span data-ttu-id="59d4d-122">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="59d4d-122">Location of the resource.</span></span>

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

### <span data-ttu-id="59d4d-123">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="59d4d-123">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="59d4d-124">Maximalt antal prenumerationer per konto.</span><span class="sxs-lookup"><span data-stu-id="59d4d-124">Maximum subscriptions per account.</span></span>

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

### <span data-ttu-id="59d4d-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="59d4d-125">-Name</span></span>
<span data-ttu-id="59d4d-126">Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="59d4d-126">Name of an offer.</span></span>

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

### <span data-ttu-id="59d4d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59d4d-127">-ResourceGroupName</span></span>
<span data-ttu-id="59d4d-128">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="59d4d-128">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="59d4d-129">-State</span><span class="sxs-lookup"><span data-stu-id="59d4d-129">-State</span></span>
<span data-ttu-id="59d4d-130">Ge hjälpmedels status.</span><span class="sxs-lookup"><span data-stu-id="59d4d-130">Offer accessibility state.</span></span>
<span data-ttu-id="59d4d-131">Standardvärdet är Private.</span><span class="sxs-lookup"><span data-stu-id="59d4d-131">Default value is Private.</span></span>
<span data-ttu-id="59d4d-132">Den här parametern blir föråldrad i framtida versioner</span><span class="sxs-lookup"><span data-stu-id="59d4d-132">This parameter will be deprecated in a future release</span></span>

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

### <span data-ttu-id="59d4d-133">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="59d4d-133">-SubscriptionCount</span></span>
<span data-ttu-id="59d4d-134">Aktuellt antal prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="59d4d-134">Current subscription count.</span></span>

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

### <span data-ttu-id="59d4d-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="59d4d-135">-Confirm</span></span>
<span data-ttu-id="59d4d-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="59d4d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59d4d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59d4d-137">-WhatIf</span></span>
<span data-ttu-id="59d4d-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="59d4d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59d4d-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="59d4d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59d4d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59d4d-140">CommonParameters</span></span>
<span data-ttu-id="59d4d-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59d4d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59d4d-142">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59d4d-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59d4d-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="59d4d-143">INPUTS</span></span>

## <span data-ttu-id="59d4d-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="59d4d-144">OUTPUTS</span></span>

### <span data-ttu-id="59d4d-145">Microsoft. AzureStack. Management. abonnemang. admin. Models. erbjuda</span><span class="sxs-lookup"><span data-stu-id="59d4d-145">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="59d4d-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="59d4d-146">NOTES</span></span>

## <span data-ttu-id="59d4d-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="59d4d-147">RELATED LINKS</span></span>

