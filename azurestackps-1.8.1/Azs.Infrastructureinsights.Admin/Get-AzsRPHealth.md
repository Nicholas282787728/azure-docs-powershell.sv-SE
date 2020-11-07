---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 752bd7f183bf5a5bdad7950e6567024cbe5b8dec
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921839"
---
# <span data-ttu-id="495af-101">Get-AzsRPHealth</span><span class="sxs-lookup"><span data-stu-id="495af-101">Get-AzsRPHealth</span></span>

## <span data-ttu-id="495af-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="495af-102">SYNOPSIS</span></span>
<span data-ttu-id="495af-103">Returnerar en lista över tjänstens status.</span><span class="sxs-lookup"><span data-stu-id="495af-103">Returns a list of each service's health.</span></span>

## <span data-ttu-id="495af-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="495af-104">SYNTAX</span></span>

### <span data-ttu-id="495af-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="495af-105">List (Default)</span></span>
```
Get-AzsRPHealth [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="495af-106">Lära</span><span class="sxs-lookup"><span data-stu-id="495af-106">Get</span></span>
```
Get-AzsRPHealth [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="495af-107">ID</span><span class="sxs-lookup"><span data-stu-id="495af-107">ResourceId</span></span>
```
Get-AzsRPHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="495af-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="495af-108">DESCRIPTION</span></span>
<span data-ttu-id="495af-109">Returnerar en lista över tjänstens status.</span><span class="sxs-lookup"><span data-stu-id="495af-109">Returns a list of each service's health.</span></span> <span data-ttu-id="495af-110">Egenskapen AlertSummary innehåller information om antalet varningar och fel.</span><span class="sxs-lookup"><span data-stu-id="495af-110">The AlertSummary property includes details on warning/error counts.</span></span>

## <span data-ttu-id="495af-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="495af-111">EXAMPLES</span></span>

### <span data-ttu-id="495af-112">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="495af-112">EXAMPLE 1</span></span>
```
Get-AzsRPHealth
```

<span data-ttu-id="495af-113">Returnerar en lista över tjänstens status.</span><span class="sxs-lookup"><span data-stu-id="495af-113">Returns a list of each service's health.</span></span>

### <span data-ttu-id="495af-114">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="495af-114">EXAMPLE 2</span></span>
```
Get-AzsRPHealth -Name "e56bc7b8-c8b5-4e25-b00c-4f951effb22c"
```

<span data-ttu-id="495af-115">Returnerar tjänstens status.</span><span class="sxs-lookup"><span data-stu-id="495af-115">Returns a service's health.</span></span>

## <span data-ttu-id="495af-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="495af-116">PARAMETERS</span></span>

### <span data-ttu-id="495af-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="495af-117">-Name</span></span>
<span data-ttu-id="495af-118">Tjänstens hälso namn.</span><span class="sxs-lookup"><span data-stu-id="495af-118">Service Health name.</span></span>

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

### <span data-ttu-id="495af-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="495af-119">-Location</span></span>
<span data-ttu-id="495af-120">Regionens namn</span><span class="sxs-lookup"><span data-stu-id="495af-120">Name of the region</span></span>

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

### <span data-ttu-id="495af-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="495af-121">-ResourceGroupName</span></span>
<span data-ttu-id="495af-122">Namnet på resurs gruppen, valfritt.</span><span class="sxs-lookup"><span data-stu-id="495af-122">Name of the resource group, optional.</span></span>

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

### <span data-ttu-id="495af-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="495af-123">-ResourceId</span></span>
<span data-ttu-id="495af-124">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="495af-124">The resource id.</span></span>

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

### <span data-ttu-id="495af-125">-Filter</span><span class="sxs-lookup"><span data-stu-id="495af-125">-Filter</span></span>
<span data-ttu-id="495af-126">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="495af-126">OData filter parameter.</span></span>

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

### <span data-ttu-id="495af-127">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="495af-127">-Skip</span></span>
<span data-ttu-id="495af-128">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="495af-128">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="495af-129">-Överst</span><span class="sxs-lookup"><span data-stu-id="495af-129">-Top</span></span>
<span data-ttu-id="495af-130">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="495af-130">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="495af-131">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="495af-131">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="495af-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="495af-132">CommonParameters</span></span>
<span data-ttu-id="495af-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="495af-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="495af-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="495af-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="495af-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="495af-135">INPUTS</span></span>

## <span data-ttu-id="495af-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="495af-136">OUTPUTS</span></span>

### <span data-ttu-id="495af-137">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. ServiceHealth</span><span class="sxs-lookup"><span data-stu-id="495af-137">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.ServiceHealth</span></span>

## <span data-ttu-id="495af-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="495af-138">NOTES</span></span>

## <span data-ttu-id="495af-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="495af-139">RELATED LINKS</span></span>
