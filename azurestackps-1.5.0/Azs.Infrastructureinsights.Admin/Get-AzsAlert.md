---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8fbec7ec2f8bcfc0d7595658f84866cf449d3e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571711"
---
# <span data-ttu-id="23e66-101">Get-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="23e66-101">Get-AzsAlert</span></span>

## <span data-ttu-id="23e66-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="23e66-102">SYNOPSIS</span></span>
<span data-ttu-id="23e66-103">Returnerar listan över alla aviseringar på en given plats.</span><span class="sxs-lookup"><span data-stu-id="23e66-103">Returns the list of all alerts in a given location.</span></span>

## <span data-ttu-id="23e66-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="23e66-104">SYNTAX</span></span>

### <span data-ttu-id="23e66-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="23e66-105">List (Default)</span></span>
```
Get-AzsAlert [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>]
 [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="23e66-106">Lära</span><span class="sxs-lookup"><span data-stu-id="23e66-106">Get</span></span>
```
Get-AzsAlert [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="23e66-107">ID</span><span class="sxs-lookup"><span data-stu-id="23e66-107">ResourceId</span></span>
```
Get-AzsAlert -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="23e66-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="23e66-108">DESCRIPTION</span></span>
<span data-ttu-id="23e66-109">Returnerar listan över alla aviseringar på en given plats.</span><span class="sxs-lookup"><span data-stu-id="23e66-109">Returns the list of all alerts in a given location.</span></span>

## <span data-ttu-id="23e66-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="23e66-110">EXAMPLES</span></span>

### <span data-ttu-id="23e66-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="23e66-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsAlert -Name 7f58eb8b-e39f-45d0-8ae7-9920b8f22f5f
```

<span data-ttu-id="23e66-112">Få en avisering efter namn.</span><span class="sxs-lookup"><span data-stu-id="23e66-112">Get an alert by Name.</span></span>

### <span data-ttu-id="23e66-113">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="23e66-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAlert | Where State -EQ 'active' | select FaultTypeId, Title
```

<span data-ttu-id="23e66-114">Få alla aktiva aviseringar och visa deras fel och titel.</span><span class="sxs-lookup"><span data-stu-id="23e66-114">Get all active alerts and display their fault and title.</span></span>

## <span data-ttu-id="23e66-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="23e66-115">PARAMETERS</span></span>

### <span data-ttu-id="23e66-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="23e66-116">-Filter</span></span>
<span data-ttu-id="23e66-117">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="23e66-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="23e66-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="23e66-118">-Location</span></span>
<span data-ttu-id="23e66-119">Namn på platsen.</span><span class="sxs-lookup"><span data-stu-id="23e66-119">Name of the location.</span></span>

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

### <span data-ttu-id="23e66-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="23e66-120">-Name</span></span>
<span data-ttu-id="23e66-121">Aviserings-ID.</span><span class="sxs-lookup"><span data-stu-id="23e66-121">The alert identifier.</span></span>

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

### <span data-ttu-id="23e66-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23e66-122">-ResourceGroupName</span></span>
<span data-ttu-id="23e66-123">Resurs grupp namn som resursen finns.</span><span class="sxs-lookup"><span data-stu-id="23e66-123">Resource group name which the resource resides.</span></span>

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

### <span data-ttu-id="23e66-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23e66-124">-ResourceId</span></span>
<span data-ttu-id="23e66-125">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="23e66-125">The resource id.</span></span>

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

### <span data-ttu-id="23e66-126">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="23e66-126">-Skip</span></span>
<span data-ttu-id="23e66-127">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="23e66-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="23e66-128">-Överst</span><span class="sxs-lookup"><span data-stu-id="23e66-128">-Top</span></span>
<span data-ttu-id="23e66-129">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="23e66-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="23e66-130">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="23e66-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="23e66-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23e66-131">CommonParameters</span></span>
<span data-ttu-id="23e66-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23e66-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23e66-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23e66-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23e66-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="23e66-134">INPUTS</span></span>

## <span data-ttu-id="23e66-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="23e66-135">OUTPUTS</span></span>

### <span data-ttu-id="23e66-136">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. Alert</span><span class="sxs-lookup"><span data-stu-id="23e66-136">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.Alert</span></span>

## <span data-ttu-id="23e66-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="23e66-137">NOTES</span></span>

## <span data-ttu-id="23e66-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="23e66-138">RELATED LINKS</span></span>

