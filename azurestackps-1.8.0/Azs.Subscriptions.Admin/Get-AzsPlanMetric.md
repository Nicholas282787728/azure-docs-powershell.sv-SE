---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8ef41d414d12182c15d9ec5b01138e0110dee9f
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921508"
---
# <span data-ttu-id="e56eb-101">Get-AzsPlanMetric</span><span class="sxs-lookup"><span data-stu-id="e56eb-101">Get-AzsPlanMetric</span></span>

## <span data-ttu-id="e56eb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e56eb-102">SYNOPSIS</span></span>
<span data-ttu-id="e56eb-103">Få plan måtten.</span><span class="sxs-lookup"><span data-stu-id="e56eb-103">Get the plan metrics.</span></span>

## <span data-ttu-id="e56eb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e56eb-104">SYNTAX</span></span>

```
Get-AzsPlanMetric [-ResourceGroupName] <String> [-PlanName] <String> [<CommonParameters>]
```

## <span data-ttu-id="e56eb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e56eb-105">DESCRIPTION</span></span>
<span data-ttu-id="e56eb-106">Få plan måtten.</span><span class="sxs-lookup"><span data-stu-id="e56eb-106">Get the plan metrics.</span></span>

## <span data-ttu-id="e56eb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e56eb-107">EXAMPLES</span></span>

### <span data-ttu-id="e56eb-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e56eb-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlanMetric -ResourceGroupName rg1 -PlanName plan1
```

<span data-ttu-id="e56eb-109">Få en plans mått.</span><span class="sxs-lookup"><span data-stu-id="e56eb-109">Get a plan's metrics.</span></span>

## <span data-ttu-id="e56eb-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e56eb-110">PARAMETERS</span></span>

### <span data-ttu-id="e56eb-111">-PlanName</span><span class="sxs-lookup"><span data-stu-id="e56eb-111">-PlanName</span></span>
<span data-ttu-id="e56eb-112">Namn på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="e56eb-112">Name of the plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e56eb-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e56eb-113">-ResourceGroupName</span></span>
<span data-ttu-id="e56eb-114">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="e56eb-114">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="e56eb-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e56eb-115">CommonParameters</span></span>
<span data-ttu-id="e56eb-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e56eb-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e56eb-117">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e56eb-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e56eb-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e56eb-118">INPUTS</span></span>

## <span data-ttu-id="e56eb-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e56eb-119">OUTPUTS</span></span>

### <span data-ttu-id="e56eb-120">Microsoft. AzureStack. Management. abonnemang. admin. Models. Metric</span><span class="sxs-lookup"><span data-stu-id="e56eb-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Metric</span></span>

## <span data-ttu-id="e56eb-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e56eb-121">NOTES</span></span>

## <span data-ttu-id="e56eb-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e56eb-122">RELATED LINKS</span></span>

