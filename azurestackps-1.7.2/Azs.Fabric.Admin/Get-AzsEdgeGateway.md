---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a81fcf688e1c269aabd64250e9b0694730edc8f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921100"
---
# <span data-ttu-id="1a874-101">Get-AzsEdgeGateway</span><span class="sxs-lookup"><span data-stu-id="1a874-101">Get-AzsEdgeGateway</span></span>

## <span data-ttu-id="1a874-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1a874-102">SYNOPSIS</span></span>
<span data-ttu-id="1a874-103">Returnerar listan över alla Edge-gateways på en viss plats.</span><span class="sxs-lookup"><span data-stu-id="1a874-103">Returns the list of all edge gateways at a certain location.</span></span>

## <span data-ttu-id="1a874-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1a874-104">SYNTAX</span></span>

### <span data-ttu-id="1a874-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="1a874-105">List (Default)</span></span>
```
Get-AzsEdgeGateway [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="1a874-106">Lära</span><span class="sxs-lookup"><span data-stu-id="1a874-106">Get</span></span>
```
Get-AzsEdgeGateway [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="1a874-107">ID</span><span class="sxs-lookup"><span data-stu-id="1a874-107">ResourceId</span></span>
```
Get-AzsEdgeGateway -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="1a874-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1a874-108">DESCRIPTION</span></span>
<span data-ttu-id="1a874-109">Returnerar listan över alla Edge-gateways på en viss plats.</span><span class="sxs-lookup"><span data-stu-id="1a874-109">Returns the list of all edge gateways at a certain location.</span></span>

## <span data-ttu-id="1a874-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1a874-110">EXAMPLES</span></span>

### <span data-ttu-id="1a874-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1a874-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsEdgeGateway
```

<span data-ttu-id="1a874-112">Få en lista över alla Edge-gateways.</span><span class="sxs-lookup"><span data-stu-id="1a874-112">Get a list of all edge gateways.</span></span>

### <span data-ttu-id="1a874-113">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="1a874-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsEdgeGateway -Name "AzS-Gwy01"
```

<span data-ttu-id="1a874-114">Skaffa en specifik Gateway för Edge.</span><span class="sxs-lookup"><span data-stu-id="1a874-114">Get a specific edge gateway.</span></span>

## <span data-ttu-id="1a874-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1a874-115">PARAMETERS</span></span>

### <span data-ttu-id="1a874-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="1a874-116">-Filter</span></span>
<span data-ttu-id="1a874-117">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="1a874-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="1a874-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="1a874-118">-Location</span></span>
<span data-ttu-id="1a874-119">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="1a874-119">Location of the resource.</span></span>

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

### <span data-ttu-id="1a874-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="1a874-120">-Name</span></span>
<span data-ttu-id="1a874-121">Namn på Edge Gateway.</span><span class="sxs-lookup"><span data-stu-id="1a874-121">Name of the edge gateway.</span></span>

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

### <span data-ttu-id="1a874-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a874-122">-ResourceGroupName</span></span>
<span data-ttu-id="1a874-123">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="1a874-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="1a874-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a874-124">-ResourceId</span></span>
<span data-ttu-id="1a874-125">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="1a874-125">The resource id.</span></span>

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

### <span data-ttu-id="1a874-126">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="1a874-126">-Skip</span></span>
<span data-ttu-id="1a874-127">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="1a874-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="1a874-128">-Överst</span><span class="sxs-lookup"><span data-stu-id="1a874-128">-Top</span></span>
<span data-ttu-id="1a874-129">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="1a874-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="1a874-130">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="1a874-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="1a874-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a874-131">CommonParameters</span></span>
<span data-ttu-id="1a874-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a874-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a874-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a874-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a874-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1a874-134">INPUTS</span></span>

## <span data-ttu-id="1a874-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1a874-135">OUTPUTS</span></span>

### <span data-ttu-id="1a874-136">Microsoft. AzureStack. Management. Fabric. admin. Models. EdgeGateway</span><span class="sxs-lookup"><span data-stu-id="1a874-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.EdgeGateway</span></span>

## <span data-ttu-id="1a874-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1a874-137">NOTES</span></span>

## <span data-ttu-id="1a874-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1a874-138">RELATED LINKS</span></span>

