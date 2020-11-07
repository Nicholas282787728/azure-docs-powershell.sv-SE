---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c1affc11e3e5ff360cf08468c4935b6d48d68321
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921882"
---
# <span data-ttu-id="737b1-101">Get-AzsTableServiceMetric</span><span class="sxs-lookup"><span data-stu-id="737b1-101">Get-AzsTableServiceMetric</span></span>

## <span data-ttu-id="737b1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="737b1-102">SYNOPSIS</span></span>
<span data-ttu-id="737b1-103">Returnerar en lista med mått för tabell tjänsten.</span><span class="sxs-lookup"><span data-stu-id="737b1-103">Returns a list of metrics for table service.</span></span>

## <span data-ttu-id="737b1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="737b1-104">SYNTAX</span></span>

```
Get-AzsTableServiceMetric [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="737b1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="737b1-105">DESCRIPTION</span></span>
<span data-ttu-id="737b1-106">Returnerar en lista med mått för tabell tjänsten.</span><span class="sxs-lookup"><span data-stu-id="737b1-106">Returns a list of metrics for table service.</span></span>

## <span data-ttu-id="737b1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="737b1-107">EXAMPLES</span></span>

### <span data-ttu-id="737b1-108">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="737b1-108">EXAMPLE 1</span></span>
```
Get-AzsTableServiceMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="737b1-109">Hämta listan med mät värden för tabell tjänsten.</span><span class="sxs-lookup"><span data-stu-id="737b1-109">Get the list of metrics for table service.</span></span>

## <span data-ttu-id="737b1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="737b1-110">PARAMETERS</span></span>

### <span data-ttu-id="737b1-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="737b1-111">-FarmName</span></span>
<span data-ttu-id="737b1-112">Server grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="737b1-112">Farm Id.</span></span>

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

### <span data-ttu-id="737b1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="737b1-113">-ResourceGroupName</span></span>
<span data-ttu-id="737b1-114">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="737b1-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="737b1-115">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="737b1-115">-Skip</span></span>
<span data-ttu-id="737b1-116">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="737b1-116">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="737b1-117">-Överst</span><span class="sxs-lookup"><span data-stu-id="737b1-117">-Top</span></span>
<span data-ttu-id="737b1-118">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="737b1-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="737b1-119">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="737b1-119">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="737b1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="737b1-120">CommonParameters</span></span>
<span data-ttu-id="737b1-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="737b1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="737b1-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="737b1-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="737b1-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="737b1-123">INPUTS</span></span>

## <span data-ttu-id="737b1-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="737b1-124">OUTPUTS</span></span>

### <span data-ttu-id="737b1-125">Microsoft. AzureStack. Management. Storage. admin. Models. Metric</span><span class="sxs-lookup"><span data-stu-id="737b1-125">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="737b1-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="737b1-126">NOTES</span></span>

## <span data-ttu-id="737b1-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="737b1-127">RELATED LINKS</span></span>
