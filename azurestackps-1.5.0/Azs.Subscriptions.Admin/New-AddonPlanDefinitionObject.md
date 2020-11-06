---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7074752cda5997bba0536cf891675f59e734e509
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572296"
---
# <span data-ttu-id="bda0a-101">New-AddonPlanDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="bda0a-101">New-AddonPlanDefinitionObject</span></span>

## <span data-ttu-id="bda0a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bda0a-102">SYNOPSIS</span></span>
<span data-ttu-id="bda0a-103">Innehåller namnet på önskat schema som ska länkas eller kopplas från ett bud.</span><span class="sxs-lookup"><span data-stu-id="bda0a-103">Contains the name of the desired plan to be linked or unlinked from an offer.</span></span>

## <span data-ttu-id="bda0a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bda0a-104">SYNTAX</span></span>

```
New-AddonPlanDefinitionObject [[-PlanId] <String>] [[-MaxAcquisitionCount] <Int64>] [<CommonParameters>]
```

## <span data-ttu-id="bda0a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bda0a-105">DESCRIPTION</span></span>
<span data-ttu-id="bda0a-106">Innehåller namnet på önskat schema som ska länkas eller kopplas från ett bud.</span><span class="sxs-lookup"><span data-stu-id="bda0a-106">Contains the name of the desired plan to be linked or unlinked from an offer.</span></span>

## <span data-ttu-id="bda0a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bda0a-107">EXAMPLES</span></span>

### <span data-ttu-id="bda0a-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="bda0a-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AddonPlanDefinitionObject -PlanId $planIdentifier -MaxAcquisitionCount 500
```

<span data-ttu-id="bda0a-109">Skapa ett nytt plan definitions objekt för det angivna abonnemanget med inköps gränsen på 500.</span><span class="sxs-lookup"><span data-stu-id="bda0a-109">Create a new plan definition object for the specified plan with the acquisition limit of 500.</span></span>

## <span data-ttu-id="bda0a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bda0a-110">PARAMETERS</span></span>

### <span data-ttu-id="bda0a-111">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="bda0a-111">-MaxAcquisitionCount</span></span>
<span data-ttu-id="bda0a-112">Maximalt antal instanser som kan erhållas av en enda prenumeration.</span><span class="sxs-lookup"><span data-stu-id="bda0a-112">Maximum number of instances that can be acquired by a single subscription.</span></span>
<span data-ttu-id="bda0a-113">Om det inte anges är det förmodade värdet 1.</span><span class="sxs-lookup"><span data-stu-id="bda0a-113">If not specified, the assumed value is 1.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bda0a-114">-PlanId</span><span class="sxs-lookup"><span data-stu-id="bda0a-114">-PlanId</span></span>
<span data-ttu-id="bda0a-115">Plan-ID.</span><span class="sxs-lookup"><span data-stu-id="bda0a-115">Plan identifier.</span></span>

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

### <span data-ttu-id="bda0a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bda0a-116">CommonParameters</span></span>
<span data-ttu-id="bda0a-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bda0a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bda0a-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bda0a-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bda0a-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bda0a-119">INPUTS</span></span>

## <span data-ttu-id="bda0a-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bda0a-120">OUTPUTS</span></span>

## <span data-ttu-id="bda0a-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bda0a-121">NOTES</span></span>

## <span data-ttu-id="bda0a-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bda0a-122">RELATED LINKS</span></span>

