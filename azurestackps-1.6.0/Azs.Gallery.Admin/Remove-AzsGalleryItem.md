---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 148cfa9db340b4a10e02b0870fc2edb5efb20a9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754987"
---
# <span data-ttu-id="4fcd8-101">Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="4fcd8-101">Remove-AzsGalleryItem</span></span>

## <span data-ttu-id="4fcd8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4fcd8-102">SYNOPSIS</span></span>
<span data-ttu-id="4fcd8-103">Ta bort ett specifikt Galleri objekt.</span><span class="sxs-lookup"><span data-stu-id="4fcd8-103">Delete a specific gallery item.</span></span>

## <span data-ttu-id="4fcd8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4fcd8-104">SYNTAX</span></span>

### <span data-ttu-id="4fcd8-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="4fcd8-105">Delete (Default)</span></span>
```
Remove-AzsGalleryItem [-Name] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fcd8-106">ID</span><span class="sxs-lookup"><span data-stu-id="4fcd8-106">ResourceId</span></span>
```
Remove-AzsGalleryItem -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fcd8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4fcd8-107">DESCRIPTION</span></span>
<span data-ttu-id="4fcd8-108">Ta bort ett specifikt Galleri objekt.</span><span class="sxs-lookup"><span data-stu-id="4fcd8-108">Delete a specific gallery item.</span></span>

## <span data-ttu-id="4fcd8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4fcd8-109">EXAMPLES</span></span>

### <span data-ttu-id="4fcd8-110">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4fcd8-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsGalleryItem -Name "microsoft.vmss.1.3.6"
```

<span data-ttu-id="4fcd8-111">Ta bort ett GALLERYITEM-objekt.</span><span class="sxs-lookup"><span data-stu-id="4fcd8-111">Delete a gallery item.</span></span>

## <span data-ttu-id="4fcd8-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4fcd8-112">PARAMETERS</span></span>

### <span data-ttu-id="4fcd8-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4fcd8-113">-Force</span></span>
<span data-ttu-id="4fcd8-114">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="4fcd8-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="4fcd8-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="4fcd8-115">-Name</span></span>
<span data-ttu-id="4fcd8-116">Identitet för GALLERYITEM.</span><span class="sxs-lookup"><span data-stu-id="4fcd8-116">Identity of the gallery item.</span></span>
<span data-ttu-id="4fcd8-117">Inkluderar Publisher-namn, artikel namn och kan innehålla version avgränsad efter period tecken.</span><span class="sxs-lookup"><span data-stu-id="4fcd8-117">Includes publisher name, item name, and may include version separated by period character.</span></span>

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

### <span data-ttu-id="4fcd8-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4fcd8-118">-ResourceId</span></span>
<span data-ttu-id="4fcd8-119">Fullständigt kvalificerat Azure Resource-ID.</span><span class="sxs-lookup"><span data-stu-id="4fcd8-119">Fully qualified Azure resource Id.</span></span>

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

### <span data-ttu-id="4fcd8-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4fcd8-120">-Confirm</span></span>
<span data-ttu-id="4fcd8-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4fcd8-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fcd8-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fcd8-122">-WhatIf</span></span>
<span data-ttu-id="4fcd8-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4fcd8-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fcd8-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4fcd8-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fcd8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fcd8-125">CommonParameters</span></span>
<span data-ttu-id="4fcd8-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fcd8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fcd8-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fcd8-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fcd8-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4fcd8-128">INPUTS</span></span>

## <span data-ttu-id="4fcd8-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4fcd8-129">OUTPUTS</span></span>

## <span data-ttu-id="4fcd8-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4fcd8-130">NOTES</span></span>

## <span data-ttu-id="4fcd8-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4fcd8-131">RELATED LINKS</span></span>

