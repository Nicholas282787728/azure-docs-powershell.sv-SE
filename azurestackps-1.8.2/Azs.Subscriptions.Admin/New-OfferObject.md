---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5526ccd8fe050f9aa81974c8ea4ae1872125c087
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94099924"
---
# <span data-ttu-id="b0fda-101">New-OfferObject</span><span class="sxs-lookup"><span data-stu-id="b0fda-101">New-OfferObject</span></span>

## <span data-ttu-id="b0fda-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b0fda-102">SYNOPSIS</span></span>
<span data-ttu-id="b0fda-103">Representerar ett utbud av tjänster som ett abonnemang kan skapas för.</span><span class="sxs-lookup"><span data-stu-id="b0fda-103">Represents an offering of services against which a subscription can be created.</span></span>

## <span data-ttu-id="b0fda-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b0fda-104">SYNTAX</span></span>

```
New-OfferObject [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-Type] <String>] [[-MaxSubscriptionsPerAccount] <Int64>] [[-Name] <String>] [[-BasePlanIds] <String[]>]
 [[-DisplayName] <String>] [[-Description] <String>] [[-ExternalReferenceId] <String>] [[-State] <String>]
 [[-Id] <String>] [[-Location] <String>] [[-SubscriptionCount] <Int64>]
 [[-AddonPlanDefinition] <AddonPlanDefinition[]>] [<CommonParameters>]
```

## <span data-ttu-id="b0fda-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b0fda-105">DESCRIPTION</span></span>
<span data-ttu-id="b0fda-106">Representerar ett utbud av tjänster som ett abonnemang kan skapas för.</span><span class="sxs-lookup"><span data-stu-id="b0fda-106">Represents an offering of services against which a subscription can be created.</span></span>

## <span data-ttu-id="b0fda-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b0fda-107">EXAMPLES</span></span>

### <span data-ttu-id="b0fda-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b0fda-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="b0fda-109">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="b0fda-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="b0fda-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b0fda-110">PARAMETERS</span></span>

### <span data-ttu-id="b0fda-111">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="b0fda-111">-AddonPlanDefinition</span></span>
<span data-ttu-id="b0fda-112">Referenser till tilläggs planer som en klient organisation kan erhålla för att bli en del av det.</span><span class="sxs-lookup"><span data-stu-id="b0fda-112">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>

```yaml
Type: AddonPlanDefinition[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0fda-113">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="b0fda-113">-BasePlanIds</span></span>
<span data-ttu-id="b0fda-114">Identifierare för de grundläggande abonnemang som blir tillgängliga för klient organisationen omedelbart när en klient organisation abonnerar på ett bud.</span><span class="sxs-lookup"><span data-stu-id="b0fda-114">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0fda-115">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="b0fda-115">-Description</span></span>
<span data-ttu-id="b0fda-116">Beskrivning av bud.</span><span class="sxs-lookup"><span data-stu-id="b0fda-116">Description of offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0fda-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b0fda-117">-DisplayName</span></span>
<span data-ttu-id="b0fda-118">Visnings namn för bud.</span><span class="sxs-lookup"><span data-stu-id="b0fda-118">Display name of offer.</span></span>

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

### <span data-ttu-id="b0fda-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="b0fda-119">-ExternalReferenceId</span></span>
<span data-ttu-id="b0fda-120">Extern referens-ID.</span><span class="sxs-lookup"><span data-stu-id="b0fda-120">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0fda-121">-ID</span><span class="sxs-lookup"><span data-stu-id="b0fda-121">-Id</span></span>
<span data-ttu-id="b0fda-122">URI för resursen.</span><span class="sxs-lookup"><span data-stu-id="b0fda-122">URI of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0fda-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="b0fda-123">-Location</span></span>
<span data-ttu-id="b0fda-124">Plats där resursen är plats.</span><span class="sxs-lookup"><span data-stu-id="b0fda-124">Location where resource is location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0fda-125">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="b0fda-125">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="b0fda-126">Maximalt antal prenumerationer per konto.</span><span class="sxs-lookup"><span data-stu-id="b0fda-126">Maximum subscriptions per account.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0fda-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="b0fda-127">-Name</span></span>
<span data-ttu-id="b0fda-128">Namnet på resursen.</span><span class="sxs-lookup"><span data-stu-id="b0fda-128">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0fda-129">-State</span><span class="sxs-lookup"><span data-stu-id="b0fda-129">-State</span></span>
<span data-ttu-id="b0fda-130">Ge hjälpmedels status.</span><span class="sxs-lookup"><span data-stu-id="b0fda-130">Offer accessibility state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0fda-131">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="b0fda-131">-SubscriptionCount</span></span>
<span data-ttu-id="b0fda-132">Aktuellt antal prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="b0fda-132">Current subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0fda-133">-Taggar</span><span class="sxs-lookup"><span data-stu-id="b0fda-133">-Tags</span></span>
<span data-ttu-id="b0fda-134">Lista över par med nyckelord.</span><span class="sxs-lookup"><span data-stu-id="b0fda-134">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0fda-135">– Skriv</span><span class="sxs-lookup"><span data-stu-id="b0fda-135">-Type</span></span>
<span data-ttu-id="b0fda-136">Typ av resurs.</span><span class="sxs-lookup"><span data-stu-id="b0fda-136">Type of resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0fda-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0fda-137">CommonParameters</span></span>
<span data-ttu-id="b0fda-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0fda-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0fda-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0fda-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0fda-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b0fda-140">INPUTS</span></span>

## <span data-ttu-id="b0fda-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b0fda-141">OUTPUTS</span></span>

## <span data-ttu-id="b0fda-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b0fda-142">NOTES</span></span>

## <span data-ttu-id="b0fda-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b0fda-143">RELATED LINKS</span></span>

