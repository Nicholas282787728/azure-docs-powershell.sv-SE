---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: fdceee36319d1c9ea950dbf5573b4ba0e3c614ee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572216"
---
# <span data-ttu-id="78b79-101">Remove-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="78b79-101">Remove-AzsSubscription</span></span>

## <span data-ttu-id="78b79-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="78b79-102">SYNOPSIS</span></span>
<span data-ttu-id="78b79-103">Ta bort det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="78b79-103">Delete the specifed subscription.</span></span>

## <span data-ttu-id="78b79-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="78b79-104">SYNTAX</span></span>

```
Remove-AzsSubscription [-SubscriptionId] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78b79-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="78b79-105">DESCRIPTION</span></span>
<span data-ttu-id="78b79-106">Ta bort det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="78b79-106">Delete the specifed subscription.</span></span>

## <span data-ttu-id="78b79-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="78b79-107">EXAMPLES</span></span>

### <span data-ttu-id="78b79-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="78b79-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsSubscription -SubscriptionId d387f779-85d8-40b6-8607-8306295ebff9
```

<span data-ttu-id="78b79-109">Ta bort det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="78b79-109">Delete the specifed subscription.</span></span>

## <span data-ttu-id="78b79-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="78b79-110">PARAMETERS</span></span>

### <span data-ttu-id="78b79-111">-Force</span><span class="sxs-lookup"><span data-stu-id="78b79-111">-Force</span></span>
<span data-ttu-id="78b79-112">Ta bort abonnemang utan att fråga</span><span class="sxs-lookup"><span data-stu-id="78b79-112">Remove subscription without prompting</span></span>

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

### <span data-ttu-id="78b79-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="78b79-113">-SubscriptionId</span></span>
<span data-ttu-id="78b79-114">ID för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="78b79-114">Id of the subscription.</span></span>

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

### <span data-ttu-id="78b79-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="78b79-115">-Confirm</span></span>
<span data-ttu-id="78b79-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="78b79-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78b79-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78b79-117">-WhatIf</span></span>
<span data-ttu-id="78b79-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="78b79-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78b79-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="78b79-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78b79-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78b79-120">CommonParameters</span></span>
<span data-ttu-id="78b79-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78b79-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78b79-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78b79-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78b79-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="78b79-123">INPUTS</span></span>

## <span data-ttu-id="78b79-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="78b79-124">OUTPUTS</span></span>

## <span data-ttu-id="78b79-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="78b79-125">NOTES</span></span>

## <span data-ttu-id="78b79-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="78b79-126">RELATED LINKS</span></span>

