---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
ms.openlocfilehash: 8ef13dd067cd0cf1161e3aa58b52a961fe90a949
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270299"
---
# <span data-ttu-id="9e9ae-101">New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="9e9ae-101">New-AzGalleryImageVersion</span></span>

## <span data-ttu-id="9e9ae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9e9ae-102">SYNOPSIS</span></span>
<span data-ttu-id="9e9ae-103">Skapa en galleri bild version.</span><span class="sxs-lookup"><span data-stu-id="9e9ae-103">Create a gallery image version.</span></span>

## <span data-ttu-id="9e9ae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9e9ae-104">SYNTAX</span></span>

```
New-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] -Location <String>
 [-DataDiskImage <GalleryDataDiskImage[]>] [-OSDiskImage <GalleryOSDiskImage>]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>]
 [-SourceImageId <String>] [-StorageAccountType <String>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e9ae-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9e9ae-105">DESCRIPTION</span></span>
<span data-ttu-id="9e9ae-106">Skapa en galleri bild version.</span><span class="sxs-lookup"><span data-stu-id="9e9ae-106">Create a gallery image version.</span></span>

## <span data-ttu-id="9e9ae-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9e9ae-107">EXAMPLES</span></span>

### <span data-ttu-id="9e9ae-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9e9ae-108">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageDefinitionName $imageDefinitionName -Name $versionName -Location $location -SourceImageId $sourceImageId -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="9e9ae-109">Skapa en galleri bild version.</span><span class="sxs-lookup"><span data-stu-id="9e9ae-109">Create a gallery image version.</span></span>

### <span data-ttu-id="9e9ae-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="9e9ae-110">Example 2</span></span>
```powershell
PS C:\> $osDiskImageEncryption = @{DiskEncryptionSetId='subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Compute/diskEncryptionSets/myDES'}
PS C:\> $dataDiskImageEncryption1 = @{DiskEncryptionSetId='subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Compute/diskEncryptionSets/myDES1';Lun=1}
PS C:\> $dataDiskImageEncryption2 = @{DiskEncryptionSetId='subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Compute/diskEncryptionSets/myDES2';Lun=2}
PS C:\> $dataDiskImageEncryptions = @($dataDiskImageEncryption1,$dataDiskImageEncryption2)
PS C:\> $encryption1 = @{OSDiskImage=$osDiskImageEncryption;DataDiskImages=$dataDiskImageEncryptions}
PS C:\> $region1 = @{Name='West US';ReplicaCount=1;StorageAccountType=Standard_LRS;Encryption=$encryption1}
PS C:\> $targetRegions = @{$region1}
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageDefinitionName $imageDefinitionName -Name $versionName -Location $location -SourceImageId $SourceImageId -ReplicaCount 2 -StorageAccountType Standard_LRS -PublishingProfileExcludeFromLatest -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegion
```

<span data-ttu-id="9e9ae-111">Skapa en galleri bild version med disk bild kryptering.</span><span class="sxs-lookup"><span data-stu-id="9e9ae-111">Create a gallery image version with disk image encryption.</span></span>

## <span data-ttu-id="9e9ae-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9e9ae-112">PARAMETERS</span></span>

### <span data-ttu-id="9e9ae-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e9ae-113">-AsJob</span></span>
<span data-ttu-id="9e9ae-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="9e9ae-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9e9ae-115">-DataDiskImage</span><span class="sxs-lookup"><span data-stu-id="9e9ae-115">-DataDiskImage</span></span>
<span data-ttu-id="9e9ae-116">Data disk bilder.</span><span class="sxs-lookup"><span data-stu-id="9e9ae-116">Data disk images.</span></span>   <span data-ttu-id="9e9ae-117">t. @ {source = @ {ID =<source_id>}; LUN = 1; SizeInGB = 100; HostCaching = "ReadOnly"}</span><span class="sxs-lookup"><span data-stu-id="9e9ae-117">e.g. @{Source = @{Id=<source_id>}; Lun=1; SizeInGB = 100; HostCaching = "ReadOnly" }</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.GalleryDataDiskImage[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e9ae-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e9ae-118">-DefaultProfile</span></span>
<span data-ttu-id="9e9ae-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9e9ae-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e9ae-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="9e9ae-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="9e9ae-121">Namnet på galleriet.</span><span class="sxs-lookup"><span data-stu-id="9e9ae-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="9e9ae-122">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="9e9ae-122">-GalleryName</span></span>
<span data-ttu-id="9e9ae-123">Namnet på galleriet.</span><span class="sxs-lookup"><span data-stu-id="9e9ae-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="9e9ae-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="9e9ae-124">-Location</span></span>
<span data-ttu-id="9e9ae-125">Resurs plats</span><span class="sxs-lookup"><span data-stu-id="9e9ae-125">Resource location</span></span>

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

### <span data-ttu-id="9e9ae-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="9e9ae-126">-Name</span></span>
<span data-ttu-id="9e9ae-127">Namnet på Galleri bild versionen.</span><span class="sxs-lookup"><span data-stu-id="9e9ae-127">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="9e9ae-128">-OSDiskImage</span><span class="sxs-lookup"><span data-stu-id="9e9ae-128">-OSDiskImage</span></span>
<span data-ttu-id="9e9ae-129">OS-diskavbildning till exempel. @ {source = @ {ID =<source_id>}; SizeInGB = 100; HostCaching = "ReadOnly"}</span><span class="sxs-lookup"><span data-stu-id="9e9ae-129">OS disk image   e.g. @{Source = @{Id=<source_id>}; SizeInGB = 100; HostCaching = "ReadOnly" }</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.GalleryOSDiskImage
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e9ae-130">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="9e9ae-130">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="9e9ae-131">Livs cykel datum för bild versionen för galleriet.</span><span class="sxs-lookup"><span data-stu-id="9e9ae-131">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="9e9ae-132">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="9e9ae-132">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="9e9ae-133">Om den är angiven kommer virtuella datorer som distribueras från den senaste versionen av bild definitionen inte att använda denna bild version.</span><span class="sxs-lookup"><span data-stu-id="9e9ae-133">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="9e9ae-134">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="9e9ae-134">-ReplicaCount</span></span>
<span data-ttu-id="9e9ae-135">Antalet repliker av den bild version som ska skapas per region.</span><span class="sxs-lookup"><span data-stu-id="9e9ae-135">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="9e9ae-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e9ae-136">-ResourceGroupName</span></span>
<span data-ttu-id="9e9ae-137">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9e9ae-137">The name of the resource group.</span></span>

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

### <span data-ttu-id="9e9ae-138">-SourceImageId</span><span class="sxs-lookup"><span data-stu-id="9e9ae-138">-SourceImageId</span></span>
<span data-ttu-id="9e9ae-139">ID för käll bilden från vilken bild versionen ska skapas.</span><span class="sxs-lookup"><span data-stu-id="9e9ae-139">The ID of the source image from which the Image Version is going to be created.</span></span>

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

### <span data-ttu-id="9e9ae-140">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="9e9ae-140">-StorageAccountType</span></span>
<span data-ttu-id="9e9ae-141">Anger den typ av lagrings konto som ska användas för att lagra bilden.</span><span class="sxs-lookup"><span data-stu-id="9e9ae-141">Specifies the storage account type to be used to store the image.</span></span> <span data-ttu-id="9e9ae-142">Det går inte att uppdatera den här egenskapen.</span><span class="sxs-lookup"><span data-stu-id="9e9ae-142">This property is not updatable.</span></span> <span data-ttu-id="9e9ae-143">Tillgängliga värden är Standard_LRS, Standard_ZRS och Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="9e9ae-143">Available values are Standard_LRS, Standard_ZRS and Premium_LRS.</span></span>

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

### <span data-ttu-id="9e9ae-144">-Tagg</span><span class="sxs-lookup"><span data-stu-id="9e9ae-144">-Tag</span></span>
<span data-ttu-id="9e9ae-145">Resursfiler</span><span class="sxs-lookup"><span data-stu-id="9e9ae-145">Resource tags</span></span>

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

### <span data-ttu-id="9e9ae-146">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="9e9ae-146">-TargetRegion</span></span>
<span data-ttu-id="9e9ae-147">De mål områden där bild versionen ska replikeras till.</span><span class="sxs-lookup"><span data-stu-id="9e9ae-147">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="9e9ae-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9e9ae-148">-Confirm</span></span>
<span data-ttu-id="9e9ae-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9e9ae-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e9ae-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e9ae-150">-WhatIf</span></span>
<span data-ttu-id="9e9ae-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9e9ae-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e9ae-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9e9ae-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e9ae-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e9ae-153">CommonParameters</span></span>
<span data-ttu-id="9e9ae-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e9ae-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e9ae-155">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e9ae-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e9ae-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9e9ae-156">INPUTS</span></span>

### <span data-ttu-id="9e9ae-157">System. String</span><span class="sxs-lookup"><span data-stu-id="9e9ae-157">System.String</span></span>

### <span data-ttu-id="9e9ae-158">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="9e9ae-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="9e9ae-159">System. Int32</span><span class="sxs-lookup"><span data-stu-id="9e9ae-159">System.Int32</span></span>

### <span data-ttu-id="9e9ae-160">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9e9ae-160">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="9e9ae-161">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="9e9ae-161">System.DateTime</span></span>

### <span data-ttu-id="9e9ae-162">System. Collections. hash-program []</span><span class="sxs-lookup"><span data-stu-id="9e9ae-162">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="9e9ae-163">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9e9ae-163">OUTPUTS</span></span>

### <span data-ttu-id="9e9ae-164">Microsoft. Azure. commands. Compute. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="9e9ae-164">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="9e9ae-165">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9e9ae-165">NOTES</span></span>

## <span data-ttu-id="9e9ae-166">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9e9ae-166">RELATED LINKS</span></span>