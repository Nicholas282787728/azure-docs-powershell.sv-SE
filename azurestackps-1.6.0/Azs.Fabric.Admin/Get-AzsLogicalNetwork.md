---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fdf0c09e087779e9a08161f2af6f9070f193c31b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571488"
---
# <span data-ttu-id="f1b5b-101">Get-AzsLogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="f1b5b-101">Get-AzsLogicalNetwork</span></span>

## <span data-ttu-id="f1b5b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f1b5b-102">SYNOPSIS</span></span>
<span data-ttu-id="f1b5b-103">Returnerar en lista över alla logiska nätverk på en plats.</span><span class="sxs-lookup"><span data-stu-id="f1b5b-103">Returns a list of all logical networks at a location.</span></span>

## <span data-ttu-id="f1b5b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f1b5b-104">SYNTAX</span></span>

### <span data-ttu-id="f1b5b-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="f1b5b-105">List (Default)</span></span>
```
Get-AzsLogicalNetwork [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="f1b5b-106">Lära</span><span class="sxs-lookup"><span data-stu-id="f1b5b-106">Get</span></span>
```
Get-AzsLogicalNetwork [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="f1b5b-107">ID</span><span class="sxs-lookup"><span data-stu-id="f1b5b-107">ResourceId</span></span>
```
Get-AzsLogicalNetwork -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="f1b5b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f1b5b-108">DESCRIPTION</span></span>
<span data-ttu-id="f1b5b-109">Returnerar en lista över alla logiska nätverk på en plats.</span><span class="sxs-lookup"><span data-stu-id="f1b5b-109">Returns a list of all logical networks at a location.</span></span>

## <span data-ttu-id="f1b5b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f1b5b-110">EXAMPLES</span></span>

### <span data-ttu-id="f1b5b-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f1b5b-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsLogicalNetwork
```

<span data-ttu-id="f1b5b-112">Skaffa alla logiska nätverk på en plats.</span><span class="sxs-lookup"><span data-stu-id="f1b5b-112">Get all logical networks at a location.</span></span>

### <span data-ttu-id="f1b5b-113">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="f1b5b-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsLogicalNetwork -Name "bb6c6f28-bad9-441b-8e62-57d2be255904"
```

<span data-ttu-id="f1b5b-114">Skaffa ett specifikt logiskt nätverk på en plats baserat på ett namn.</span><span class="sxs-lookup"><span data-stu-id="f1b5b-114">Get a specific logical networks at a location based on a name.</span></span>

## <span data-ttu-id="f1b5b-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f1b5b-115">PARAMETERS</span></span>

### <span data-ttu-id="f1b5b-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="f1b5b-116">-Filter</span></span>
<span data-ttu-id="f1b5b-117">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="f1b5b-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="f1b5b-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="f1b5b-118">-Location</span></span>
<span data-ttu-id="f1b5b-119">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="f1b5b-119">Location of the resource.</span></span>

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

### <span data-ttu-id="f1b5b-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="f1b5b-120">-Name</span></span>
<span data-ttu-id="f1b5b-121">Namn på det logiska nätverket.</span><span class="sxs-lookup"><span data-stu-id="f1b5b-121">Name of the logical network.</span></span>

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

### <span data-ttu-id="f1b5b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1b5b-122">-ResourceGroupName</span></span>
<span data-ttu-id="f1b5b-123">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="f1b5b-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="f1b5b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1b5b-124">-ResourceId</span></span>
<span data-ttu-id="f1b5b-125">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="f1b5b-125">The resource id.</span></span>

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

### <span data-ttu-id="f1b5b-126">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="f1b5b-126">-Skip</span></span>
<span data-ttu-id="f1b5b-127">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="f1b5b-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="f1b5b-128">-Överst</span><span class="sxs-lookup"><span data-stu-id="f1b5b-128">-Top</span></span>
<span data-ttu-id="f1b5b-129">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="f1b5b-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="f1b5b-130">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="f1b5b-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="f1b5b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1b5b-131">CommonParameters</span></span>
<span data-ttu-id="f1b5b-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1b5b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1b5b-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1b5b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1b5b-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f1b5b-134">INPUTS</span></span>

## <span data-ttu-id="f1b5b-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f1b5b-135">OUTPUTS</span></span>

### <span data-ttu-id="f1b5b-136">Microsoft. AzureStack. Management. Fabric. admin. Models. LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="f1b5b-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.LogicalNetwork</span></span>

## <span data-ttu-id="f1b5b-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f1b5b-137">NOTES</span></span>

## <span data-ttu-id="f1b5b-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f1b5b-138">RELATED LINKS</span></span>

