---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3760ecd9c0bc9fd62e49ee8163dfe24ae190985e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921348"
---
# <span data-ttu-id="1d09d-101">Get-AzsStorageSystem</span><span class="sxs-lookup"><span data-stu-id="1d09d-101">Get-AzsStorageSystem</span></span>

## <span data-ttu-id="1d09d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1d09d-102">SYNOPSIS</span></span>
<span data-ttu-id="1d09d-103">Returnerar en lista över alla lagrings under system för en plats.</span><span class="sxs-lookup"><span data-stu-id="1d09d-103">Returns a list of all storage subsystems for a location.</span></span>

## <span data-ttu-id="1d09d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1d09d-104">SYNTAX</span></span>

### <span data-ttu-id="1d09d-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="1d09d-105">List (Default)</span></span>
```
Get-AzsStorageSystem [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="1d09d-106">Lära</span><span class="sxs-lookup"><span data-stu-id="1d09d-106">Get</span></span>
```
Get-AzsStorageSystem [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="1d09d-107">ID</span><span class="sxs-lookup"><span data-stu-id="1d09d-107">ResourceId</span></span>
```
Get-AzsStorageSystem -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="1d09d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1d09d-108">DESCRIPTION</span></span>
<span data-ttu-id="1d09d-109">Returnerar en lista över alla lagrings under system för en plats.</span><span class="sxs-lookup"><span data-stu-id="1d09d-109">Returns a list of all storage subsystems for a location.</span></span>

## <span data-ttu-id="1d09d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1d09d-110">EXAMPLES</span></span>

### <span data-ttu-id="1d09d-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="1d09d-111">EXAMPLE 1</span></span>
```
Get-AzsStorageSystem
```

<span data-ttu-id="1d09d-112">Hämta alla lagrings under system från en plats.</span><span class="sxs-lookup"><span data-stu-id="1d09d-112">Get all storage subsystems from a location.</span></span>

### <span data-ttu-id="1d09d-113">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="1d09d-113">EXAMPLE 2</span></span>
```
Get-AzsStorageSystem -Name S-Cluster.azurestack.local
```

<span data-ttu-id="1d09d-114">Hämta ett underlag rings system med en plats och ett namn.</span><span class="sxs-lookup"><span data-stu-id="1d09d-114">Get a storage subsystem given a location and name.</span></span>

## <span data-ttu-id="1d09d-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1d09d-115">PARAMETERS</span></span>

### <span data-ttu-id="1d09d-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="1d09d-116">-Name</span></span>
<span data-ttu-id="1d09d-117">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="1d09d-117">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="1d09d-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="1d09d-118">-Location</span></span>
<span data-ttu-id="1d09d-119">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="1d09d-119">Location of the resource.</span></span>

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

### <span data-ttu-id="1d09d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d09d-120">-ResourceGroupName</span></span>
<span data-ttu-id="1d09d-121">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="1d09d-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="1d09d-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d09d-122">-ResourceId</span></span>
<span data-ttu-id="1d09d-123">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="1d09d-123">The resource id.</span></span>

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

### <span data-ttu-id="1d09d-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="1d09d-124">-Filter</span></span>
<span data-ttu-id="1d09d-125">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="1d09d-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="1d09d-126">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="1d09d-126">-Skip</span></span>
<span data-ttu-id="1d09d-127">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="1d09d-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="1d09d-128">-Överst</span><span class="sxs-lookup"><span data-stu-id="1d09d-128">-Top</span></span>
<span data-ttu-id="1d09d-129">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="1d09d-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="1d09d-130">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="1d09d-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="1d09d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d09d-131">CommonParameters</span></span>
<span data-ttu-id="1d09d-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d09d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d09d-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d09d-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d09d-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1d09d-134">INPUTS</span></span>

## <span data-ttu-id="1d09d-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1d09d-135">OUTPUTS</span></span>

### <span data-ttu-id="1d09d-136">Microsoft. AzureStack. Management. Fabric. admin. Models. StorageSystem</span><span class="sxs-lookup"><span data-stu-id="1d09d-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.StorageSystem</span></span>

## <span data-ttu-id="1d09d-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1d09d-137">NOTES</span></span>

## <span data-ttu-id="1d09d-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1d09d-138">RELATED LINKS</span></span>