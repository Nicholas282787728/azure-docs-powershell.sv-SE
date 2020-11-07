---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f0eadd6f0561ca5b44a588397f46d6ad3d7a1c3c
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921899"
---
# <span data-ttu-id="d6676-101">Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="d6676-101">Add-AzsGalleryItem</span></span>

## <span data-ttu-id="d6676-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d6676-102">SYNOPSIS</span></span>
<span data-ttu-id="d6676-103">Laddar upp ett tjänst Galleri objekt till lagrings platsen.</span><span class="sxs-lookup"><span data-stu-id="d6676-103">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="d6676-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d6676-104">SYNTAX</span></span>

```
Add-AzsGalleryItem [-GalleryItemUri] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6676-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d6676-105">DESCRIPTION</span></span>
<span data-ttu-id="d6676-106">Laddar upp ett tjänst Galleri objekt till lagrings platsen.</span><span class="sxs-lookup"><span data-stu-id="d6676-106">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="d6676-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d6676-107">EXAMPLES</span></span>

### <span data-ttu-id="d6676-108">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="d6676-108">EXAMPLE 1</span></span>
```
Add-AzsGalleryItem -GalleryItemUri 'http://galleryitemuri'
```

<span data-ttu-id="d6676-109">Skapa ett nytt Galleri objekt.</span><span class="sxs-lookup"><span data-stu-id="d6676-109">Create a new gallery item.</span></span>

## <span data-ttu-id="d6676-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d6676-110">PARAMETERS</span></span>

### <span data-ttu-id="d6676-111">-GalleryItemUri</span><span class="sxs-lookup"><span data-stu-id="d6676-111">-GalleryItemUri</span></span>
<span data-ttu-id="d6676-112">URI till JSON-filen för GALLERYITEM.</span><span class="sxs-lookup"><span data-stu-id="d6676-112">The URI to the gallery item JSON file.</span></span>

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

### <span data-ttu-id="d6676-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d6676-113">-Force</span></span>
<span data-ttu-id="d6676-114">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="d6676-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="d6676-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6676-115">-WhatIf</span></span>
<span data-ttu-id="d6676-116">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d6676-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6676-117">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d6676-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6676-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d6676-118">-Confirm</span></span>
<span data-ttu-id="d6676-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d6676-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6676-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6676-120">CommonParameters</span></span>
<span data-ttu-id="d6676-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6676-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6676-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6676-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6676-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d6676-123">INPUTS</span></span>

## <span data-ttu-id="d6676-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d6676-124">OUTPUTS</span></span>

### <span data-ttu-id="d6676-125">Microsoft. AzureStack. Management. Gallery. admin. Models. GalleryItem</span><span class="sxs-lookup"><span data-stu-id="d6676-125">Microsoft.AzureStack.Management.Gallery.Admin.Models.GalleryItem</span></span>

## <span data-ttu-id="d6676-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d6676-126">NOTES</span></span>

## <span data-ttu-id="d6676-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d6676-127">RELATED LINKS</span></span>
