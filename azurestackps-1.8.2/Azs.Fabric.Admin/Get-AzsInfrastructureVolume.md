---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: deaefa8e98e27572fb3faa9443c296e5a15accb0
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100360"
---
# <span data-ttu-id="b47b8-101">Get-AzsInfrastructureVolume</span><span class="sxs-lookup"><span data-stu-id="b47b8-101">Get-AzsInfrastructureVolume</span></span>

## <span data-ttu-id="b47b8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b47b8-102">SYNOPSIS</span></span>
<span data-ttu-id="b47b8-103">Returnerar en lista över alla lagrings volymer på en plats.</span><span class="sxs-lookup"><span data-stu-id="b47b8-103">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="b47b8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b47b8-104">SYNTAX</span></span>

### <span data-ttu-id="b47b8-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="b47b8-105">List (Default)</span></span>
```
Get-AzsInfrastructureVolume -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="b47b8-106">Lära</span><span class="sxs-lookup"><span data-stu-id="b47b8-106">Get</span></span>
```
Get-AzsInfrastructureVolume -Name <String> -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="b47b8-107">ID</span><span class="sxs-lookup"><span data-stu-id="b47b8-107">ResourceId</span></span>
```
Get-AzsInfrastructureVolume -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="b47b8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b47b8-108">DESCRIPTION</span></span>
<span data-ttu-id="b47b8-109">Returnerar en lista över alla lagrings volymer på en plats.</span><span class="sxs-lookup"><span data-stu-id="b47b8-109">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="b47b8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b47b8-110">EXAMPLES</span></span>

### <span data-ttu-id="b47b8-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="b47b8-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local
```

<span data-ttu-id="b47b8-112">Få en lista över alla lagrings volymer på en viss plats.</span><span class="sxs-lookup"><span data-stu-id="b47b8-112">Get a list of all storage volumes at a given location.</span></span>

### <span data-ttu-id="b47b8-113">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="b47b8-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local -Name a42d219b
```

<span data-ttu-id="b47b8-114">Skaffa en lagrings volym med namn på en viss plats.</span><span class="sxs-lookup"><span data-stu-id="b47b8-114">Get a storage volume by name at a given location.</span></span>

## <span data-ttu-id="b47b8-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b47b8-115">PARAMETERS</span></span>

### <span data-ttu-id="b47b8-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="b47b8-116">-Name</span></span>
<span data-ttu-id="b47b8-117">Namn på lagrings volymen.</span><span class="sxs-lookup"><span data-stu-id="b47b8-117">Name of the storage volume.</span></span>

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

### <span data-ttu-id="b47b8-118">-StoragePool</span><span class="sxs-lookup"><span data-stu-id="b47b8-118">-StoragePool</span></span>
<span data-ttu-id="b47b8-119">Namn på lagringspool.</span><span class="sxs-lookup"><span data-stu-id="b47b8-119">Storage pool name.</span></span>

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

### <span data-ttu-id="b47b8-120">-StorageSystem</span><span class="sxs-lookup"><span data-stu-id="b47b8-120">-StorageSystem</span></span>
<span data-ttu-id="b47b8-121">Representation av en lagrings system resurs.</span><span class="sxs-lookup"><span data-stu-id="b47b8-121">Representation of a storage system resource.</span></span>

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

### <span data-ttu-id="b47b8-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="b47b8-122">-Location</span></span>
<span data-ttu-id="b47b8-123">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="b47b8-123">Location of the resource.</span></span>

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

### <span data-ttu-id="b47b8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b47b8-124">-ResourceGroupName</span></span>
<span data-ttu-id="b47b8-125">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="b47b8-125">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="b47b8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b47b8-126">-ResourceId</span></span>
<span data-ttu-id="b47b8-127">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="b47b8-127">The resource id.</span></span>

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

### <span data-ttu-id="b47b8-128">-Filter</span><span class="sxs-lookup"><span data-stu-id="b47b8-128">-Filter</span></span>
<span data-ttu-id="b47b8-129">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="b47b8-129">OData filter parameter.</span></span>

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

### <span data-ttu-id="b47b8-130">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="b47b8-130">-Skip</span></span>
<span data-ttu-id="b47b8-131">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="b47b8-131">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="b47b8-132">-Överst</span><span class="sxs-lookup"><span data-stu-id="b47b8-132">-Top</span></span>
<span data-ttu-id="b47b8-133">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="b47b8-133">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b47b8-134">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="b47b8-134">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="b47b8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b47b8-135">CommonParameters</span></span>
<span data-ttu-id="b47b8-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b47b8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b47b8-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b47b8-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b47b8-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b47b8-138">INPUTS</span></span>

## <span data-ttu-id="b47b8-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b47b8-139">OUTPUTS</span></span>

### <span data-ttu-id="b47b8-140">Microsoft. AzureStack. Management. Fabric. admin. Models. Volume</span><span class="sxs-lookup"><span data-stu-id="b47b8-140">Microsoft.AzureStack.Management.Fabric.Admin.Models.Volume</span></span>

## <span data-ttu-id="b47b8-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b47b8-141">NOTES</span></span>

## <span data-ttu-id="b47b8-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b47b8-142">RELATED LINKS</span></span>
