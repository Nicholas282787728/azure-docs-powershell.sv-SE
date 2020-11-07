---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 04c79f659f2dcf1d4100151ff0506722482aaad5
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921315"
---
# <span data-ttu-id="ff4bb-101">New-PlanObject</span><span class="sxs-lookup"><span data-stu-id="ff4bb-101">New-PlanObject</span></span>

## <span data-ttu-id="ff4bb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ff4bb-102">SYNOPSIS</span></span>
<span data-ttu-id="ff4bb-103">En plan representerar ett paket med kvoter och funktioner som erbjuds klient organisationer.</span><span class="sxs-lookup"><span data-stu-id="ff4bb-103">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="ff4bb-104">En klient organisation kan erhålla detta abonnemang via ett anbud för att uppgradera hans åtkomst till underliggande moln tjänster.</span><span class="sxs-lookup"><span data-stu-id="ff4bb-104">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>

## <span data-ttu-id="ff4bb-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ff4bb-105">SYNTAX</span></span>

```
New-PlanObject [[-Description] <String>] [[-Id] <String>] [[-Type] <String>] [[-SkuIds] <String[]>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-ExternalReferenceId] <String>] [[-Name] <String>] [[-DisplayName] <String>] [[-Location] <String>]
 [[-QuotaIds] <String[]>] [[-SubscriptionCount] <Int64>] [<CommonParameters>]
```

## <span data-ttu-id="ff4bb-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ff4bb-106">DESCRIPTION</span></span>
<span data-ttu-id="ff4bb-107">En plan representerar ett paket med kvoter och funktioner som erbjuds klient organisationer.</span><span class="sxs-lookup"><span data-stu-id="ff4bb-107">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="ff4bb-108">En klient organisation kan erhålla detta abonnemang via ett anbud för att uppgradera hans åtkomst till underliggande moln tjänster.</span><span class="sxs-lookup"><span data-stu-id="ff4bb-108">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>

## <span data-ttu-id="ff4bb-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ff4bb-109">EXAMPLES</span></span>

### <span data-ttu-id="ff4bb-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ff4bb-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="ff4bb-111">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="ff4bb-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="ff4bb-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ff4bb-112">PARAMETERS</span></span>

### <span data-ttu-id="ff4bb-113">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="ff4bb-113">-Description</span></span>
<span data-ttu-id="ff4bb-114">Beskrivning av planen.</span><span class="sxs-lookup"><span data-stu-id="ff4bb-114">Description of the plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff4bb-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ff4bb-115">-DisplayName</span></span>
<span data-ttu-id="ff4bb-116">Visnings namn.</span><span class="sxs-lookup"><span data-stu-id="ff4bb-116">Display name.</span></span>

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

### <span data-ttu-id="ff4bb-117">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="ff4bb-117">-ExternalReferenceId</span></span>
<span data-ttu-id="ff4bb-118">Extern referens-ID.</span><span class="sxs-lookup"><span data-stu-id="ff4bb-118">External reference identifier.</span></span>

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

### <span data-ttu-id="ff4bb-119">-ID</span><span class="sxs-lookup"><span data-stu-id="ff4bb-119">-Id</span></span>
<span data-ttu-id="ff4bb-120">URI för resursen.</span><span class="sxs-lookup"><span data-stu-id="ff4bb-120">URI of the resource.</span></span>

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

### <span data-ttu-id="ff4bb-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="ff4bb-121">-Location</span></span>
<span data-ttu-id="ff4bb-122">Plats där resursen är plats.</span><span class="sxs-lookup"><span data-stu-id="ff4bb-122">Location where resource is location.</span></span>

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

### <span data-ttu-id="ff4bb-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="ff4bb-123">-Name</span></span>
<span data-ttu-id="ff4bb-124">Namnet på resursen.</span><span class="sxs-lookup"><span data-stu-id="ff4bb-124">Name of the resource.</span></span>

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

### <span data-ttu-id="ff4bb-125">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="ff4bb-125">-QuotaIds</span></span>
<span data-ttu-id="ff4bb-126">Kvot-ID: n under abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="ff4bb-126">Quota identifiers under the plan.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff4bb-127">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="ff4bb-127">-SkuIds</span></span>
<span data-ttu-id="ff4bb-128">SKU-identifierare.</span><span class="sxs-lookup"><span data-stu-id="ff4bb-128">SKU identifiers.</span></span>

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

### <span data-ttu-id="ff4bb-129">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="ff4bb-129">-SubscriptionCount</span></span>
<span data-ttu-id="ff4bb-130">Antal prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="ff4bb-130">Subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff4bb-131">-Taggar</span><span class="sxs-lookup"><span data-stu-id="ff4bb-131">-Tags</span></span>
<span data-ttu-id="ff4bb-132">Lista över par med nyckelord.</span><span class="sxs-lookup"><span data-stu-id="ff4bb-132">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff4bb-133">– Skriv</span><span class="sxs-lookup"><span data-stu-id="ff4bb-133">-Type</span></span>
<span data-ttu-id="ff4bb-134">Typ av resurs.</span><span class="sxs-lookup"><span data-stu-id="ff4bb-134">Type of resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff4bb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff4bb-135">CommonParameters</span></span>
<span data-ttu-id="ff4bb-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff4bb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff4bb-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff4bb-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff4bb-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ff4bb-138">INPUTS</span></span>

## <span data-ttu-id="ff4bb-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ff4bb-139">OUTPUTS</span></span>

## <span data-ttu-id="ff4bb-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ff4bb-140">NOTES</span></span>

## <span data-ttu-id="ff4bb-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ff4bb-141">RELATED LINKS</span></span>

