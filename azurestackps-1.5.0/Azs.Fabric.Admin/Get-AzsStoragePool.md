---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25243539ef01a7476b6b0befb2d5cb29595001ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571775"
---
# <span data-ttu-id="9d288-101">Get-AzsStoragePool</span><span class="sxs-lookup"><span data-stu-id="9d288-101">Get-AzsStoragePool</span></span>

## <span data-ttu-id="9d288-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9d288-102">SYNOPSIS</span></span>
<span data-ttu-id="9d288-103">Returnerar en lista över alla lagringspooler för en plats.</span><span class="sxs-lookup"><span data-stu-id="9d288-103">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="9d288-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9d288-104">SYNTAX</span></span>

### <span data-ttu-id="9d288-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="9d288-105">List (Default)</span></span>
```
Get-AzsStoragePool -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="9d288-106">Lära</span><span class="sxs-lookup"><span data-stu-id="9d288-106">Get</span></span>
```
Get-AzsStoragePool -Name <String> -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="9d288-107">ID</span><span class="sxs-lookup"><span data-stu-id="9d288-107">ResourceId</span></span>
```
Get-AzsStoragePool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="9d288-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9d288-108">DESCRIPTION</span></span>
<span data-ttu-id="9d288-109">Returnerar en lista över alla lagringspooler för en plats.</span><span class="sxs-lookup"><span data-stu-id="9d288-109">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="9d288-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9d288-110">EXAMPLES</span></span>

### <span data-ttu-id="9d288-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9d288-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStoragePool -StorageSubSystem S-Cluster.azurestack.local
```

<span data-ttu-id="9d288-112">Hämta alla lagringspooler på en viss plats.</span><span class="sxs-lookup"><span data-stu-id="9d288-112">Get all storage pools at a given location.</span></span>

### <span data-ttu-id="9d288-113">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="9d288-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStoragePool -StorageSubSystem S-Cluster.azurestack.local -Name "SU1_Pool"
```

<span data-ttu-id="9d288-114">Skaffa en lagringspooler på en viss plats med ett namn på en lagringspool.</span><span class="sxs-lookup"><span data-stu-id="9d288-114">Get a storage pools at a given location given a storage pool name.</span></span>

## <span data-ttu-id="9d288-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9d288-115">PARAMETERS</span></span>

### <span data-ttu-id="9d288-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="9d288-116">-Filter</span></span>
<span data-ttu-id="9d288-117">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="9d288-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="9d288-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="9d288-118">-Location</span></span>
<span data-ttu-id="9d288-119">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="9d288-119">Location of the resource.</span></span>

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

### <span data-ttu-id="9d288-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="9d288-120">-Name</span></span>
<span data-ttu-id="9d288-121">Namn på lagringspool.</span><span class="sxs-lookup"><span data-stu-id="9d288-121">Storage pool name.</span></span>

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

### <span data-ttu-id="9d288-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d288-122">-ResourceGroupName</span></span>
<span data-ttu-id="9d288-123">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="9d288-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="9d288-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d288-124">-ResourceId</span></span>
<span data-ttu-id="9d288-125">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="9d288-125">The resource id.</span></span>

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

### <span data-ttu-id="9d288-126">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="9d288-126">-Skip</span></span>
<span data-ttu-id="9d288-127">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="9d288-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="9d288-128">-StorageSystem</span><span class="sxs-lookup"><span data-stu-id="9d288-128">-StorageSystem</span></span>
<span data-ttu-id="9d288-129">Lagrings system där lagringspoolen lagras.</span><span class="sxs-lookup"><span data-stu-id="9d288-129">Storage system in which the storage pool is located.</span></span>

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

### <span data-ttu-id="9d288-130">-Överst</span><span class="sxs-lookup"><span data-stu-id="9d288-130">-Top</span></span>
<span data-ttu-id="9d288-131">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="9d288-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="9d288-132">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="9d288-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="9d288-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d288-133">CommonParameters</span></span>
<span data-ttu-id="9d288-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d288-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d288-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d288-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d288-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9d288-136">INPUTS</span></span>

## <span data-ttu-id="9d288-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9d288-137">OUTPUTS</span></span>

### <span data-ttu-id="9d288-138">Microsoft. AzureStack. Management. Fabric. admin. Models. StoragePool</span><span class="sxs-lookup"><span data-stu-id="9d288-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.StoragePool</span></span>

## <span data-ttu-id="9d288-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9d288-139">NOTES</span></span>

## <span data-ttu-id="9d288-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9d288-140">RELATED LINKS</span></span>

