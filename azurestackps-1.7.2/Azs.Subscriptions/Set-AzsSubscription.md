---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb23765090b0edfd14fa355b9809a2385900396e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921265"
---
# <span data-ttu-id="ed15b-101">Set-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="ed15b-101">Set-AzsSubscription</span></span>

## <span data-ttu-id="ed15b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ed15b-102">SYNOPSIS</span></span>
<span data-ttu-id="ed15b-103">Skapa eller uppdatera ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="ed15b-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="ed15b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ed15b-104">SYNTAX</span></span>

### <span data-ttu-id="ed15b-105">Ange (standard)</span><span class="sxs-lookup"><span data-stu-id="ed15b-105">Set (Default)</span></span>
```
Set-AzsSubscription [-OfferId <String>] [-Type <String>]
 [-Tags <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -SubscriptionId <String>
 [-State <String>] [-TenantId <String>] [-DisplayName <String>] [-Location <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ed15b-106">ID</span><span class="sxs-lookup"><span data-stu-id="ed15b-106">ResourceId</span></span>
```
Set-AzsSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed15b-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="ed15b-107">InputObject</span></span>
```
Set-AzsSubscription -InputObject <SubscriptionModel> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed15b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ed15b-108">DESCRIPTION</span></span>
<span data-ttu-id="ed15b-109">Skapa eller uppdatera ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="ed15b-109">Create or updates a subscription.</span></span>

## <span data-ttu-id="ed15b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ed15b-110">EXAMPLES</span></span>

### <span data-ttu-id="ed15b-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ed15b-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsSubscription -SubscriptionId 2d9f5af9-3397-44fb-8700-d98762c2422a -DisplayName MyTestSub -State Enabled -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="ed15b-112">Skapa eller uppdatera ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="ed15b-112">Create or updates a subscription.</span></span>

## <span data-ttu-id="ed15b-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ed15b-113">PARAMETERS</span></span>

### <span data-ttu-id="ed15b-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ed15b-114">-DisplayName</span></span>
<span data-ttu-id="ed15b-115">Prenumerationens namn.</span><span class="sxs-lookup"><span data-stu-id="ed15b-115">Subscription name.</span></span>

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

### <span data-ttu-id="ed15b-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed15b-116">-InputObject</span></span>
<span data-ttu-id="ed15b-117">Posbbily ändrade nätverks kvot som returneras av Get-AzsNetworkQuota.</span><span class="sxs-lookup"><span data-stu-id="ed15b-117">Posbbily modified network quota returned by Get-AzsNetworkQuota.</span></span>

```yaml
Type: SubscriptionModel
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed15b-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="ed15b-118">-Location</span></span>
<span data-ttu-id="ed15b-119">Plats där resursen är plats.</span><span class="sxs-lookup"><span data-stu-id="ed15b-119">Location where resource is location.</span></span>

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

### <span data-ttu-id="ed15b-120">-OfferId</span><span class="sxs-lookup"><span data-stu-id="ed15b-120">-OfferId</span></span>
<span data-ttu-id="ed15b-121">Identifierare för det som erbjuds under scopet för en delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="ed15b-121">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="ed15b-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed15b-122">-ResourceId</span></span>
<span data-ttu-id="ed15b-123">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="ed15b-123">The resource ID.</span></span>

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

### <span data-ttu-id="ed15b-124">-State</span><span class="sxs-lookup"><span data-stu-id="ed15b-124">-State</span></span>
<span data-ttu-id="ed15b-125">Abonnemangs status.</span><span class="sxs-lookup"><span data-stu-id="ed15b-125">Subscription state.</span></span>

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

### <span data-ttu-id="ed15b-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ed15b-126">-SubscriptionId</span></span>
<span data-ttu-id="ed15b-127">Prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="ed15b-127">Subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed15b-128">-Taggar</span><span class="sxs-lookup"><span data-stu-id="ed15b-128">-Tags</span></span>
<span data-ttu-id="ed15b-129">Lista över par med nyckelord.</span><span class="sxs-lookup"><span data-stu-id="ed15b-129">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed15b-130">-TenantId</span><span class="sxs-lookup"><span data-stu-id="ed15b-130">-TenantId</span></span>
<span data-ttu-id="ed15b-131">Identifierare för katalog klient organisation.</span><span class="sxs-lookup"><span data-stu-id="ed15b-131">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="ed15b-132">– Skriv</span><span class="sxs-lookup"><span data-stu-id="ed15b-132">-Type</span></span>
<span data-ttu-id="ed15b-133">Typ av resurs.</span><span class="sxs-lookup"><span data-stu-id="ed15b-133">Type of resource.</span></span>

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

### <span data-ttu-id="ed15b-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ed15b-134">-Confirm</span></span>
<span data-ttu-id="ed15b-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ed15b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed15b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed15b-136">-WhatIf</span></span>
<span data-ttu-id="ed15b-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ed15b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed15b-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ed15b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed15b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed15b-139">CommonParameters</span></span>
<span data-ttu-id="ed15b-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed15b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed15b-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed15b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed15b-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ed15b-142">INPUTS</span></span>

## <span data-ttu-id="ed15b-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ed15b-143">OUTPUTS</span></span>

### <span data-ttu-id="ed15b-144">Microsoft. AzureStack. Management. Subscription. Models. SubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="ed15b-144">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="ed15b-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ed15b-145">NOTES</span></span>

## <span data-ttu-id="ed15b-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ed15b-146">RELATED LINKS</span></span>
