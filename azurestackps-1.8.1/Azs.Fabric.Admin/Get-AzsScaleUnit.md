---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 475f8913731e8663cec6c6de4c89254c47d7af5e
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921755"
---
# <span data-ttu-id="b8873-101">Get-AzsScaleUnit</span><span class="sxs-lookup"><span data-stu-id="b8873-101">Get-AzsScaleUnit</span></span>

## <span data-ttu-id="b8873-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b8873-102">SYNOPSIS</span></span>
<span data-ttu-id="b8873-103">Returnerar en lista över alla skal enheter på en plats.</span><span class="sxs-lookup"><span data-stu-id="b8873-103">Returns a list of all scale units at a location.</span></span>

## <span data-ttu-id="b8873-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b8873-104">SYNTAX</span></span>

### <span data-ttu-id="b8873-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="b8873-105">List (Default)</span></span>
```
Get-AzsScaleUnit [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="b8873-106">Lära</span><span class="sxs-lookup"><span data-stu-id="b8873-106">Get</span></span>
```
Get-AzsScaleUnit [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="b8873-107">ID</span><span class="sxs-lookup"><span data-stu-id="b8873-107">ResourceId</span></span>
```
Get-AzsScaleUnit -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="b8873-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b8873-108">DESCRIPTION</span></span>
<span data-ttu-id="b8873-109">Returnerar en lista över alla skal enheter på en plats.</span><span class="sxs-lookup"><span data-stu-id="b8873-109">Returns a list of all scale units at a location.</span></span>

## <span data-ttu-id="b8873-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b8873-110">EXAMPLES</span></span>

### <span data-ttu-id="b8873-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="b8873-111">EXAMPLE 1</span></span>
```
Get-AzsScaleUnit
```

<span data-ttu-id="b8873-112">Returnera en lista med information om skalnings enheter.</span><span class="sxs-lookup"><span data-stu-id="b8873-112">Return a list of information about scale units.</span></span>

### <span data-ttu-id="b8873-113">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="b8873-113">EXAMPLE 2</span></span>
```
Get-AzsScaleUnit -Name "S-Cluster"
```

<span data-ttu-id="b8873-114">Returnera information om en viss enhet.</span><span class="sxs-lookup"><span data-stu-id="b8873-114">Return information about a specific scale unit.</span></span>

## <span data-ttu-id="b8873-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b8873-115">PARAMETERS</span></span>

### <span data-ttu-id="b8873-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="b8873-116">-Name</span></span>
<span data-ttu-id="b8873-117">Namnet på enheten.</span><span class="sxs-lookup"><span data-stu-id="b8873-117">Name of the scale units.</span></span>

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

### <span data-ttu-id="b8873-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="b8873-118">-Location</span></span>
<span data-ttu-id="b8873-119">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="b8873-119">Location of the resource.</span></span>

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

### <span data-ttu-id="b8873-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8873-120">-ResourceGroupName</span></span>
<span data-ttu-id="b8873-121">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="b8873-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="b8873-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8873-122">-ResourceId</span></span>
<span data-ttu-id="b8873-123">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="b8873-123">The resource id.</span></span>

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

### <span data-ttu-id="b8873-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="b8873-124">-Filter</span></span>
<span data-ttu-id="b8873-125">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="b8873-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="b8873-126">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="b8873-126">-Skip</span></span>
<span data-ttu-id="b8873-127">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="b8873-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="b8873-128">-Överst</span><span class="sxs-lookup"><span data-stu-id="b8873-128">-Top</span></span>
<span data-ttu-id="b8873-129">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="b8873-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b8873-130">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="b8873-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="b8873-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8873-131">CommonParameters</span></span>
<span data-ttu-id="b8873-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8873-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8873-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8873-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8873-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b8873-134">INPUTS</span></span>

## <span data-ttu-id="b8873-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b8873-135">OUTPUTS</span></span>

### <span data-ttu-id="b8873-136">Microsoft. AzureStack. Management. Fabric. admin. Models. ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="b8873-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.ScaleUnit</span></span>

## <span data-ttu-id="b8873-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b8873-137">NOTES</span></span>

## <span data-ttu-id="b8873-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b8873-138">RELATED LINKS</span></span>
