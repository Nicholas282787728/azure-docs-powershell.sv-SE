---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcd5d112fea0ec68e372a5ad282b3d661f9481ea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743353"
---
# <span data-ttu-id="1ae68-101">Get-AzsInfrastructureLocation</span><span class="sxs-lookup"><span data-stu-id="1ae68-101">Get-AzsInfrastructureLocation</span></span>

## <span data-ttu-id="1ae68-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1ae68-102">SYNOPSIS</span></span>
<span data-ttu-id="1ae68-103">Returnerar en lista över alla infrastruktur platser.</span><span class="sxs-lookup"><span data-stu-id="1ae68-103">Returns a list of all fabric locations.</span></span>

## <span data-ttu-id="1ae68-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1ae68-104">SYNTAX</span></span>

### <span data-ttu-id="1ae68-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="1ae68-105">List (Default)</span></span>
```
Get-AzsInfrastructureLocation [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="1ae68-106">Lära</span><span class="sxs-lookup"><span data-stu-id="1ae68-106">Get</span></span>
```
Get-AzsInfrastructureLocation [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="1ae68-107">ID</span><span class="sxs-lookup"><span data-stu-id="1ae68-107">ResourceId</span></span>
```
Get-AzsInfrastructureLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="1ae68-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1ae68-108">DESCRIPTION</span></span>
<span data-ttu-id="1ae68-109">Returnerar en lista över alla infrastruktur platser.</span><span class="sxs-lookup"><span data-stu-id="1ae68-109">Returns a list of all fabric locations.</span></span>

## <span data-ttu-id="1ae68-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1ae68-110">EXAMPLES</span></span>

### <span data-ttu-id="1ae68-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1ae68-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureLocation
```

<span data-ttu-id="1ae68-112">Returnera en lista över alla infrastruktur platser.</span><span class="sxs-lookup"><span data-stu-id="1ae68-112">Return a list of all fabric locations.</span></span>

### <span data-ttu-id="1ae68-113">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="1ae68-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureLocation -Location "local"
```

<span data-ttu-id="1ae68-114">Returnera en plats utifrån namnet.</span><span class="sxs-lookup"><span data-stu-id="1ae68-114">Return a location based on the name.</span></span>

## <span data-ttu-id="1ae68-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1ae68-115">PARAMETERS</span></span>

### <span data-ttu-id="1ae68-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="1ae68-116">-Filter</span></span>
<span data-ttu-id="1ae68-117">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="1ae68-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="1ae68-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="1ae68-118">-Location</span></span>
<span data-ttu-id="1ae68-119">Fabric-plats.</span><span class="sxs-lookup"><span data-stu-id="1ae68-119">Fabric location.</span></span>

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

### <span data-ttu-id="1ae68-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ae68-120">-ResourceGroupName</span></span>
<span data-ttu-id="1ae68-121">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="1ae68-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="1ae68-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ae68-122">-ResourceId</span></span>
<span data-ttu-id="1ae68-123">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="1ae68-123">The resource id.</span></span>

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

### <span data-ttu-id="1ae68-124">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="1ae68-124">-Skip</span></span>
<span data-ttu-id="1ae68-125">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="1ae68-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="1ae68-126">-Överst</span><span class="sxs-lookup"><span data-stu-id="1ae68-126">-Top</span></span>
<span data-ttu-id="1ae68-127">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="1ae68-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="1ae68-128">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="1ae68-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="1ae68-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ae68-129">CommonParameters</span></span>
<span data-ttu-id="1ae68-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ae68-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ae68-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ae68-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ae68-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1ae68-132">INPUTS</span></span>

## <span data-ttu-id="1ae68-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1ae68-133">OUTPUTS</span></span>

### <span data-ttu-id="1ae68-134">Microsoft. AzureStack. Management. Fabric. admin. Models. FabricLocation</span><span class="sxs-lookup"><span data-stu-id="1ae68-134">Microsoft.AzureStack.Management.Fabric.Admin.Models.FabricLocation</span></span>

## <span data-ttu-id="1ae68-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1ae68-135">NOTES</span></span>

## <span data-ttu-id="1ae68-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1ae68-136">RELATED LINKS</span></span>

