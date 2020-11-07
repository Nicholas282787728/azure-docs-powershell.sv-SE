---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: deaefa8e98e27572fb3faa9443c296e5a15accb0
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921369"
---
# <span data-ttu-id="5df63-101">Get-AzsInfrastructureVolume</span><span class="sxs-lookup"><span data-stu-id="5df63-101">Get-AzsInfrastructureVolume</span></span>

## <span data-ttu-id="5df63-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5df63-102">SYNOPSIS</span></span>
<span data-ttu-id="5df63-103">Returnerar en lista över alla lagrings volymer på en plats.</span><span class="sxs-lookup"><span data-stu-id="5df63-103">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="5df63-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5df63-104">SYNTAX</span></span>

### <span data-ttu-id="5df63-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="5df63-105">List (Default)</span></span>
```
Get-AzsInfrastructureVolume -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="5df63-106">Lära</span><span class="sxs-lookup"><span data-stu-id="5df63-106">Get</span></span>
```
Get-AzsInfrastructureVolume -Name <String> -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="5df63-107">ID</span><span class="sxs-lookup"><span data-stu-id="5df63-107">ResourceId</span></span>
```
Get-AzsInfrastructureVolume -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="5df63-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5df63-108">DESCRIPTION</span></span>
<span data-ttu-id="5df63-109">Returnerar en lista över alla lagrings volymer på en plats.</span><span class="sxs-lookup"><span data-stu-id="5df63-109">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="5df63-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5df63-110">EXAMPLES</span></span>

### <span data-ttu-id="5df63-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="5df63-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local
```

<span data-ttu-id="5df63-112">Få en lista över alla lagrings volymer på en viss plats.</span><span class="sxs-lookup"><span data-stu-id="5df63-112">Get a list of all storage volumes at a given location.</span></span>

### <span data-ttu-id="5df63-113">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="5df63-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local -Name a42d219b
```

<span data-ttu-id="5df63-114">Skaffa en lagrings volym med namn på en viss plats.</span><span class="sxs-lookup"><span data-stu-id="5df63-114">Get a storage volume by name at a given location.</span></span>

## <span data-ttu-id="5df63-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5df63-115">PARAMETERS</span></span>

### <span data-ttu-id="5df63-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="5df63-116">-Name</span></span>
<span data-ttu-id="5df63-117">Namn på lagrings volymen.</span><span class="sxs-lookup"><span data-stu-id="5df63-117">Name of the storage volume.</span></span>

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

### <span data-ttu-id="5df63-118">-StoragePool</span><span class="sxs-lookup"><span data-stu-id="5df63-118">-StoragePool</span></span>
<span data-ttu-id="5df63-119">Namn på lagringspool.</span><span class="sxs-lookup"><span data-stu-id="5df63-119">Storage pool name.</span></span>

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

### <span data-ttu-id="5df63-120">-StorageSystem</span><span class="sxs-lookup"><span data-stu-id="5df63-120">-StorageSystem</span></span>
<span data-ttu-id="5df63-121">Representation av en lagrings system resurs.</span><span class="sxs-lookup"><span data-stu-id="5df63-121">Representation of a storage system resource.</span></span>

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

### <span data-ttu-id="5df63-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="5df63-122">-Location</span></span>
<span data-ttu-id="5df63-123">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="5df63-123">Location of the resource.</span></span>

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

### <span data-ttu-id="5df63-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5df63-124">-ResourceGroupName</span></span>
<span data-ttu-id="5df63-125">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="5df63-125">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="5df63-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5df63-126">-ResourceId</span></span>
<span data-ttu-id="5df63-127">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="5df63-127">The resource id.</span></span>

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

### <span data-ttu-id="5df63-128">-Filter</span><span class="sxs-lookup"><span data-stu-id="5df63-128">-Filter</span></span>
<span data-ttu-id="5df63-129">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="5df63-129">OData filter parameter.</span></span>

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

### <span data-ttu-id="5df63-130">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="5df63-130">-Skip</span></span>
<span data-ttu-id="5df63-131">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="5df63-131">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="5df63-132">-Överst</span><span class="sxs-lookup"><span data-stu-id="5df63-132">-Top</span></span>
<span data-ttu-id="5df63-133">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="5df63-133">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="5df63-134">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="5df63-134">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="5df63-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5df63-135">CommonParameters</span></span>
<span data-ttu-id="5df63-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5df63-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5df63-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5df63-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5df63-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5df63-138">INPUTS</span></span>

## <span data-ttu-id="5df63-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5df63-139">OUTPUTS</span></span>

### <span data-ttu-id="5df63-140">Microsoft. AzureStack. Management. Fabric. admin. Models. Volume</span><span class="sxs-lookup"><span data-stu-id="5df63-140">Microsoft.AzureStack.Management.Fabric.Admin.Models.Volume</span></span>

## <span data-ttu-id="5df63-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5df63-141">NOTES</span></span>

## <span data-ttu-id="5df63-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5df63-142">RELATED LINKS</span></span>
