---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c5fe6e28ff87cfd3f365441d0e09f09ef21dc454
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921371"
---
# <span data-ttu-id="56c95-101">Get-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="56c95-101">Get-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="56c95-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="56c95-102">SYNOPSIS</span></span>
<span data-ttu-id="56c95-103">Returnerar en lista över alla infrastruktur roll instanser på en plats.</span><span class="sxs-lookup"><span data-stu-id="56c95-103">Returns a list of all infrastructure role instances at a location.</span></span>

## <span data-ttu-id="56c95-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="56c95-104">SYNTAX</span></span>

### <span data-ttu-id="56c95-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="56c95-105">List (Default)</span></span>
```
Get-AzsInfrastructureRoleInstance [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="56c95-106">Lära</span><span class="sxs-lookup"><span data-stu-id="56c95-106">Get</span></span>
```
Get-AzsInfrastructureRoleInstance [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="56c95-107">ID</span><span class="sxs-lookup"><span data-stu-id="56c95-107">ResourceId</span></span>
```
Get-AzsInfrastructureRoleInstance -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="56c95-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="56c95-108">DESCRIPTION</span></span>
<span data-ttu-id="56c95-109">Returnerar en lista över alla infrastruktur roll instanser på en plats.</span><span class="sxs-lookup"><span data-stu-id="56c95-109">Returns a list of all infrastructure role instances at a location.</span></span>

## <span data-ttu-id="56c95-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="56c95-110">EXAMPLES</span></span>

### <span data-ttu-id="56c95-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="56c95-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureRoleInstance
```

<span data-ttu-id="56c95-112">Returnera en lista över alla infrastruktur roll instanser.</span><span class="sxs-lookup"><span data-stu-id="56c95-112">Return a list of all infrastructure role instances.</span></span>

### <span data-ttu-id="56c95-113">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="56c95-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="56c95-114">Returnera en enskild infrastrukturs instans baserat på namn.</span><span class="sxs-lookup"><span data-stu-id="56c95-114">Return a single infrastructure role instance based on name.</span></span>

## <span data-ttu-id="56c95-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="56c95-115">PARAMETERS</span></span>

### <span data-ttu-id="56c95-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="56c95-116">-Name</span></span>
<span data-ttu-id="56c95-117">Namn på en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="56c95-117">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="56c95-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="56c95-118">-Location</span></span>
<span data-ttu-id="56c95-119">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="56c95-119">Location of the resource.</span></span>

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

### <span data-ttu-id="56c95-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56c95-120">-ResourceGroupName</span></span>
<span data-ttu-id="56c95-121">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="56c95-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="56c95-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56c95-122">-ResourceId</span></span>
<span data-ttu-id="56c95-123">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="56c95-123">The resource id.</span></span>

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

### <span data-ttu-id="56c95-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="56c95-124">-Filter</span></span>
<span data-ttu-id="56c95-125">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="56c95-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="56c95-126">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="56c95-126">-Skip</span></span>
<span data-ttu-id="56c95-127">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="56c95-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="56c95-128">-Överst</span><span class="sxs-lookup"><span data-stu-id="56c95-128">-Top</span></span>
<span data-ttu-id="56c95-129">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="56c95-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="56c95-130">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="56c95-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="56c95-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56c95-131">CommonParameters</span></span>
<span data-ttu-id="56c95-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56c95-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56c95-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56c95-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56c95-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="56c95-134">INPUTS</span></span>

## <span data-ttu-id="56c95-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="56c95-135">OUTPUTS</span></span>

### <span data-ttu-id="56c95-136">Microsoft. AzureStack. Management. Fabric. admin. Models. InfraRoleInstance</span><span class="sxs-lookup"><span data-stu-id="56c95-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.InfraRoleInstance</span></span>

## <span data-ttu-id="56c95-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="56c95-137">NOTES</span></span>

## <span data-ttu-id="56c95-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="56c95-138">RELATED LINKS</span></span>
