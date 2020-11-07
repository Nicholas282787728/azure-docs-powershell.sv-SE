---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2abc9073b9e7bcbcd4644150ada4c19cd351f660
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920844"
---
# <span data-ttu-id="7fcda-101">Get-AzsStorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="7fcda-101">Get-AzsStorageSubSystem</span></span>

## <span data-ttu-id="7fcda-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7fcda-102">SYNOPSIS</span></span>
<span data-ttu-id="7fcda-103">Returnerar en lista över alla lagrings under system för en skalen het.</span><span class="sxs-lookup"><span data-stu-id="7fcda-103">Returns a list of all storage subsystems for a scale unit.</span></span>

## <span data-ttu-id="7fcda-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7fcda-104">SYNTAX</span></span>

### <span data-ttu-id="7fcda-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="7fcda-105">List (Default)</span></span>
```
Get-AzsStorageSubSystem -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="7fcda-106">Lära</span><span class="sxs-lookup"><span data-stu-id="7fcda-106">Get</span></span>
```
Get-AzsStorageSubSystem [-Name] <String> -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="7fcda-107">ID</span><span class="sxs-lookup"><span data-stu-id="7fcda-107">ResourceId</span></span>
```
Get-AzsStorageSubSystem -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="7fcda-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7fcda-108">DESCRIPTION</span></span>
<span data-ttu-id="7fcda-109">Returnerar en lista över alla lagrings under system för en skalen het.</span><span class="sxs-lookup"><span data-stu-id="7fcda-109">Returns a list of all storage subsystems for a scale unit.</span></span>

## <span data-ttu-id="7fcda-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7fcda-110">EXAMPLES</span></span>

### <span data-ttu-id="7fcda-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7fcda-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageSubSystem -ScaleUnit S-Cluster
```

<span data-ttu-id="7fcda-112">Hämta alla lagrings under system från en enhet.</span><span class="sxs-lookup"><span data-stu-id="7fcda-112">Get all storage subsystems from a scale unit.</span></span>

### <span data-ttu-id="7fcda-113">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="7fcda-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageSubSystem -ScaleUnit S-Cluster -Name S-Cluster.azurestack.local
```

<span data-ttu-id="7fcda-114">Skaffa ett underlag rings system med en enhet och ett namn.</span><span class="sxs-lookup"><span data-stu-id="7fcda-114">Get a storage subsystem given a scale unit and name.</span></span>

## <span data-ttu-id="7fcda-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7fcda-115">PARAMETERS</span></span>

### <span data-ttu-id="7fcda-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="7fcda-116">-Filter</span></span>
<span data-ttu-id="7fcda-117">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="7fcda-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="7fcda-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="7fcda-118">-Location</span></span>
<span data-ttu-id="7fcda-119">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="7fcda-119">Location of the resource.</span></span>

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

### <span data-ttu-id="7fcda-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="7fcda-120">-Name</span></span>
<span data-ttu-id="7fcda-121">Namn på lagrings del systemet.</span><span class="sxs-lookup"><span data-stu-id="7fcda-121">Name of the storage subsystem.</span></span>

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

### <span data-ttu-id="7fcda-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fcda-122">-ResourceGroupName</span></span>
<span data-ttu-id="7fcda-123">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="7fcda-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="7fcda-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7fcda-124">-ResourceId</span></span>
<span data-ttu-id="7fcda-125">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="7fcda-125">The resource id.</span></span>

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

### <span data-ttu-id="7fcda-126">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="7fcda-126">-ScaleUnit</span></span>
<span data-ttu-id="7fcda-127">Namn på enheten.</span><span class="sxs-lookup"><span data-stu-id="7fcda-127">Name of the scale unit.</span></span>

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

### <span data-ttu-id="7fcda-128">-Överst</span><span class="sxs-lookup"><span data-stu-id="7fcda-128">-Top</span></span>
<span data-ttu-id="7fcda-129">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="7fcda-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="7fcda-130">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="7fcda-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="7fcda-131">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="7fcda-131">-Skip</span></span>
<span data-ttu-id="7fcda-132">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="7fcda-132">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="7fcda-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fcda-133">CommonParameters</span></span>
<span data-ttu-id="7fcda-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fcda-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fcda-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fcda-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fcda-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7fcda-136">INPUTS</span></span>

## <span data-ttu-id="7fcda-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7fcda-137">OUTPUTS</span></span>

### <span data-ttu-id="7fcda-138">Microsoft. AzureStack. Management. Fabric. admin. Models. StorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="7fcda-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.StorageSubSystem</span></span>
## <span data-ttu-id="7fcda-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7fcda-139">NOTES</span></span>

## <span data-ttu-id="7fcda-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7fcda-140">RELATED LINKS</span></span>
