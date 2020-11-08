---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/new-AzImageBuilderDistributorObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderDistributorObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderDistributorObject.md
ms.openlocfilehash: 4b2af3797bde0d27f9f4f18cfd42acdddb4ffcf4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102274"
---
# <span data-ttu-id="a354f-101">New-AzImageBuilderDistributorObject</span><span class="sxs-lookup"><span data-stu-id="a354f-101">New-AzImageBuilderDistributorObject</span></span>

## <span data-ttu-id="a354f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a354f-102">SYNOPSIS</span></span>
<span data-ttu-id="a354f-103">Generiskt distributions objekt</span><span class="sxs-lookup"><span data-stu-id="a354f-103">Generic distribution object</span></span>

## <span data-ttu-id="a354f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a354f-104">SYNTAX</span></span>

### <span data-ttu-id="a354f-105">ManagedImageDistributor (standard)</span><span class="sxs-lookup"><span data-stu-id="a354f-105">ManagedImageDistributor (Default)</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -ImageId <String> -Location <String>
 -ManagedImageDistributor -RunOutputName <String> [<CommonParameters>]
```

### <span data-ttu-id="a354f-106">SharedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="a354f-106">SharedImageDistributor</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -ExcludeFromLatest <Boolean>
 -GalleryImageId <String> -ReplicationRegion <String[]> -RunOutputName <String> -SharedImageDistributor
 [-StorageAccountType <SharedImageStorageAccountType>] [<CommonParameters>]
```

### <span data-ttu-id="a354f-107">VhdDistributor</span><span class="sxs-lookup"><span data-stu-id="a354f-107">VhdDistributor</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -RunOutputName <String> -VhdDistributor
 [<CommonParameters>]
```

## <span data-ttu-id="a354f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a354f-108">DESCRIPTION</span></span>
<span data-ttu-id="a354f-109">Generiskt distributions objekt</span><span class="sxs-lookup"><span data-stu-id="a354f-109">Generic distribution object</span></span>

## <span data-ttu-id="a354f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a354f-110">EXAMPLES</span></span>

### <span data-ttu-id="a354f-111">Exempel 1: skapa en hanterad bild distributör</span><span class="sxs-lookup"><span data-stu-id="a354f-111">Example 1: Create a managed image distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -ManagedImageDistributor  -ArtifactTag @{tag='lucasManage'} -ImageId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/lucas-linux-imageshare -RunOutputName luacas-runout -Location eastus

RunOutputName Type         ImageId                                                                                                                                           Location
------------- ----         -------                                                                                                                                           --------
luacas-runout ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/lucas-linux-imageshare eastus
```

<span data-ttu-id="a354f-112">Det här kommandot skapar en hanterad bild distributör.</span><span class="sxs-lookup"><span data-stu-id="a354f-112">This command creates a managed image distributor.</span></span>

### <span data-ttu-id="a354f-113">Exempel 2: skapa en VHD-distributör</span><span class="sxs-lookup"><span data-stu-id="a354f-113">Example 2: Create a VHD distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -ArtifactTag @{tag='vhd'} -VhdDistributor -RunOutputName image-vhd

RunOutputName Type
------------- ----
image-vhd     Vhd
```

<span data-ttu-id="a354f-114">Det här kommandot skapar en VHD-distributör.</span><span class="sxs-lookup"><span data-stu-id="a354f-114">This command creates a VHD distributor.</span></span>

### <span data-ttu-id="a354f-115">Exempel 3: skapa en distribuerad bild-distributör</span><span class="sxs-lookup"><span data-stu-id="a354f-115">Example 3: Create a shared image distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -SharedImageDistributor -ArtifactTag @{tag='dis-share'} -GalleryImageId '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/myimagegallery/images/lcuas-linux-share' -ReplicationRegion eastus2 -RunOutputName 'outname' -ExcludeFromLatest $false 

RunOutputName Type        ExcludeFromLatest GalleryImageId                                                                                                                                                        ReplicationRegi
                                                                                                                                                                                                                  on
------------- ----        ----------------- --------------                                                                                                                                                        ---------------
outname       SharedImage False             /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/myimagegallery/images/lcuas-linux-share {eastus2}
```

<span data-ttu-id="a354f-116">Det här kommandot skapar en delad bild distributör.</span><span class="sxs-lookup"><span data-stu-id="a354f-116">This command creates a shared image distributor.</span></span>

## <span data-ttu-id="a354f-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a354f-117">PARAMETERS</span></span>

### <span data-ttu-id="a354f-118">-ArtifactTag</span><span class="sxs-lookup"><span data-stu-id="a354f-118">-ArtifactTag</span></span>
<span data-ttu-id="a354f-119">Taggar som kommer att tillämpas på artefakten när den har skapats/uppdaterats av distributören.</span><span class="sxs-lookup"><span data-stu-id="a354f-119">Tags that will be applied to the artifact once it has been created/updated by the distributor.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a354f-120">-ExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="a354f-120">-ExcludeFromLatest</span></span>
<span data-ttu-id="a354f-121">Flagga som anger om skapad bild version ska uteslutas från senaste.</span><span class="sxs-lookup"><span data-stu-id="a354f-121">Flag that indicates whether created image version should be excluded from latest.</span></span>
<span data-ttu-id="a354f-122">Utelämna för att använda standardvärdet (false).</span><span class="sxs-lookup"><span data-stu-id="a354f-122">Omit to use the default (false).</span></span>

```yaml
Type: System.Boolean
Parameter Sets: SharedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a354f-123">-GalleryImageId</span><span class="sxs-lookup"><span data-stu-id="a354f-123">-GalleryImageId</span></span>
<span data-ttu-id="a354f-124">Resurs-ID för bild av delad bild.</span><span class="sxs-lookup"><span data-stu-id="a354f-124">Resource Id of the Shared Image Gallery image.</span></span>

```yaml
Type: System.String
Parameter Sets: SharedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a354f-125">-ImageId</span><span class="sxs-lookup"><span data-stu-id="a354f-125">-ImageId</span></span>
<span data-ttu-id="a354f-126">Resurs-ID för den hanterade disk avbildningen.</span><span class="sxs-lookup"><span data-stu-id="a354f-126">Resource Id of the Managed Disk Image.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a354f-127">-Plats</span><span class="sxs-lookup"><span data-stu-id="a354f-127">-Location</span></span>
<span data-ttu-id="a354f-128">Azure-plats för bilden, ska passa om bilden redan finns.</span><span class="sxs-lookup"><span data-stu-id="a354f-128">Azure location for the image, should match if image already exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a354f-129">-ManagedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="a354f-129">-ManagedImageDistributor</span></span>
<span data-ttu-id="a354f-130">Distribuera som en hanterad skiv bild.</span><span class="sxs-lookup"><span data-stu-id="a354f-130">Distribute as a Managed Disk Image.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a354f-131">-ReplicationRegion</span><span class="sxs-lookup"><span data-stu-id="a354f-131">-ReplicationRegion</span></span>
<span data-ttu-id="a354f-132">En lista över områden som bilden kommer att replikeras till.</span><span class="sxs-lookup"><span data-stu-id="a354f-132">A list of regions that the image will be replicated to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SharedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a354f-133">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="a354f-133">-RunOutputName</span></span>
<span data-ttu-id="a354f-134">Namnet som ska användas för den associerade RunOutput.</span><span class="sxs-lookup"><span data-stu-id="a354f-134">The name to be used for the associated RunOutput.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a354f-135">-SharedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="a354f-135">-SharedImageDistributor</span></span>
<span data-ttu-id="a354f-136">Distribuera via delad bild galleri.</span><span class="sxs-lookup"><span data-stu-id="a354f-136">Distribute via Shared Image Gallery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SharedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a354f-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="a354f-137">-StorageAccountType</span></span>
<span data-ttu-id="a354f-138">Lagrings konto typ som ska användas för att lagra den delade bilden.</span><span class="sxs-lookup"><span data-stu-id="a354f-138">Storage account type to be used to store the shared image.</span></span>
<span data-ttu-id="a354f-139">Utelämna för att använda standardvärdet (Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="a354f-139">Omit to use the default (Standard_LRS).</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Support.SharedImageStorageAccountType
Parameter Sets: SharedImageDistributor
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a354f-140">-VhdDistributor</span><span class="sxs-lookup"><span data-stu-id="a354f-140">-VhdDistributor</span></span>
<span data-ttu-id="a354f-141">Distribuera via VHD i ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="a354f-141">Distribute via VHD in a storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VhdDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a354f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a354f-142">CommonParameters</span></span>
<span data-ttu-id="a354f-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a354f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a354f-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a354f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a354f-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a354f-145">INPUTS</span></span>

## <span data-ttu-id="a354f-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a354f-146">OUTPUTS</span></span>

### <span data-ttu-id="a354f-147">Microsoft. Azure. PowerShell. cmdletar. ImageBuilder. Models. Api20200214. IImageTemplateDistributor</span><span class="sxs-lookup"><span data-stu-id="a354f-147">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateDistributor</span></span>

## <span data-ttu-id="a354f-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a354f-148">NOTES</span></span>

<span data-ttu-id="a354f-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a354f-149">ALIASES</span></span>

## <span data-ttu-id="a354f-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a354f-150">RELATED LINKS</span></span>

