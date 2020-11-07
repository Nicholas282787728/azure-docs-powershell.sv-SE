---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
ms.openlocfilehash: 7c62860f3829c07621c951175b00a4be4960c95f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745050"
---
# <span data-ttu-id="f5f5e-101">Remove-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="f5f5e-101">Remove-AzGalleryImageVersion</span></span>

## <span data-ttu-id="f5f5e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f5f5e-102">SYNOPSIS</span></span>
<span data-ttu-id="f5f5e-103">Ta bort en galleri bild version.</span><span class="sxs-lookup"><span data-stu-id="f5f5e-103">Delete a gallery image version.</span></span>

## <span data-ttu-id="f5f5e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f5f5e-104">SYNTAX</span></span>

### <span data-ttu-id="f5f5e-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="f5f5e-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5f5e-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="f5f5e-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5f5e-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="f5f5e-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5f5e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f5f5e-108">DESCRIPTION</span></span>
<span data-ttu-id="f5f5e-109">Ta bort en galleri bild version.</span><span class="sxs-lookup"><span data-stu-id="f5f5e-109">Delete a gallery image version.</span></span>

## <span data-ttu-id="f5f5e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f5f5e-110">EXAMPLES</span></span>

### <span data-ttu-id="f5f5e-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f5f5e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -ImageDefinitionName $image -GalleryImageVersionName $version
```

<span data-ttu-id="f5f5e-112">Ta bort den angivna galleri bild versionen.</span><span class="sxs-lookup"><span data-stu-id="f5f5e-112">Delete the given gallery image version.</span></span>

## <span data-ttu-id="f5f5e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f5f5e-113">PARAMETERS</span></span>

### <span data-ttu-id="f5f5e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5f5e-114">-AsJob</span></span>
<span data-ttu-id="f5f5e-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="f5f5e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f5f5e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5f5e-116">-DefaultProfile</span></span>
<span data-ttu-id="f5f5e-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f5f5e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5f5e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f5f5e-118">-Force</span></span>
<span data-ttu-id="f5f5e-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="f5f5e-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f5f5e-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="f5f5e-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="f5f5e-121">Namnet på bild definitionen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="f5f5e-121">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5f5e-122">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="f5f5e-122">-GalleryName</span></span>
<span data-ttu-id="f5f5e-123">Namnet på galleriet.</span><span class="sxs-lookup"><span data-stu-id="f5f5e-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="f5f5e-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5f5e-124">-InputObject</span></span>
<span data-ttu-id="f5f5e-125">Versions objekt för PS-galleriet</span><span class="sxs-lookup"><span data-stu-id="f5f5e-125">The PS Gallery Image Version Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion
Parameter Sets: ObjectParameter
Aliases: GalleryImageVersion

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5f5e-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="f5f5e-126">-Name</span></span>
<span data-ttu-id="f5f5e-127">Namnet på Galleri bild versionen.</span><span class="sxs-lookup"><span data-stu-id="f5f5e-127">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageVersionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5f5e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5f5e-128">-ResourceGroupName</span></span>
<span data-ttu-id="f5f5e-129">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f5f5e-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="f5f5e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5f5e-130">-ResourceId</span></span>
<span data-ttu-id="f5f5e-131">Resurs-ID för galleriet bild version</span><span class="sxs-lookup"><span data-stu-id="f5f5e-131">The resource ID for gallery image version</span></span>

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

### <span data-ttu-id="f5f5e-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f5f5e-132">-Confirm</span></span>
<span data-ttu-id="f5f5e-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f5f5e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5f5e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5f5e-134">-WhatIf</span></span>
<span data-ttu-id="f5f5e-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f5f5e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5f5e-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f5f5e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5f5e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5f5e-137">CommonParameters</span></span>
<span data-ttu-id="f5f5e-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5f5e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5f5e-139">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f5f5e-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5f5e-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f5f5e-140">INPUTS</span></span>

### <span data-ttu-id="f5f5e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f5f5e-141">System.String</span></span>

### <span data-ttu-id="f5f5e-142">Microsoft. Azure. commands. Compute. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="f5f5e-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="f5f5e-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f5f5e-143">OUTPUTS</span></span>

### <span data-ttu-id="f5f5e-144">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="f5f5e-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="f5f5e-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f5f5e-145">NOTES</span></span>

## <span data-ttu-id="f5f5e-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f5f5e-146">RELATED LINKS</span></span>
