---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
ms.openlocfilehash: 80536a8bfce32d713649f3feab4d77b1662206b8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745103"
---
# <span data-ttu-id="bdce7-101">New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="bdce7-101">New-AzGalleryImageVersion</span></span>

## <span data-ttu-id="bdce7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bdce7-102">SYNOPSIS</span></span>
<span data-ttu-id="bdce7-103">Skapa en galleri bild version.</span><span class="sxs-lookup"><span data-stu-id="bdce7-103">Create a gallery image version.</span></span>

## <span data-ttu-id="bdce7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bdce7-104">SYNTAX</span></span>

```
New-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] -Location <String> -SourceImageId <String>
 [-Tag <Hashtable>] [-ReplicaCount <Int32>] [-PublishingProfileExcludeFromLatest]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-StorageAccountType <String>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdce7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bdce7-105">DESCRIPTION</span></span>
<span data-ttu-id="bdce7-106">Skapa en galleri bild version.</span><span class="sxs-lookup"><span data-stu-id="bdce7-106">Create a gallery image version.</span></span>

## <span data-ttu-id="bdce7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bdce7-107">EXAMPLES</span></span>

### <span data-ttu-id="bdce7-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bdce7-108">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -Location $location -SourceImageId $sourceImageId -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="bdce7-109">Skapa en galleri bild version.</span><span class="sxs-lookup"><span data-stu-id="bdce7-109">Create a gallery image version.</span></span>

## <span data-ttu-id="bdce7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bdce7-110">PARAMETERS</span></span>

### <span data-ttu-id="bdce7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bdce7-111">-AsJob</span></span>
<span data-ttu-id="bdce7-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="bdce7-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bdce7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdce7-113">-DefaultProfile</span></span>
<span data-ttu-id="bdce7-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bdce7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdce7-115">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="bdce7-115">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="bdce7-116">Namnet på galleriet.</span><span class="sxs-lookup"><span data-stu-id="bdce7-116">The name of the gallery.</span></span>

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

### <span data-ttu-id="bdce7-117">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="bdce7-117">-GalleryName</span></span>
<span data-ttu-id="bdce7-118">Namnet på galleriet.</span><span class="sxs-lookup"><span data-stu-id="bdce7-118">The name of the gallery.</span></span>

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

### <span data-ttu-id="bdce7-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="bdce7-119">-Location</span></span>
<span data-ttu-id="bdce7-120">Resurs plats</span><span class="sxs-lookup"><span data-stu-id="bdce7-120">Resource location</span></span>

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

### <span data-ttu-id="bdce7-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="bdce7-121">-Name</span></span>
<span data-ttu-id="bdce7-122">Namnet på Galleri bild versionen.</span><span class="sxs-lookup"><span data-stu-id="bdce7-122">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="bdce7-123">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="bdce7-123">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="bdce7-124">Livs cykel datum för bild versionen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="bdce7-124">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="bdce7-125">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="bdce7-125">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="bdce7-126">Om den är angiven kommer virtuella datorer som distribueras från den senaste versionen av bild definitionen inte att använda denna bild version.</span><span class="sxs-lookup"><span data-stu-id="bdce7-126">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="bdce7-127">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="bdce7-127">-ReplicaCount</span></span>
<span data-ttu-id="bdce7-128">Antalet repliker av den bild version som ska skapas per region.</span><span class="sxs-lookup"><span data-stu-id="bdce7-128">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="bdce7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdce7-129">-ResourceGroupName</span></span>
<span data-ttu-id="bdce7-130">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="bdce7-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="bdce7-131">-SourceImageId</span><span class="sxs-lookup"><span data-stu-id="bdce7-131">-SourceImageId</span></span>
<span data-ttu-id="bdce7-132">ID för käll bilden från vilken bild versionen ska skapas.</span><span class="sxs-lookup"><span data-stu-id="bdce7-132">The ID of the source image from which the Image Version is going to be created.</span></span>

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

### <span data-ttu-id="bdce7-133">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="bdce7-133">-StorageAccountType</span></span>
<span data-ttu-id="bdce7-134">Anger den typ av lagrings konto som ska användas för att lagra bilden.</span><span class="sxs-lookup"><span data-stu-id="bdce7-134">Specifies the storage account type to be used to store the image.</span></span> <span data-ttu-id="bdce7-135">Det går inte att uppdatera den här egenskapen.</span><span class="sxs-lookup"><span data-stu-id="bdce7-135">This property is not updatable.</span></span> <span data-ttu-id="bdce7-136">Tillgängliga värden är Standard_LRS och Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="bdce7-136">Available values are Standard_LRS and Standard_ZRS.</span></span>

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

### <span data-ttu-id="bdce7-137">-Tagg</span><span class="sxs-lookup"><span data-stu-id="bdce7-137">-Tag</span></span>
<span data-ttu-id="bdce7-138">Resursfiler</span><span class="sxs-lookup"><span data-stu-id="bdce7-138">Resource tags</span></span>

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

### <span data-ttu-id="bdce7-139">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="bdce7-139">-TargetRegion</span></span>
<span data-ttu-id="bdce7-140">De mål områden där bild versionen ska replikeras till.</span><span class="sxs-lookup"><span data-stu-id="bdce7-140">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="bdce7-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bdce7-141">-Confirm</span></span>
<span data-ttu-id="bdce7-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bdce7-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdce7-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdce7-143">-WhatIf</span></span>
<span data-ttu-id="bdce7-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bdce7-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdce7-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bdce7-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdce7-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdce7-146">CommonParameters</span></span>
<span data-ttu-id="bdce7-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdce7-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdce7-148">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bdce7-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdce7-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bdce7-149">INPUTS</span></span>

### <span data-ttu-id="bdce7-150">System. String</span><span class="sxs-lookup"><span data-stu-id="bdce7-150">System.String</span></span>

### <span data-ttu-id="bdce7-151">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="bdce7-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="bdce7-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="bdce7-152">System.Int32</span></span>

### <span data-ttu-id="bdce7-153">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bdce7-153">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="bdce7-154">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="bdce7-154">System.DateTime</span></span>

### <span data-ttu-id="bdce7-155">System. Collections. hash-program []</span><span class="sxs-lookup"><span data-stu-id="bdce7-155">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="bdce7-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bdce7-156">OUTPUTS</span></span>

### <span data-ttu-id="bdce7-157">Microsoft. Azure. commands. Compute. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="bdce7-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="bdce7-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bdce7-158">NOTES</span></span>

## <span data-ttu-id="bdce7-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bdce7-159">RELATED LINKS</span></span>
