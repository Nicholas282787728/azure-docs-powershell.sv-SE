---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc074d17ea73bf54f623ea3e8ec72567ef2bcffe
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921374"
---
# <span data-ttu-id="df60f-101">Get-AzsInfrastructureLocation</span><span class="sxs-lookup"><span data-stu-id="df60f-101">Get-AzsInfrastructureLocation</span></span>

## <span data-ttu-id="df60f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="df60f-102">SYNOPSIS</span></span>
<span data-ttu-id="df60f-103">Returnerar en lista över alla infrastruktur platser.</span><span class="sxs-lookup"><span data-stu-id="df60f-103">Returns a list of all fabric locations.</span></span>

## <span data-ttu-id="df60f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="df60f-104">SYNTAX</span></span>

### <span data-ttu-id="df60f-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="df60f-105">List (Default)</span></span>
```
Get-AzsInfrastructureLocation [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="df60f-106">Lära</span><span class="sxs-lookup"><span data-stu-id="df60f-106">Get</span></span>
```
Get-AzsInfrastructureLocation [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="df60f-107">ID</span><span class="sxs-lookup"><span data-stu-id="df60f-107">ResourceId</span></span>
```
Get-AzsInfrastructureLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="df60f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="df60f-108">DESCRIPTION</span></span>
<span data-ttu-id="df60f-109">Returnerar en lista över alla infrastruktur platser.</span><span class="sxs-lookup"><span data-stu-id="df60f-109">Returns a list of all fabric locations.</span></span>

## <span data-ttu-id="df60f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="df60f-110">EXAMPLES</span></span>

### <span data-ttu-id="df60f-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="df60f-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureLocation
```

<span data-ttu-id="df60f-112">Returnera en lista över alla infrastruktur platser.</span><span class="sxs-lookup"><span data-stu-id="df60f-112">Return a list of all fabric locations.</span></span>

### <span data-ttu-id="df60f-113">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="df60f-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureLocation -Location "local"
```

<span data-ttu-id="df60f-114">Returnera en plats utifrån namnet.</span><span class="sxs-lookup"><span data-stu-id="df60f-114">Return a location based on the name.</span></span>

## <span data-ttu-id="df60f-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="df60f-115">PARAMETERS</span></span>

### <span data-ttu-id="df60f-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="df60f-116">-Location</span></span>
<span data-ttu-id="df60f-117">Fabric-plats.</span><span class="sxs-lookup"><span data-stu-id="df60f-117">Fabric location.</span></span>

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

### <span data-ttu-id="df60f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df60f-118">-ResourceGroupName</span></span>
<span data-ttu-id="df60f-119">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="df60f-119">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="df60f-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df60f-120">-ResourceId</span></span>
<span data-ttu-id="df60f-121">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="df60f-121">The resource id.</span></span>

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

### <span data-ttu-id="df60f-122">-Filter</span><span class="sxs-lookup"><span data-stu-id="df60f-122">-Filter</span></span>
<span data-ttu-id="df60f-123">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="df60f-123">OData filter parameter.</span></span>

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

### <span data-ttu-id="df60f-124">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="df60f-124">-Skip</span></span>
<span data-ttu-id="df60f-125">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="df60f-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="df60f-126">-Överst</span><span class="sxs-lookup"><span data-stu-id="df60f-126">-Top</span></span>
<span data-ttu-id="df60f-127">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="df60f-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="df60f-128">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="df60f-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="df60f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df60f-129">CommonParameters</span></span>
<span data-ttu-id="df60f-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df60f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df60f-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df60f-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df60f-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="df60f-132">INPUTS</span></span>

## <span data-ttu-id="df60f-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="df60f-133">OUTPUTS</span></span>

### <span data-ttu-id="df60f-134">Microsoft. AzureStack. Management. Fabric. admin. Models. FabricLocation</span><span class="sxs-lookup"><span data-stu-id="df60f-134">Microsoft.AzureStack.Management.Fabric.Admin.Models.FabricLocation</span></span>

## <span data-ttu-id="df60f-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="df60f-135">NOTES</span></span>

## <span data-ttu-id="df60f-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="df60f-136">RELATED LINKS</span></span>
