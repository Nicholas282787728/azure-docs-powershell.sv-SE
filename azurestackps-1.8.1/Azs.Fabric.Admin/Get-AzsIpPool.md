---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d5999718cc3085eb69da482df27fa0cb4379ed40
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921706"
---
# <span data-ttu-id="324d0-101">Get-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="324d0-101">Get-AzsIpPool</span></span>

## <span data-ttu-id="324d0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="324d0-102">SYNOPSIS</span></span>
<span data-ttu-id="324d0-103">Returnerar en lista över alla IP-pooler på en viss plats.</span><span class="sxs-lookup"><span data-stu-id="324d0-103">Returns a list of all IP pools at a certain location.</span></span>

## <span data-ttu-id="324d0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="324d0-104">SYNTAX</span></span>

### <span data-ttu-id="324d0-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="324d0-105">List (Default)</span></span>
```
Get-AzsIpPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="324d0-106">Lära</span><span class="sxs-lookup"><span data-stu-id="324d0-106">Get</span></span>
```
Get-AzsIpPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="324d0-107">ID</span><span class="sxs-lookup"><span data-stu-id="324d0-107">ResourceId</span></span>
```
Get-AzsIpPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="324d0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="324d0-108">DESCRIPTION</span></span>
<span data-ttu-id="324d0-109">Returnerar en lista över alla IP-pooler på en viss plats.</span><span class="sxs-lookup"><span data-stu-id="324d0-109">Returns a list of all IP pools at a certain location.</span></span>

## <span data-ttu-id="324d0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="324d0-110">EXAMPLES</span></span>

### <span data-ttu-id="324d0-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="324d0-111">EXAMPLE 1</span></span>
```
Get-AzsIpPool
```

<span data-ttu-id="324d0-112">Skaffa en IP-pool för alla infrastrukturer.</span><span class="sxs-lookup"><span data-stu-id="324d0-112">Get an all infrastructure ip pools.</span></span>

### <span data-ttu-id="324d0-113">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="324d0-113">EXAMPLE 2</span></span>
```
Get-AzsIpPool -Name "08786a0f-ad8c-43aa-a154-06083abfc1ac"
```

<span data-ttu-id="324d0-114">Skaffa en IP-adresspool för infrastruktur baserat på namn.</span><span class="sxs-lookup"><span data-stu-id="324d0-114">Get an infrastructure ip pool based on name.</span></span>

## <span data-ttu-id="324d0-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="324d0-115">PARAMETERS</span></span>

### <span data-ttu-id="324d0-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="324d0-116">-Name</span></span>
<span data-ttu-id="324d0-117">IP-poolnamn.</span><span class="sxs-lookup"><span data-stu-id="324d0-117">IP pool name.</span></span>

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

### <span data-ttu-id="324d0-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="324d0-118">-Location</span></span>
<span data-ttu-id="324d0-119">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="324d0-119">Location of the resource.</span></span>

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

### <span data-ttu-id="324d0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="324d0-120">-ResourceGroupName</span></span>
<span data-ttu-id="324d0-121">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="324d0-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="324d0-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="324d0-122">-ResourceId</span></span>
<span data-ttu-id="324d0-123">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="324d0-123">The resource id.</span></span>

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

### <span data-ttu-id="324d0-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="324d0-124">-Filter</span></span>
<span data-ttu-id="324d0-125">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="324d0-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="324d0-126">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="324d0-126">-Skip</span></span>
<span data-ttu-id="324d0-127">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="324d0-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="324d0-128">-Överst</span><span class="sxs-lookup"><span data-stu-id="324d0-128">-Top</span></span>
<span data-ttu-id="324d0-129">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="324d0-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="324d0-130">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="324d0-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="324d0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="324d0-131">CommonParameters</span></span>
<span data-ttu-id="324d0-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="324d0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="324d0-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="324d0-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="324d0-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="324d0-134">INPUTS</span></span>

## <span data-ttu-id="324d0-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="324d0-135">OUTPUTS</span></span>

### <span data-ttu-id="324d0-136">Microsoft. AzureStack. Management. Fabric. admin. Models. IpPool</span><span class="sxs-lookup"><span data-stu-id="324d0-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.IpPool</span></span>

## <span data-ttu-id="324d0-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="324d0-137">NOTES</span></span>

## <span data-ttu-id="324d0-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="324d0-138">RELATED LINKS</span></span>
