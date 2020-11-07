---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ecc0e931c97a60d35db48dbceb1446ff944ee689
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921764"
---
# <span data-ttu-id="604e9-101">Get-AzsStorageFarmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="604e9-101">Get-AzsStorageFarmMetricDefinition</span></span>

## <span data-ttu-id="604e9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="604e9-102">SYNOPSIS</span></span>
<span data-ttu-id="604e9-103">Returnerar en lista med mått definitioner för en lagrings grupp.</span><span class="sxs-lookup"><span data-stu-id="604e9-103">Returns a list of metric definitions for a storage farm.</span></span>

## <span data-ttu-id="604e9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="604e9-104">SYNTAX</span></span>

```
Get-AzsStorageFarmMetricDefinition [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="604e9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="604e9-105">DESCRIPTION</span></span>
<span data-ttu-id="604e9-106">Returnerar en lista med mått definitioner för en lagrings grupp.</span><span class="sxs-lookup"><span data-stu-id="604e9-106">Returns a list of metric definitions for a storage farm.</span></span>

## <span data-ttu-id="604e9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="604e9-107">EXAMPLES</span></span>

### <span data-ttu-id="604e9-108">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="604e9-108">EXAMPLE 1</span></span>
```
Get-AzsStorageFarmMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="604e9-109">Hämta listan med mått definitioner för en lagrings grupp.</span><span class="sxs-lookup"><span data-stu-id="604e9-109">Get the list of metric definitions for a storage farm.</span></span>

## <span data-ttu-id="604e9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="604e9-110">PARAMETERS</span></span>

### <span data-ttu-id="604e9-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="604e9-111">-FarmName</span></span>
<span data-ttu-id="604e9-112">Server grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="604e9-112">Farm Id.</span></span>

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

### <span data-ttu-id="604e9-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="604e9-113">-ResourceGroupName</span></span>
<span data-ttu-id="604e9-114">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="604e9-114">Resource group name.</span></span>

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

### <span data-ttu-id="604e9-115">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="604e9-115">-Skip</span></span>
<span data-ttu-id="604e9-116">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="604e9-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="604e9-117">-Överst</span><span class="sxs-lookup"><span data-stu-id="604e9-117">-Top</span></span>
<span data-ttu-id="604e9-118">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="604e9-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="604e9-119">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="604e9-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="604e9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="604e9-120">CommonParameters</span></span>
<span data-ttu-id="604e9-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="604e9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="604e9-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="604e9-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="604e9-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="604e9-123">INPUTS</span></span>

## <span data-ttu-id="604e9-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="604e9-124">OUTPUTS</span></span>

### <span data-ttu-id="604e9-125">Microsoft. AzureStack. Management. Storage. admin. Models. MetricDefinition</span><span class="sxs-lookup"><span data-stu-id="604e9-125">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="604e9-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="604e9-126">NOTES</span></span>

## <span data-ttu-id="604e9-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="604e9-127">RELATED LINKS</span></span>
