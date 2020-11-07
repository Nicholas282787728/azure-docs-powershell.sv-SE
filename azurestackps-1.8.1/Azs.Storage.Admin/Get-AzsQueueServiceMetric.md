---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e2776c768f49dabdea8483ff601f129e80bfc2dc
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921804"
---
# <span data-ttu-id="b0144-101">Get-AzsQueueServiceMetric</span><span class="sxs-lookup"><span data-stu-id="b0144-101">Get-AzsQueueServiceMetric</span></span>

## <span data-ttu-id="b0144-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b0144-102">SYNOPSIS</span></span>
<span data-ttu-id="b0144-103">Returnerar en lista med mät värden för kötjänsten.</span><span class="sxs-lookup"><span data-stu-id="b0144-103">Returns a list of metrics for the queue service.</span></span>

## <span data-ttu-id="b0144-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b0144-104">SYNTAX</span></span>

```
Get-AzsQueueServiceMetric [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="b0144-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b0144-105">DESCRIPTION</span></span>
<span data-ttu-id="b0144-106">Returnerar en lista med mät värden för kötjänsten.</span><span class="sxs-lookup"><span data-stu-id="b0144-106">Returns a list of metrics for the queue service.</span></span>

## <span data-ttu-id="b0144-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b0144-107">EXAMPLES</span></span>

### <span data-ttu-id="b0144-108">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="b0144-108">EXAMPLE 1</span></span>
```
Get-AzsQueueServiceMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="b0144-109">Få en lista över Mät värden för kötjänsten.</span><span class="sxs-lookup"><span data-stu-id="b0144-109">Get the list of metrics for queue service.</span></span>

## <span data-ttu-id="b0144-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b0144-110">PARAMETERS</span></span>

### <span data-ttu-id="b0144-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="b0144-111">-FarmName</span></span>
<span data-ttu-id="b0144-112">Server grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="b0144-112">Farm Id.</span></span>

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

### <span data-ttu-id="b0144-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0144-113">-ResourceGroupName</span></span>
<span data-ttu-id="b0144-114">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="b0144-114">Resource group name.</span></span>

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

### <span data-ttu-id="b0144-115">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="b0144-115">-Skip</span></span>
<span data-ttu-id="b0144-116">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="b0144-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="b0144-117">-Överst</span><span class="sxs-lookup"><span data-stu-id="b0144-117">-Top</span></span>
<span data-ttu-id="b0144-118">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="b0144-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b0144-119">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="b0144-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="b0144-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0144-120">CommonParameters</span></span>
<span data-ttu-id="b0144-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0144-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0144-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0144-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0144-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b0144-123">INPUTS</span></span>

## <span data-ttu-id="b0144-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b0144-124">OUTPUTS</span></span>

### <span data-ttu-id="b0144-125">Microsoft. AzureStack. Management. Storage. admin. Models. Metric</span><span class="sxs-lookup"><span data-stu-id="b0144-125">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="b0144-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b0144-126">NOTES</span></span>

## <span data-ttu-id="b0144-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b0144-127">RELATED LINKS</span></span>
