---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25bd0c892c8c5978493d855246be994bc96158db
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921299"
---
# <span data-ttu-id="4f0a3-101">Set-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="4f0a3-101">Set-AzsSubscription</span></span>

## <span data-ttu-id="4f0a3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4f0a3-102">SYNOPSIS</span></span>
<span data-ttu-id="4f0a3-103">Skapa eller uppdatera ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="4f0a3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4f0a3-104">SYNTAX</span></span>

### <span data-ttu-id="4f0a3-105">Ange (standard)</span><span class="sxs-lookup"><span data-stu-id="4f0a3-105">Set (Default)</span></span>
```
Set-AzsSubscription [-OfferId <String>] [-Type <String>]
 [-Tags <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -SubscriptionId <String>
 [-State <String>] [-TenantId <String>] [-DisplayName <String>] [-Location <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4f0a3-106">ID</span><span class="sxs-lookup"><span data-stu-id="4f0a3-106">ResourceId</span></span>
```
Set-AzsSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f0a3-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="4f0a3-107">InputObject</span></span>
```
Set-AzsSubscription -InputObject <SubscriptionModel> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f0a3-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4f0a3-108">DESCRIPTION</span></span>
<span data-ttu-id="4f0a3-109">Skapa eller uppdatera ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-109">Create or updates a subscription.</span></span>

## <span data-ttu-id="4f0a3-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4f0a3-110">EXAMPLES</span></span>

### <span data-ttu-id="4f0a3-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="4f0a3-111">EXAMPLE 1</span></span>
```
Set-AzsSubscription -SubscriptionId 2d9f5af9-3397-44fb-8700-d98762c2422a -DisplayName MyTestSub -State Enabled -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="4f0a3-112">Skapa eller uppdatera ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-112">Create or updates a subscription.</span></span>

## <span data-ttu-id="4f0a3-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4f0a3-113">PARAMETERS</span></span>

### <span data-ttu-id="4f0a3-114">-OfferId</span><span class="sxs-lookup"><span data-stu-id="4f0a3-114">-OfferId</span></span>
<span data-ttu-id="4f0a3-115">Identifierare för det som erbjuds under scopet för en delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-115">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="4f0a3-116">– Skriv</span><span class="sxs-lookup"><span data-stu-id="4f0a3-116">-Type</span></span>
<span data-ttu-id="4f0a3-117">Typ av resurs.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-117">Type of resource.</span></span>

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

### <span data-ttu-id="4f0a3-118">-Taggar</span><span class="sxs-lookup"><span data-stu-id="4f0a3-118">-Tags</span></span>
<span data-ttu-id="4f0a3-119">Lista över par med nyckelord.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-119">List of key-value pairs.</span></span>

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

### <span data-ttu-id="4f0a3-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4f0a3-120">-SubscriptionId</span></span>
<span data-ttu-id="4f0a3-121">Prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-121">Subscription identifier.</span></span>

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

### <span data-ttu-id="4f0a3-122">-State</span><span class="sxs-lookup"><span data-stu-id="4f0a3-122">-State</span></span>
<span data-ttu-id="4f0a3-123">Abonnemangs status.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-123">Subscription state.</span></span>

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

### <span data-ttu-id="4f0a3-124">-TenantId</span><span class="sxs-lookup"><span data-stu-id="4f0a3-124">-TenantId</span></span>
<span data-ttu-id="4f0a3-125">Identifierare för katalog klient organisation.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-125">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="4f0a3-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4f0a3-126">-DisplayName</span></span>
<span data-ttu-id="4f0a3-127">Prenumerationens namn.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-127">Subscription name.</span></span>

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

### <span data-ttu-id="4f0a3-128">-Plats</span><span class="sxs-lookup"><span data-stu-id="4f0a3-128">-Location</span></span>
<span data-ttu-id="4f0a3-129">Plats där resursen är plats.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-129">Location where resource is location.</span></span>

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

### <span data-ttu-id="4f0a3-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f0a3-130">-ResourceId</span></span>
<span data-ttu-id="4f0a3-131">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-131">The resource ID.</span></span>

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

### <span data-ttu-id="4f0a3-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f0a3-132">-InputObject</span></span>
<span data-ttu-id="4f0a3-133">Posbbily ändrade nätverks kvot som returneras av Get-AzsNetworkQuota.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-133">Posbbily modified network quota returned by Get-AzsNetworkQuota.</span></span>

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

### <span data-ttu-id="4f0a3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f0a3-134">-WhatIf</span></span>
<span data-ttu-id="4f0a3-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f0a3-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f0a3-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4f0a3-137">-Confirm</span></span>
<span data-ttu-id="4f0a3-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f0a3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f0a3-139">CommonParameters</span></span>
<span data-ttu-id="4f0a3-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f0a3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f0a3-141">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f0a3-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f0a3-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4f0a3-142">INPUTS</span></span>

## <span data-ttu-id="4f0a3-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4f0a3-143">OUTPUTS</span></span>

### <span data-ttu-id="4f0a3-144">Microsoft. AzureStack. Management. Subscription. Models. SubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="4f0a3-144">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="4f0a3-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4f0a3-145">NOTES</span></span>

## <span data-ttu-id="4f0a3-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4f0a3-146">RELATED LINKS</span></span>
