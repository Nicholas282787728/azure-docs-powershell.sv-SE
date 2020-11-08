---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8fc33149fa47c6c70207bebfe87e554fe7eb60cf
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100368"
---
# <span data-ttu-id="2674e-101">Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="2674e-101">Remove-AzsGalleryItem</span></span>

## <span data-ttu-id="2674e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2674e-102">SYNOPSIS</span></span>
<span data-ttu-id="2674e-103">Ta bort ett specifikt Galleri objekt.</span><span class="sxs-lookup"><span data-stu-id="2674e-103">Delete a specific gallery item.</span></span>

## <span data-ttu-id="2674e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2674e-104">SYNTAX</span></span>

### <span data-ttu-id="2674e-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="2674e-105">Delete (Default)</span></span>
```
Remove-AzsGalleryItem [-Name] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2674e-106">ID</span><span class="sxs-lookup"><span data-stu-id="2674e-106">ResourceId</span></span>
```
Remove-AzsGalleryItem -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2674e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2674e-107">DESCRIPTION</span></span>
<span data-ttu-id="2674e-108">Ta bort ett specifikt Galleri objekt.</span><span class="sxs-lookup"><span data-stu-id="2674e-108">Delete a specific gallery item.</span></span>

## <span data-ttu-id="2674e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2674e-109">EXAMPLES</span></span>

### <span data-ttu-id="2674e-110">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="2674e-110">EXAMPLE 1</span></span>
```
Remove-AzsGalleryItem -Name "microsoft.vmss.1.3.6"
```

<span data-ttu-id="2674e-111">Ta bort ett GALLERYITEM-objekt.</span><span class="sxs-lookup"><span data-stu-id="2674e-111">Delete a gallery item.</span></span>

## <span data-ttu-id="2674e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2674e-112">PARAMETERS</span></span>

### <span data-ttu-id="2674e-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="2674e-113">-Name</span></span>
<span data-ttu-id="2674e-114">Identitet för GALLERYITEM.</span><span class="sxs-lookup"><span data-stu-id="2674e-114">Identity of the gallery item.</span></span>
<span data-ttu-id="2674e-115">Inkluderar Publisher-namn, artikel namn och kan innehålla version avgränsad efter period tecken.</span><span class="sxs-lookup"><span data-stu-id="2674e-115">Includes publisher name, item name, and may include version separated by period character.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2674e-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2674e-116">-ResourceId</span></span>
<span data-ttu-id="2674e-117">Fullständigt kvalificerat Azure Resource-ID.</span><span class="sxs-lookup"><span data-stu-id="2674e-117">Fully qualified Azure resource Id.</span></span>

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

### <span data-ttu-id="2674e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="2674e-118">-Force</span></span>
<span data-ttu-id="2674e-119">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="2674e-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="2674e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2674e-120">-WhatIf</span></span>
<span data-ttu-id="2674e-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2674e-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2674e-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2674e-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2674e-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2674e-123">-Confirm</span></span>
<span data-ttu-id="2674e-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2674e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2674e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2674e-125">CommonParameters</span></span>
<span data-ttu-id="2674e-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2674e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2674e-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2674e-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2674e-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2674e-128">INPUTS</span></span>

## <span data-ttu-id="2674e-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2674e-129">OUTPUTS</span></span>

## <span data-ttu-id="2674e-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2674e-130">NOTES</span></span>

## <span data-ttu-id="2674e-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2674e-131">RELATED LINKS</span></span>