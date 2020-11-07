---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c5fe6e28ff87cfd3f365441d0e09f09ef21dc454
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921711"
---
# <span data-ttu-id="31944-101">Get-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="31944-101">Get-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="31944-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="31944-102">SYNOPSIS</span></span>
<span data-ttu-id="31944-103">Returnerar en lista över alla infrastruktur roll instanser på en plats.</span><span class="sxs-lookup"><span data-stu-id="31944-103">Returns a list of all infrastructure role instances at a location.</span></span>

## <span data-ttu-id="31944-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="31944-104">SYNTAX</span></span>

### <span data-ttu-id="31944-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="31944-105">List (Default)</span></span>
```
Get-AzsInfrastructureRoleInstance [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="31944-106">Lära</span><span class="sxs-lookup"><span data-stu-id="31944-106">Get</span></span>
```
Get-AzsInfrastructureRoleInstance [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="31944-107">ID</span><span class="sxs-lookup"><span data-stu-id="31944-107">ResourceId</span></span>
```
Get-AzsInfrastructureRoleInstance -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="31944-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="31944-108">DESCRIPTION</span></span>
<span data-ttu-id="31944-109">Returnerar en lista över alla infrastruktur roll instanser på en plats.</span><span class="sxs-lookup"><span data-stu-id="31944-109">Returns a list of all infrastructure role instances at a location.</span></span>

## <span data-ttu-id="31944-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="31944-110">EXAMPLES</span></span>

### <span data-ttu-id="31944-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="31944-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureRoleInstance
```

<span data-ttu-id="31944-112">Returnera en lista över alla infrastruktur roll instanser.</span><span class="sxs-lookup"><span data-stu-id="31944-112">Return a list of all infrastructure role instances.</span></span>

### <span data-ttu-id="31944-113">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="31944-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="31944-114">Returnera en enskild infrastrukturs instans baserat på namn.</span><span class="sxs-lookup"><span data-stu-id="31944-114">Return a single infrastructure role instance based on name.</span></span>

## <span data-ttu-id="31944-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="31944-115">PARAMETERS</span></span>

### <span data-ttu-id="31944-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="31944-116">-Name</span></span>
<span data-ttu-id="31944-117">Namn på en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="31944-117">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="31944-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="31944-118">-Location</span></span>
<span data-ttu-id="31944-119">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="31944-119">Location of the resource.</span></span>

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

### <span data-ttu-id="31944-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31944-120">-ResourceGroupName</span></span>
<span data-ttu-id="31944-121">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="31944-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="31944-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31944-122">-ResourceId</span></span>
<span data-ttu-id="31944-123">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="31944-123">The resource id.</span></span>

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

### <span data-ttu-id="31944-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="31944-124">-Filter</span></span>
<span data-ttu-id="31944-125">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="31944-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="31944-126">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="31944-126">-Skip</span></span>
<span data-ttu-id="31944-127">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="31944-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="31944-128">-Överst</span><span class="sxs-lookup"><span data-stu-id="31944-128">-Top</span></span>
<span data-ttu-id="31944-129">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="31944-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="31944-130">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="31944-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="31944-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31944-131">CommonParameters</span></span>
<span data-ttu-id="31944-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31944-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31944-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31944-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31944-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="31944-134">INPUTS</span></span>

## <span data-ttu-id="31944-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="31944-135">OUTPUTS</span></span>

### <span data-ttu-id="31944-136">Microsoft. AzureStack. Management. Fabric. admin. Models. InfraRoleInstance</span><span class="sxs-lookup"><span data-stu-id="31944-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.InfraRoleInstance</span></span>

## <span data-ttu-id="31944-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="31944-137">NOTES</span></span>

## <span data-ttu-id="31944-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="31944-138">RELATED LINKS</span></span>
