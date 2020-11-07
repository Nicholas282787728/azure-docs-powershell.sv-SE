---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d5999718cc3085eb69da482df27fa0cb4379ed40
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921366"
---
# <span data-ttu-id="72d82-101">Get-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="72d82-101">Get-AzsIpPool</span></span>

## <span data-ttu-id="72d82-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="72d82-102">SYNOPSIS</span></span>
<span data-ttu-id="72d82-103">Returnerar en lista över alla IP-pooler på en viss plats.</span><span class="sxs-lookup"><span data-stu-id="72d82-103">Returns a list of all IP pools at a certain location.</span></span>

## <span data-ttu-id="72d82-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="72d82-104">SYNTAX</span></span>

### <span data-ttu-id="72d82-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="72d82-105">List (Default)</span></span>
```
Get-AzsIpPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="72d82-106">Lära</span><span class="sxs-lookup"><span data-stu-id="72d82-106">Get</span></span>
```
Get-AzsIpPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="72d82-107">ID</span><span class="sxs-lookup"><span data-stu-id="72d82-107">ResourceId</span></span>
```
Get-AzsIpPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="72d82-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="72d82-108">DESCRIPTION</span></span>
<span data-ttu-id="72d82-109">Returnerar en lista över alla IP-pooler på en viss plats.</span><span class="sxs-lookup"><span data-stu-id="72d82-109">Returns a list of all IP pools at a certain location.</span></span>

## <span data-ttu-id="72d82-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="72d82-110">EXAMPLES</span></span>

### <span data-ttu-id="72d82-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="72d82-111">EXAMPLE 1</span></span>
```
Get-AzsIpPool
```

<span data-ttu-id="72d82-112">Skaffa en IP-pool för alla infrastrukturer.</span><span class="sxs-lookup"><span data-stu-id="72d82-112">Get an all infrastructure ip pools.</span></span>

### <span data-ttu-id="72d82-113">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="72d82-113">EXAMPLE 2</span></span>
```
Get-AzsIpPool -Name "08786a0f-ad8c-43aa-a154-06083abfc1ac"
```

<span data-ttu-id="72d82-114">Skaffa en IP-adresspool för infrastruktur baserat på namn.</span><span class="sxs-lookup"><span data-stu-id="72d82-114">Get an infrastructure ip pool based on name.</span></span>

## <span data-ttu-id="72d82-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="72d82-115">PARAMETERS</span></span>

### <span data-ttu-id="72d82-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="72d82-116">-Name</span></span>
<span data-ttu-id="72d82-117">IP-poolnamn.</span><span class="sxs-lookup"><span data-stu-id="72d82-117">IP pool name.</span></span>

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

### <span data-ttu-id="72d82-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="72d82-118">-Location</span></span>
<span data-ttu-id="72d82-119">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="72d82-119">Location of the resource.</span></span>

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

### <span data-ttu-id="72d82-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72d82-120">-ResourceGroupName</span></span>
<span data-ttu-id="72d82-121">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="72d82-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="72d82-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72d82-122">-ResourceId</span></span>
<span data-ttu-id="72d82-123">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="72d82-123">The resource id.</span></span>

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

### <span data-ttu-id="72d82-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="72d82-124">-Filter</span></span>
<span data-ttu-id="72d82-125">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="72d82-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="72d82-126">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="72d82-126">-Skip</span></span>
<span data-ttu-id="72d82-127">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="72d82-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="72d82-128">-Överst</span><span class="sxs-lookup"><span data-stu-id="72d82-128">-Top</span></span>
<span data-ttu-id="72d82-129">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="72d82-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="72d82-130">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="72d82-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="72d82-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72d82-131">CommonParameters</span></span>
<span data-ttu-id="72d82-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72d82-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72d82-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72d82-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72d82-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="72d82-134">INPUTS</span></span>

## <span data-ttu-id="72d82-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="72d82-135">OUTPUTS</span></span>

### <span data-ttu-id="72d82-136">Microsoft. AzureStack. Management. Fabric. admin. Models. IpPool</span><span class="sxs-lookup"><span data-stu-id="72d82-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.IpPool</span></span>

## <span data-ttu-id="72d82-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="72d82-137">NOTES</span></span>

## <span data-ttu-id="72d82-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="72d82-138">RELATED LINKS</span></span>
