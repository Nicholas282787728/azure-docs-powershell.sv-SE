---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 475f8913731e8663cec6c6de4c89254c47d7af5e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921360"
---
# <span data-ttu-id="ca4f3-101">Get-AzsScaleUnit</span><span class="sxs-lookup"><span data-stu-id="ca4f3-101">Get-AzsScaleUnit</span></span>

## <span data-ttu-id="ca4f3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ca4f3-102">SYNOPSIS</span></span>
<span data-ttu-id="ca4f3-103">Returnerar en lista över alla skal enheter på en plats.</span><span class="sxs-lookup"><span data-stu-id="ca4f3-103">Returns a list of all scale units at a location.</span></span>

## <span data-ttu-id="ca4f3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ca4f3-104">SYNTAX</span></span>

### <span data-ttu-id="ca4f3-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="ca4f3-105">List (Default)</span></span>
```
Get-AzsScaleUnit [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="ca4f3-106">Lära</span><span class="sxs-lookup"><span data-stu-id="ca4f3-106">Get</span></span>
```
Get-AzsScaleUnit [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="ca4f3-107">ID</span><span class="sxs-lookup"><span data-stu-id="ca4f3-107">ResourceId</span></span>
```
Get-AzsScaleUnit -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="ca4f3-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ca4f3-108">DESCRIPTION</span></span>
<span data-ttu-id="ca4f3-109">Returnerar en lista över alla skal enheter på en plats.</span><span class="sxs-lookup"><span data-stu-id="ca4f3-109">Returns a list of all scale units at a location.</span></span>

## <span data-ttu-id="ca4f3-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ca4f3-110">EXAMPLES</span></span>

### <span data-ttu-id="ca4f3-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="ca4f3-111">EXAMPLE 1</span></span>
```
Get-AzsScaleUnit
```

<span data-ttu-id="ca4f3-112">Returnera en lista med information om skalnings enheter.</span><span class="sxs-lookup"><span data-stu-id="ca4f3-112">Return a list of information about scale units.</span></span>

### <span data-ttu-id="ca4f3-113">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="ca4f3-113">EXAMPLE 2</span></span>
```
Get-AzsScaleUnit -Name "S-Cluster"
```

<span data-ttu-id="ca4f3-114">Returnera information om en viss enhet.</span><span class="sxs-lookup"><span data-stu-id="ca4f3-114">Return information about a specific scale unit.</span></span>

## <span data-ttu-id="ca4f3-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ca4f3-115">PARAMETERS</span></span>

### <span data-ttu-id="ca4f3-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="ca4f3-116">-Name</span></span>
<span data-ttu-id="ca4f3-117">Namnet på enheten.</span><span class="sxs-lookup"><span data-stu-id="ca4f3-117">Name of the scale units.</span></span>

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

### <span data-ttu-id="ca4f3-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="ca4f3-118">-Location</span></span>
<span data-ttu-id="ca4f3-119">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="ca4f3-119">Location of the resource.</span></span>

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

### <span data-ttu-id="ca4f3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca4f3-120">-ResourceGroupName</span></span>
<span data-ttu-id="ca4f3-121">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="ca4f3-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="ca4f3-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca4f3-122">-ResourceId</span></span>
<span data-ttu-id="ca4f3-123">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="ca4f3-123">The resource id.</span></span>

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

### <span data-ttu-id="ca4f3-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="ca4f3-124">-Filter</span></span>
<span data-ttu-id="ca4f3-125">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="ca4f3-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="ca4f3-126">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="ca4f3-126">-Skip</span></span>
<span data-ttu-id="ca4f3-127">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="ca4f3-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="ca4f3-128">-Överst</span><span class="sxs-lookup"><span data-stu-id="ca4f3-128">-Top</span></span>
<span data-ttu-id="ca4f3-129">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="ca4f3-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="ca4f3-130">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="ca4f3-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="ca4f3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca4f3-131">CommonParameters</span></span>
<span data-ttu-id="ca4f3-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca4f3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca4f3-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca4f3-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca4f3-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ca4f3-134">INPUTS</span></span>

## <span data-ttu-id="ca4f3-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ca4f3-135">OUTPUTS</span></span>

### <span data-ttu-id="ca4f3-136">Microsoft. AzureStack. Management. Fabric. admin. Models. ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="ca4f3-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.ScaleUnit</span></span>

## <span data-ttu-id="ca4f3-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ca4f3-137">NOTES</span></span>

## <span data-ttu-id="ca4f3-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ca4f3-138">RELATED LINKS</span></span>
