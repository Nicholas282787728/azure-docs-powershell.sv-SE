---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cab0b994648a414aa164b746a02e3fe1fb848e9c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921052"
---
# <span data-ttu-id="c78ed-101">Get-AzsDrive</span><span class="sxs-lookup"><span data-stu-id="c78ed-101">Get-AzsDrive</span></span>

## <span data-ttu-id="c78ed-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c78ed-102">SYNOPSIS</span></span>
<span data-ttu-id="c78ed-103">Returnerar en lista över alla lagrings enheter för ett visst kluster.</span><span class="sxs-lookup"><span data-stu-id="c78ed-103">Returns a list of all storage drives for a given cluster.</span></span>

## <span data-ttu-id="c78ed-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c78ed-104">SYNTAX</span></span>

### <span data-ttu-id="c78ed-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="c78ed-105">List (Default)</span></span>
```
Get-AzsDrive -StorageSubSystem <String> -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="c78ed-106">Lära</span><span class="sxs-lookup"><span data-stu-id="c78ed-106">Get</span></span>
```
Get-AzsDrive -Name <String> -StorageSubSystem <String> -ScaleUnit <String> [-Location <String>]
 [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="c78ed-107">ID</span><span class="sxs-lookup"><span data-stu-id="c78ed-107">ResourceId</span></span>
```
Get-AzsDrive -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="c78ed-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c78ed-108">DESCRIPTION</span></span>
<span data-ttu-id="c78ed-109">Returnerar en lista över alla lagrings enheter för ett visst kluster.</span><span class="sxs-lookup"><span data-stu-id="c78ed-109">Returns a list of all storage drives for a given cluster.</span></span>

## <span data-ttu-id="c78ed-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c78ed-110">EXAMPLES</span></span>

### <span data-ttu-id="c78ed-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c78ed-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDrive -ScaleUnit S-Cluster -StorageSubSystem S-Cluster.azurestack.local
```

<span data-ttu-id="c78ed-112">Få en lista över alla lagrings enheter för ett visst kluster.</span><span class="sxs-lookup"><span data-stu-id="c78ed-112">Get a list of all storage drives for a given cluster.</span></span>

### <span data-ttu-id="c78ed-113">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="c78ed-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsDrive -ScaleUnit S-Cluster -StorageSubSystem S-Cluster.azurestack.local -Name a654528c-60bb-18e1-457c-51b7cdb7e14a
```

<span data-ttu-id="c78ed-114">Skaffa en lagrings enhet per namn för ett visst kluster.</span><span class="sxs-lookup"><span data-stu-id="c78ed-114">Get a storage drive by name for a given cluster.</span></span>

## <span data-ttu-id="c78ed-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c78ed-115">PARAMETERS</span></span>

### <span data-ttu-id="c78ed-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="c78ed-116">-Filter</span></span>
<span data-ttu-id="c78ed-117">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="c78ed-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="c78ed-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="c78ed-118">-Location</span></span>
<span data-ttu-id="c78ed-119">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="c78ed-119">Location of the resource.</span></span>

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

### <span data-ttu-id="c78ed-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="c78ed-120">-Name</span></span>
<span data-ttu-id="c78ed-121">Namn på lagrings enheten.</span><span class="sxs-lookup"><span data-stu-id="c78ed-121">Name of the storage drive.</span></span>

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

### <span data-ttu-id="c78ed-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c78ed-122">-ResourceGroupName</span></span>
<span data-ttu-id="c78ed-123">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="c78ed-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="c78ed-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c78ed-124">-ResourceId</span></span>
<span data-ttu-id="c78ed-125">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="c78ed-125">The resource id.</span></span>

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

### <span data-ttu-id="c78ed-126">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="c78ed-126">-ScaleUnit</span></span>
<span data-ttu-id="c78ed-127">Namn på enheten.</span><span class="sxs-lookup"><span data-stu-id="c78ed-127">Name of the scale unit.</span></span>

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

### <span data-ttu-id="c78ed-128">-StorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="c78ed-128">-StorageSubSystem</span></span>
<span data-ttu-id="c78ed-129">Underlag rings system där enheten finns.</span><span class="sxs-lookup"><span data-stu-id="c78ed-129">Storage subsystem in which the drive is located.</span></span>

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

### <span data-ttu-id="c78ed-130">-Överst</span><span class="sxs-lookup"><span data-stu-id="c78ed-130">-Top</span></span>
<span data-ttu-id="c78ed-131">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="c78ed-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="c78ed-132">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="c78ed-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="c78ed-133">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="c78ed-133">-Skip</span></span>
<span data-ttu-id="c78ed-134">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="c78ed-134">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="c78ed-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c78ed-135">CommonParameters</span></span>
<span data-ttu-id="c78ed-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c78ed-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c78ed-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c78ed-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c78ed-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c78ed-138">INPUTS</span></span>

## <span data-ttu-id="c78ed-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c78ed-139">OUTPUTS</span></span>

### <span data-ttu-id="c78ed-140">Microsoft. AzureStack. Management. Fabric. admin. Models. Drive</span><span class="sxs-lookup"><span data-stu-id="c78ed-140">Microsoft.AzureStack.Management.Fabric.Admin.Models.Drive</span></span>
## <span data-ttu-id="c78ed-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c78ed-141">NOTES</span></span>

## <span data-ttu-id="c78ed-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c78ed-142">RELATED LINKS</span></span>