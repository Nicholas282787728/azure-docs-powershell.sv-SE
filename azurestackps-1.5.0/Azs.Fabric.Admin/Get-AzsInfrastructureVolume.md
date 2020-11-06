---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ffdb6542f9e7bfd594130374d5d72fed8b26596e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572051"
---
# <span data-ttu-id="91e99-101">Get-AzsInfrastructureVolume</span><span class="sxs-lookup"><span data-stu-id="91e99-101">Get-AzsInfrastructureVolume</span></span>

## <span data-ttu-id="91e99-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="91e99-102">SYNOPSIS</span></span>
<span data-ttu-id="91e99-103">Returnerar en lista över alla lagrings volymer på en plats.</span><span class="sxs-lookup"><span data-stu-id="91e99-103">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="91e99-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="91e99-104">SYNTAX</span></span>

### <span data-ttu-id="91e99-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="91e99-105">List (Default)</span></span>
```
Get-AzsInfrastructureVolume -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="91e99-106">Lära</span><span class="sxs-lookup"><span data-stu-id="91e99-106">Get</span></span>
```
Get-AzsInfrastructureVolume -Name <String> -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="91e99-107">ID</span><span class="sxs-lookup"><span data-stu-id="91e99-107">ResourceId</span></span>
```
Get-AzsInfrastructureVolume -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="91e99-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="91e99-108">DESCRIPTION</span></span>
<span data-ttu-id="91e99-109">Returnerar en lista över alla lagrings volymer på en plats.</span><span class="sxs-lookup"><span data-stu-id="91e99-109">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="91e99-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="91e99-110">EXAMPLES</span></span>

### <span data-ttu-id="91e99-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="91e99-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local
```

<span data-ttu-id="91e99-112">Få en lista över alla lagrings volymer på en viss plats.</span><span class="sxs-lookup"><span data-stu-id="91e99-112">Get a list of all storage volumes at a given location.</span></span>

### <span data-ttu-id="91e99-113">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="91e99-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local -Name a42d219b
```

<span data-ttu-id="91e99-114">Skaffa en lagrings volym med namn på en viss plats.</span><span class="sxs-lookup"><span data-stu-id="91e99-114">Get a storage volume by name at a given location.</span></span>

## <span data-ttu-id="91e99-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="91e99-115">PARAMETERS</span></span>

### <span data-ttu-id="91e99-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="91e99-116">-Filter</span></span>
<span data-ttu-id="91e99-117">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="91e99-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="91e99-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="91e99-118">-Location</span></span>
<span data-ttu-id="91e99-119">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="91e99-119">Location of the resource.</span></span>

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

### <span data-ttu-id="91e99-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="91e99-120">-Name</span></span>
<span data-ttu-id="91e99-121">Namn på lagrings volymen.</span><span class="sxs-lookup"><span data-stu-id="91e99-121">Name of the storage volume.</span></span>

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

### <span data-ttu-id="91e99-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91e99-122">-ResourceGroupName</span></span>
<span data-ttu-id="91e99-123">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="91e99-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="91e99-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91e99-124">-ResourceId</span></span>
<span data-ttu-id="91e99-125">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="91e99-125">The resource id.</span></span>

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

### <span data-ttu-id="91e99-126">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="91e99-126">-Skip</span></span>
<span data-ttu-id="91e99-127">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="91e99-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="91e99-128">-StoragePool</span><span class="sxs-lookup"><span data-stu-id="91e99-128">-StoragePool</span></span>
<span data-ttu-id="91e99-129">Namn på lagringspool.</span><span class="sxs-lookup"><span data-stu-id="91e99-129">Storage pool name.</span></span>

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

### <span data-ttu-id="91e99-130">-StorageSystem</span><span class="sxs-lookup"><span data-stu-id="91e99-130">-StorageSystem</span></span>
<span data-ttu-id="91e99-131">Lagrings system där infrastruktur volymen finns.</span><span class="sxs-lookup"><span data-stu-id="91e99-131">Storage system in which the infrastructure volume is located.</span></span>

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

### <span data-ttu-id="91e99-132">-Överst</span><span class="sxs-lookup"><span data-stu-id="91e99-132">-Top</span></span>
<span data-ttu-id="91e99-133">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="91e99-133">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="91e99-134">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="91e99-134">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="91e99-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91e99-135">CommonParameters</span></span>
<span data-ttu-id="91e99-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91e99-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91e99-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91e99-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91e99-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="91e99-138">INPUTS</span></span>

## <span data-ttu-id="91e99-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="91e99-139">OUTPUTS</span></span>

### <span data-ttu-id="91e99-140">Microsoft. AzureStack. Management. Fabric. admin. Models. Volume</span><span class="sxs-lookup"><span data-stu-id="91e99-140">Microsoft.AzureStack.Management.Fabric.Admin.Models.Volume</span></span>

## <span data-ttu-id="91e99-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="91e99-141">NOTES</span></span>

## <span data-ttu-id="91e99-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="91e99-142">RELATED LINKS</span></span>

