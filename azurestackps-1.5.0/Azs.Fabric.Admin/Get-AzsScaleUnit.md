---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 869cd48507ba9384026f8e58b9cd7853179b844f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754928"
---
# <span data-ttu-id="e4b62-101">Get-AzsScaleUnit</span><span class="sxs-lookup"><span data-stu-id="e4b62-101">Get-AzsScaleUnit</span></span>

## <span data-ttu-id="e4b62-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e4b62-102">SYNOPSIS</span></span>
<span data-ttu-id="e4b62-103">Returnerar en lista över alla skal enheter på en plats.</span><span class="sxs-lookup"><span data-stu-id="e4b62-103">Returns a list of all scale units at a location.</span></span>

## <span data-ttu-id="e4b62-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e4b62-104">SYNTAX</span></span>

### <span data-ttu-id="e4b62-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="e4b62-105">List (Default)</span></span>
```
Get-AzsScaleUnit [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="e4b62-106">Lära</span><span class="sxs-lookup"><span data-stu-id="e4b62-106">Get</span></span>
```
Get-AzsScaleUnit [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="e4b62-107">ID</span><span class="sxs-lookup"><span data-stu-id="e4b62-107">ResourceId</span></span>
```
Get-AzsScaleUnit -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="e4b62-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e4b62-108">DESCRIPTION</span></span>
<span data-ttu-id="e4b62-109">Returnerar en lista över alla skal enheter på en plats.</span><span class="sxs-lookup"><span data-stu-id="e4b62-109">Returns a list of all scale units at a location.</span></span>

## <span data-ttu-id="e4b62-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e4b62-110">EXAMPLES</span></span>

### <span data-ttu-id="e4b62-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e4b62-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsScaleUnit
```

<span data-ttu-id="e4b62-112">Returnera en lista med information om skalnings enheter.</span><span class="sxs-lookup"><span data-stu-id="e4b62-112">Return a list of information about scale units.</span></span>

### <span data-ttu-id="e4b62-113">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="e4b62-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsScaleUnit -Name "S-Cluster"
```

<span data-ttu-id="e4b62-114">Returnera information om en viss enhet.</span><span class="sxs-lookup"><span data-stu-id="e4b62-114">Return information about a specific scale unit.</span></span>

## <span data-ttu-id="e4b62-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e4b62-115">PARAMETERS</span></span>

### <span data-ttu-id="e4b62-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="e4b62-116">-Filter</span></span>
<span data-ttu-id="e4b62-117">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="e4b62-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="e4b62-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="e4b62-118">-Location</span></span>
<span data-ttu-id="e4b62-119">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="e4b62-119">Location of the resource.</span></span>

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

### <span data-ttu-id="e4b62-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="e4b62-120">-Name</span></span>
<span data-ttu-id="e4b62-121">Namnet på enheten.</span><span class="sxs-lookup"><span data-stu-id="e4b62-121">Name of the scale units.</span></span>

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

### <span data-ttu-id="e4b62-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4b62-122">-ResourceGroupName</span></span>
<span data-ttu-id="e4b62-123">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="e4b62-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="e4b62-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4b62-124">-ResourceId</span></span>
<span data-ttu-id="e4b62-125">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="e4b62-125">The resource id.</span></span>

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

### <span data-ttu-id="e4b62-126">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="e4b62-126">-Skip</span></span>
<span data-ttu-id="e4b62-127">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="e4b62-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="e4b62-128">-Överst</span><span class="sxs-lookup"><span data-stu-id="e4b62-128">-Top</span></span>
<span data-ttu-id="e4b62-129">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="e4b62-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="e4b62-130">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="e4b62-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="e4b62-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4b62-131">CommonParameters</span></span>
<span data-ttu-id="e4b62-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4b62-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4b62-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4b62-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4b62-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e4b62-134">INPUTS</span></span>

## <span data-ttu-id="e4b62-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e4b62-135">OUTPUTS</span></span>

### <span data-ttu-id="e4b62-136">Microsoft. AzureStack. Management. Fabric. admin. Models. ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="e4b62-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.ScaleUnit</span></span>

## <span data-ttu-id="e4b62-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e4b62-137">NOTES</span></span>

## <span data-ttu-id="e4b62-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e4b62-138">RELATED LINKS</span></span>

