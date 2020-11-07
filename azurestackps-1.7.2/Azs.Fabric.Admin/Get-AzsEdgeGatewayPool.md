---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67a49abc82ba1ec8d9411141d456b8f71f75600f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743352"
---
# <span data-ttu-id="a8118-101">Get-AzsEdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="a8118-101">Get-AzsEdgeGatewayPool</span></span>

## <span data-ttu-id="a8118-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a8118-102">SYNOPSIS</span></span>
<span data-ttu-id="a8118-103">Returnerar Gateway-poolnamn på en plats.</span><span class="sxs-lookup"><span data-stu-id="a8118-103">Returns gateway pool objects at a location.</span></span>

## <span data-ttu-id="a8118-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a8118-104">SYNTAX</span></span>

### <span data-ttu-id="a8118-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="a8118-105">List (Default)</span></span>
```
Get-AzsEdgeGatewayPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="a8118-106">Lära</span><span class="sxs-lookup"><span data-stu-id="a8118-106">Get</span></span>
```
Get-AzsEdgeGatewayPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="a8118-107">ID</span><span class="sxs-lookup"><span data-stu-id="a8118-107">ResourceId</span></span>
```
Get-AzsEdgeGatewayPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="a8118-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a8118-108">DESCRIPTION</span></span>
<span data-ttu-id="a8118-109">Returnerar Edge Gateway pool-objekt på en plats.</span><span class="sxs-lookup"><span data-stu-id="a8118-109">Returns edge gateway pool objects at a location.</span></span>

## <span data-ttu-id="a8118-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a8118-110">EXAMPLES</span></span>

### <span data-ttu-id="a8118-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a8118-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsEdgeGatewayPool
```

<span data-ttu-id="a8118-112">Få en lista över alla yttre Gateway-pooler.</span><span class="sxs-lookup"><span data-stu-id="a8118-112">Get a list of all Edge Gateway pools.</span></span>

### <span data-ttu-id="a8118-113">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="a8118-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsEdgeGatewayPool -Name "AzS-Gwy01"
```

<span data-ttu-id="a8118-114">Skaffa en specifik pool för gateway.</span><span class="sxs-lookup"><span data-stu-id="a8118-114">Get a specific edge gateway pool.</span></span>

## <span data-ttu-id="a8118-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a8118-115">PARAMETERS</span></span>

### <span data-ttu-id="a8118-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="a8118-116">-Filter</span></span>
<span data-ttu-id="a8118-117">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="a8118-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="a8118-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="a8118-118">-Location</span></span>
<span data-ttu-id="a8118-119">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="a8118-119">Location of the resource.</span></span>

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

### <span data-ttu-id="a8118-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="a8118-120">-Name</span></span>
<span data-ttu-id="a8118-121">Namnet på Edge Gateway-poolen.</span><span class="sxs-lookup"><span data-stu-id="a8118-121">Name of the edge gateway pool.</span></span>

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

### <span data-ttu-id="a8118-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8118-122">-ResourceGroupName</span></span>
<span data-ttu-id="a8118-123">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="a8118-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="a8118-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8118-124">-ResourceId</span></span>
<span data-ttu-id="a8118-125">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="a8118-125">The resource id.</span></span>

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

### <span data-ttu-id="a8118-126">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="a8118-126">-Skip</span></span>
<span data-ttu-id="a8118-127">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="a8118-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="a8118-128">-Överst</span><span class="sxs-lookup"><span data-stu-id="a8118-128">-Top</span></span>
<span data-ttu-id="a8118-129">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="a8118-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="a8118-130">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="a8118-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="a8118-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8118-131">CommonParameters</span></span>
<span data-ttu-id="a8118-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8118-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8118-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8118-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8118-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a8118-134">INPUTS</span></span>

## <span data-ttu-id="a8118-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a8118-135">OUTPUTS</span></span>

### <span data-ttu-id="a8118-136">Microsoft. AzureStack. Management. Fabric. admin. Models. EdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="a8118-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.EdgeGatewayPool</span></span>

## <span data-ttu-id="a8118-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a8118-137">NOTES</span></span>

## <span data-ttu-id="a8118-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a8118-138">RELATED LINKS</span></span>

