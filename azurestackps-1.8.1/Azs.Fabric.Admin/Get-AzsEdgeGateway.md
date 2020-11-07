---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 793bf4a4b5b9dfb448c5b2a1baf9d74af592a23e
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921720"
---
# <span data-ttu-id="527ec-101">Get-AzsEdgeGateway</span><span class="sxs-lookup"><span data-stu-id="527ec-101">Get-AzsEdgeGateway</span></span>

## <span data-ttu-id="527ec-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="527ec-102">SYNOPSIS</span></span>
<span data-ttu-id="527ec-103">Returnerar listan över alla Edge-gateways på en viss plats.</span><span class="sxs-lookup"><span data-stu-id="527ec-103">Returns the list of all edge gateways at a certain location.</span></span>

## <span data-ttu-id="527ec-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="527ec-104">SYNTAX</span></span>

### <span data-ttu-id="527ec-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="527ec-105">List (Default)</span></span>
```
Get-AzsEdgeGateway [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="527ec-106">Lära</span><span class="sxs-lookup"><span data-stu-id="527ec-106">Get</span></span>
```
Get-AzsEdgeGateway [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="527ec-107">ID</span><span class="sxs-lookup"><span data-stu-id="527ec-107">ResourceId</span></span>
```
Get-AzsEdgeGateway -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="527ec-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="527ec-108">DESCRIPTION</span></span>
<span data-ttu-id="527ec-109">Returnerar listan över alla Edge-gateways på en viss plats.</span><span class="sxs-lookup"><span data-stu-id="527ec-109">Returns the list of all edge gateways at a certain location.</span></span>

## <span data-ttu-id="527ec-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="527ec-110">EXAMPLES</span></span>

### <span data-ttu-id="527ec-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="527ec-111">EXAMPLE 1</span></span>
```
Get-AzsEdgeGateway
```

<span data-ttu-id="527ec-112">Få en lista över alla Edge-gateways.</span><span class="sxs-lookup"><span data-stu-id="527ec-112">Get a list of all edge gateways.</span></span>

### <span data-ttu-id="527ec-113">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="527ec-113">EXAMPLE 2</span></span>
```
Get-AzsEdgeGateway -Name "AzS-Gwy01"
```

<span data-ttu-id="527ec-114">Skaffa en specifik Gateway för Edge.</span><span class="sxs-lookup"><span data-stu-id="527ec-114">Get a specific edge gateway.</span></span>

## <span data-ttu-id="527ec-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="527ec-115">PARAMETERS</span></span>

### <span data-ttu-id="527ec-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="527ec-116">-Name</span></span>
<span data-ttu-id="527ec-117">Namn på Edge Gateway.</span><span class="sxs-lookup"><span data-stu-id="527ec-117">Name of the edge gateway.</span></span>

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

### <span data-ttu-id="527ec-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="527ec-118">-Location</span></span>
<span data-ttu-id="527ec-119">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="527ec-119">Location of the resource.</span></span>

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

### <span data-ttu-id="527ec-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="527ec-120">-ResourceGroupName</span></span>
<span data-ttu-id="527ec-121">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="527ec-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="527ec-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="527ec-122">-ResourceId</span></span>
<span data-ttu-id="527ec-123">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="527ec-123">The resource id.</span></span>

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

### <span data-ttu-id="527ec-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="527ec-124">-Filter</span></span>
<span data-ttu-id="527ec-125">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="527ec-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="527ec-126">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="527ec-126">-Skip</span></span>
<span data-ttu-id="527ec-127">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="527ec-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="527ec-128">-Överst</span><span class="sxs-lookup"><span data-stu-id="527ec-128">-Top</span></span>
<span data-ttu-id="527ec-129">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="527ec-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="527ec-130">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="527ec-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="527ec-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="527ec-131">CommonParameters</span></span>
<span data-ttu-id="527ec-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="527ec-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="527ec-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="527ec-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="527ec-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="527ec-134">INPUTS</span></span>

## <span data-ttu-id="527ec-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="527ec-135">OUTPUTS</span></span>

### <span data-ttu-id="527ec-136">Microsoft. AzureStack. Management. Fabric. admin. Models. EdgeGateway</span><span class="sxs-lookup"><span data-stu-id="527ec-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.EdgeGateway</span></span>

## <span data-ttu-id="527ec-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="527ec-137">NOTES</span></span>

## <span data-ttu-id="527ec-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="527ec-138">RELATED LINKS</span></span>
