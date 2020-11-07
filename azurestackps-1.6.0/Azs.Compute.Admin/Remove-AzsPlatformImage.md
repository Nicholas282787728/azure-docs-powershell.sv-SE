---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 947bb6b453d92897f7901a00ed5a43efa4ac640e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754917"
---
# <span data-ttu-id="5f03b-101">Remove-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="5f03b-101">Remove-AzsPlatformImage</span></span>

## <span data-ttu-id="5f03b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5f03b-102">SYNOPSIS</span></span>
<span data-ttu-id="5f03b-103">Ta bort en virtuell dator bild från Platform image lagring.</span><span class="sxs-lookup"><span data-stu-id="5f03b-103">Delete a virtual machine image from the platform image repository.</span></span>

## <span data-ttu-id="5f03b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5f03b-104">SYNTAX</span></span>

### <span data-ttu-id="5f03b-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="5f03b-105">Delete (Default)</span></span>
```
Remove-AzsPlatformImage -Publisher <String> -Offer <String> -Sku <String> -Version <String>
 [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f03b-106">ID</span><span class="sxs-lookup"><span data-stu-id="5f03b-106">ResourceId</span></span>
```
Remove-AzsPlatformImage -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f03b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5f03b-107">DESCRIPTION</span></span>
<span data-ttu-id="5f03b-108">Ta bort en plattforms bild</span><span class="sxs-lookup"><span data-stu-id="5f03b-108">Delete a platform image</span></span>

## <span data-ttu-id="5f03b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5f03b-109">EXAMPLES</span></span>

### <span data-ttu-id="5f03b-110">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5f03b-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlatformImage -Publisher Test -Offer UbuntuServer -Version 1.0.0 -Sku 16.04-LTS
```

<span data-ttu-id="5f03b-111">Ta bort en befintlig plattforms bild.</span><span class="sxs-lookup"><span data-stu-id="5f03b-111">Delete an existing platform image.</span></span>

## <span data-ttu-id="5f03b-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5f03b-112">PARAMETERS</span></span>

### <span data-ttu-id="5f03b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="5f03b-113">-Force</span></span>
<span data-ttu-id="5f03b-114">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="5f03b-114">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f03b-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="5f03b-115">-Location</span></span>
<span data-ttu-id="5f03b-116">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="5f03b-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f03b-117">-Ge</span><span class="sxs-lookup"><span data-stu-id="5f03b-117">-Offer</span></span>
<span data-ttu-id="5f03b-118">Namn på offerter.</span><span class="sxs-lookup"><span data-stu-id="5f03b-118">Name of the offer.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f03b-119">-Publisher</span><span class="sxs-lookup"><span data-stu-id="5f03b-119">-Publisher</span></span>
<span data-ttu-id="5f03b-120">Namnet på utgivaren.</span><span class="sxs-lookup"><span data-stu-id="5f03b-120">Name of the publisher.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f03b-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f03b-121">-ResourceId</span></span>
<span data-ttu-id="5f03b-122">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="5f03b-122">The resource id.</span></span>

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

### <span data-ttu-id="5f03b-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="5f03b-123">-Sku</span></span>
<span data-ttu-id="5f03b-124">Namn på SKU.</span><span class="sxs-lookup"><span data-stu-id="5f03b-124">Name of the SKU.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f03b-125">-Version</span><span class="sxs-lookup"><span data-stu-id="5f03b-125">-Version</span></span>
<span data-ttu-id="5f03b-126">Den virtuella datorns version.</span><span class="sxs-lookup"><span data-stu-id="5f03b-126">The version of the virtual machine image.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f03b-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5f03b-127">-Confirm</span></span>
<span data-ttu-id="5f03b-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5f03b-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f03b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f03b-129">-WhatIf</span></span>
<span data-ttu-id="5f03b-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5f03b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f03b-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5f03b-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f03b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f03b-132">CommonParameters</span></span>
<span data-ttu-id="5f03b-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f03b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f03b-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f03b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f03b-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5f03b-135">INPUTS</span></span>

## <span data-ttu-id="5f03b-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5f03b-136">OUTPUTS</span></span>

## <span data-ttu-id="5f03b-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5f03b-137">NOTES</span></span>

## <span data-ttu-id="5f03b-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5f03b-138">RELATED LINKS</span></span>

