---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcc4dbfdd4634c53835c588947a77c4c2e773af4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100245"
---
# <span data-ttu-id="4149e-101">Get-AzsStoragePool</span><span class="sxs-lookup"><span data-stu-id="4149e-101">Get-AzsStoragePool</span></span>

## <span data-ttu-id="4149e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4149e-102">SYNOPSIS</span></span>
<span data-ttu-id="4149e-103">Returnerar en lista över alla lagringspooler för en plats.</span><span class="sxs-lookup"><span data-stu-id="4149e-103">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="4149e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4149e-104">SYNTAX</span></span>

### <span data-ttu-id="4149e-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="4149e-105">List (Default)</span></span>
```
Get-AzsStoragePool -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="4149e-106">Lära</span><span class="sxs-lookup"><span data-stu-id="4149e-106">Get</span></span>
```
Get-AzsStoragePool -Name <String> -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="4149e-107">ID</span><span class="sxs-lookup"><span data-stu-id="4149e-107">ResourceId</span></span>
```
Get-AzsStoragePool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="4149e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4149e-108">DESCRIPTION</span></span>
<span data-ttu-id="4149e-109">Returnerar en lista över alla lagringspooler för en plats.</span><span class="sxs-lookup"><span data-stu-id="4149e-109">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="4149e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4149e-110">EXAMPLES</span></span>

### <span data-ttu-id="4149e-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="4149e-111">EXAMPLE 1</span></span>
```
Get-AzsStoragePool -StorageSystem S-Cluster.azurestack.local
```

<span data-ttu-id="4149e-112">Hämta alla lagringspooler på en viss plats.</span><span class="sxs-lookup"><span data-stu-id="4149e-112">Get all storage pools at a given location.</span></span>

### <span data-ttu-id="4149e-113">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="4149e-113">EXAMPLE 2</span></span>
```
Get-AzsStoragePool -StorageSystem S-Cluster.azurestack.local -Name "SU1_Pool"
```

<span data-ttu-id="4149e-114">Skaffa en lagringspooler på en viss plats med ett namn på en lagringspool.</span><span class="sxs-lookup"><span data-stu-id="4149e-114">Get a storage pools at a given location given a storage pool name.</span></span>

## <span data-ttu-id="4149e-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4149e-115">PARAMETERS</span></span>

### <span data-ttu-id="4149e-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="4149e-116">-Name</span></span>
<span data-ttu-id="4149e-117">Namn på lagringspool.</span><span class="sxs-lookup"><span data-stu-id="4149e-117">Storage pool name.</span></span>

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

### <span data-ttu-id="4149e-118">-StorageSystem</span><span class="sxs-lookup"><span data-stu-id="4149e-118">-StorageSystem</span></span>
<span data-ttu-id="4149e-119">Namn på lagrings del systemet.</span><span class="sxs-lookup"><span data-stu-id="4149e-119">Name of the Storage Sub System.</span></span>

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

### <span data-ttu-id="4149e-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="4149e-120">-Location</span></span>
<span data-ttu-id="4149e-121">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="4149e-121">Location of the resource.</span></span>

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

### <span data-ttu-id="4149e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4149e-122">-ResourceGroupName</span></span>
<span data-ttu-id="4149e-123">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="4149e-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="4149e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4149e-124">-ResourceId</span></span>
<span data-ttu-id="4149e-125">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="4149e-125">The resource id.</span></span>

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

### <span data-ttu-id="4149e-126">-Filter</span><span class="sxs-lookup"><span data-stu-id="4149e-126">-Filter</span></span>
<span data-ttu-id="4149e-127">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="4149e-127">OData filter parameter.</span></span>

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

### <span data-ttu-id="4149e-128">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="4149e-128">-Skip</span></span>
<span data-ttu-id="4149e-129">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="4149e-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="4149e-130">-Överst</span><span class="sxs-lookup"><span data-stu-id="4149e-130">-Top</span></span>
<span data-ttu-id="4149e-131">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="4149e-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="4149e-132">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="4149e-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="4149e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4149e-133">CommonParameters</span></span>
<span data-ttu-id="4149e-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4149e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4149e-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4149e-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4149e-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4149e-136">INPUTS</span></span>

## <span data-ttu-id="4149e-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4149e-137">OUTPUTS</span></span>

### <span data-ttu-id="4149e-138">Microsoft. AzureStack. Management. Fabric. admin. Models. StoragePool</span><span class="sxs-lookup"><span data-stu-id="4149e-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.StoragePool</span></span>

## <span data-ttu-id="4149e-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4149e-139">NOTES</span></span>

## <span data-ttu-id="4149e-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4149e-140">RELATED LINKS</span></span>