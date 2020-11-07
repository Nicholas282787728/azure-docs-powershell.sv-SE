---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 39955a2b99ffd7e3c604b4fc288f117face8205f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754944"
---
# <span data-ttu-id="e0147-101">Get-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="e0147-101">Get-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="e0147-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e0147-102">SYNOPSIS</span></span>
<span data-ttu-id="e0147-103">Returnerar en lista över alla infrastruktur roll instanser på en plats.</span><span class="sxs-lookup"><span data-stu-id="e0147-103">Returns a list of all infrastructure role instances at a location.</span></span>

## <span data-ttu-id="e0147-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e0147-104">SYNTAX</span></span>

### <span data-ttu-id="e0147-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="e0147-105">List (Default)</span></span>
```
Get-AzsInfrastructureRoleInstance [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="e0147-106">Lära</span><span class="sxs-lookup"><span data-stu-id="e0147-106">Get</span></span>
```
Get-AzsInfrastructureRoleInstance [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="e0147-107">ID</span><span class="sxs-lookup"><span data-stu-id="e0147-107">ResourceId</span></span>
```
Get-AzsInfrastructureRoleInstance -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="e0147-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e0147-108">DESCRIPTION</span></span>
<span data-ttu-id="e0147-109">Returnerar en lista över alla infrastruktur roll instanser på en plats.</span><span class="sxs-lookup"><span data-stu-id="e0147-109">Returns a list of all infrastructure role instances at a location.</span></span>

## <span data-ttu-id="e0147-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e0147-110">EXAMPLES</span></span>

### <span data-ttu-id="e0147-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e0147-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureRoleInstance
```

<span data-ttu-id="e0147-112">Returnera en lista över alla infrastruktur roll instanser.</span><span class="sxs-lookup"><span data-stu-id="e0147-112">Return a list of all infrastructure role instances.</span></span>

### <span data-ttu-id="e0147-113">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="e0147-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="e0147-114">Returnera en enskild infrastrukturs instans baserat på namn.</span><span class="sxs-lookup"><span data-stu-id="e0147-114">Return a single infrastructure role instance based on name.</span></span>

## <span data-ttu-id="e0147-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e0147-115">PARAMETERS</span></span>

### <span data-ttu-id="e0147-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="e0147-116">-Filter</span></span>
<span data-ttu-id="e0147-117">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="e0147-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="e0147-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="e0147-118">-Location</span></span>
<span data-ttu-id="e0147-119">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="e0147-119">Location of the resource.</span></span>

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

### <span data-ttu-id="e0147-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="e0147-120">-Name</span></span>
<span data-ttu-id="e0147-121">Namn på en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="e0147-121">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="e0147-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0147-122">-ResourceGroupName</span></span>
<span data-ttu-id="e0147-123">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="e0147-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="e0147-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0147-124">-ResourceId</span></span>
<span data-ttu-id="e0147-125">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="e0147-125">The resource id.</span></span>

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

### <span data-ttu-id="e0147-126">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="e0147-126">-Skip</span></span>
<span data-ttu-id="e0147-127">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="e0147-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="e0147-128">-Överst</span><span class="sxs-lookup"><span data-stu-id="e0147-128">-Top</span></span>
<span data-ttu-id="e0147-129">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="e0147-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="e0147-130">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="e0147-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="e0147-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0147-131">CommonParameters</span></span>
<span data-ttu-id="e0147-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0147-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0147-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0147-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0147-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e0147-134">INPUTS</span></span>

## <span data-ttu-id="e0147-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e0147-135">OUTPUTS</span></span>

### <span data-ttu-id="e0147-136">Microsoft. AzureStack. Management. Fabric. admin. Models. InfraRoleInstance</span><span class="sxs-lookup"><span data-stu-id="e0147-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.InfraRoleInstance</span></span>

## <span data-ttu-id="e0147-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e0147-137">NOTES</span></span>

## <span data-ttu-id="e0147-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e0147-138">RELATED LINKS</span></span>

