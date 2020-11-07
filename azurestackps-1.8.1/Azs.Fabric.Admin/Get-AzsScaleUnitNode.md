---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 07cb5e675003eccc9fad54e723e80a0ddb73ff9a
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921862"
---
# <span data-ttu-id="0cdda-101">Get-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="0cdda-101">Get-AzsScaleUnitNode</span></span>

## <span data-ttu-id="0cdda-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0cdda-102">SYNOPSIS</span></span>
<span data-ttu-id="0cdda-103">Returnerar en lista över alla noder för skalnings enhet på en plats.</span><span class="sxs-lookup"><span data-stu-id="0cdda-103">Returns a list of all scale unit nodes in a location.</span></span>

## <span data-ttu-id="0cdda-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0cdda-104">SYNTAX</span></span>

### <span data-ttu-id="0cdda-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="0cdda-105">List (Default)</span></span>
```
Get-AzsScaleUnitNode [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="0cdda-106">Lära</span><span class="sxs-lookup"><span data-stu-id="0cdda-106">Get</span></span>
```
Get-AzsScaleUnitNode [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="0cdda-107">ID</span><span class="sxs-lookup"><span data-stu-id="0cdda-107">ResourceId</span></span>
```
Get-AzsScaleUnitNode -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="0cdda-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0cdda-108">DESCRIPTION</span></span>
<span data-ttu-id="0cdda-109">Returnerar en lista över alla noder för skalnings enhet på en plats.</span><span class="sxs-lookup"><span data-stu-id="0cdda-109">Returns a list of all scale unit nodes in a location.</span></span>

## <span data-ttu-id="0cdda-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0cdda-110">EXAMPLES</span></span>

### <span data-ttu-id="0cdda-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="0cdda-111">EXAMPLE 1</span></span>
```
Get-AzsScaleUnitNode
```

<span data-ttu-id="0cdda-112">Hämta alla enheter för mått enhet på en plats.</span><span class="sxs-lookup"><span data-stu-id="0cdda-112">Get all scale unit nodes at a location.</span></span>

### <span data-ttu-id="0cdda-113">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="0cdda-113">EXAMPLE 2</span></span>
```
Get-AzsScaleUnitNode -Name "HC1n25r2231"
```

<span data-ttu-id="0cdda-114">Skaffa en särskild nod för Scale Unit på en plats med ett namn.</span><span class="sxs-lookup"><span data-stu-id="0cdda-114">Get a specific scale unit node at a location given a name.</span></span>

## <span data-ttu-id="0cdda-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0cdda-115">PARAMETERS</span></span>

### <span data-ttu-id="0cdda-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="0cdda-116">-Name</span></span>
<span data-ttu-id="0cdda-117">Namn på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="0cdda-117">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="0cdda-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="0cdda-118">-Location</span></span>
<span data-ttu-id="0cdda-119">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="0cdda-119">Location of the resource.</span></span>

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

### <span data-ttu-id="0cdda-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cdda-120">-ResourceGroupName</span></span>
<span data-ttu-id="0cdda-121">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="0cdda-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="0cdda-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0cdda-122">-ResourceId</span></span>
<span data-ttu-id="0cdda-123">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="0cdda-123">The resource id.</span></span>

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

### <span data-ttu-id="0cdda-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="0cdda-124">-Filter</span></span>
<span data-ttu-id="0cdda-125">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="0cdda-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="0cdda-126">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="0cdda-126">-Skip</span></span>
<span data-ttu-id="0cdda-127">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="0cdda-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="0cdda-128">-Överst</span><span class="sxs-lookup"><span data-stu-id="0cdda-128">-Top</span></span>
<span data-ttu-id="0cdda-129">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="0cdda-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="0cdda-130">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="0cdda-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="0cdda-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cdda-131">CommonParameters</span></span>
<span data-ttu-id="0cdda-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cdda-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cdda-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cdda-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cdda-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0cdda-134">INPUTS</span></span>

## <span data-ttu-id="0cdda-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0cdda-135">OUTPUTS</span></span>

### <span data-ttu-id="0cdda-136">Microsoft. AzureStack. Management. Fabric. admin. Models. ScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="0cdda-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.ScaleUnitNode</span></span>

## <span data-ttu-id="0cdda-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0cdda-137">NOTES</span></span>

## <span data-ttu-id="0cdda-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0cdda-138">RELATED LINKS</span></span>
