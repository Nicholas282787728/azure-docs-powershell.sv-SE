---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 752bd7f183bf5a5bdad7950e6567024cbe5b8dec
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100344"
---
# <span data-ttu-id="1103a-101">Get-AzsRPHealth</span><span class="sxs-lookup"><span data-stu-id="1103a-101">Get-AzsRPHealth</span></span>

## <span data-ttu-id="1103a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1103a-102">SYNOPSIS</span></span>
<span data-ttu-id="1103a-103">Returnerar en lista över tjänstens status.</span><span class="sxs-lookup"><span data-stu-id="1103a-103">Returns a list of each service's health.</span></span>

## <span data-ttu-id="1103a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1103a-104">SYNTAX</span></span>

### <span data-ttu-id="1103a-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="1103a-105">List (Default)</span></span>
```
Get-AzsRPHealth [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="1103a-106">Lära</span><span class="sxs-lookup"><span data-stu-id="1103a-106">Get</span></span>
```
Get-AzsRPHealth [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="1103a-107">ID</span><span class="sxs-lookup"><span data-stu-id="1103a-107">ResourceId</span></span>
```
Get-AzsRPHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="1103a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1103a-108">DESCRIPTION</span></span>
<span data-ttu-id="1103a-109">Returnerar en lista över tjänstens status.</span><span class="sxs-lookup"><span data-stu-id="1103a-109">Returns a list of each service's health.</span></span> <span data-ttu-id="1103a-110">Egenskapen AlertSummary innehåller information om antalet varningar och fel.</span><span class="sxs-lookup"><span data-stu-id="1103a-110">The AlertSummary property includes details on warning/error counts.</span></span>

## <span data-ttu-id="1103a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1103a-111">EXAMPLES</span></span>

### <span data-ttu-id="1103a-112">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="1103a-112">EXAMPLE 1</span></span>
```
Get-AzsRPHealth
```

<span data-ttu-id="1103a-113">Returnerar en lista över tjänstens status.</span><span class="sxs-lookup"><span data-stu-id="1103a-113">Returns a list of each service's health.</span></span>

### <span data-ttu-id="1103a-114">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="1103a-114">EXAMPLE 2</span></span>
```
Get-AzsRPHealth -Name "e56bc7b8-c8b5-4e25-b00c-4f951effb22c"
```

<span data-ttu-id="1103a-115">Returnerar tjänstens status.</span><span class="sxs-lookup"><span data-stu-id="1103a-115">Returns a service's health.</span></span>

## <span data-ttu-id="1103a-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1103a-116">PARAMETERS</span></span>

### <span data-ttu-id="1103a-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="1103a-117">-Name</span></span>
<span data-ttu-id="1103a-118">Tjänstens hälso namn.</span><span class="sxs-lookup"><span data-stu-id="1103a-118">Service Health name.</span></span>

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

### <span data-ttu-id="1103a-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="1103a-119">-Location</span></span>
<span data-ttu-id="1103a-120">Regionens namn</span><span class="sxs-lookup"><span data-stu-id="1103a-120">Name of the region</span></span>

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

### <span data-ttu-id="1103a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1103a-121">-ResourceGroupName</span></span>
<span data-ttu-id="1103a-122">Namnet på resurs gruppen, valfritt.</span><span class="sxs-lookup"><span data-stu-id="1103a-122">Name of the resource group, optional.</span></span>

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

### <span data-ttu-id="1103a-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1103a-123">-ResourceId</span></span>
<span data-ttu-id="1103a-124">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="1103a-124">The resource id.</span></span>

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

### <span data-ttu-id="1103a-125">-Filter</span><span class="sxs-lookup"><span data-stu-id="1103a-125">-Filter</span></span>
<span data-ttu-id="1103a-126">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="1103a-126">OData filter parameter.</span></span>

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

### <span data-ttu-id="1103a-127">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="1103a-127">-Skip</span></span>
<span data-ttu-id="1103a-128">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="1103a-128">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="1103a-129">-Överst</span><span class="sxs-lookup"><span data-stu-id="1103a-129">-Top</span></span>
<span data-ttu-id="1103a-130">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="1103a-130">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="1103a-131">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="1103a-131">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="1103a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1103a-132">CommonParameters</span></span>
<span data-ttu-id="1103a-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1103a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1103a-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1103a-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1103a-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1103a-135">INPUTS</span></span>

## <span data-ttu-id="1103a-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1103a-136">OUTPUTS</span></span>

### <span data-ttu-id="1103a-137">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. ServiceHealth</span><span class="sxs-lookup"><span data-stu-id="1103a-137">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.ServiceHealth</span></span>

## <span data-ttu-id="1103a-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1103a-138">NOTES</span></span>

## <span data-ttu-id="1103a-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1103a-139">RELATED LINKS</span></span>
