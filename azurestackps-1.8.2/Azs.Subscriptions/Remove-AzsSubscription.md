---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6e6588eed555062aaf6dbb4075dffd9506c05503
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100175"
---
# <span data-ttu-id="ad3ea-101">Remove-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="ad3ea-101">Remove-AzsSubscription</span></span>

## <span data-ttu-id="ad3ea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ad3ea-102">SYNOPSIS</span></span>
<span data-ttu-id="ad3ea-103">Ta bort det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="ad3ea-103">Delete the specifed subscription.</span></span>

## <span data-ttu-id="ad3ea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ad3ea-104">SYNTAX</span></span>

```
Remove-AzsSubscription [-SubscriptionId] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad3ea-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ad3ea-105">DESCRIPTION</span></span>
<span data-ttu-id="ad3ea-106">Ta bort det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="ad3ea-106">Delete the specifed subscription.</span></span>

## <span data-ttu-id="ad3ea-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ad3ea-107">EXAMPLES</span></span>

### <span data-ttu-id="ad3ea-108">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="ad3ea-108">EXAMPLE 1</span></span>
```
Remove-AzsSubscription -SubscriptionId d387f779-85d8-40b6-8607-8306295ebff9
```

<span data-ttu-id="ad3ea-109">Ta bort det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="ad3ea-109">Delete the specifed subscription.</span></span>

## <span data-ttu-id="ad3ea-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ad3ea-110">PARAMETERS</span></span>

### <span data-ttu-id="ad3ea-111">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ad3ea-111">-SubscriptionId</span></span>
<span data-ttu-id="ad3ea-112">ID för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="ad3ea-112">Id of the subscription.</span></span>

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

### <span data-ttu-id="ad3ea-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ad3ea-113">-Force</span></span>
<span data-ttu-id="ad3ea-114">Ta bort abonnemang utan att fråga</span><span class="sxs-lookup"><span data-stu-id="ad3ea-114">Remove subscription without prompting</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad3ea-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad3ea-115">-WhatIf</span></span>
<span data-ttu-id="ad3ea-116">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ad3ea-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad3ea-117">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ad3ea-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad3ea-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ad3ea-118">-Confirm</span></span>
<span data-ttu-id="ad3ea-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ad3ea-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad3ea-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad3ea-120">CommonParameters</span></span>
<span data-ttu-id="ad3ea-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad3ea-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad3ea-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad3ea-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad3ea-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ad3ea-123">INPUTS</span></span>

## <span data-ttu-id="ad3ea-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ad3ea-124">OUTPUTS</span></span>

## <span data-ttu-id="ad3ea-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ad3ea-125">NOTES</span></span>

## <span data-ttu-id="ad3ea-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ad3ea-126">RELATED LINKS</span></span>
