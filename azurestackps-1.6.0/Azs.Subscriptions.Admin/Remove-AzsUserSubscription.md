---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d76356e99419ff345e2eccc025c91637417de1a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754963"
---
# <span data-ttu-id="35a64-101">Remove-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="35a64-101">Remove-AzsUserSubscription</span></span>

## <span data-ttu-id="35a64-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="35a64-102">SYNOPSIS</span></span>
<span data-ttu-id="35a64-103">Tar bort den angivna klient-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="35a64-103">Removes the specified tenant subscription.</span></span>

## <span data-ttu-id="35a64-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="35a64-104">SYNTAX</span></span>

```
Remove-AzsUserSubscription [-SubscriptionId] <Guid> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35a64-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="35a64-105">DESCRIPTION</span></span>
<span data-ttu-id="35a64-106">Tar bort den angivna klient-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="35a64-106">Removes the specified tenant subscription.</span></span>

## <span data-ttu-id="35a64-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="35a64-107">EXAMPLES</span></span>

### <span data-ttu-id="35a64-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="35a64-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsUserSubscription -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="35a64-109">Ta bort den angivna klient prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="35a64-109">Remove the specified tenant subscription.</span></span>

## <span data-ttu-id="35a64-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="35a64-110">PARAMETERS</span></span>

### <span data-ttu-id="35a64-111">-Force</span><span class="sxs-lookup"><span data-stu-id="35a64-111">-Force</span></span>
<span data-ttu-id="35a64-112">Flagga för att ta bort objektet utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="35a64-112">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="35a64-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="35a64-113">-SubscriptionId</span></span>
<span data-ttu-id="35a64-114">Parametern prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="35a64-114">Subscription Id parameter.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35a64-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="35a64-115">-Confirm</span></span>
<span data-ttu-id="35a64-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="35a64-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35a64-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35a64-117">-WhatIf</span></span>
<span data-ttu-id="35a64-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="35a64-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35a64-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="35a64-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35a64-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35a64-120">CommonParameters</span></span>
<span data-ttu-id="35a64-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35a64-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35a64-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35a64-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35a64-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="35a64-123">INPUTS</span></span>

## <span data-ttu-id="35a64-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="35a64-124">OUTPUTS</span></span>

## <span data-ttu-id="35a64-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="35a64-125">NOTES</span></span>

## <span data-ttu-id="35a64-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="35a64-126">RELATED LINKS</span></span>

