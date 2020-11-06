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
ms.locfileid: "93572196"
---
# <span data-ttu-id="91136-101">Get-AzsEdgeGateway</span><span class="sxs-lookup"><span data-stu-id="91136-101">Get-AzsEdgeGateway</span></span>

## <span data-ttu-id="91136-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="91136-102">SYNOPSIS</span></span>
<span data-ttu-id="91136-103">Returnerar listan över alla Edge-gateways på en viss plats.</span><span class="sxs-lookup"><span data-stu-id="91136-103">Returns the list of all edge gateways at a certain location.</span></span>

## <span data-ttu-id="91136-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="91136-104">SYNTAX</span></span>

### <span data-ttu-id="91136-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="91136-105">List (Default)</span></span>
```
Get-AzsEdgeGateway [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="91136-106">Lära</span><span class="sxs-lookup"><span data-stu-id="91136-106">Get</span></span>
```
Get-AzsEdgeGateway [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="91136-107">ID</span><span class="sxs-lookup"><span data-stu-id="91136-107">ResourceId</span></span>
```
Get-AzsEdgeGateway -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="91136-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="91136-108">DESCRIPTION</span></span>
<span data-ttu-id="91136-109">Returnerar listan över alla Edge-gateways på en viss plats.</span><span class="sxs-lookup"><span data-stu-id="91136-109">Returns the list of all edge gateways at a certain location.</span></span>

## <span data-ttu-id="91136-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="91136-110">EXAMPLES</span></span>

### <span data-ttu-id="91136-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="91136-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsEdgeGateway
```

<span data-ttu-id="91136-112">Få en lista över alla Edge-gateways.</span><span class="sxs-lookup"><span data-stu-id="91136-112">Get a list of all edge gateways.</span></span>

### <span data-ttu-id="91136-113">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="91136-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsEdgeGateway -Name "AzS-Gwy01"
```

<span data-ttu-id="91136-114">Skaffa en specifik Gateway för Edge.</span><span class="sxs-lookup"><span data-stu-id="91136-114">Get a specific edge gateway.</span></span>

## <span data-ttu-id="91136-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="91136-115">PARAMETERS</span></span>

### <span data-ttu-id="91136-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="91136-116">-Filter</span></span>
<span data-ttu-id="91136-117">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="91136-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="91136-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="91136-118">-Location</span></span>
<span data-ttu-id="91136-119">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="91136-119">Location of the resource.</span></span>

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

### <span data-ttu-id="91136-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="91136-120">-Name</span></span>
<span data-ttu-id="91136-121">Namn på Edge Gateway.</span><span class="sxs-lookup"><span data-stu-id="91136-121">Name of the edge gateway.</span></span>

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

### <span data-ttu-id="91136-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91136-122">-ResourceGroupName</span></span>
<span data-ttu-id="91136-123">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="91136-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="91136-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91136-124">-ResourceId</span></span>
<span data-ttu-id="91136-125">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="91136-125">The resource id.</span></span>

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

### <span data-ttu-id="91136-126">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="91136-126">-Skip</span></span>
<span data-ttu-id="91136-127">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="91136-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="91136-128">-Överst</span><span class="sxs-lookup"><span data-stu-id="91136-128">-Top</span></span>
<span data-ttu-id="91136-129">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="91136-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="91136-130">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="91136-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="91136-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91136-131">CommonParameters</span></span>
<span data-ttu-id="91136-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91136-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91136-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91136-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91136-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="91136-134">INPUTS</span></span>

## <span data-ttu-id="91136-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="91136-135">OUTPUTS</span></span>

### <span data-ttu-id="91136-136">Microsoft. AzureStack. Management. Fabric. admin. Models. EdgeGateway</span><span class="sxs-lookup"><span data-stu-id="91136-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.EdgeGateway</span></span>

## <span data-ttu-id="91136-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="91136-137">NOTES</span></span>

## <span data-ttu-id="91136-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="91136-138">RELATED LINKS</span></span>

