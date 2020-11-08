---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 403f980af6b00272ca67b3ba180808ba8c82ebce
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921408"
---
# <span data-ttu-id="df0e8-101">Get-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="df0e8-101">Get-AzsPlatformImage</span></span>

## <span data-ttu-id="df0e8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="df0e8-102">SYNOPSIS</span></span>
<span data-ttu-id="df0e8-103">Returnerar virtuella dator bilder som laddats till plattforms bild lagringen.</span><span class="sxs-lookup"><span data-stu-id="df0e8-103">Returns virtual machine images loaded into the platform image repository.</span></span>

## <span data-ttu-id="df0e8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="df0e8-104">SYNTAX</span></span>

### <span data-ttu-id="df0e8-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="df0e8-105">List (Default)</span></span>
```
Get-AzsPlatformImage [-Publisher <String>] [-Offer <String>] [-Sku <String>] [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="df0e8-106">Lära</span><span class="sxs-lookup"><span data-stu-id="df0e8-106">Get</span></span>
```
Get-AzsPlatformImage -Publisher <String> -Offer <String> -Sku <String> -Version <String> [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="df0e8-107">ID</span><span class="sxs-lookup"><span data-stu-id="df0e8-107">ResourceId</span></span>
```
Get-AzsPlatformImage -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="df0e8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="df0e8-108">DESCRIPTION</span></span>
<span data-ttu-id="df0e8-109">Returnerar plattforms bilder.</span><span class="sxs-lookup"><span data-stu-id="df0e8-109">Returns platform images.</span></span>

## <span data-ttu-id="df0e8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="df0e8-110">EXAMPLES</span></span>

### <span data-ttu-id="df0e8-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="df0e8-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlatformImage
```

<span data-ttu-id="df0e8-112">Returnerar virtuella dator bilder som är inlästa i Platform image lagring på platsen lokal.</span><span class="sxs-lookup"><span data-stu-id="df0e8-112">Returns virtual machine images loaded into the platform image repository at the location local.</span></span>

### <span data-ttu-id="df0e8-113">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="df0e8-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsPlatformImage -Publisher Canonical -Offer UbuntuServer -Sku 16.04-LTS -Version 0.1.0
```

<span data-ttu-id="df0e8-114">Skaffa en särskild plattforms bild.</span><span class="sxs-lookup"><span data-stu-id="df0e8-114">Get a specific platform image.</span></span>

## <span data-ttu-id="df0e8-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="df0e8-115">PARAMETERS</span></span>

### <span data-ttu-id="df0e8-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="df0e8-116">-Location</span></span>
<span data-ttu-id="df0e8-117">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="df0e8-117">Location of the resource.</span></span>

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

### <span data-ttu-id="df0e8-118">-Ge</span><span class="sxs-lookup"><span data-stu-id="df0e8-118">-Offer</span></span>
<span data-ttu-id="df0e8-119">Namn på offerter.</span><span class="sxs-lookup"><span data-stu-id="df0e8-119">Name of the offer.</span></span>

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

### <span data-ttu-id="df0e8-120">-Publisher</span><span class="sxs-lookup"><span data-stu-id="df0e8-120">-Publisher</span></span>
<span data-ttu-id="df0e8-121">Namnet på utgivaren.</span><span class="sxs-lookup"><span data-stu-id="df0e8-121">Name of the publisher.</span></span>

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

### <span data-ttu-id="df0e8-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df0e8-122">-ResourceId</span></span>
<span data-ttu-id="df0e8-123">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="df0e8-123">The resource id.</span></span>

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

### <span data-ttu-id="df0e8-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="df0e8-124">-Sku</span></span>
<span data-ttu-id="df0e8-125">Namn på SKU.</span><span class="sxs-lookup"><span data-stu-id="df0e8-125">Name of the SKU.</span></span>

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

### <span data-ttu-id="df0e8-126">-Version</span><span class="sxs-lookup"><span data-stu-id="df0e8-126">-Version</span></span>
<span data-ttu-id="df0e8-127">Versionen av plattforms bilden.</span><span class="sxs-lookup"><span data-stu-id="df0e8-127">The version of the platform image.</span></span>

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

### <span data-ttu-id="df0e8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df0e8-128">CommonParameters</span></span>
<span data-ttu-id="df0e8-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df0e8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df0e8-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df0e8-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df0e8-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="df0e8-131">INPUTS</span></span>

## <span data-ttu-id="df0e8-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="df0e8-132">OUTPUTS</span></span>

### <span data-ttu-id="df0e8-133">PlatformImageObject</span><span class="sxs-lookup"><span data-stu-id="df0e8-133">PlatformImageObject</span></span>

## <span data-ttu-id="df0e8-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="df0e8-134">NOTES</span></span>

## <span data-ttu-id="df0e8-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="df0e8-135">RELATED LINKS</span></span>
