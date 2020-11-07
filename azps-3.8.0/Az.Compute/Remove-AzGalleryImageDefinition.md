---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
ms.openlocfilehash: 81323c1a35e36b036e759911bbfec2dde764ac8f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93928229"
---
# <span data-ttu-id="cc1b8-101">Remove-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="cc1b8-101">Remove-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="cc1b8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cc1b8-102">SYNOPSIS</span></span>
<span data-ttu-id="cc1b8-103">Ta bort en bild definition för galleriet.</span><span class="sxs-lookup"><span data-stu-id="cc1b8-103">Delete a gallery image definition.</span></span>

## <span data-ttu-id="cc1b8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cc1b8-104">SYNTAX</span></span>

### <span data-ttu-id="cc1b8-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="cc1b8-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc1b8-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="cc1b8-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc1b8-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="cc1b8-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-InputObject] <PSGalleryImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc1b8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cc1b8-108">DESCRIPTION</span></span>
<span data-ttu-id="cc1b8-109">Ta bort en bild definition för galleriet.</span><span class="sxs-lookup"><span data-stu-id="cc1b8-109">Delete a gallery image definition.</span></span>

## <span data-ttu-id="cc1b8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cc1b8-110">EXAMPLES</span></span>

### <span data-ttu-id="cc1b8-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cc1b8-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageDefinition -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $galleryImage
```

<span data-ttu-id="cc1b8-112">Ta bort bild definitionen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="cc1b8-112">Remove the gallery image definition.</span></span>

## <span data-ttu-id="cc1b8-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cc1b8-113">PARAMETERS</span></span>

### <span data-ttu-id="cc1b8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc1b8-114">-AsJob</span></span>
<span data-ttu-id="cc1b8-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="cc1b8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cc1b8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc1b8-116">-DefaultProfile</span></span>
<span data-ttu-id="cc1b8-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cc1b8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc1b8-118">-Force</span><span class="sxs-lookup"><span data-stu-id="cc1b8-118">-Force</span></span>
<span data-ttu-id="cc1b8-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="cc1b8-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cc1b8-120">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="cc1b8-120">-GalleryName</span></span>
<span data-ttu-id="cc1b8-121">Namnet på galleriet.</span><span class="sxs-lookup"><span data-stu-id="cc1b8-121">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc1b8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc1b8-122">-InputObject</span></span>
<span data-ttu-id="cc1b8-123">Bild definitions objekt för PS-galleriet</span><span class="sxs-lookup"><span data-stu-id="cc1b8-123">The PS Gallery Image Definition Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage
Parameter Sets: ObjectParameter
Aliases: GalleryImageDefinition

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc1b8-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="cc1b8-124">-Name</span></span>
<span data-ttu-id="cc1b8-125">Namnet på bild definitionen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="cc1b8-125">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc1b8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc1b8-126">-ResourceGroupName</span></span>
<span data-ttu-id="cc1b8-127">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="cc1b8-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc1b8-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc1b8-128">-ResourceId</span></span>
<span data-ttu-id="cc1b8-129">Resurs-ID för bild definitionen för galleriet</span><span class="sxs-lookup"><span data-stu-id="cc1b8-129">The resource ID for the gallery image definition</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc1b8-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cc1b8-130">-Confirm</span></span>
<span data-ttu-id="cc1b8-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cc1b8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc1b8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc1b8-132">-WhatIf</span></span>
<span data-ttu-id="cc1b8-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cc1b8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc1b8-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cc1b8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc1b8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc1b8-135">CommonParameters</span></span>
<span data-ttu-id="cc1b8-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc1b8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc1b8-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc1b8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc1b8-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cc1b8-138">INPUTS</span></span>

### <span data-ttu-id="cc1b8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="cc1b8-139">System.String</span></span>

### <span data-ttu-id="cc1b8-140">Microsoft. Azure. commands. Compute. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="cc1b8-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="cc1b8-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cc1b8-141">OUTPUTS</span></span>

### <span data-ttu-id="cc1b8-142">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="cc1b8-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="cc1b8-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cc1b8-143">NOTES</span></span>

## <span data-ttu-id="cc1b8-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cc1b8-144">RELATED LINKS</span></span>
