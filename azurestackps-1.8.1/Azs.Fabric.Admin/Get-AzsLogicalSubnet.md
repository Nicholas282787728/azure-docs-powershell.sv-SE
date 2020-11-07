---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb535146787c4c33a57ad406f05544f18ba74eb0
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921703"
---
# <span data-ttu-id="5caa1-101">Get-AzsLogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="5caa1-101">Get-AzsLogicalSubnet</span></span>

## <span data-ttu-id="5caa1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5caa1-102">SYNOPSIS</span></span>
<span data-ttu-id="5caa1-103">Returnerar en lista över alla logiska undernät.</span><span class="sxs-lookup"><span data-stu-id="5caa1-103">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="5caa1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5caa1-104">SYNTAX</span></span>

### <span data-ttu-id="5caa1-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="5caa1-105">List (Default)</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="5caa1-106">Lära</span><span class="sxs-lookup"><span data-stu-id="5caa1-106">Get</span></span>
```
Get-AzsLogicalSubnet -Name <String> -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="5caa1-107">ID</span><span class="sxs-lookup"><span data-stu-id="5caa1-107">ResourceId</span></span>
```
Get-AzsLogicalSubnet -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="5caa1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5caa1-108">DESCRIPTION</span></span>
<span data-ttu-id="5caa1-109">Returnerar en lista över alla logiska undernät.</span><span class="sxs-lookup"><span data-stu-id="5caa1-109">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="5caa1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5caa1-110">EXAMPLES</span></span>

### <span data-ttu-id="5caa1-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="5caa1-111">EXAMPLE 1</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001"
```

<span data-ttu-id="5caa1-112">Få en lista över alla logiska undernät för ett givet logiskt nätverk och en given plats.</span><span class="sxs-lookup"><span data-stu-id="5caa1-112">Get a list of all logical subnets for a given logical network and location.</span></span>

### <span data-ttu-id="5caa1-113">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="5caa1-113">EXAMPLE 2</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001" -Name "d8cfef2d-c0c8-4cdb-b0a8-fb1bdf3f2ad7"
```

<span data-ttu-id="5caa1-114">Skaffa ett specifikt logiskt undernät för ett angivet logiskt nätverk och plats baserat på namn.</span><span class="sxs-lookup"><span data-stu-id="5caa1-114">Get a specific logical subnet for a given logical network and location based on name.</span></span>

## <span data-ttu-id="5caa1-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5caa1-115">PARAMETERS</span></span>

### <span data-ttu-id="5caa1-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="5caa1-116">-Name</span></span>
<span data-ttu-id="5caa1-117">Namnet på det logiska under nätet.</span><span class="sxs-lookup"><span data-stu-id="5caa1-117">Name of the logical subnet.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5caa1-118">-LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="5caa1-118">-LogicalNetwork</span></span>
<span data-ttu-id="5caa1-119">Namn på det logiska nätverket.</span><span class="sxs-lookup"><span data-stu-id="5caa1-119">Name of the logical network.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5caa1-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="5caa1-120">-Location</span></span>
<span data-ttu-id="5caa1-121">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="5caa1-121">Location of the resource.</span></span>

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

### <span data-ttu-id="5caa1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5caa1-122">-ResourceGroupName</span></span>
<span data-ttu-id="5caa1-123">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="5caa1-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="5caa1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5caa1-124">-ResourceId</span></span>
<span data-ttu-id="5caa1-125">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="5caa1-125">The resource id.</span></span>

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

### <span data-ttu-id="5caa1-126">-Filter</span><span class="sxs-lookup"><span data-stu-id="5caa1-126">-Filter</span></span>
<span data-ttu-id="5caa1-127">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="5caa1-127">OData filter parameter.</span></span>

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

### <span data-ttu-id="5caa1-128">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="5caa1-128">-Skip</span></span>
<span data-ttu-id="5caa1-129">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="5caa1-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="5caa1-130">-Överst</span><span class="sxs-lookup"><span data-stu-id="5caa1-130">-Top</span></span>
<span data-ttu-id="5caa1-131">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="5caa1-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="5caa1-132">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="5caa1-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="5caa1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5caa1-133">CommonParameters</span></span>
<span data-ttu-id="5caa1-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5caa1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5caa1-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5caa1-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5caa1-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5caa1-136">INPUTS</span></span>

## <span data-ttu-id="5caa1-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5caa1-137">OUTPUTS</span></span>

### <span data-ttu-id="5caa1-138">Microsoft. AzureStack. Management. Fabric. admin. Models. LogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="5caa1-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.LogicalSubnet</span></span>

## <span data-ttu-id="5caa1-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5caa1-139">NOTES</span></span>

## <span data-ttu-id="5caa1-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5caa1-140">RELATED LINKS</span></span>
