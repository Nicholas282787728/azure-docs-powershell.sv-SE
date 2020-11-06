---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 82ef5db457846f6fdf0dcd0a0a32b37cab96a557
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572328"
---
# <span data-ttu-id="6892c-101">Get-AzsLogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="6892c-101">Get-AzsLogicalSubnet</span></span>

## <span data-ttu-id="6892c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6892c-102">SYNOPSIS</span></span>
<span data-ttu-id="6892c-103">Returnerar en lista över alla logiska undernät.</span><span class="sxs-lookup"><span data-stu-id="6892c-103">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="6892c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6892c-104">SYNTAX</span></span>

### <span data-ttu-id="6892c-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="6892c-105">List (Default)</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="6892c-106">Lära</span><span class="sxs-lookup"><span data-stu-id="6892c-106">Get</span></span>
```
Get-AzsLogicalSubnet -Name <String> -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="6892c-107">ID</span><span class="sxs-lookup"><span data-stu-id="6892c-107">ResourceId</span></span>
```
Get-AzsLogicalSubnet -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="6892c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6892c-108">DESCRIPTION</span></span>
<span data-ttu-id="6892c-109">Returnerar en lista över alla logiska undernät.</span><span class="sxs-lookup"><span data-stu-id="6892c-109">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="6892c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6892c-110">EXAMPLES</span></span>

### <span data-ttu-id="6892c-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6892c-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001"
```

<span data-ttu-id="6892c-112">Få en lista över alla logiska undernät för ett givet logiskt nätverk och en given plats.</span><span class="sxs-lookup"><span data-stu-id="6892c-112">Get a list of all logical subnets for a given logical network and location.</span></span>

### <span data-ttu-id="6892c-113">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="6892c-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001" -Name "d8cfef2d-c0c8-4cdb-b0a8-fb1bdf3f2ad7"
```

<span data-ttu-id="6892c-114">Skaffa ett specifikt logiskt undernät för ett angivet logiskt nätverk och plats baserat på namn.</span><span class="sxs-lookup"><span data-stu-id="6892c-114">Get a specific logical subnet for a given logical network and location based on name.</span></span>

## <span data-ttu-id="6892c-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6892c-115">PARAMETERS</span></span>

### <span data-ttu-id="6892c-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="6892c-116">-Filter</span></span>
<span data-ttu-id="6892c-117">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="6892c-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="6892c-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="6892c-118">-Location</span></span>
<span data-ttu-id="6892c-119">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="6892c-119">Location of the resource.</span></span>

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

### <span data-ttu-id="6892c-120">-LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="6892c-120">-LogicalNetwork</span></span>
<span data-ttu-id="6892c-121">Namn på det logiska nätverket.</span><span class="sxs-lookup"><span data-stu-id="6892c-121">Name of the logical network.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6892c-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="6892c-122">-Name</span></span>
<span data-ttu-id="6892c-123">Namnet på det logiska under nätet.</span><span class="sxs-lookup"><span data-stu-id="6892c-123">Name of the logical subnet.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6892c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6892c-124">-ResourceGroupName</span></span>
<span data-ttu-id="6892c-125">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="6892c-125">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="6892c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6892c-126">-ResourceId</span></span>
<span data-ttu-id="6892c-127">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="6892c-127">The resource id.</span></span>

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

### <span data-ttu-id="6892c-128">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="6892c-128">-Skip</span></span>
<span data-ttu-id="6892c-129">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="6892c-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="6892c-130">-Överst</span><span class="sxs-lookup"><span data-stu-id="6892c-130">-Top</span></span>
<span data-ttu-id="6892c-131">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="6892c-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="6892c-132">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="6892c-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="6892c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6892c-133">CommonParameters</span></span>
<span data-ttu-id="6892c-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6892c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6892c-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6892c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6892c-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6892c-136">INPUTS</span></span>

## <span data-ttu-id="6892c-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6892c-137">OUTPUTS</span></span>

### <span data-ttu-id="6892c-138">Microsoft. AzureStack. Management. Fabric. admin. Models. LogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="6892c-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.LogicalSubnet</span></span>

## <span data-ttu-id="6892c-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6892c-139">NOTES</span></span>

## <span data-ttu-id="6892c-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6892c-140">RELATED LINKS</span></span>

