---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 687838573459c09ceaf08c0d1c3335caa4a99769
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100396"
---
# <span data-ttu-id="126a1-101">Get-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="126a1-101">Get-AzsStorageQuota</span></span>

## <span data-ttu-id="126a1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="126a1-102">SYNOPSIS</span></span>
<span data-ttu-id="126a1-103">Returnerar en lista med lagrings kvoter på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="126a1-103">Returns a list of storage quotas at the given location.</span></span>

## <span data-ttu-id="126a1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="126a1-104">SYNTAX</span></span>

### <span data-ttu-id="126a1-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="126a1-105">List (Default)</span></span>
```
Get-AzsStorageQuota [-Location <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="126a1-106">Lära</span><span class="sxs-lookup"><span data-stu-id="126a1-106">Get</span></span>
```
Get-AzsStorageQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="126a1-107">ID</span><span class="sxs-lookup"><span data-stu-id="126a1-107">ResourceId</span></span>
```
Get-AzsStorageQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="126a1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="126a1-108">DESCRIPTION</span></span>
<span data-ttu-id="126a1-109">Returnerar en lista med lagrings kvoter på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="126a1-109">Returns a list of storage quotas at the given location.</span></span>

## <span data-ttu-id="126a1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="126a1-110">EXAMPLES</span></span>

### <span data-ttu-id="126a1-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="126a1-111">EXAMPLE 1</span></span>
```
Get-AzsStorageQuota
```

<span data-ttu-id="126a1-112">Hämta listan med lagrings kvoter.</span><span class="sxs-lookup"><span data-stu-id="126a1-112">Get the list of storage quotas.</span></span>

### <span data-ttu-id="126a1-113">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="126a1-113">EXAMPLE 2</span></span>
```
Get-AzsStorageQuota -Name "storagequota1"
```

<span data-ttu-id="126a1-114">Få information om den angivna lagrings kvoten efter namn.</span><span class="sxs-lookup"><span data-stu-id="126a1-114">Get details of the specified storage quota by name.</span></span>

## <span data-ttu-id="126a1-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="126a1-115">PARAMETERS</span></span>

### <span data-ttu-id="126a1-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="126a1-116">-Name</span></span>
<span data-ttu-id="126a1-117">Namnet på lagrings kvoten.</span><span class="sxs-lookup"><span data-stu-id="126a1-117">The name of the storage quota.</span></span>

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

### <span data-ttu-id="126a1-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="126a1-118">-Location</span></span>
<span data-ttu-id="126a1-119">Resurs plats.</span><span class="sxs-lookup"><span data-stu-id="126a1-119">Resource location.</span></span>

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

### <span data-ttu-id="126a1-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="126a1-120">-ResourceId</span></span>
<span data-ttu-id="126a1-121">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="126a1-121">The resource id.</span></span>

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

### <span data-ttu-id="126a1-122">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="126a1-122">-Skip</span></span>
<span data-ttu-id="126a1-123">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="126a1-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="126a1-124">-Överst</span><span class="sxs-lookup"><span data-stu-id="126a1-124">-Top</span></span>
<span data-ttu-id="126a1-125">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="126a1-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="126a1-126">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="126a1-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="126a1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="126a1-127">CommonParameters</span></span>
<span data-ttu-id="126a1-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="126a1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="126a1-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="126a1-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="126a1-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="126a1-130">INPUTS</span></span>

## <span data-ttu-id="126a1-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="126a1-131">OUTPUTS</span></span>

### <span data-ttu-id="126a1-132">Microsoft. AzureStack. Management. Storage. admin. Models. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="126a1-132">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="126a1-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="126a1-133">NOTES</span></span>

## <span data-ttu-id="126a1-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="126a1-134">RELATED LINKS</span></span>
