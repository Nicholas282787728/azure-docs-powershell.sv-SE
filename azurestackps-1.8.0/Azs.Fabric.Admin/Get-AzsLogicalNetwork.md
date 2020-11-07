---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88d9fc8456c86f0806313bb0234e145b7f4d727a
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921364"
---
# <span data-ttu-id="bacdc-101">Get-AzsLogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="bacdc-101">Get-AzsLogicalNetwork</span></span>

## <span data-ttu-id="bacdc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bacdc-102">SYNOPSIS</span></span>
<span data-ttu-id="bacdc-103">Returnerar en lista över alla logiska nätverk på en plats.</span><span class="sxs-lookup"><span data-stu-id="bacdc-103">Returns a list of all logical networks at a location.</span></span>

## <span data-ttu-id="bacdc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bacdc-104">SYNTAX</span></span>

### <span data-ttu-id="bacdc-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="bacdc-105">List (Default)</span></span>
```
Get-AzsLogicalNetwork [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="bacdc-106">Lära</span><span class="sxs-lookup"><span data-stu-id="bacdc-106">Get</span></span>
```
Get-AzsLogicalNetwork [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="bacdc-107">ID</span><span class="sxs-lookup"><span data-stu-id="bacdc-107">ResourceId</span></span>
```
Get-AzsLogicalNetwork -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="bacdc-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bacdc-108">DESCRIPTION</span></span>
<span data-ttu-id="bacdc-109">Returnerar en lista över alla logiska nätverk på en plats.</span><span class="sxs-lookup"><span data-stu-id="bacdc-109">Returns a list of all logical networks at a location.</span></span>

## <span data-ttu-id="bacdc-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bacdc-110">EXAMPLES</span></span>

### <span data-ttu-id="bacdc-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="bacdc-111">EXAMPLE 1</span></span>
```
Get-AzsLogicalNetwork
```

<span data-ttu-id="bacdc-112">Skaffa alla logiska nätverk på en plats.</span><span class="sxs-lookup"><span data-stu-id="bacdc-112">Get all logical networks at a location.</span></span>

### <span data-ttu-id="bacdc-113">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="bacdc-113">EXAMPLE 2</span></span>
```
Get-AzsLogicalNetwork -Name "bb6c6f28-bad9-441b-8e62-57d2be255904"
```

<span data-ttu-id="bacdc-114">Skaffa ett specifikt logiskt nätverk på en plats baserat på ett namn.</span><span class="sxs-lookup"><span data-stu-id="bacdc-114">Get a specific logical networks at a location based on a name.</span></span>

## <span data-ttu-id="bacdc-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bacdc-115">PARAMETERS</span></span>

### <span data-ttu-id="bacdc-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="bacdc-116">-Name</span></span>
<span data-ttu-id="bacdc-117">Namn på det logiska nätverket.</span><span class="sxs-lookup"><span data-stu-id="bacdc-117">Name of the logical network.</span></span>

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

### <span data-ttu-id="bacdc-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="bacdc-118">-Location</span></span>
<span data-ttu-id="bacdc-119">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="bacdc-119">Location of the resource.</span></span>

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

### <span data-ttu-id="bacdc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bacdc-120">-ResourceGroupName</span></span>
<span data-ttu-id="bacdc-121">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="bacdc-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="bacdc-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bacdc-122">-ResourceId</span></span>
<span data-ttu-id="bacdc-123">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="bacdc-123">The resource id.</span></span>

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

### <span data-ttu-id="bacdc-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="bacdc-124">-Filter</span></span>
<span data-ttu-id="bacdc-125">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="bacdc-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="bacdc-126">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="bacdc-126">-Skip</span></span>
<span data-ttu-id="bacdc-127">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="bacdc-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="bacdc-128">-Överst</span><span class="sxs-lookup"><span data-stu-id="bacdc-128">-Top</span></span>
<span data-ttu-id="bacdc-129">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="bacdc-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="bacdc-130">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="bacdc-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="bacdc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bacdc-131">CommonParameters</span></span>
<span data-ttu-id="bacdc-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bacdc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bacdc-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bacdc-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bacdc-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bacdc-134">INPUTS</span></span>

## <span data-ttu-id="bacdc-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bacdc-135">OUTPUTS</span></span>

### <span data-ttu-id="bacdc-136">Microsoft. AzureStack. Management. Fabric. admin. Models. LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="bacdc-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.LogicalNetwork</span></span>

## <span data-ttu-id="bacdc-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bacdc-137">NOTES</span></span>

## <span data-ttu-id="bacdc-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bacdc-138">RELATED LINKS</span></span>
