---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25bd0c892c8c5978493d855246be994bc96158db
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100176"
---
# <span data-ttu-id="abc65-101">Set-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="abc65-101">Set-AzsSubscription</span></span>

## <span data-ttu-id="abc65-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="abc65-102">SYNOPSIS</span></span>
<span data-ttu-id="abc65-103">Skapa eller uppdatera ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="abc65-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="abc65-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="abc65-104">SYNTAX</span></span>

### <span data-ttu-id="abc65-105">Ange (standard)</span><span class="sxs-lookup"><span data-stu-id="abc65-105">Set (Default)</span></span>
```
Set-AzsSubscription [-OfferId <String>] [-Type <String>]
 [-Tags <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -SubscriptionId <String>
 [-State <String>] [-TenantId <String>] [-DisplayName <String>] [-Location <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="abc65-106">ID</span><span class="sxs-lookup"><span data-stu-id="abc65-106">ResourceId</span></span>
```
Set-AzsSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abc65-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="abc65-107">InputObject</span></span>
```
Set-AzsSubscription -InputObject <SubscriptionModel> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abc65-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="abc65-108">DESCRIPTION</span></span>
<span data-ttu-id="abc65-109">Skapa eller uppdatera ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="abc65-109">Create or updates a subscription.</span></span>

## <span data-ttu-id="abc65-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="abc65-110">EXAMPLES</span></span>

### <span data-ttu-id="abc65-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="abc65-111">EXAMPLE 1</span></span>
```
Set-AzsSubscription -SubscriptionId 2d9f5af9-3397-44fb-8700-d98762c2422a -DisplayName MyTestSub -State Enabled -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="abc65-112">Skapa eller uppdatera ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="abc65-112">Create or updates a subscription.</span></span>

## <span data-ttu-id="abc65-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="abc65-113">PARAMETERS</span></span>

### <span data-ttu-id="abc65-114">-OfferId</span><span class="sxs-lookup"><span data-stu-id="abc65-114">-OfferId</span></span>
<span data-ttu-id="abc65-115">Identifierare för det som erbjuds under scopet för en delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="abc65-115">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="abc65-116">– Skriv</span><span class="sxs-lookup"><span data-stu-id="abc65-116">-Type</span></span>
<span data-ttu-id="abc65-117">Typ av resurs.</span><span class="sxs-lookup"><span data-stu-id="abc65-117">Type of resource.</span></span>

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

### <span data-ttu-id="abc65-118">-Taggar</span><span class="sxs-lookup"><span data-stu-id="abc65-118">-Tags</span></span>
<span data-ttu-id="abc65-119">Lista över par med nyckelord.</span><span class="sxs-lookup"><span data-stu-id="abc65-119">List of key-value pairs.</span></span>

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

### <span data-ttu-id="abc65-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="abc65-120">-SubscriptionId</span></span>
<span data-ttu-id="abc65-121">Prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="abc65-121">Subscription identifier.</span></span>

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

### <span data-ttu-id="abc65-122">-State</span><span class="sxs-lookup"><span data-stu-id="abc65-122">-State</span></span>
<span data-ttu-id="abc65-123">Abonnemangs status.</span><span class="sxs-lookup"><span data-stu-id="abc65-123">Subscription state.</span></span>

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

### <span data-ttu-id="abc65-124">-TenantId</span><span class="sxs-lookup"><span data-stu-id="abc65-124">-TenantId</span></span>
<span data-ttu-id="abc65-125">Identifierare för katalog klient organisation.</span><span class="sxs-lookup"><span data-stu-id="abc65-125">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="abc65-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="abc65-126">-DisplayName</span></span>
<span data-ttu-id="abc65-127">Prenumerationens namn.</span><span class="sxs-lookup"><span data-stu-id="abc65-127">Subscription name.</span></span>

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

### <span data-ttu-id="abc65-128">-Plats</span><span class="sxs-lookup"><span data-stu-id="abc65-128">-Location</span></span>
<span data-ttu-id="abc65-129">Plats där resursen är plats.</span><span class="sxs-lookup"><span data-stu-id="abc65-129">Location where resource is location.</span></span>

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

### <span data-ttu-id="abc65-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="abc65-130">-ResourceId</span></span>
<span data-ttu-id="abc65-131">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="abc65-131">The resource ID.</span></span>

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

### <span data-ttu-id="abc65-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="abc65-132">-InputObject</span></span>
<span data-ttu-id="abc65-133">Posbbily ändrade nätverks kvot som returneras av Get-AzsNetworkQuota.</span><span class="sxs-lookup"><span data-stu-id="abc65-133">Posbbily modified network quota returned by Get-AzsNetworkQuota.</span></span>

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

### <span data-ttu-id="abc65-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abc65-134">-WhatIf</span></span>
<span data-ttu-id="abc65-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="abc65-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abc65-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="abc65-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abc65-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="abc65-137">-Confirm</span></span>
<span data-ttu-id="abc65-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="abc65-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abc65-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abc65-139">CommonParameters</span></span>
<span data-ttu-id="abc65-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abc65-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abc65-141">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abc65-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abc65-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="abc65-142">INPUTS</span></span>

## <span data-ttu-id="abc65-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="abc65-143">OUTPUTS</span></span>

### <span data-ttu-id="abc65-144">Microsoft. AzureStack. Management. Subscription. Models. SubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="abc65-144">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="abc65-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="abc65-145">NOTES</span></span>

## <span data-ttu-id="abc65-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="abc65-146">RELATED LINKS</span></span>
