---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67835cc0ae5191f50aefb79f76148752c68508bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920843"
---
# <span data-ttu-id="64222-101">Get-AzsVolume</span><span class="sxs-lookup"><span data-stu-id="64222-101">Get-AzsVolume</span></span>

## <span data-ttu-id="64222-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="64222-102">SYNOPSIS</span></span>
<span data-ttu-id="64222-103">Returnerar en lista över alla lagrings volymer på en plats.</span><span class="sxs-lookup"><span data-stu-id="64222-103">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="64222-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="64222-104">SYNTAX</span></span>

### <span data-ttu-id="64222-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="64222-105">List (Default)</span></span>
```
Get-AzsVolume -StorageSubSystem <String> -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="64222-106">Lära</span><span class="sxs-lookup"><span data-stu-id="64222-106">Get</span></span>
```
Get-AzsVolume -Name <String> -StorageSubSystem <String> -ScaleUnit <String> [-Location <String>]
 [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="64222-107">ID</span><span class="sxs-lookup"><span data-stu-id="64222-107">ResourceId</span></span>
```
Get-AzsVolume -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="64222-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="64222-108">DESCRIPTION</span></span>
<span data-ttu-id="64222-109">Returnerar en lista över alla lagrings volymer på en plats.</span><span class="sxs-lookup"><span data-stu-id="64222-109">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="64222-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="64222-110">EXAMPLES</span></span>

### <span data-ttu-id="64222-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="64222-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsVolume -ScaleUnit S-Cluster -StorageSubSystem S-Cluster.azurestack.local
```

<span data-ttu-id="64222-112">Få en lista över alla lagrings volymer på en viss plats.</span><span class="sxs-lookup"><span data-stu-id="64222-112">Get a list of all storage volumes at a given location.</span></span>

### <span data-ttu-id="64222-113">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="64222-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsVolume -ScaleUnit S-Cluster -StorageSubSystem S-Cluster.azurestack.local -Name a42d219b
```

<span data-ttu-id="64222-114">Skaffa en lagrings volym med namn på en viss plats.</span><span class="sxs-lookup"><span data-stu-id="64222-114">Get a storage volume by name at a given location.</span></span>

## <span data-ttu-id="64222-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="64222-115">PARAMETERS</span></span>

### <span data-ttu-id="64222-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="64222-116">-Filter</span></span>
<span data-ttu-id="64222-117">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="64222-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="64222-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="64222-118">-Location</span></span>
<span data-ttu-id="64222-119">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="64222-119">Location of the resource.</span></span>

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

### <span data-ttu-id="64222-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="64222-120">-Name</span></span>
<span data-ttu-id="64222-121">Namn på lagrings volymen.</span><span class="sxs-lookup"><span data-stu-id="64222-121">Name of the storage volume.</span></span>

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

### <span data-ttu-id="64222-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64222-122">-ResourceGroupName</span></span>
<span data-ttu-id="64222-123">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="64222-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="64222-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="64222-124">-ResourceId</span></span>
<span data-ttu-id="64222-125">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="64222-125">The resource id.</span></span>

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

### <span data-ttu-id="64222-126">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="64222-126">-ScaleUnit</span></span>
<span data-ttu-id="64222-127">Namn på enheten.</span><span class="sxs-lookup"><span data-stu-id="64222-127">Name of the scale unit.</span></span>

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

### <span data-ttu-id="64222-128">-StorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="64222-128">-StorageSubSystem</span></span>
<span data-ttu-id="64222-129">Underlag rings system där volymen finns.</span><span class="sxs-lookup"><span data-stu-id="64222-129">Storage subsystem in which the volume is located.</span></span>

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

### <span data-ttu-id="64222-130">-Överst</span><span class="sxs-lookup"><span data-stu-id="64222-130">-Top</span></span>
<span data-ttu-id="64222-131">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="64222-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="64222-132">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="64222-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="64222-133">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="64222-133">-Skip</span></span>
<span data-ttu-id="64222-134">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="64222-134">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="64222-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64222-135">CommonParameters</span></span>
<span data-ttu-id="64222-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64222-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64222-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64222-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64222-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="64222-138">INPUTS</span></span>

## <span data-ttu-id="64222-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="64222-139">OUTPUTS</span></span>

### <span data-ttu-id="64222-140">Microsoft. AzureStack. Management. Fabric. admin. Models. Volume</span><span class="sxs-lookup"><span data-stu-id="64222-140">Microsoft.AzureStack.Management.Fabric.Admin.Models.Volume</span></span>
## <span data-ttu-id="64222-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="64222-141">NOTES</span></span>

## <span data-ttu-id="64222-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="64222-142">RELATED LINKS</span></span>
