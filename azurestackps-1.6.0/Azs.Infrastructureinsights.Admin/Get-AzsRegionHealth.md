---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b6713b912f962a7a85627ca2280d6195cc5c5d88
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571952"
---
# <span data-ttu-id="a31a8-101">Get-AzsRegionHealth</span><span class="sxs-lookup"><span data-stu-id="a31a8-101">Get-AzsRegionHealth</span></span>

## <span data-ttu-id="a31a8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a31a8-102">SYNOPSIS</span></span>
<span data-ttu-id="a31a8-103">Returnerar en lista över områdets hälso status.</span><span class="sxs-lookup"><span data-stu-id="a31a8-103">Returns a list of region's health status.</span></span>

## <span data-ttu-id="a31a8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a31a8-104">SYNTAX</span></span>

### <span data-ttu-id="a31a8-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="a31a8-105">List (Default)</span></span>
```
Get-AzsRegionHealth [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="a31a8-106">Lära</span><span class="sxs-lookup"><span data-stu-id="a31a8-106">Get</span></span>
```
Get-AzsRegionHealth [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="a31a8-107">ID</span><span class="sxs-lookup"><span data-stu-id="a31a8-107">ResourceId</span></span>
```
Get-AzsRegionHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="a31a8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a31a8-108">DESCRIPTION</span></span>
<span data-ttu-id="a31a8-109">Returnerar en lista över områdets hälso status.</span><span class="sxs-lookup"><span data-stu-id="a31a8-109">Returns a list of region's health status.</span></span>

## <span data-ttu-id="a31a8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a31a8-110">EXAMPLES</span></span>

### <span data-ttu-id="a31a8-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a31a8-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsRegionHealth
```

<span data-ttu-id="a31a8-112">Returnerar en lista över områdets hälso status.</span><span class="sxs-lookup"><span data-stu-id="a31a8-112">Returns a list of region's health status.</span></span>

## <span data-ttu-id="a31a8-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a31a8-113">PARAMETERS</span></span>

### <span data-ttu-id="a31a8-114">-Filter</span><span class="sxs-lookup"><span data-stu-id="a31a8-114">-Filter</span></span>
<span data-ttu-id="a31a8-115">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="a31a8-115">OData filter parameter.</span></span>

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

### <span data-ttu-id="a31a8-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="a31a8-116">-Location</span></span>
<span data-ttu-id="a31a8-117">Regionens namn</span><span class="sxs-lookup"><span data-stu-id="a31a8-117">Name of the region</span></span>

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

### <span data-ttu-id="a31a8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a31a8-118">-ResourceGroupName</span></span>
<span data-ttu-id="a31a8-119">Resurs grupp namn som resursen finns.</span><span class="sxs-lookup"><span data-stu-id="a31a8-119">Resource group name which the resource resides.</span></span>

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

### <span data-ttu-id="a31a8-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a31a8-120">-ResourceId</span></span>
<span data-ttu-id="a31a8-121">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="a31a8-121">The resource id.</span></span>

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

### <span data-ttu-id="a31a8-122">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="a31a8-122">-Skip</span></span>
<span data-ttu-id="a31a8-123">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="a31a8-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="a31a8-124">-Överst</span><span class="sxs-lookup"><span data-stu-id="a31a8-124">-Top</span></span>
<span data-ttu-id="a31a8-125">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="a31a8-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="a31a8-126">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="a31a8-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="a31a8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a31a8-127">CommonParameters</span></span>
<span data-ttu-id="a31a8-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a31a8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a31a8-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a31a8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a31a8-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a31a8-130">INPUTS</span></span>

## <span data-ttu-id="a31a8-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a31a8-131">OUTPUTS</span></span>

### <span data-ttu-id="a31a8-132">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. RegionHealth</span><span class="sxs-lookup"><span data-stu-id="a31a8-132">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.RegionHealth</span></span>

## <span data-ttu-id="a31a8-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a31a8-133">NOTES</span></span>

## <span data-ttu-id="a31a8-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a31a8-134">RELATED LINKS</span></span>

