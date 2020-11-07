---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2d07aad989b08909228aebca7538b007f36bfcab
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921840"
---
# <span data-ttu-id="b56c1-101">Get-AzsRegionHealth</span><span class="sxs-lookup"><span data-stu-id="b56c1-101">Get-AzsRegionHealth</span></span>

## <span data-ttu-id="b56c1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b56c1-102">SYNOPSIS</span></span>
<span data-ttu-id="b56c1-103">Returnerar en lista över områdets hälso status.</span><span class="sxs-lookup"><span data-stu-id="b56c1-103">Returns a list of region's health status.</span></span>

## <span data-ttu-id="b56c1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b56c1-104">SYNTAX</span></span>

### <span data-ttu-id="b56c1-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="b56c1-105">List (Default)</span></span>
```
Get-AzsRegionHealth [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="b56c1-106">Lära</span><span class="sxs-lookup"><span data-stu-id="b56c1-106">Get</span></span>
```
Get-AzsRegionHealth [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="b56c1-107">ID</span><span class="sxs-lookup"><span data-stu-id="b56c1-107">ResourceId</span></span>
```
Get-AzsRegionHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="b56c1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b56c1-108">DESCRIPTION</span></span>
<span data-ttu-id="b56c1-109">Returnerar en lista över områdets hälso status.</span><span class="sxs-lookup"><span data-stu-id="b56c1-109">Returns a list of region's health status.</span></span>

## <span data-ttu-id="b56c1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b56c1-110">EXAMPLES</span></span>

### <span data-ttu-id="b56c1-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="b56c1-111">EXAMPLE 1</span></span>
```
Get-AzsRegionHealth
```

<span data-ttu-id="b56c1-112">Returnerar en lista över områdets hälso status.</span><span class="sxs-lookup"><span data-stu-id="b56c1-112">Returns a list of region's health status.</span></span>

## <span data-ttu-id="b56c1-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b56c1-113">PARAMETERS</span></span>

### <span data-ttu-id="b56c1-114">-Plats</span><span class="sxs-lookup"><span data-stu-id="b56c1-114">-Location</span></span>
<span data-ttu-id="b56c1-115">Regionens namn</span><span class="sxs-lookup"><span data-stu-id="b56c1-115">Name of the region</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b56c1-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b56c1-116">-ResourceGroupName</span></span>
<span data-ttu-id="b56c1-117">Resurs grupps namn, valfritt.</span><span class="sxs-lookup"><span data-stu-id="b56c1-117">Resource group name, optional.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b56c1-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b56c1-118">-ResourceId</span></span>
<span data-ttu-id="b56c1-119">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="b56c1-119">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b56c1-120">-Filter</span><span class="sxs-lookup"><span data-stu-id="b56c1-120">-Filter</span></span>
<span data-ttu-id="b56c1-121">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="b56c1-121">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b56c1-122">-Överst</span><span class="sxs-lookup"><span data-stu-id="b56c1-122">-Top</span></span>
<span data-ttu-id="b56c1-123">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="b56c1-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b56c1-124">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="b56c1-124">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b56c1-125">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="b56c1-125">-Skip</span></span>
<span data-ttu-id="b56c1-126">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="b56c1-126">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b56c1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b56c1-127">CommonParameters</span></span>
<span data-ttu-id="b56c1-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b56c1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b56c1-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b56c1-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b56c1-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b56c1-130">INPUTS</span></span>

## <span data-ttu-id="b56c1-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b56c1-131">OUTPUTS</span></span>

### <span data-ttu-id="b56c1-132">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. RegionHealth</span><span class="sxs-lookup"><span data-stu-id="b56c1-132">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.RegionHealth</span></span>

## <span data-ttu-id="b56c1-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b56c1-133">NOTES</span></span>

## <span data-ttu-id="b56c1-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b56c1-134">RELATED LINKS</span></span>
