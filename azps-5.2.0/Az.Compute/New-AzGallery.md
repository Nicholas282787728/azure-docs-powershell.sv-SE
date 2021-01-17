---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
ms.openlocfilehash: d1a25b3e8466c691272f4c556fe728cbce47a718
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408459"
---
# <span data-ttu-id="3e1e9-101">New-AzGallery</span><span class="sxs-lookup"><span data-stu-id="3e1e9-101">New-AzGallery</span></span>

## <span data-ttu-id="3e1e9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3e1e9-102">SYNOPSIS</span></span>
<span data-ttu-id="3e1e9-103">Skapa ett galleri.</span><span class="sxs-lookup"><span data-stu-id="3e1e9-103">Create a gallery.</span></span>

## <span data-ttu-id="3e1e9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3e1e9-104">SYNTAX</span></span>

```
New-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Location] <String>
 [-Description <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3e1e9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3e1e9-105">DESCRIPTION</span></span>
<span data-ttu-id="3e1e9-106">Skapa ett galleri.</span><span class="sxs-lookup"><span data-stu-id="3e1e9-106">Create a gallery.</span></span>

## <span data-ttu-id="3e1e9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3e1e9-107">EXAMPLES</span></span>

### <span data-ttu-id="3e1e9-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3e1e9-108">Example 1</span></span>
```powershell
PS C:\> New-AzGallery -ResourceGroupName $rgname -Name $galleryName -Location $location -Description $galleryDescription
```

<span data-ttu-id="3e1e9-109">Skapa ett galleri.</span><span class="sxs-lookup"><span data-stu-id="3e1e9-109">Create a gallery.</span></span>

## <span data-ttu-id="3e1e9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3e1e9-110">PARAMETERS</span></span>

### <span data-ttu-id="3e1e9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e1e9-111">-AsJob</span></span>
<span data-ttu-id="3e1e9-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="3e1e9-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3e1e9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e1e9-113">-DefaultProfile</span></span>
<span data-ttu-id="3e1e9-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3e1e9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e1e9-115">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="3e1e9-115">-Description</span></span>
<span data-ttu-id="3e1e9-116">Beskrivning av Galleri resursen.</span><span class="sxs-lookup"><span data-stu-id="3e1e9-116">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="3e1e9-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="3e1e9-117">-Location</span></span>
<span data-ttu-id="3e1e9-118">Resurs plats</span><span class="sxs-lookup"><span data-stu-id="3e1e9-118">Resource location</span></span>

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

### <span data-ttu-id="3e1e9-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="3e1e9-119">-Name</span></span>
<span data-ttu-id="3e1e9-120">Namnet på galleriet.</span><span class="sxs-lookup"><span data-stu-id="3e1e9-120">The name of the gallery.</span></span>

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

### <span data-ttu-id="3e1e9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e1e9-121">-ResourceGroupName</span></span>
<span data-ttu-id="3e1e9-122">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3e1e9-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="3e1e9-123">-Tagg</span><span class="sxs-lookup"><span data-stu-id="3e1e9-123">-Tag</span></span>
<span data-ttu-id="3e1e9-124">Resursfiler</span><span class="sxs-lookup"><span data-stu-id="3e1e9-124">Resource tags</span></span>

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

### <span data-ttu-id="3e1e9-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3e1e9-125">-Confirm</span></span>
<span data-ttu-id="3e1e9-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3e1e9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e1e9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e1e9-127">-WhatIf</span></span>
<span data-ttu-id="3e1e9-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3e1e9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e1e9-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3e1e9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e1e9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e1e9-130">CommonParameters</span></span>
<span data-ttu-id="3e1e9-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e1e9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e1e9-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e1e9-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e1e9-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3e1e9-133">INPUTS</span></span>

### <span data-ttu-id="3e1e9-134">System. String</span><span class="sxs-lookup"><span data-stu-id="3e1e9-134">System.String</span></span>

### <span data-ttu-id="3e1e9-135">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="3e1e9-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3e1e9-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3e1e9-136">OUTPUTS</span></span>

### <span data-ttu-id="3e1e9-137">Microsoft. Azure. commands. Compute. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="3e1e9-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="3e1e9-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3e1e9-138">NOTES</span></span>

## <span data-ttu-id="3e1e9-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3e1e9-139">RELATED LINKS</span></span>
