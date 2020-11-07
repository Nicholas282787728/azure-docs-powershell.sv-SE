---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8ea8b09e956410184dbc2dd2ed7fa8fc8b89c69b
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921489"
---
# <span data-ttu-id="b81e3-101">New-OfferDelegationObject</span><span class="sxs-lookup"><span data-stu-id="b81e3-101">New-OfferDelegationObject</span></span>

## <span data-ttu-id="b81e3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b81e3-102">SYNOPSIS</span></span>
<span data-ttu-id="b81e3-103">Ge ombud.</span><span class="sxs-lookup"><span data-stu-id="b81e3-103">Offer delegation.</span></span>

## <span data-ttu-id="b81e3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b81e3-104">SYNTAX</span></span>

```
New-OfferDelegationObject [[-Id] <String>] [[-Type] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [[-SubscriptionId] <String>]
 [[-Name] <String>] [[-Location] <String>] [<CommonParameters>]
```

## <span data-ttu-id="b81e3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b81e3-105">DESCRIPTION</span></span>
<span data-ttu-id="b81e3-106">Ge ombud.</span><span class="sxs-lookup"><span data-stu-id="b81e3-106">Offer delegation.</span></span>

## <span data-ttu-id="b81e3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b81e3-107">EXAMPLES</span></span>

### <span data-ttu-id="b81e3-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b81e3-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="b81e3-109">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="b81e3-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="b81e3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b81e3-110">PARAMETERS</span></span>

### <span data-ttu-id="b81e3-111">-ID</span><span class="sxs-lookup"><span data-stu-id="b81e3-111">-Id</span></span>
<span data-ttu-id="b81e3-112">URI för resursen.</span><span class="sxs-lookup"><span data-stu-id="b81e3-112">URI of the resource.</span></span>

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

### <span data-ttu-id="b81e3-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="b81e3-113">-Location</span></span>
<span data-ttu-id="b81e3-114">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="b81e3-114">Location of the resource.</span></span>

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

### <span data-ttu-id="b81e3-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="b81e3-115">-Name</span></span>
<span data-ttu-id="b81e3-116">Namnet på resursen.</span><span class="sxs-lookup"><span data-stu-id="b81e3-116">Name of the resource.</span></span>

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

### <span data-ttu-id="b81e3-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b81e3-117">-SubscriptionId</span></span>
<span data-ttu-id="b81e3-118">ID för det abonnemang som tar emot det delegerade erbjudandet.</span><span class="sxs-lookup"><span data-stu-id="b81e3-118">Identifier of the subscription receiving the delegated offer.</span></span>

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

### <span data-ttu-id="b81e3-119">-Taggar</span><span class="sxs-lookup"><span data-stu-id="b81e3-119">-Tags</span></span>
<span data-ttu-id="b81e3-120">Lista över par med nyckelord.</span><span class="sxs-lookup"><span data-stu-id="b81e3-120">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b81e3-121">– Skriv</span><span class="sxs-lookup"><span data-stu-id="b81e3-121">-Type</span></span>
<span data-ttu-id="b81e3-122">Typ av resurs.</span><span class="sxs-lookup"><span data-stu-id="b81e3-122">Type of resource.</span></span>

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

### <span data-ttu-id="b81e3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b81e3-123">CommonParameters</span></span>
<span data-ttu-id="b81e3-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b81e3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b81e3-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b81e3-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b81e3-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b81e3-126">INPUTS</span></span>

## <span data-ttu-id="b81e3-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b81e3-127">OUTPUTS</span></span>

## <span data-ttu-id="b81e3-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b81e3-128">NOTES</span></span>

## <span data-ttu-id="b81e3-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b81e3-129">RELATED LINKS</span></span>

