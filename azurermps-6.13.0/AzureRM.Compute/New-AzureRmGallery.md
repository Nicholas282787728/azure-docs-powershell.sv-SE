---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmGallery.md
ms.openlocfilehash: bb743768654dcaeec9a39e7b590abe71b155cc17
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757918"
---
# <span data-ttu-id="ce9dc-101">New-AzureRmGallery</span><span class="sxs-lookup"><span data-stu-id="ce9dc-101">New-AzureRmGallery</span></span>

## <span data-ttu-id="ce9dc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ce9dc-102">SYNOPSIS</span></span>
<span data-ttu-id="ce9dc-103">Skapa ett galleri.</span><span class="sxs-lookup"><span data-stu-id="ce9dc-103">Create a gallery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce9dc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ce9dc-104">SYNTAX</span></span>

```
New-AzureRmGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Location] <String>
 [-Description <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ce9dc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ce9dc-105">DESCRIPTION</span></span>
<span data-ttu-id="ce9dc-106">Skapa ett galleri.</span><span class="sxs-lookup"><span data-stu-id="ce9dc-106">Create a gallery.</span></span>

## <span data-ttu-id="ce9dc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ce9dc-107">EXAMPLES</span></span>

### <span data-ttu-id="ce9dc-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ce9dc-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmGallery -ResourceGroupName $rgname -Name $galleryName -Location $location -Description $galleryDescription
```

<span data-ttu-id="ce9dc-109">Skapa ett galleri.</span><span class="sxs-lookup"><span data-stu-id="ce9dc-109">Create a gallery.</span></span>

## <span data-ttu-id="ce9dc-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ce9dc-110">PARAMETERS</span></span>

### <span data-ttu-id="ce9dc-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce9dc-111">-AsJob</span></span>
<span data-ttu-id="ce9dc-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="ce9dc-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce9dc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce9dc-113">-DefaultProfile</span></span>
<span data-ttu-id="ce9dc-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ce9dc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce9dc-115">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="ce9dc-115">-Description</span></span>
<span data-ttu-id="ce9dc-116">Beskrivning av Galleri resursen.</span><span class="sxs-lookup"><span data-stu-id="ce9dc-116">The description of the gallery resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce9dc-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="ce9dc-117">-Location</span></span>
<span data-ttu-id="ce9dc-118">Resurs plats</span><span class="sxs-lookup"><span data-stu-id="ce9dc-118">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce9dc-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="ce9dc-119">-Name</span></span>
<span data-ttu-id="ce9dc-120">Namnet på galleriet.</span><span class="sxs-lookup"><span data-stu-id="ce9dc-120">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GalleryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce9dc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce9dc-121">-ResourceGroupName</span></span>
<span data-ttu-id="ce9dc-122">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ce9dc-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce9dc-123">-Tagg</span><span class="sxs-lookup"><span data-stu-id="ce9dc-123">-Tag</span></span>
<span data-ttu-id="ce9dc-124">Resursfiler</span><span class="sxs-lookup"><span data-stu-id="ce9dc-124">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce9dc-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ce9dc-125">-Confirm</span></span>
<span data-ttu-id="ce9dc-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ce9dc-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce9dc-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce9dc-127">-WhatIf</span></span>
<span data-ttu-id="ce9dc-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ce9dc-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce9dc-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ce9dc-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce9dc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce9dc-130">CommonParameters</span></span>
<span data-ttu-id="ce9dc-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce9dc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce9dc-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce9dc-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce9dc-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ce9dc-133">INPUTS</span></span>

### <span data-ttu-id="ce9dc-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ce9dc-134">System.String</span></span>

### <span data-ttu-id="ce9dc-135">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="ce9dc-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ce9dc-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ce9dc-136">OUTPUTS</span></span>

### <span data-ttu-id="ce9dc-137">Microsoft. Azure. commands. Compute. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="ce9dc-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="ce9dc-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ce9dc-138">NOTES</span></span>

## <span data-ttu-id="ce9dc-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ce9dc-139">RELATED LINKS</span></span>