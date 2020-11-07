---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2d07aad989b08909228aebca7538b007f36bfcab
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921432"
---
# <span data-ttu-id="09a16-101">Get-AzsRegionHealth</span><span class="sxs-lookup"><span data-stu-id="09a16-101">Get-AzsRegionHealth</span></span>

## <span data-ttu-id="09a16-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="09a16-102">SYNOPSIS</span></span>
<span data-ttu-id="09a16-103">Returnerar en lista över områdets hälso status.</span><span class="sxs-lookup"><span data-stu-id="09a16-103">Returns a list of region's health status.</span></span>

## <span data-ttu-id="09a16-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="09a16-104">SYNTAX</span></span>

### <span data-ttu-id="09a16-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="09a16-105">List (Default)</span></span>
```
Get-AzsRegionHealth [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="09a16-106">Lära</span><span class="sxs-lookup"><span data-stu-id="09a16-106">Get</span></span>
```
Get-AzsRegionHealth [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="09a16-107">ID</span><span class="sxs-lookup"><span data-stu-id="09a16-107">ResourceId</span></span>
```
Get-AzsRegionHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="09a16-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="09a16-108">DESCRIPTION</span></span>
<span data-ttu-id="09a16-109">Returnerar en lista över områdets hälso status.</span><span class="sxs-lookup"><span data-stu-id="09a16-109">Returns a list of region's health status.</span></span>

## <span data-ttu-id="09a16-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="09a16-110">EXAMPLES</span></span>

### <span data-ttu-id="09a16-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="09a16-111">EXAMPLE 1</span></span>
```
Get-AzsRegionHealth
```

<span data-ttu-id="09a16-112">Returnerar en lista över områdets hälso status.</span><span class="sxs-lookup"><span data-stu-id="09a16-112">Returns a list of region's health status.</span></span>

## <span data-ttu-id="09a16-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="09a16-113">PARAMETERS</span></span>

### <span data-ttu-id="09a16-114">-Plats</span><span class="sxs-lookup"><span data-stu-id="09a16-114">-Location</span></span>
<span data-ttu-id="09a16-115">Regionens namn</span><span class="sxs-lookup"><span data-stu-id="09a16-115">Name of the region</span></span>

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

### <span data-ttu-id="09a16-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09a16-116">-ResourceGroupName</span></span>
<span data-ttu-id="09a16-117">Resurs grupps namn, valfritt.</span><span class="sxs-lookup"><span data-stu-id="09a16-117">Resource group name, optional.</span></span>

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

### <span data-ttu-id="09a16-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09a16-118">-ResourceId</span></span>
<span data-ttu-id="09a16-119">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="09a16-119">The resource id.</span></span>

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

### <span data-ttu-id="09a16-120">-Filter</span><span class="sxs-lookup"><span data-stu-id="09a16-120">-Filter</span></span>
<span data-ttu-id="09a16-121">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="09a16-121">OData filter parameter.</span></span>

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

### <span data-ttu-id="09a16-122">-Överst</span><span class="sxs-lookup"><span data-stu-id="09a16-122">-Top</span></span>
<span data-ttu-id="09a16-123">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="09a16-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="09a16-124">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="09a16-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="09a16-125">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="09a16-125">-Skip</span></span>
<span data-ttu-id="09a16-126">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="09a16-126">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="09a16-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09a16-127">CommonParameters</span></span>
<span data-ttu-id="09a16-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09a16-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09a16-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09a16-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09a16-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="09a16-130">INPUTS</span></span>

## <span data-ttu-id="09a16-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="09a16-131">OUTPUTS</span></span>

### <span data-ttu-id="09a16-132">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. RegionHealth</span><span class="sxs-lookup"><span data-stu-id="09a16-132">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.RegionHealth</span></span>

## <span data-ttu-id="09a16-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="09a16-133">NOTES</span></span>

## <span data-ttu-id="09a16-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="09a16-134">RELATED LINKS</span></span>
