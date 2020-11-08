---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2d07aad989b08909228aebca7538b007f36bfcab
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100340"
---
# <span data-ttu-id="ea19e-101">Get-AzsRegionHealth</span><span class="sxs-lookup"><span data-stu-id="ea19e-101">Get-AzsRegionHealth</span></span>

## <span data-ttu-id="ea19e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ea19e-102">SYNOPSIS</span></span>
<span data-ttu-id="ea19e-103">Returnerar en lista över områdets hälso status.</span><span class="sxs-lookup"><span data-stu-id="ea19e-103">Returns a list of region's health status.</span></span>

## <span data-ttu-id="ea19e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ea19e-104">SYNTAX</span></span>

### <span data-ttu-id="ea19e-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="ea19e-105">List (Default)</span></span>
```
Get-AzsRegionHealth [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="ea19e-106">Lära</span><span class="sxs-lookup"><span data-stu-id="ea19e-106">Get</span></span>
```
Get-AzsRegionHealth [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="ea19e-107">ID</span><span class="sxs-lookup"><span data-stu-id="ea19e-107">ResourceId</span></span>
```
Get-AzsRegionHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="ea19e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ea19e-108">DESCRIPTION</span></span>
<span data-ttu-id="ea19e-109">Returnerar en lista över områdets hälso status.</span><span class="sxs-lookup"><span data-stu-id="ea19e-109">Returns a list of region's health status.</span></span>

## <span data-ttu-id="ea19e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ea19e-110">EXAMPLES</span></span>

### <span data-ttu-id="ea19e-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="ea19e-111">EXAMPLE 1</span></span>
```
Get-AzsRegionHealth
```

<span data-ttu-id="ea19e-112">Returnerar en lista över områdets hälso status.</span><span class="sxs-lookup"><span data-stu-id="ea19e-112">Returns a list of region's health status.</span></span>

## <span data-ttu-id="ea19e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ea19e-113">PARAMETERS</span></span>

### <span data-ttu-id="ea19e-114">-Plats</span><span class="sxs-lookup"><span data-stu-id="ea19e-114">-Location</span></span>
<span data-ttu-id="ea19e-115">Regionens namn</span><span class="sxs-lookup"><span data-stu-id="ea19e-115">Name of the region</span></span>

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

### <span data-ttu-id="ea19e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea19e-116">-ResourceGroupName</span></span>
<span data-ttu-id="ea19e-117">Resurs grupps namn, valfritt.</span><span class="sxs-lookup"><span data-stu-id="ea19e-117">Resource group name, optional.</span></span>

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

### <span data-ttu-id="ea19e-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea19e-118">-ResourceId</span></span>
<span data-ttu-id="ea19e-119">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="ea19e-119">The resource id.</span></span>

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

### <span data-ttu-id="ea19e-120">-Filter</span><span class="sxs-lookup"><span data-stu-id="ea19e-120">-Filter</span></span>
<span data-ttu-id="ea19e-121">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="ea19e-121">OData filter parameter.</span></span>

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

### <span data-ttu-id="ea19e-122">-Överst</span><span class="sxs-lookup"><span data-stu-id="ea19e-122">-Top</span></span>
<span data-ttu-id="ea19e-123">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="ea19e-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="ea19e-124">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="ea19e-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="ea19e-125">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="ea19e-125">-Skip</span></span>
<span data-ttu-id="ea19e-126">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="ea19e-126">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="ea19e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea19e-127">CommonParameters</span></span>
<span data-ttu-id="ea19e-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea19e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea19e-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea19e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea19e-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ea19e-130">INPUTS</span></span>

## <span data-ttu-id="ea19e-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ea19e-131">OUTPUTS</span></span>

### <span data-ttu-id="ea19e-132">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. RegionHealth</span><span class="sxs-lookup"><span data-stu-id="ea19e-132">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.RegionHealth</span></span>

## <span data-ttu-id="ea19e-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ea19e-133">NOTES</span></span>

## <span data-ttu-id="ea19e-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ea19e-134">RELATED LINKS</span></span>
