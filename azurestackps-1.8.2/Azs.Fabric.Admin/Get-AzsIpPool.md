---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d5999718cc3085eb69da482df27fa0cb4379ed40
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94099897"
---
# <span data-ttu-id="32370-101">Get-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="32370-101">Get-AzsIpPool</span></span>

## <span data-ttu-id="32370-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="32370-102">SYNOPSIS</span></span>
<span data-ttu-id="32370-103">Returnerar en lista över alla IP-pooler på en viss plats.</span><span class="sxs-lookup"><span data-stu-id="32370-103">Returns a list of all IP pools at a certain location.</span></span>

## <span data-ttu-id="32370-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="32370-104">SYNTAX</span></span>

### <span data-ttu-id="32370-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="32370-105">List (Default)</span></span>
```
Get-AzsIpPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="32370-106">Lära</span><span class="sxs-lookup"><span data-stu-id="32370-106">Get</span></span>
```
Get-AzsIpPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="32370-107">ID</span><span class="sxs-lookup"><span data-stu-id="32370-107">ResourceId</span></span>
```
Get-AzsIpPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="32370-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="32370-108">DESCRIPTION</span></span>
<span data-ttu-id="32370-109">Returnerar en lista över alla IP-pooler på en viss plats.</span><span class="sxs-lookup"><span data-stu-id="32370-109">Returns a list of all IP pools at a certain location.</span></span>

## <span data-ttu-id="32370-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="32370-110">EXAMPLES</span></span>

### <span data-ttu-id="32370-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="32370-111">EXAMPLE 1</span></span>
```
Get-AzsIpPool
```

<span data-ttu-id="32370-112">Skaffa en IP-pool för alla infrastrukturer.</span><span class="sxs-lookup"><span data-stu-id="32370-112">Get an all infrastructure ip pools.</span></span>

### <span data-ttu-id="32370-113">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="32370-113">EXAMPLE 2</span></span>
```
Get-AzsIpPool -Name "08786a0f-ad8c-43aa-a154-06083abfc1ac"
```

<span data-ttu-id="32370-114">Skaffa en IP-adresspool för infrastruktur baserat på namn.</span><span class="sxs-lookup"><span data-stu-id="32370-114">Get an infrastructure ip pool based on name.</span></span>

## <span data-ttu-id="32370-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="32370-115">PARAMETERS</span></span>

### <span data-ttu-id="32370-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="32370-116">-Name</span></span>
<span data-ttu-id="32370-117">IP-poolnamn.</span><span class="sxs-lookup"><span data-stu-id="32370-117">IP pool name.</span></span>

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

### <span data-ttu-id="32370-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="32370-118">-Location</span></span>
<span data-ttu-id="32370-119">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="32370-119">Location of the resource.</span></span>

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

### <span data-ttu-id="32370-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32370-120">-ResourceGroupName</span></span>
<span data-ttu-id="32370-121">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="32370-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="32370-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="32370-122">-ResourceId</span></span>
<span data-ttu-id="32370-123">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="32370-123">The resource id.</span></span>

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

### <span data-ttu-id="32370-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="32370-124">-Filter</span></span>
<span data-ttu-id="32370-125">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="32370-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="32370-126">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="32370-126">-Skip</span></span>
<span data-ttu-id="32370-127">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="32370-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="32370-128">-Överst</span><span class="sxs-lookup"><span data-stu-id="32370-128">-Top</span></span>
<span data-ttu-id="32370-129">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="32370-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="32370-130">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="32370-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="32370-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32370-131">CommonParameters</span></span>
<span data-ttu-id="32370-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32370-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32370-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32370-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32370-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="32370-134">INPUTS</span></span>

## <span data-ttu-id="32370-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="32370-135">OUTPUTS</span></span>

### <span data-ttu-id="32370-136">Microsoft. AzureStack. Management. Fabric. admin. Models. IpPool</span><span class="sxs-lookup"><span data-stu-id="32370-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.IpPool</span></span>

## <span data-ttu-id="32370-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="32370-137">NOTES</span></span>

## <span data-ttu-id="32370-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="32370-138">RELATED LINKS</span></span>
