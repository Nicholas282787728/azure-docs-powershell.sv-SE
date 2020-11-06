---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2528d9b4f9443d8857006b6fc1e94100b0b477ec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572048"
---
# <span data-ttu-id="12555-101">Get-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="12555-101">Get-AzsIpPool</span></span>

## <span data-ttu-id="12555-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="12555-102">SYNOPSIS</span></span>
<span data-ttu-id="12555-103">Returnerar en lista över alla IP-pooler på en viss plats.</span><span class="sxs-lookup"><span data-stu-id="12555-103">Returns a list of all IP pools at a certain location.</span></span>

## <span data-ttu-id="12555-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="12555-104">SYNTAX</span></span>

### <span data-ttu-id="12555-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="12555-105">List (Default)</span></span>
```
Get-AzsIpPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="12555-106">Lära</span><span class="sxs-lookup"><span data-stu-id="12555-106">Get</span></span>
```
Get-AzsIpPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="12555-107">ID</span><span class="sxs-lookup"><span data-stu-id="12555-107">ResourceId</span></span>
```
Get-AzsIpPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="12555-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="12555-108">DESCRIPTION</span></span>
<span data-ttu-id="12555-109">Returnerar en lista över alla IP-pooler på en viss plats.</span><span class="sxs-lookup"><span data-stu-id="12555-109">Returns a list of all IP pools at a certain location.</span></span>

## <span data-ttu-id="12555-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="12555-110">EXAMPLES</span></span>

### <span data-ttu-id="12555-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="12555-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsIpPool
```

<span data-ttu-id="12555-112">Skaffa en IP-pool för alla infrastrukturer.</span><span class="sxs-lookup"><span data-stu-id="12555-112">Get an all infrastructure ip pools.</span></span>

### <span data-ttu-id="12555-113">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="12555-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsIpPool -Name "08786a0f-ad8c-43aa-a154-06083abfc1ac"
```

<span data-ttu-id="12555-114">Skaffa en IP-adresspool för infrastruktur baserat på namn.</span><span class="sxs-lookup"><span data-stu-id="12555-114">Get an infrastructure ip pool based on name.</span></span>

## <span data-ttu-id="12555-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="12555-115">PARAMETERS</span></span>

### <span data-ttu-id="12555-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="12555-116">-Filter</span></span>
<span data-ttu-id="12555-117">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="12555-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="12555-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="12555-118">-Location</span></span>
<span data-ttu-id="12555-119">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="12555-119">Location of the resource.</span></span>

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

### <span data-ttu-id="12555-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="12555-120">-Name</span></span>
<span data-ttu-id="12555-121">IP-poolnamn.</span><span class="sxs-lookup"><span data-stu-id="12555-121">IP pool name.</span></span>

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

### <span data-ttu-id="12555-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12555-122">-ResourceGroupName</span></span>
<span data-ttu-id="12555-123">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="12555-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="12555-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12555-124">-ResourceId</span></span>
<span data-ttu-id="12555-125">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="12555-125">The resource id.</span></span>

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

### <span data-ttu-id="12555-126">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="12555-126">-Skip</span></span>
<span data-ttu-id="12555-127">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="12555-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="12555-128">-Överst</span><span class="sxs-lookup"><span data-stu-id="12555-128">-Top</span></span>
<span data-ttu-id="12555-129">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="12555-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="12555-130">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="12555-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="12555-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12555-131">CommonParameters</span></span>
<span data-ttu-id="12555-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12555-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12555-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12555-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12555-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="12555-134">INPUTS</span></span>

## <span data-ttu-id="12555-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="12555-135">OUTPUTS</span></span>

### <span data-ttu-id="12555-136">Microsoft. AzureStack. Management. Fabric. admin. Models. IpPool</span><span class="sxs-lookup"><span data-stu-id="12555-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.IpPool</span></span>

## <span data-ttu-id="12555-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="12555-137">NOTES</span></span>

## <span data-ttu-id="12555-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="12555-138">RELATED LINKS</span></span>

