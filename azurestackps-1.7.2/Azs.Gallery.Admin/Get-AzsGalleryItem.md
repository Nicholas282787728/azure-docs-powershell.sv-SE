---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2020caba1d7cac4ed1830fbc1b6a3ccdb4c71f27
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921189"
---
# <span data-ttu-id="c42f7-101">Get-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="c42f7-101">Get-AzsGalleryItem</span></span>

## <span data-ttu-id="c42f7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c42f7-102">SYNOPSIS</span></span>
<span data-ttu-id="c42f7-103">Visar en lista med Galleri objekt.</span><span class="sxs-lookup"><span data-stu-id="c42f7-103">Lists gallery items.</span></span>

## <span data-ttu-id="c42f7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c42f7-104">SYNTAX</span></span>

### <span data-ttu-id="c42f7-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="c42f7-105">List (Default)</span></span>
```
Get-AzsGalleryItem [<CommonParameters>]
```

### <span data-ttu-id="c42f7-106">Lära</span><span class="sxs-lookup"><span data-stu-id="c42f7-106">Get</span></span>
```
Get-AzsGalleryItem [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="c42f7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c42f7-107">DESCRIPTION</span></span>
<span data-ttu-id="c42f7-108">Få en lista med tillgängliga Galleri objekt i Azure Stack Marketplace</span><span class="sxs-lookup"><span data-stu-id="c42f7-108">Get a list of gallery items available in Azure Stack Marketplace</span></span>

## <span data-ttu-id="c42f7-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c42f7-109">EXAMPLES</span></span>

### <span data-ttu-id="c42f7-110">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c42f7-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsGalleryItem
```

<span data-ttu-id="c42f7-111">List Galleri objekt.</span><span class="sxs-lookup"><span data-stu-id="c42f7-111">List gallery items.</span></span>

### <span data-ttu-id="c42f7-112">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="c42f7-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsGalleryItem -Name 'microsoft.vmss.1.3.6'
```

<span data-ttu-id="c42f7-113">Hämta ett galleri objekt efter namn.</span><span class="sxs-lookup"><span data-stu-id="c42f7-113">Get a gallery item by name.</span></span>

## <span data-ttu-id="c42f7-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c42f7-114">PARAMETERS</span></span>

### <span data-ttu-id="c42f7-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="c42f7-115">-Name</span></span>
<span data-ttu-id="c42f7-116">Identitet för GALLERYITEM.</span><span class="sxs-lookup"><span data-stu-id="c42f7-116">Identity of the gallery item.</span></span>
<span data-ttu-id="c42f7-117">Inkluderar Publisher-namn, artikel namn och kan innehålla version avgränsad efter period tecken.</span><span class="sxs-lookup"><span data-stu-id="c42f7-117">Includes publisher name, item name, and may include version separated by period character.</span></span>

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

### <span data-ttu-id="c42f7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c42f7-118">CommonParameters</span></span>
<span data-ttu-id="c42f7-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c42f7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c42f7-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c42f7-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c42f7-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c42f7-121">INPUTS</span></span>

## <span data-ttu-id="c42f7-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c42f7-122">OUTPUTS</span></span>

### <span data-ttu-id="c42f7-123">Microsoft. AzureStack. Management. Gallery. admin. Models. GalleryItem</span><span class="sxs-lookup"><span data-stu-id="c42f7-123">Microsoft.AzureStack.Management.Gallery.Admin.Models.GalleryItem</span></span>

## <span data-ttu-id="c42f7-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c42f7-124">NOTES</span></span>

## <span data-ttu-id="c42f7-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c42f7-125">RELATED LINKS</span></span>
