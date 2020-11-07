---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e42278eb4ed402d561399dbd1077f819ef3d2cd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921182"
---
# <span data-ttu-id="0f9a8-101">Get-AzsRPHealth</span><span class="sxs-lookup"><span data-stu-id="0f9a8-101">Get-AzsRPHealth</span></span>

## <span data-ttu-id="0f9a8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0f9a8-102">SYNOPSIS</span></span>
<span data-ttu-id="0f9a8-103">Returnerar en lista över tjänstens status.</span><span class="sxs-lookup"><span data-stu-id="0f9a8-103">Returns a list of each service's health.</span></span>

## <span data-ttu-id="0f9a8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0f9a8-104">SYNTAX</span></span>

### <span data-ttu-id="0f9a8-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="0f9a8-105">List (Default)</span></span>
```
Get-AzsRPHealth [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="0f9a8-106">Lära</span><span class="sxs-lookup"><span data-stu-id="0f9a8-106">Get</span></span>
```
Get-AzsRPHealth [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="0f9a8-107">ID</span><span class="sxs-lookup"><span data-stu-id="0f9a8-107">ResourceId</span></span>
```
Get-AzsRPHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="0f9a8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0f9a8-108">DESCRIPTION</span></span>
<span data-ttu-id="0f9a8-109">Returnerar en lista över tjänstens status.</span><span class="sxs-lookup"><span data-stu-id="0f9a8-109">Returns a list of each service's health.</span></span> <span data-ttu-id="0f9a8-110">Egenskapen AlertSummary innehåller information om antalet varningar och fel.</span><span class="sxs-lookup"><span data-stu-id="0f9a8-110">The AlertSummary property includes details on warning/error counts.</span></span>

## <span data-ttu-id="0f9a8-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0f9a8-111">EXAMPLES</span></span>

### <span data-ttu-id="0f9a8-112">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0f9a8-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsRPHealth
```

<span data-ttu-id="0f9a8-113">Returnerar en lista över tjänstens status.</span><span class="sxs-lookup"><span data-stu-id="0f9a8-113">Returns a list of each service's health.</span></span>

### <span data-ttu-id="0f9a8-114">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="0f9a8-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsRPHealth -Name "e56bc7b8-c8b5-4e25-b00c-4f951effb22c"
```

<span data-ttu-id="0f9a8-115">Returnerar tjänstens status.</span><span class="sxs-lookup"><span data-stu-id="0f9a8-115">Returns a service's health.</span></span>

## <span data-ttu-id="0f9a8-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0f9a8-116">PARAMETERS</span></span>

### <span data-ttu-id="0f9a8-117">-Filter</span><span class="sxs-lookup"><span data-stu-id="0f9a8-117">-Filter</span></span>
<span data-ttu-id="0f9a8-118">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="0f9a8-118">OData filter parameter.</span></span>

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

### <span data-ttu-id="0f9a8-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="0f9a8-119">-Location</span></span>
<span data-ttu-id="0f9a8-120">Regionens namn</span><span class="sxs-lookup"><span data-stu-id="0f9a8-120">Name of the region</span></span>

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

### <span data-ttu-id="0f9a8-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="0f9a8-121">-Name</span></span>
<span data-ttu-id="0f9a8-122">Tjänstens hälso namn.</span><span class="sxs-lookup"><span data-stu-id="0f9a8-122">Service Health name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: ServiceHealth

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f9a8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f9a8-123">-ResourceGroupName</span></span>
<span data-ttu-id="0f9a8-124">Resurs grupp namn som resursen finns.</span><span class="sxs-lookup"><span data-stu-id="0f9a8-124">Resource group name which the resource resides.</span></span>

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

### <span data-ttu-id="0f9a8-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f9a8-125">-ResourceId</span></span>
<span data-ttu-id="0f9a8-126">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="0f9a8-126">The resource id.</span></span>

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

### <span data-ttu-id="0f9a8-127">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="0f9a8-127">-Skip</span></span>
<span data-ttu-id="0f9a8-128">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="0f9a8-128">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="0f9a8-129">-Överst</span><span class="sxs-lookup"><span data-stu-id="0f9a8-129">-Top</span></span>
<span data-ttu-id="0f9a8-130">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="0f9a8-130">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="0f9a8-131">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="0f9a8-131">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="0f9a8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f9a8-132">CommonParameters</span></span>
<span data-ttu-id="0f9a8-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f9a8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f9a8-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f9a8-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f9a8-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0f9a8-135">INPUTS</span></span>

## <span data-ttu-id="0f9a8-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0f9a8-136">OUTPUTS</span></span>

### <span data-ttu-id="0f9a8-137">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. ServiceHealth</span><span class="sxs-lookup"><span data-stu-id="0f9a8-137">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.ServiceHealth</span></span>

## <span data-ttu-id="0f9a8-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0f9a8-138">NOTES</span></span>

## <span data-ttu-id="0f9a8-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0f9a8-139">RELATED LINKS</span></span>

