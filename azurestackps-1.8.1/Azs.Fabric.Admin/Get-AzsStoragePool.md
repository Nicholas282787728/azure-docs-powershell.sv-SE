---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcc4dbfdd4634c53835c588947a77c4c2e773af4
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921691"
---
# <span data-ttu-id="33a78-101">Get-AzsStoragePool</span><span class="sxs-lookup"><span data-stu-id="33a78-101">Get-AzsStoragePool</span></span>

## <span data-ttu-id="33a78-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="33a78-102">SYNOPSIS</span></span>
<span data-ttu-id="33a78-103">Returnerar en lista över alla lagringspooler för en plats.</span><span class="sxs-lookup"><span data-stu-id="33a78-103">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="33a78-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="33a78-104">SYNTAX</span></span>

### <span data-ttu-id="33a78-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="33a78-105">List (Default)</span></span>
```
Get-AzsStoragePool -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="33a78-106">Lära</span><span class="sxs-lookup"><span data-stu-id="33a78-106">Get</span></span>
```
Get-AzsStoragePool -Name <String> -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="33a78-107">ID</span><span class="sxs-lookup"><span data-stu-id="33a78-107">ResourceId</span></span>
```
Get-AzsStoragePool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="33a78-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="33a78-108">DESCRIPTION</span></span>
<span data-ttu-id="33a78-109">Returnerar en lista över alla lagringspooler för en plats.</span><span class="sxs-lookup"><span data-stu-id="33a78-109">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="33a78-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="33a78-110">EXAMPLES</span></span>

### <span data-ttu-id="33a78-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="33a78-111">EXAMPLE 1</span></span>
```
Get-AzsStoragePool -StorageSystem S-Cluster.azurestack.local
```

<span data-ttu-id="33a78-112">Hämta alla lagringspooler på en viss plats.</span><span class="sxs-lookup"><span data-stu-id="33a78-112">Get all storage pools at a given location.</span></span>

### <span data-ttu-id="33a78-113">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="33a78-113">EXAMPLE 2</span></span>
```
Get-AzsStoragePool -StorageSystem S-Cluster.azurestack.local -Name "SU1_Pool"
```

<span data-ttu-id="33a78-114">Skaffa en lagringspooler på en viss plats med ett namn på en lagringspool.</span><span class="sxs-lookup"><span data-stu-id="33a78-114">Get a storage pools at a given location given a storage pool name.</span></span>

## <span data-ttu-id="33a78-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="33a78-115">PARAMETERS</span></span>

### <span data-ttu-id="33a78-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="33a78-116">-Name</span></span>
<span data-ttu-id="33a78-117">Namn på lagringspool.</span><span class="sxs-lookup"><span data-stu-id="33a78-117">Storage pool name.</span></span>

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

### <span data-ttu-id="33a78-118">-StorageSystem</span><span class="sxs-lookup"><span data-stu-id="33a78-118">-StorageSystem</span></span>
<span data-ttu-id="33a78-119">Namn på lagrings del systemet.</span><span class="sxs-lookup"><span data-stu-id="33a78-119">Name of the Storage Sub System.</span></span>

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

### <span data-ttu-id="33a78-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="33a78-120">-Location</span></span>
<span data-ttu-id="33a78-121">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="33a78-121">Location of the resource.</span></span>

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

### <span data-ttu-id="33a78-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33a78-122">-ResourceGroupName</span></span>
<span data-ttu-id="33a78-123">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="33a78-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="33a78-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33a78-124">-ResourceId</span></span>
<span data-ttu-id="33a78-125">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="33a78-125">The resource id.</span></span>

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

### <span data-ttu-id="33a78-126">-Filter</span><span class="sxs-lookup"><span data-stu-id="33a78-126">-Filter</span></span>
<span data-ttu-id="33a78-127">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="33a78-127">OData filter parameter.</span></span>

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

### <span data-ttu-id="33a78-128">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="33a78-128">-Skip</span></span>
<span data-ttu-id="33a78-129">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="33a78-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="33a78-130">-Överst</span><span class="sxs-lookup"><span data-stu-id="33a78-130">-Top</span></span>
<span data-ttu-id="33a78-131">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="33a78-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="33a78-132">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="33a78-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="33a78-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33a78-133">CommonParameters</span></span>
<span data-ttu-id="33a78-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33a78-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33a78-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33a78-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33a78-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="33a78-136">INPUTS</span></span>

## <span data-ttu-id="33a78-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="33a78-137">OUTPUTS</span></span>

### <span data-ttu-id="33a78-138">Microsoft. AzureStack. Management. Fabric. admin. Models. StoragePool</span><span class="sxs-lookup"><span data-stu-id="33a78-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.StoragePool</span></span>

## <span data-ttu-id="33a78-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="33a78-139">NOTES</span></span>

## <span data-ttu-id="33a78-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="33a78-140">RELATED LINKS</span></span>
