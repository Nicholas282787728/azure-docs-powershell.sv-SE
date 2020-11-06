---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: db1f78f3adec999cdf8839eb972a71595f6c15b5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571964"
---
# <span data-ttu-id="42b78-101">Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="42b78-101">Add-AzsGalleryItem</span></span>

## <span data-ttu-id="42b78-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="42b78-102">SYNOPSIS</span></span>
<span data-ttu-id="42b78-103">Laddar upp ett tjänst Galleri objekt till lagrings platsen.</span><span class="sxs-lookup"><span data-stu-id="42b78-103">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="42b78-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="42b78-104">SYNTAX</span></span>

```
Add-AzsGalleryItem [-GalleryItemUri] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42b78-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="42b78-105">DESCRIPTION</span></span>
<span data-ttu-id="42b78-106">Laddar upp ett tjänst Galleri objekt till lagrings platsen.</span><span class="sxs-lookup"><span data-stu-id="42b78-106">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="42b78-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="42b78-107">EXAMPLES</span></span>

### <span data-ttu-id="42b78-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="42b78-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsGalleryItem -GalleryItemUri 'http://galleryitemuri'
```

<span data-ttu-id="42b78-109">Skapa ett nytt Galleri objekt.</span><span class="sxs-lookup"><span data-stu-id="42b78-109">Create a new gallery item.</span></span>

## <span data-ttu-id="42b78-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="42b78-110">PARAMETERS</span></span>

### <span data-ttu-id="42b78-111">-Force</span><span class="sxs-lookup"><span data-stu-id="42b78-111">-Force</span></span>
<span data-ttu-id="42b78-112">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="42b78-112">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="42b78-113">-GalleryItemUri</span><span class="sxs-lookup"><span data-stu-id="42b78-113">-GalleryItemUri</span></span>
<span data-ttu-id="42b78-114">URI till JSON-filen för GALLERYITEM.</span><span class="sxs-lookup"><span data-stu-id="42b78-114">The URI to the gallery item JSON file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b78-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="42b78-115">-Confirm</span></span>
<span data-ttu-id="42b78-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="42b78-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42b78-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42b78-117">-WhatIf</span></span>
<span data-ttu-id="42b78-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="42b78-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42b78-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="42b78-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42b78-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42b78-120">CommonParameters</span></span>
<span data-ttu-id="42b78-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42b78-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42b78-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42b78-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42b78-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="42b78-123">INPUTS</span></span>

## <span data-ttu-id="42b78-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="42b78-124">OUTPUTS</span></span>

### <span data-ttu-id="42b78-125">Microsoft. AzureStack. Management. Gallery. admin. Models. GalleryItem</span><span class="sxs-lookup"><span data-stu-id="42b78-125">Microsoft.AzureStack.Management.Gallery.Admin.Models.GalleryItem</span></span>

## <span data-ttu-id="42b78-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="42b78-126">NOTES</span></span>

## <span data-ttu-id="42b78-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="42b78-127">RELATED LINKS</span></span>

