---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e2580e2b6de179cdc3a9407b514848cc832e798e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571339"
---
# <span data-ttu-id="90c69-101">Get-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="90c69-101">Get-AzsPlatformImage</span></span>

## <span data-ttu-id="90c69-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="90c69-102">SYNOPSIS</span></span>
<span data-ttu-id="90c69-103">Returnerar virtuella dator bilder som laddats till plattforms bild lagringen.</span><span class="sxs-lookup"><span data-stu-id="90c69-103">Returns virtual machine images loaded into the platform image repository.</span></span>

## <span data-ttu-id="90c69-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="90c69-104">SYNTAX</span></span>

### <span data-ttu-id="90c69-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="90c69-105">List (Default)</span></span>
```
Get-AzsPlatformImage [-Publisher <String>] [-Offer <String>] [-Sku <String>] [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="90c69-106">Lära</span><span class="sxs-lookup"><span data-stu-id="90c69-106">Get</span></span>
```
Get-AzsPlatformImage -Publisher <String> -Offer <String> -Sku <String> -Version <String> [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="90c69-107">ID</span><span class="sxs-lookup"><span data-stu-id="90c69-107">ResourceId</span></span>
```
Get-AzsPlatformImage -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="90c69-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="90c69-108">DESCRIPTION</span></span>
<span data-ttu-id="90c69-109">Returnerar plattforms bilder.</span><span class="sxs-lookup"><span data-stu-id="90c69-109">Returns platform images.</span></span>

## <span data-ttu-id="90c69-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="90c69-110">EXAMPLES</span></span>

### <span data-ttu-id="90c69-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="90c69-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlatformImage
```

<span data-ttu-id="90c69-112">Returnerar virtuella dator bilder som är inlästa i Platform image lagring på platsen lokal.</span><span class="sxs-lookup"><span data-stu-id="90c69-112">Returns virtual machine images loaded into the platform image repository at the location local.</span></span>

### <span data-ttu-id="90c69-113">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="90c69-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsPlatformImage -Publisher Canonical -Offer UbuntuServer -Sku 16.04-LTS -Version 0.1.0
```

<span data-ttu-id="90c69-114">Skaffa en särskild plattforms bild.</span><span class="sxs-lookup"><span data-stu-id="90c69-114">Get a specific platform image.</span></span>

## <span data-ttu-id="90c69-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="90c69-115">PARAMETERS</span></span>

### <span data-ttu-id="90c69-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="90c69-116">-Location</span></span>
<span data-ttu-id="90c69-117">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="90c69-117">Location of the resource.</span></span>

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

### <span data-ttu-id="90c69-118">-Ge</span><span class="sxs-lookup"><span data-stu-id="90c69-118">-Offer</span></span>
<span data-ttu-id="90c69-119">Namn på offerter.</span><span class="sxs-lookup"><span data-stu-id="90c69-119">Name of the offer.</span></span>

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

### <span data-ttu-id="90c69-120">-Publisher</span><span class="sxs-lookup"><span data-stu-id="90c69-120">-Publisher</span></span>
<span data-ttu-id="90c69-121">Namnet på utgivaren.</span><span class="sxs-lookup"><span data-stu-id="90c69-121">Name of the publisher.</span></span>

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

### <span data-ttu-id="90c69-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="90c69-122">-ResourceId</span></span>
<span data-ttu-id="90c69-123">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="90c69-123">The resource id.</span></span>

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

### <span data-ttu-id="90c69-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="90c69-124">-Sku</span></span>
<span data-ttu-id="90c69-125">Namn på SKU.</span><span class="sxs-lookup"><span data-stu-id="90c69-125">Name of the SKU.</span></span>

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

### <span data-ttu-id="90c69-126">-Version</span><span class="sxs-lookup"><span data-stu-id="90c69-126">-Version</span></span>
<span data-ttu-id="90c69-127">Versionen av plattforms bilden.</span><span class="sxs-lookup"><span data-stu-id="90c69-127">The version of the platform image.</span></span>

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

### <span data-ttu-id="90c69-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90c69-128">CommonParameters</span></span>
<span data-ttu-id="90c69-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90c69-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90c69-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90c69-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90c69-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="90c69-131">INPUTS</span></span>

## <span data-ttu-id="90c69-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="90c69-132">OUTPUTS</span></span>

### <span data-ttu-id="90c69-133">PlatformImageObject</span><span class="sxs-lookup"><span data-stu-id="90c69-133">PlatformImageObject</span></span>

## <span data-ttu-id="90c69-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="90c69-134">NOTES</span></span>

## <span data-ttu-id="90c69-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="90c69-135">RELATED LINKS</span></span>

