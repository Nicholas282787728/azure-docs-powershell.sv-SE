---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc074d17ea73bf54f623ea3e8ec72567ef2bcffe
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921718"
---
# <span data-ttu-id="fea1b-101">Get-AzsInfrastructureLocation</span><span class="sxs-lookup"><span data-stu-id="fea1b-101">Get-AzsInfrastructureLocation</span></span>

## <span data-ttu-id="fea1b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fea1b-102">SYNOPSIS</span></span>
<span data-ttu-id="fea1b-103">Returnerar en lista över alla infrastruktur platser.</span><span class="sxs-lookup"><span data-stu-id="fea1b-103">Returns a list of all fabric locations.</span></span>

## <span data-ttu-id="fea1b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fea1b-104">SYNTAX</span></span>

### <span data-ttu-id="fea1b-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="fea1b-105">List (Default)</span></span>
```
Get-AzsInfrastructureLocation [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="fea1b-106">Lära</span><span class="sxs-lookup"><span data-stu-id="fea1b-106">Get</span></span>
```
Get-AzsInfrastructureLocation [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="fea1b-107">ID</span><span class="sxs-lookup"><span data-stu-id="fea1b-107">ResourceId</span></span>
```
Get-AzsInfrastructureLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="fea1b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fea1b-108">DESCRIPTION</span></span>
<span data-ttu-id="fea1b-109">Returnerar en lista över alla infrastruktur platser.</span><span class="sxs-lookup"><span data-stu-id="fea1b-109">Returns a list of all fabric locations.</span></span>

## <span data-ttu-id="fea1b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fea1b-110">EXAMPLES</span></span>

### <span data-ttu-id="fea1b-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="fea1b-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureLocation
```

<span data-ttu-id="fea1b-112">Returnera en lista över alla infrastruktur platser.</span><span class="sxs-lookup"><span data-stu-id="fea1b-112">Return a list of all fabric locations.</span></span>

### <span data-ttu-id="fea1b-113">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="fea1b-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureLocation -Location "local"
```

<span data-ttu-id="fea1b-114">Returnera en plats utifrån namnet.</span><span class="sxs-lookup"><span data-stu-id="fea1b-114">Return a location based on the name.</span></span>

## <span data-ttu-id="fea1b-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fea1b-115">PARAMETERS</span></span>

### <span data-ttu-id="fea1b-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="fea1b-116">-Location</span></span>
<span data-ttu-id="fea1b-117">Fabric-plats.</span><span class="sxs-lookup"><span data-stu-id="fea1b-117">Fabric location.</span></span>

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

### <span data-ttu-id="fea1b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fea1b-118">-ResourceGroupName</span></span>
<span data-ttu-id="fea1b-119">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="fea1b-119">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="fea1b-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fea1b-120">-ResourceId</span></span>
<span data-ttu-id="fea1b-121">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="fea1b-121">The resource id.</span></span>

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

### <span data-ttu-id="fea1b-122">-Filter</span><span class="sxs-lookup"><span data-stu-id="fea1b-122">-Filter</span></span>
<span data-ttu-id="fea1b-123">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="fea1b-123">OData filter parameter.</span></span>

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

### <span data-ttu-id="fea1b-124">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="fea1b-124">-Skip</span></span>
<span data-ttu-id="fea1b-125">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="fea1b-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="fea1b-126">-Överst</span><span class="sxs-lookup"><span data-stu-id="fea1b-126">-Top</span></span>
<span data-ttu-id="fea1b-127">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="fea1b-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="fea1b-128">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="fea1b-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="fea1b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fea1b-129">CommonParameters</span></span>
<span data-ttu-id="fea1b-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fea1b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fea1b-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fea1b-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fea1b-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fea1b-132">INPUTS</span></span>

## <span data-ttu-id="fea1b-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fea1b-133">OUTPUTS</span></span>

### <span data-ttu-id="fea1b-134">Microsoft. AzureStack. Management. Fabric. admin. Models. FabricLocation</span><span class="sxs-lookup"><span data-stu-id="fea1b-134">Microsoft.AzureStack.Management.Fabric.Admin.Models.FabricLocation</span></span>

## <span data-ttu-id="fea1b-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fea1b-135">NOTES</span></span>

## <span data-ttu-id="fea1b-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fea1b-136">RELATED LINKS</span></span>
