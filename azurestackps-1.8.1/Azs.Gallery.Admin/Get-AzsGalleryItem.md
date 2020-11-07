---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0fa95e34c6a220a496a79f7a72c65c222f1376f1
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921897"
---
# <span data-ttu-id="7f621-101">Get-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="7f621-101">Get-AzsGalleryItem</span></span>

## <span data-ttu-id="7f621-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7f621-102">SYNOPSIS</span></span>
<span data-ttu-id="7f621-103">Visar en lista med Galleri objekt.</span><span class="sxs-lookup"><span data-stu-id="7f621-103">Lists gallery items.</span></span>

## <span data-ttu-id="7f621-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7f621-104">SYNTAX</span></span>

### <span data-ttu-id="7f621-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="7f621-105">List (Default)</span></span>
```
Get-AzsGalleryItem [<CommonParameters>]
```

### <span data-ttu-id="7f621-106">Lära</span><span class="sxs-lookup"><span data-stu-id="7f621-106">Get</span></span>
```
Get-AzsGalleryItem [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="7f621-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7f621-107">DESCRIPTION</span></span>
<span data-ttu-id="7f621-108">Få en lista med tillgängliga Galleri objekt i Azure Stack Marketplace</span><span class="sxs-lookup"><span data-stu-id="7f621-108">Get a list of gallery items available in Azure Stack Marketplace</span></span>

## <span data-ttu-id="7f621-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7f621-109">EXAMPLES</span></span>

### <span data-ttu-id="7f621-110">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="7f621-110">EXAMPLE 1</span></span>
```
Get-AzsGalleryItem
```

<span data-ttu-id="7f621-111">List Galleri objekt.</span><span class="sxs-lookup"><span data-stu-id="7f621-111">List gallery items.</span></span>

### <span data-ttu-id="7f621-112">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="7f621-112">EXAMPLE 2</span></span>
```
Get-AzsGalleryItem -Name 'microsoft.vmss.1.3.6'
```

<span data-ttu-id="7f621-113">Hämta ett galleri objekt efter namn.</span><span class="sxs-lookup"><span data-stu-id="7f621-113">Get a gallery item by name.</span></span>

## <span data-ttu-id="7f621-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7f621-114">PARAMETERS</span></span>

### <span data-ttu-id="7f621-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="7f621-115">-Name</span></span>
<span data-ttu-id="7f621-116">Identitet för GALLERYITEM.</span><span class="sxs-lookup"><span data-stu-id="7f621-116">Identity of the gallery item.</span></span>
<span data-ttu-id="7f621-117">Inkluderar Publisher-namn, artikel namn och kan innehålla version avgränsad efter period tecken.</span><span class="sxs-lookup"><span data-stu-id="7f621-117">Includes publisher name, item name, and may include version separated by period character.</span></span>

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

### <span data-ttu-id="7f621-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f621-118">CommonParameters</span></span>
<span data-ttu-id="7f621-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f621-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f621-120">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f621-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f621-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7f621-121">INPUTS</span></span>

## <span data-ttu-id="7f621-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7f621-122">OUTPUTS</span></span>

### <span data-ttu-id="7f621-123">Microsoft. AzureStack. Management. Gallery. admin. Models. GalleryItem</span><span class="sxs-lookup"><span data-stu-id="7f621-123">Microsoft.AzureStack.Management.Gallery.Admin.Models.GalleryItem</span></span>

## <span data-ttu-id="7f621-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7f621-124">NOTES</span></span>

## <span data-ttu-id="7f621-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7f621-125">RELATED LINKS</span></span>
