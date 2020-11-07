---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6e6588eed555062aaf6dbb4075dffd9506c05503
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921782"
---
# <span data-ttu-id="2c9fb-101">Remove-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="2c9fb-101">Remove-AzsSubscription</span></span>

## <span data-ttu-id="2c9fb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2c9fb-102">SYNOPSIS</span></span>
<span data-ttu-id="2c9fb-103">Ta bort det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="2c9fb-103">Delete the specifed subscription.</span></span>

## <span data-ttu-id="2c9fb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2c9fb-104">SYNTAX</span></span>

```
Remove-AzsSubscription [-SubscriptionId] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c9fb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2c9fb-105">DESCRIPTION</span></span>
<span data-ttu-id="2c9fb-106">Ta bort det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="2c9fb-106">Delete the specifed subscription.</span></span>

## <span data-ttu-id="2c9fb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2c9fb-107">EXAMPLES</span></span>

### <span data-ttu-id="2c9fb-108">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="2c9fb-108">EXAMPLE 1</span></span>
```
Remove-AzsSubscription -SubscriptionId d387f779-85d8-40b6-8607-8306295ebff9
```

<span data-ttu-id="2c9fb-109">Ta bort det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="2c9fb-109">Delete the specifed subscription.</span></span>

## <span data-ttu-id="2c9fb-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2c9fb-110">PARAMETERS</span></span>

### <span data-ttu-id="2c9fb-111">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2c9fb-111">-SubscriptionId</span></span>
<span data-ttu-id="2c9fb-112">ID för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="2c9fb-112">Id of the subscription.</span></span>

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

### <span data-ttu-id="2c9fb-113">-Force</span><span class="sxs-lookup"><span data-stu-id="2c9fb-113">-Force</span></span>
<span data-ttu-id="2c9fb-114">Ta bort abonnemang utan att fråga</span><span class="sxs-lookup"><span data-stu-id="2c9fb-114">Remove subscription without prompting</span></span>

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

### <span data-ttu-id="2c9fb-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c9fb-115">-WhatIf</span></span>
<span data-ttu-id="2c9fb-116">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2c9fb-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c9fb-117">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2c9fb-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c9fb-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2c9fb-118">-Confirm</span></span>
<span data-ttu-id="2c9fb-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2c9fb-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c9fb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c9fb-120">CommonParameters</span></span>
<span data-ttu-id="2c9fb-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c9fb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c9fb-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c9fb-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c9fb-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2c9fb-123">INPUTS</span></span>

## <span data-ttu-id="2c9fb-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2c9fb-124">OUTPUTS</span></span>

## <span data-ttu-id="2c9fb-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2c9fb-125">NOTES</span></span>

## <span data-ttu-id="2c9fb-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2c9fb-126">RELATED LINKS</span></span>
