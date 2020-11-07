---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25bd0c892c8c5978493d855246be994bc96158db
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921776"
---
# <span data-ttu-id="dc193-101">Set-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="dc193-101">Set-AzsSubscription</span></span>

## <span data-ttu-id="dc193-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dc193-102">SYNOPSIS</span></span>
<span data-ttu-id="dc193-103">Skapa eller uppdatera ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="dc193-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="dc193-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dc193-104">SYNTAX</span></span>

### <span data-ttu-id="dc193-105">Ange (standard)</span><span class="sxs-lookup"><span data-stu-id="dc193-105">Set (Default)</span></span>
```
Set-AzsSubscription [-OfferId <String>] [-Type <String>]
 [-Tags <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -SubscriptionId <String>
 [-State <String>] [-TenantId <String>] [-DisplayName <String>] [-Location <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dc193-106">ID</span><span class="sxs-lookup"><span data-stu-id="dc193-106">ResourceId</span></span>
```
Set-AzsSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc193-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="dc193-107">InputObject</span></span>
```
Set-AzsSubscription -InputObject <SubscriptionModel> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc193-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dc193-108">DESCRIPTION</span></span>
<span data-ttu-id="dc193-109">Skapa eller uppdatera ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="dc193-109">Create or updates a subscription.</span></span>

## <span data-ttu-id="dc193-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dc193-110">EXAMPLES</span></span>

### <span data-ttu-id="dc193-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="dc193-111">EXAMPLE 1</span></span>
```
Set-AzsSubscription -SubscriptionId 2d9f5af9-3397-44fb-8700-d98762c2422a -DisplayName MyTestSub -State Enabled -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="dc193-112">Skapa eller uppdatera ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="dc193-112">Create or updates a subscription.</span></span>

## <span data-ttu-id="dc193-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dc193-113">PARAMETERS</span></span>

### <span data-ttu-id="dc193-114">-OfferId</span><span class="sxs-lookup"><span data-stu-id="dc193-114">-OfferId</span></span>
<span data-ttu-id="dc193-115">Identifierare för det som erbjuds under scopet för en delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="dc193-115">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="dc193-116">– Skriv</span><span class="sxs-lookup"><span data-stu-id="dc193-116">-Type</span></span>
<span data-ttu-id="dc193-117">Typ av resurs.</span><span class="sxs-lookup"><span data-stu-id="dc193-117">Type of resource.</span></span>

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

### <span data-ttu-id="dc193-118">-Taggar</span><span class="sxs-lookup"><span data-stu-id="dc193-118">-Tags</span></span>
<span data-ttu-id="dc193-119">Lista över par med nyckelord.</span><span class="sxs-lookup"><span data-stu-id="dc193-119">List of key-value pairs.</span></span>

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

### <span data-ttu-id="dc193-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dc193-120">-SubscriptionId</span></span>
<span data-ttu-id="dc193-121">Prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="dc193-121">Subscription identifier.</span></span>

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

### <span data-ttu-id="dc193-122">-State</span><span class="sxs-lookup"><span data-stu-id="dc193-122">-State</span></span>
<span data-ttu-id="dc193-123">Abonnemangs status.</span><span class="sxs-lookup"><span data-stu-id="dc193-123">Subscription state.</span></span>

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

### <span data-ttu-id="dc193-124">-TenantId</span><span class="sxs-lookup"><span data-stu-id="dc193-124">-TenantId</span></span>
<span data-ttu-id="dc193-125">Identifierare för katalog klient organisation.</span><span class="sxs-lookup"><span data-stu-id="dc193-125">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="dc193-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="dc193-126">-DisplayName</span></span>
<span data-ttu-id="dc193-127">Prenumerationens namn.</span><span class="sxs-lookup"><span data-stu-id="dc193-127">Subscription name.</span></span>

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

### <span data-ttu-id="dc193-128">-Plats</span><span class="sxs-lookup"><span data-stu-id="dc193-128">-Location</span></span>
<span data-ttu-id="dc193-129">Plats där resursen är plats.</span><span class="sxs-lookup"><span data-stu-id="dc193-129">Location where resource is location.</span></span>

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

### <span data-ttu-id="dc193-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc193-130">-ResourceId</span></span>
<span data-ttu-id="dc193-131">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="dc193-131">The resource ID.</span></span>

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

### <span data-ttu-id="dc193-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc193-132">-InputObject</span></span>
<span data-ttu-id="dc193-133">Posbbily ändrade nätverks kvot som returneras av Get-AzsNetworkQuota.</span><span class="sxs-lookup"><span data-stu-id="dc193-133">Posbbily modified network quota returned by Get-AzsNetworkQuota.</span></span>

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

### <span data-ttu-id="dc193-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc193-134">-WhatIf</span></span>
<span data-ttu-id="dc193-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dc193-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc193-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dc193-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc193-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dc193-137">-Confirm</span></span>
<span data-ttu-id="dc193-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dc193-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc193-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc193-139">CommonParameters</span></span>
<span data-ttu-id="dc193-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc193-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc193-141">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc193-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc193-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dc193-142">INPUTS</span></span>

## <span data-ttu-id="dc193-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dc193-143">OUTPUTS</span></span>

### <span data-ttu-id="dc193-144">Microsoft. AzureStack. Management. Subscription. Models. SubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="dc193-144">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="dc193-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dc193-145">NOTES</span></span>

## <span data-ttu-id="dc193-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dc193-146">RELATED LINKS</span></span>
