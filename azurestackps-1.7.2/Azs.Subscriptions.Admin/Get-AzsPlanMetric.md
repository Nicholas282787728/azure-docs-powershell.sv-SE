---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cadf5ad37119ab6b50191e50e8ec281fe4bce2d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921037"
---
# <span data-ttu-id="c98a8-101">Get-AzsPlanMetric</span><span class="sxs-lookup"><span data-stu-id="c98a8-101">Get-AzsPlanMetric</span></span>

## <span data-ttu-id="c98a8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c98a8-102">SYNOPSIS</span></span>
<span data-ttu-id="c98a8-103">Få plan måtten.</span><span class="sxs-lookup"><span data-stu-id="c98a8-103">Get the plan metrics.</span></span>

## <span data-ttu-id="c98a8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c98a8-104">SYNTAX</span></span>

```
Get-AzsPlanMetric [-ResourceGroupName] <String> [-PlanName] <String> [<CommonParameters>]
```

## <span data-ttu-id="c98a8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c98a8-105">DESCRIPTION</span></span>
<span data-ttu-id="c98a8-106">Få plan måtten.</span><span class="sxs-lookup"><span data-stu-id="c98a8-106">Get the plan metrics.</span></span>

## <span data-ttu-id="c98a8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c98a8-107">EXAMPLES</span></span>

### <span data-ttu-id="c98a8-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c98a8-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlanMetric -ResourceGroupName rg1 -PlanName plan1
```

<span data-ttu-id="c98a8-109">Få en plans mått.</span><span class="sxs-lookup"><span data-stu-id="c98a8-109">Get a plan's metrics.</span></span>

## <span data-ttu-id="c98a8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c98a8-110">PARAMETERS</span></span>

### <span data-ttu-id="c98a8-111">-PlanName</span><span class="sxs-lookup"><span data-stu-id="c98a8-111">-PlanName</span></span>
<span data-ttu-id="c98a8-112">Namn på abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="c98a8-112">Name of the plan.</span></span>

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

### <span data-ttu-id="c98a8-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c98a8-113">-ResourceGroupName</span></span>
<span data-ttu-id="c98a8-114">Resurs gruppen som resursen finns under.</span><span class="sxs-lookup"><span data-stu-id="c98a8-114">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="c98a8-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c98a8-115">CommonParameters</span></span>
<span data-ttu-id="c98a8-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c98a8-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c98a8-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c98a8-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c98a8-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c98a8-118">INPUTS</span></span>

## <span data-ttu-id="c98a8-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c98a8-119">OUTPUTS</span></span>

### <span data-ttu-id="c98a8-120">Microsoft. AzureStack. Management. abonnemang. admin. Models. Metric</span><span class="sxs-lookup"><span data-stu-id="c98a8-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Metric</span></span>

## <span data-ttu-id="c98a8-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c98a8-121">NOTES</span></span>

## <span data-ttu-id="c98a8-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c98a8-122">RELATED LINKS</span></span>

