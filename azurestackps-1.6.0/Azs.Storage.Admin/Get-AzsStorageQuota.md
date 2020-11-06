---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e4277ee88af840674d6fc8e4e2d5f614e745ace
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572424"
---
# <span data-ttu-id="d9fd7-101">Get-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="d9fd7-101">Get-AzsStorageQuota</span></span>

## <span data-ttu-id="d9fd7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d9fd7-102">SYNOPSIS</span></span>
<span data-ttu-id="d9fd7-103">Returnerar en lista med lagrings kvoter på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="d9fd7-103">Returns a list of storage quotas at the given location.</span></span>

## <span data-ttu-id="d9fd7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d9fd7-104">SYNTAX</span></span>

### <span data-ttu-id="d9fd7-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="d9fd7-105">List (Default)</span></span>
```
Get-AzsStorageQuota [-Location <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="d9fd7-106">Lära</span><span class="sxs-lookup"><span data-stu-id="d9fd7-106">Get</span></span>
```
Get-AzsStorageQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="d9fd7-107">ID</span><span class="sxs-lookup"><span data-stu-id="d9fd7-107">ResourceId</span></span>
```
Get-AzsStorageQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="d9fd7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d9fd7-108">DESCRIPTION</span></span>
<span data-ttu-id="d9fd7-109">Returnerar en lista med lagrings kvoter på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="d9fd7-109">Returns a list of storage quotas at the given location.</span></span>

## <span data-ttu-id="d9fd7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d9fd7-110">EXAMPLES</span></span>

### <span data-ttu-id="d9fd7-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d9fd7-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageQuota
```

<span data-ttu-id="d9fd7-112">Hämta listan med lagrings kvoter.</span><span class="sxs-lookup"><span data-stu-id="d9fd7-112">Get the list of storage quotas.</span></span>

### <span data-ttu-id="d9fd7-113">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="d9fd7-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageQuota -Name "storagequota1"
```

<span data-ttu-id="d9fd7-114">Få information om den angivna lagrings kvoten efter namn.</span><span class="sxs-lookup"><span data-stu-id="d9fd7-114">Get details of the specified storage quota by name.</span></span>

## <span data-ttu-id="d9fd7-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d9fd7-115">PARAMETERS</span></span>

### <span data-ttu-id="d9fd7-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="d9fd7-116">-Location</span></span>
<span data-ttu-id="d9fd7-117">Resurs plats.</span><span class="sxs-lookup"><span data-stu-id="d9fd7-117">Resource location.</span></span>

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

### <span data-ttu-id="d9fd7-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="d9fd7-118">-Name</span></span>
<span data-ttu-id="d9fd7-119">Namnet på lagrings kvoten.</span><span class="sxs-lookup"><span data-stu-id="d9fd7-119">The name of the storage quota.</span></span>

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

### <span data-ttu-id="d9fd7-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9fd7-120">-ResourceId</span></span>
<span data-ttu-id="d9fd7-121">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="d9fd7-121">The resource id.</span></span>

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

### <span data-ttu-id="d9fd7-122">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="d9fd7-122">-Skip</span></span>
<span data-ttu-id="d9fd7-123">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="d9fd7-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="d9fd7-124">-Överst</span><span class="sxs-lookup"><span data-stu-id="d9fd7-124">-Top</span></span>
<span data-ttu-id="d9fd7-125">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="d9fd7-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="d9fd7-126">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="d9fd7-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="d9fd7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9fd7-127">CommonParameters</span></span>
<span data-ttu-id="d9fd7-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9fd7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9fd7-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9fd7-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9fd7-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d9fd7-130">INPUTS</span></span>

## <span data-ttu-id="d9fd7-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d9fd7-131">OUTPUTS</span></span>

### <span data-ttu-id="d9fd7-132">Microsoft. AzureStack. Management. Storage. admin. Models. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="d9fd7-132">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="d9fd7-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d9fd7-133">NOTES</span></span>

## <span data-ttu-id="d9fd7-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d9fd7-134">RELATED LINKS</span></span>

