---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
ms.openlocfilehash: 6d5731916309baf93552f9b5d71f30943178f11c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754543"
---
# <span data-ttu-id="0934d-101">New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="0934d-101">New-AzGalleryImageVersion</span></span>

## <span data-ttu-id="0934d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0934d-102">SYNOPSIS</span></span>
<span data-ttu-id="0934d-103">Skapa en galleri bild version.</span><span class="sxs-lookup"><span data-stu-id="0934d-103">Create a gallery image version.</span></span>

## <span data-ttu-id="0934d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0934d-104">SYNTAX</span></span>

```
New-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] -Location <String> -SourceImageId <String>
 [-Tag <Hashtable>] [-ReplicaCount <Int32>] [-PublishingProfileExcludeFromLatest]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0934d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0934d-105">DESCRIPTION</span></span>
<span data-ttu-id="0934d-106">Skapa en galleri bild version.</span><span class="sxs-lookup"><span data-stu-id="0934d-106">Create a gallery image version.</span></span>

## <span data-ttu-id="0934d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0934d-107">EXAMPLES</span></span>

### <span data-ttu-id="0934d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0934d-108">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -Location $location -SourceImageId $sourceImageId -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="0934d-109">Skapa en galleri bild version.</span><span class="sxs-lookup"><span data-stu-id="0934d-109">Create a gallery image version.</span></span>

## <span data-ttu-id="0934d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0934d-110">PARAMETERS</span></span>

### <span data-ttu-id="0934d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0934d-111">-AsJob</span></span>
<span data-ttu-id="0934d-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="0934d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0934d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0934d-113">-DefaultProfile</span></span>
<span data-ttu-id="0934d-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0934d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0934d-115">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="0934d-115">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="0934d-116">Namnet på galleriet.</span><span class="sxs-lookup"><span data-stu-id="0934d-116">The name of the gallery.</span></span>

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

### <span data-ttu-id="0934d-117">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="0934d-117">-GalleryName</span></span>
<span data-ttu-id="0934d-118">Namnet på galleriet.</span><span class="sxs-lookup"><span data-stu-id="0934d-118">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0934d-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="0934d-119">-Location</span></span>
<span data-ttu-id="0934d-120">Resurs plats</span><span class="sxs-lookup"><span data-stu-id="0934d-120">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0934d-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="0934d-121">-Name</span></span>
<span data-ttu-id="0934d-122">Namnet på Galleri bild versionen.</span><span class="sxs-lookup"><span data-stu-id="0934d-122">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GalleryImageVersionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0934d-123">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="0934d-123">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="0934d-124">Livs cykel datum för bild versionen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="0934d-124">The end of life date of the gallery Image Version.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0934d-125">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="0934d-125">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="0934d-126">Om den är angiven kommer virtuella datorer som distribueras från den senaste versionen av bild definitionen inte att använda denna bild version.</span><span class="sxs-lookup"><span data-stu-id="0934d-126">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0934d-127">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="0934d-127">-ReplicaCount</span></span>
<span data-ttu-id="0934d-128">Antalet repliker av den bild version som ska skapas per region.</span><span class="sxs-lookup"><span data-stu-id="0934d-128">The number of replicas of the Image Version to be created per region.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0934d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0934d-129">-ResourceGroupName</span></span>
<span data-ttu-id="0934d-130">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0934d-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="0934d-131">-SourceImageId</span><span class="sxs-lookup"><span data-stu-id="0934d-131">-SourceImageId</span></span>
<span data-ttu-id="0934d-132">ID för käll bilden från vilken bild versionen ska skapas.</span><span class="sxs-lookup"><span data-stu-id="0934d-132">The ID of the source image from which the Image Version is going to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0934d-133">-Tagg</span><span class="sxs-lookup"><span data-stu-id="0934d-133">-Tag</span></span>
<span data-ttu-id="0934d-134">Resursfiler</span><span class="sxs-lookup"><span data-stu-id="0934d-134">Resource tags</span></span>

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

### <span data-ttu-id="0934d-135">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="0934d-135">-TargetRegion</span></span>
<span data-ttu-id="0934d-136">De mål områden där bild versionen ska replikeras till.</span><span class="sxs-lookup"><span data-stu-id="0934d-136">The target regions where the Image Version is going to be replicated to.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0934d-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0934d-137">-Confirm</span></span>
<span data-ttu-id="0934d-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0934d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0934d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0934d-139">-WhatIf</span></span>
<span data-ttu-id="0934d-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0934d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0934d-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0934d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0934d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0934d-142">CommonParameters</span></span>
<span data-ttu-id="0934d-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0934d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0934d-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0934d-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0934d-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0934d-145">INPUTS</span></span>

### <span data-ttu-id="0934d-146">System. String</span><span class="sxs-lookup"><span data-stu-id="0934d-146">System.String</span></span>

### <span data-ttu-id="0934d-147">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="0934d-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0934d-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="0934d-148">System.Int32</span></span>

### <span data-ttu-id="0934d-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0934d-149">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="0934d-150">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="0934d-150">System.DateTime</span></span>

### <span data-ttu-id="0934d-151">System. Collections. hash-program []</span><span class="sxs-lookup"><span data-stu-id="0934d-151">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="0934d-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0934d-152">OUTPUTS</span></span>

### <span data-ttu-id="0934d-153">Microsoft. Azure. commands. Compute. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="0934d-153">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="0934d-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0934d-154">NOTES</span></span>

## <span data-ttu-id="0934d-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0934d-155">RELATED LINKS</span></span>
