---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ba118c80656676c47a2d6740ef7c0266fd491af6
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921487"
---
# <span data-ttu-id="48d66-101">New-SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="48d66-101">New-SubscriptionObject</span></span>

## <span data-ttu-id="48d66-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="48d66-102">SYNOPSIS</span></span>
<span data-ttu-id="48d66-103">Lista över funktioner som stöds.</span><span class="sxs-lookup"><span data-stu-id="48d66-103">List of supported operations.</span></span>

## <span data-ttu-id="48d66-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="48d66-104">SYNTAX</span></span>

```
New-SubscriptionObject [[-TenantId] <String>] [[-SubscriptionId] <String>] [[-DisplayName] <String>]
 [[-DelegatedProviderSubscriptionId] <String>] [[-Name] <String>] [[-Owner] <String>]
 [[-RoutingResourceManagerType] <String>] [[-ExternalReferenceId] <String>] [[-State] <String>]
 [[-Id] <String>] [[-OfferId] <String>] [<CommonParameters>]
```

## <span data-ttu-id="48d66-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="48d66-105">DESCRIPTION</span></span>
<span data-ttu-id="48d66-106">Lista över funktioner som stöds.</span><span class="sxs-lookup"><span data-stu-id="48d66-106">List of supported operations.</span></span>

## <span data-ttu-id="48d66-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="48d66-107">EXAMPLES</span></span>

### <span data-ttu-id="48d66-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="48d66-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="48d66-109">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="48d66-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="48d66-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="48d66-110">PARAMETERS</span></span>

### <span data-ttu-id="48d66-111">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="48d66-111">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="48d66-112">Överordnat abonnemang för DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="48d66-112">Parent DelegatedProvider subscription identifier.</span></span>

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

### <span data-ttu-id="48d66-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="48d66-113">-DisplayName</span></span>
<span data-ttu-id="48d66-114">Prenumerationens namn.</span><span class="sxs-lookup"><span data-stu-id="48d66-114">Subscription name.</span></span>

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

### <span data-ttu-id="48d66-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="48d66-115">-ExternalReferenceId</span></span>
<span data-ttu-id="48d66-116">Extern referens-ID.</span><span class="sxs-lookup"><span data-stu-id="48d66-116">External reference identifier.</span></span>

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

### <span data-ttu-id="48d66-117">-ID</span><span class="sxs-lookup"><span data-stu-id="48d66-117">-Id</span></span>
<span data-ttu-id="48d66-118">Fullständigt kvalificerad identifierare.</span><span class="sxs-lookup"><span data-stu-id="48d66-118">Fully qualified identifier.</span></span>

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

### <span data-ttu-id="48d66-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="48d66-119">-Name</span></span>
<span data-ttu-id="48d66-120">Namnet på resursen.</span><span class="sxs-lookup"><span data-stu-id="48d66-120">Name of the resource.</span></span>

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

### <span data-ttu-id="48d66-121">-OfferId</span><span class="sxs-lookup"><span data-stu-id="48d66-121">-OfferId</span></span>
<span data-ttu-id="48d66-122">Identifierare för det som erbjuds under scopet för en delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="48d66-122">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="48d66-123">-Owner</span><span class="sxs-lookup"><span data-stu-id="48d66-123">-Owner</span></span>
<span data-ttu-id="48d66-124">Abonnemangs ägare.</span><span class="sxs-lookup"><span data-stu-id="48d66-124">Subscription owner.</span></span>

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

### <span data-ttu-id="48d66-125">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="48d66-125">-RoutingResourceManagerType</span></span>
<span data-ttu-id="48d66-126">Routning Resource Manager-typ.</span><span class="sxs-lookup"><span data-stu-id="48d66-126">Routing resource manager type.</span></span>

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

### <span data-ttu-id="48d66-127">-State</span><span class="sxs-lookup"><span data-stu-id="48d66-127">-State</span></span>
<span data-ttu-id="48d66-128">Abonnemangs status.</span><span class="sxs-lookup"><span data-stu-id="48d66-128">Subscription state.</span></span>

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

### <span data-ttu-id="48d66-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="48d66-129">-SubscriptionId</span></span>
<span data-ttu-id="48d66-130">Prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="48d66-130">Subscription identifier.</span></span>

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

### <span data-ttu-id="48d66-131">-TenantId</span><span class="sxs-lookup"><span data-stu-id="48d66-131">-TenantId</span></span>
<span data-ttu-id="48d66-132">Identifierare för katalog klient organisation.</span><span class="sxs-lookup"><span data-stu-id="48d66-132">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="48d66-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48d66-133">CommonParameters</span></span>
<span data-ttu-id="48d66-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48d66-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48d66-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48d66-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48d66-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="48d66-136">INPUTS</span></span>

## <span data-ttu-id="48d66-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="48d66-137">OUTPUTS</span></span>

## <span data-ttu-id="48d66-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="48d66-138">NOTES</span></span>

## <span data-ttu-id="48d66-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="48d66-139">RELATED LINKS</span></span>

